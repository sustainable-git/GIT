## [Control - Z] 되돌리기
### 직전 `commit` 수정하기
- GIT을 사용하다 보면, 실수를 저지르곤 한다. 하지만 이런 사소한 실수를 `git log`에 모두 남겨두려는 사람은 없을 것이다
- `four.txt` 파일을 생성하고, `commit`을 했지만, `commit message`를 잘못 작성하게 된 경우를 살펴보자
- 이럴 때에는 `git commit --amend`명령어를 입력하여 `commit message`만 수정이 가능하다
<p align = "center"><img src = "../imageFiles/031-wrong-commit-message.jpg?raw=true"/></p>
<p align = "center"><img src = "../imageFiles/032-amend.jpg?raw=true"/></p>

- 몇몇 파일을 빠뜨린 상태에서 `commit`을 한 경우에도 동일하다
- 해당 파일을 `git add` 한 이후 `git commit --amend`를 하면, 하나의 `commit`으로 합쳐진다
<p align = "center"><img src = "../imageFiles/033-omit.jpg?raw=true"/></p>

<br>
 <br>

### 수정한 개별 파일을 이전 `commit` 상태로 되돌리기
- 파일을 수정하였으나 수정사항이 마음에 들지 않아 이전 상태로 되돌리고 싶은 경우가 있다
- 이런 경우에는 `git restore -- 파일명` 명령어를 사용하면 해당 파일만 직전 `commit`의 상태로 되돌아간다
<p align = "center"><img src = "../imageFiles/034-restore.jpg?raw=true"/></p>
