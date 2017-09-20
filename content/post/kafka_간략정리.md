---
title: "kafka 간략정리"
date: 2017-09-19T15:13:01+09:00
draft: false
---
팀내 다른 프로젝트에서 [kafka](https://kafka.apache.org/)를 쓰고 있고, 대부분의 메시징 시스템에서 사용하고 있어 가볍게 정리하고자 남긴다.

## kafka란 무엇인가?
비동기 처리를 위한 메시징 큐의 한 종류.

## producer
- topic에 대한 메시지 생성.
- acks : producer가 메시지를 보내고 kafka가 잘 받았는지 확인을 할 것인지 안 할 것인지의 옵션 값.

## consumer
- 구독한 topic에 대해 처리.
- consumer group : consumer instance들을 대표하는 그룹.
  - 사용하는 이유
     - 그룹 내 한 서버(instance)의 장애상황에서도 그룹 내 다른 instance가 동작함으로 안정성 확보를 할 수 있다.
     - 그룹별로 offset을 관리하기 때문에, 동일한 토픽에 대해 데이터 손실이 없다.
     - 하나의 파티션에 대해 consumer group내 하나의 consumer instance만 접근할 수 있다.
- consumer instance : 하나의 프로세스 또는 하나의 서버.
- offset : 파티션안에 데이터 위치를 유니크한 숫자로 표시한 것. consumer는 자신이 어디까지 데이터를 가져갔는지 offset을 이용해서 관리한다.

## broker
- 메시지 큐.
- topic
  - 보관주기는 기본 1주일.
- 파티션이 2개 이상일경우, consumer가 가져가는 순서는 보장되지 않는다.
- replication factor
  - partition을 복제하여 클러스터에 분산시킨다.
  - leader/follower가 존재 하며, 누구나 leader가 될 수 있다.
  - leader에서만 read/write가 일어난다.

> - kafka quickstart : https://kafka.apache.org/quickstart 
- epicdevs님 블로그 : http://epicdevs.com/tag/kafka  
- 고승범님 브런치 : https://brunch.co.kr/keyword/Kafka

## 간단 예제로 테스트
- https://github.com/simplestone/kafka-spring