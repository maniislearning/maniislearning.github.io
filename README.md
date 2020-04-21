# 마니배우자

## 깃허브 블로그 만들기 과정 (jekyll 사용)

## 준비

- vscode 설치(코드 편집기)

- ruby 설치
~~~
https://rubyinstaller.org/downloads/
~~~

- rubyGems 설치
~~~
https://rubygems.org/pages/download
~~~

- 깃허브 가입

---

## 블로그 생성 및 로컬과 연결

- 깃허브 New Repository
~~~
Repository 이름: '깃허브 아이디'.github.io
~~~

- 로컬에서 작업할 폴더를 만든다.
~~~
$ cd '깃허브 로컬폴더'
$ git clone '깃허브 주소'
~~~

---

## jekyll 테마 적용하기

- jekyll 테마 다운로드
~~~
http://jekyllthemes.org/
~~~

- 압축을 풀고 깃허브 로컬폴더에 복사한 후

- 테마 주소 바꾸기(_config.yml 편집)
~~~
baseurl: ""
url: "위에서 설정한 Repository 이름"
~~~

- 이제 변경사항을 추가(add)하고 설명을 넣고(commit) 푸시(push)
~~~
$ git add .
$ git commit -m "테마 변경"
$ git push
~~~

---

## 로컬에서 jekyll 서버 사용하기

- jekyll bundler 설치
~~~
$ gem install jekyll bundler
~~~

- 깃허브 로컬폴더에서
~~~
$ bundle exec jekyll serve
~~~

- 혹시 실행에 필요한 요소가 설치되어 있지 않다면 루비 버전문제일 수 있다. 2020년 현재 루비 2.7 버전에서는 동작하지 않는다. 2.6 버전으로 설치하기 바란다.

- 정상적으로 실행된다면 브라우저를 열고 주소표시줄에 'localhost:4000'을 입력한다.
