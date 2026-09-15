# kosnoa's Personal Blog

https://kosnoa.github.io/ — 알고리즘·C++ 풀이와 JPOP 공연 경험을 기록하는 Jekyll 블로그입니다. NexT Muse 테마를 사용합니다.

## 로컬 실행

이 저장소 디렉터리에서 Ruby와 Bundler를 사용합니다. 의존성 버전은 `Gemfile.lock`을 기준으로 하며, 단순 미리보기를 위해 `bundle update`를 실행하지 않습니다.

```sh
bundle check
# 의존성이 없을 때만 실행
bundle install
bundle exec jekyll serve
```

터미널에 표시된 로컬 주소에서 결과를 확인합니다. 빌드만 하려면 `bundle exec jekyll build`를 사용합니다. 두 명령은 사이트를 원격으로 배포하지 않습니다.

## 파일 관리

- `_posts/`: 게시 글 원본. [작성 안내](posting.md)를 참고합니다.
- `post_image/`: 글에서 참조하는 사진.
- `_layouts/`, `_includes/`, `_sass/`, `assets/`: 테마와 화면 구성.
- `_config.yml`, `Gemfile`, `Gemfile.lock`: 사이트 설정과 의존성.
- `_site/`: 생성 결과물. 원본 대신 직접 수정하지 않습니다.
- `archive_post/`: 로컬 보관 글. Git 추적과 Jekyll 빌드에서 제외하며, 파일은 로컬에 보존합니다.
- `.gjc/`: 로컬 작업 기록. Git 추적과 Jekyll 빌드에서 제외합니다.

제외 규칙은 과거 커밋이나 이미 배포된 사본을 삭제하지 않습니다. 보관 글을 다시 공개하거나 Git에 강제로 추가하지 않습니다.

기존 글의 날짜·카테고리는 URL에 영향을 주므로 일괄 변경하지 않습니다. 시간대·테마·의존성 변경과 commit/push/배포는 글 작성이나 로컬 확인과 별도로 다룹니다.

## 테마 출처

[NexT](https://github.com/simpleyyt/jekyll-theme-next) 기반이며, 기존 JusticeHui 포크 안내는 아래 주석에 남겨 두었습니다. 현재 운영 절차는 위 안내와 `posting.md`를 따릅니다.

<!-- # JusticeHui가 PS하는 블로그

### 알고리즘 튜토리얼 프로젝트
[github projects](https://github.com/justiceHui/justiceHui.github.io/projects)에서 작성할 예정 혹은 너무 예전에 작성하여 수정이 필요한 게시물들을 관리하고 있습니다.<br>
원하시는 내용이나 수정해야 할 것이 있으면 issue로 넣어주시면 감사하겠습니다.

### 오류 제보
[github issues](https://github.com/justiceHui/justiceHui.github.io/issues)로 주시거나, 게시물에 댓글로 달아주시면 확인 후 수정하겠습니다.

### Pull requests
사이트 이용 중 불편하신 점을 직접 수정하고 싶으면 pull requests를 넣어주세요. 확인 후 반영하겠습니다.

### 브라우저 지원 여부
![Browser support](http://iissnan.com/nexus/next/browser-support.png)

### Repository Fork
이 블로그를 포크 후 수정해서 사용하실 생각이라면 아래 내용을 확인해주세요.

1. 이 폴더들을 **제외한** 나머지 폴더는 **필요없는 폴더입니다**.
  * `_data`, `_includes`, `_layouts`, `_posts`, `_posts`, `_sass`
  * `about`, `archives`, `assets`, `categories`, `category`, `navigator`, `tag`, `tags`
2. 아래 폴더/파일을 **삭제해주세요**.
  * `_data/teacher.yml`
  * `about/award/` 폴더 전체
  * `about/secpro/` 폴더 전체
  * `teach/` 폴더 전체
3. 이 내용들을 **수정해야 합니다**.
  * `_includes/judge_profile.html` 10번째 줄
  * `_includes/_layout.html`의 google analytics 관련 부분
  * `_includes/index.html`의 github chart 관련 부분
  * `about/index.md`, `navigator/index.html` 전체
  * `_config.yml`의 Disqus 관련 부분
  * `_includes/advertise.html` 전체
  * (사이드바에 광고를 넣지 않는다면) `_includes/_macro/sidebar.html` 하단 `{% include advertise.html %}` 부분 삭제
4.  포스팅 작성 방법은 [여기](https://github.com/justiceHui/justiceHui.github.io/blob/master/posting.md)를 참고해주세요. 

bundle exec jekyll serve 로컬로 실행

-->
