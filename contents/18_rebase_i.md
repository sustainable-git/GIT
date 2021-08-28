## Rebase -i 옵션으로 Commit 수정하기

- `rebase -i` 옵션을 이용하면 이전에 잘못한 `commit`을 수정할 수 있다
- 그러나 `rebase -i`로 수정한 `commit` 이후의 `commit`은 모두 이전과 다른 상태가 된다
- 때문에, 이미 공개 저장소에 `push`한 `commit`은 `rebase`하지 않는 것이 좋다

### `Commit message` 변경하기
- `rebase -i` 옵션을 사용할 때에는, 반드시 수정하려는 `commit` 이전의 `commit`을 사용해야 한다
- 아래와 같이 `.`으로 입력된 `commit message`를 수정하려면, 그 이전 `commit`의 `hash code`를 이용해야 한다
- 변경하려는 `commit`의 `pick` 단어를 `r`로 바꿔 주면 새로운 `commit message`를 작성할 수 있다
<p align = "center"><img src = "../imageFiles/084-rebase-i-r.jpg?raw=true"/></p>
<p align = "center"><img src = "../imageFiles/085-rebase-i-r-result.jpg?raw=true"/></p>

<br>
 <br>

### `Commit` 삭제하기
- 특정 `commit`을 삭제하려면 동일하게 `git rebase -i 해시코드`를 입력해주고, `pick`을 `d`로 변경해주자
<p align = "center"><img src = "../imageFiles/086-rebase-i-d.jpg?raw=true"/></p>

<br>
 <br>

### `Commit` 합치기
- 너무 많은 `commit`이 `log`에 포함되어 있으면, 관리 및 검색이 용이하지 않다
- 이럴 때에는 두 가지 이상의 `commit`을 합쳐서 하나의 `commit`으로 만들 수 있다
- `git rebase -i 해시코드` 후, 합칠 `commit`중 가장 위의 `commit`을 제외한 `commit`들의 `pick`을 `s`로 변경하자
- 이어서 `commit message` 까지 입력하고 저장하면 된다
<p align = "center"><img src = "../imageFiles/087-rebase-i-s.jpg?raw=true"/></p>
<p align = "center"><img src = "../imageFiles/088-rebase-i-s-result.jpg?raw=true"/></p>

<br>
 <br>

### `Commit` 분리하기
- `commit` 하나에 여러가지 기능의 수정이 포함되어 있으면, 나중에 디버깅하기 곤란한 경우가 있다
- 이럴 때에는 우선 `git rebase -i` 옵션에서 `pick`을 `e`로 변경한다
<p align = "center"><img src = "../imageFiles/089-rebase-i-e.jpg?raw=true"/></p>

- 이후 `git reset HEAD~1` 을 이용해서 수정사항들을 모두 `working directory`로 먼저 옮기자
<p align = "center"><img src = "../imageFiles/090-reset-head~1.jpg?raw=true"/></p>

- 각각의 수정사항마다 새로운 `commit`을 만들어 주고 `log`를 보면 아래와 같다
- 여기서 `git rebase --continue`를 하면 `rebase`가 완료된다
<p align = "center"><img src = "../imageFiles/091-rebase-commit.jpg?raw=true"/></p>
<p align = "center"><img src = "../imageFiles/092-rebase-continue.jpg?raw=true"/></p>

<br>
 <br>

### `Rebase Conflict`
- 동일한 파일의 수정사항을 담고 있는 두 `commit` 사이에서 변경이 발생하면 `conflict`가 발생한다
- 아래의 `fourth commit0` 는 `fourth commit`과 동일한 파일을 변경하였다
- `git rebase -i` 의 `d` 옵션으로 `fourth commit0`를 제거하면 아래와 같이 `conflict`가 발생한다
<p align = "center"><img src = "../imageFiles/093-rebase-conflict.jpg?raw=true"/></p>
<p align = "center"><img src = "../imageFiles/094-rebase-conflict-status.jpg?raw=true"/></p>

- `rebase` 이전으로 돌아가려면 `git rebase --abort` 명령어를 이용하면 된다
- 계속 `rebase`를 진행하려면 직접 파일을 수정하고 `git add` 한 후, `git rebase --continue`하면 된다
<p align = "center"><img src = "../imageFiles/095-rebase-conflict-continue.jpg?raw=true"/></p>
<p align = "center"><img src = "../imageFiles/095-rebase-result.jpg?raw=true"/></p>
