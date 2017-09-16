---
title: "Gitpage With Hugo"
date: 2017-09-17T00:28:03+09:00
draft: true
---
## github / pages
- github 계정 만들기
  - https://github.com/
- github page 용 repo 만들기, hello 생성
  - https://pages.github.com/

## hugo
- hugo 설치
  - https://gohugo.io/getting-started/installing/
  - https://gohugo.io/getting-started/quick-start/
  - https://gohugo.io/themes/installing-and-using-themes/
    - https://themes.gohugo.io
    - https://gitlab.com/beli3ver/hemingway2

## hugo on github
- hugo / host on github
  - https://gohugo.io/hosting-and-deployment/hosting-on-github/
  - git submodule
    - http://ohgyun.com/711
    - https://stackoverflow.com/a/5814351

## 새로운 글을 쓸때
- gitpages 에서 new post를 한다
- 페이지 테스트 되면, hugo를 실행하여 public으로 발행한다
- public에서 git add / commit / push를 한다
- gitpages에서 git add / commit / push를 한다
- git parent module이 sub module의 커밋해시를 바라보고 있기때문에 마지막에 커밋/푸시를 해줘야한다

