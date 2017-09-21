---
title: "Gitpage With Hugo"
date: 2017-09-17T00:28:03+09:00
draft: false
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
  - ~~git submodule~~
     - ~~http://ohgyun.com/711~~
     - ~~https://stackoverflow.com/a/5814351~~
     - ~~https://stackoverflow.com/a/36375256~~
  - publishDir 변경
     - gitpage 프로젝트와 같은 레벨에 `<username>`.github.io 페이지를 두고 그 쪽으로 발행이 되도록 수정

## 새로운 글을 쓸때
```
gitpages 에서 new post를 한다
페이지 테스트 되면, hugo를 실행하여 publishDir로 발행한다
```
- hugo commands
  - `<parent>` hugo new `<post>`/new-post-title.md
  - `<parent>` hugo
- git commands
  - `<username.github.io>` add -A / commit / push
  - `<parent>` add -A / commit / push
  - ~~`<submodule>` add / commit~~
  - ~~`<parent>` add -A / commit / push `<origin>` `<branch>`~~
  - ~~`<parent>` submodule update `--`remote~~
  - ~~`<submodule>` checkout `<branch>`~~
  - ~~`<submodule>` push `<origin>` `<branch>`~~

