# hyukjuns tech blog
## URL
[hyukjuns.github.io](https://hyukjuns.github.io)

# Post
- post 제목 양식
```
YEAR-MONTH-DAY-title.md
```
- 내용 상단 양식
```
---
title: value
excerpt: value
categories:
    - value
tags:
    - value
toc: true
toc_sticky: true
toc_label: "Contents"
last_modified_at: date
---
```

## In local
1. 포스트 작성
2. 로컬 빌드
    ```
    bundle install # gemfile 기반 빌드
    ```
3. 로컬 배포
    ```
    # --draft: 초안 표시, --livereload: 수정시 자동 새로고침
    # _config.yml 수정은 매번 다시 명령어 수행해야함
    bundle exec jekyll serve # local 4000 port로 퍼블리싱
    ```
3. git push
4. github page 빌드 후 홈페이지 확인

# 본문 화면 폭 넓히기
개발자 모드로 해당 화면의 class 알아낸 후 padding 값 수정 함
(해당 본문 구역(article)의 margin을 줄이지 않고, 오른쪽 padding을 0으로 하여 오른쪽 여백을 없앰)

*_page.scss 파일
```
.page {
  @include breakpoint($large) {
    float: right;
    width: calc(100% - #{$right-sidebar-width-narrow});
    // padding-right: $right-sidebar-width-narrow;
    padding-right: 0%;
  }

  @include breakpoint($x-large) {
    width: calc(100% - #{$right-sidebar-width});
    // padding-right: $right-sidebar-width;
    padding-right: 0%;
  }
```

### Markdown
```
문자 박스Permalink
Notice Type	Class
Default	.notice
Primary	.notice--primary
Info	.notice--info
Warning	.notice--warning
Success	.notice--success
Danger	.notice--danger
```