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