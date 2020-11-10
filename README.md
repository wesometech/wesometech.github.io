# WESOME 기술 블로그

위썸에서 제공하는 서비스 및 솔루션과 연구개발에 대한 내용을 담고 있습니다.

### 로컬에서 작업방법

> **사전준비:** git, docker, docker-compose, vscode

로컬에서 개발하기 위해서는 위 사전준비 항목을 모두 설치해야 한다.

모든 준비가 완료되었다면 아래 명령어를 순서대로 실행한다.

```bash
$ git clone https://github.com/wesometech/wesometech.github.io.git
$ cd wesometech.github.io
$ docker-compose up
```

명령어를 모두 실행 하였으면 로컬 환경에서 블로그에 접속할 수 있다.

브라우저를 통해 `http://localhost:4000` 에 접속한다.

> 기본적으로 게시글을 작성 또는 수정하게 되면 자동으로 변경된 내용이 적용된다.
>
> 하지만 설정 파일과 같은 파일들(예: _config.yml)은 변경이 되지 않으므로 컨테이너를 재시작 해주어야 한다.

모든 변경사항이 완료되었다면 해당 명령어를 통해 컨테이너를 종료한다.

```bash
$ Ctrl + C
$ docker-compose down
```



### 포스트 작성방법

> 포스트 작성에 앞서 해당 내용을 숙지해야 한다. [Jekyll Posts](https://jekyllrb.com/docs/posts/)

#### Posts 폴더

`_posts` 폴더는 블로그 게시물이있는 곳입니다. 일반적으로 Markdown으로 게시물을 작성하며 HTML도 지원됩니다.

#### Posts 생성

포스트를 생성하기 위해서는 `_posts` 폴더에 다음과 같은 파일을 생성해야 한다.

파일명의 경우 다음과 같은 포멧을 따라야 한다.

```
YEAR-MONTH-DAY-title.MARKUP
```

예를 들어 다음과 같다.

```
2011-12-31-new-years-eve-is-awesome.md
2012-09-12-how-to-write-a-blog.md
```

파일을 생성하였다면 아래의 예와 같은 내용을 통해 포스트를 작성할 수 있다.

```markdown
---
layout: post
title:  "Welcome to Jekyll!"
---

# Welcome

**Hello world**, this is my first Jekyll blog post.

I hope you like it!
```

여기서 `---` 사이의 구문은 특별한 것으로 모든 문서에 항상 필요한 것이다.

다음으로는 실제 포스트 내용을 작성한다. 포스트 내용의 경우 `markdown` 문법과 `html` 문법 등을 사용하여 작성 가능하다.

### 참고

로컬에서 개발환경 만들기

* [visual studio code에서 docker로 jekyll 블로그 로컬 환경 만들기](https://velog.io/@jundragon/visual-studio-code%EC%97%90%EC%84%9C-docker%EB%A1%9C-jekyll-%EB%B8%94%EB%A1%9C%EA%B7%B8-%EB%A1%9C%EC%BB%AC-%ED%99%98%EA%B2%BD-%EB%A7%8C%EB%93%A4%EA%B8%B0)

Jekyll

* [Jekyll](https://jekyllrb.com/)

Jekyll 테마

* [minimal-mistakes quick-start-guide](https://mmistakes.github.io/minimal-mistakes/docs/quick-start-guide/)

그외

* [쉽고 빠르게 수준 급의 GitHub 블로그 만들기 - jekyll remote theme으로](https://dreamgonfly.github.io/blog/jekyll-remote-theme/)

