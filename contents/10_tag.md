## Tag를 이용해 간단하게 버전 표시하기
<p align = "center"><img src = "https://media.vlpt.us/images/slaslaya/post/90902503-a9ba-49e1-8167-e25613aee51b/440px-Semver.jpg"/></p>

- GIT에는 `commit message`이외에도 `tag`를 이용하여 특정`version`에 표시를 하는것이 가능하다
- `tag`는 위의 그림에서 보여지는 `semantic versioning`이라는 규칙을 따라서 작성하는 것이 일반적이다
- GIT의 `tag`에는 `annotated tag`와 `lightweight tag`로 두 종류가 있다

### Lightweight Tag
- `lightweight tag`는 이름만 달아주고, 다른 정보는 저장하지 않는 `tag`이다
- 가능하면 이용하지 않거나, 임시로 `tag`가 필요할 때에만 사용하는 것이 좋다
- `git tag 태그명`을 입력하면 가장 최근의 `commit`에 `tag`를 달아줄 수 있다
- 또는 `git tag 태그명 해시코드`를 입력하여 특정 `hash code`에 `tag`를 달아주어도 된다
<>
<>
<br>
 <br>

### Annotated Tag
- `annotated tag`는 GIT 데이터베이스에 `tag`를 만든 사람의 이름, 이메일, 날짜, `tag message`를 저장한다
- `git tag -a`명령어를 사용하며, `git tag -a -m 태그명`명령어를 이용하면 `tag message`도 입력 가능하다
- <>

- `tag message`등 `tag`의 정보를 보려면 `git show 해시코드`를 이용해서 확인할 수 있다
- <>

<br>
 <br>

### Tag 조회 및 삭제
- `tag` 전체를 조회할 때에는 `git tag` 명령어를 이용하면 된다
- 특정 `tag`명을 조건으로 검색하려면 `git tag -l 태그명`을 이용하면 된다
- <>

- `tag`를 삭제하고자 할 때에는 `git tag -d 태그명`을 사용하면 된다
- <>