## GIT 도구 - Stash, Clean

### Stash, 커밋하지 않고 잠시 저장하기
- GIT 에는 작업하고 있던 일을 잠시 저장하고, 나중에 다시 돌아와서 작업을 할 수 있도록 하는 기능을 제공한다
- `tracked` 중인 파일을 수정한 경우 `git stash` 또는 `git stash push -m "스태시 메시지` 명령어를 이용하자
- `stash` 에 수정내역이 저장되고, 해당 파일은 수정 이전으로 되돌아간다
<p align = "center"><img src = "../imageFiles/064-git-stash-push.jpg?raw=true"/></p>

- `untracked` 중인 파일을 수정한 경우에는 `git stash -u` 또는 `git stash --include-untracked` 옵션을 이용한다
- `untracked` 파일까지 모두 `stash`에 저장할 수 있다
<p align = "center"><img src = "../imageFiles/065-git-stash-u.jpg?raw=true"/></p>

- `stash`에 저장하고 싶지만, `staging area`에 파일을 그대로 놔두고 싶은 경우가 있을 수 있다
- 이런 경우에는 `git stash --keep-index` 옵션을 사용하면 된다
<p align = "center"><img src = "../imageFiles/066-git-stash-keep-index.jpg?raw=true"/></p>

<br>
 <br>
 
### Working Directory 청소하기
- `stash`를 사용하다 보면, 작업중인 파일을 `stash`하지 않고 단순히 파일을 치워버리고 싶을 때가 있다
- `working directory`에서 불필요한 파일을 전부 지우려면 `git clean` 명령어를 이용하면 된다
- 추적중이지 않은 정보까지 모두 지우고 싶다면 `git clean -fd` 명령어를 이용하면 된다

<br>
 <br>

### Stash 확인하기
- 이렇게 `stash`에 저장한 것을 확인하려면 `git stash list`를 사용하면 된다
- `stash`는 `stack` 방식으로 저장되기 때문에, 가장 숫자가 낮은 것이 가장 최근에 `stash`한 것이다
<p align = "center"><img src = "../imageFiles/067-git-stash-list.jpg?raw=true"/></p>

- 각 `stash`마다 어떤 변경내역이 있는지 확인하려면 `git stash show 스태시` 를 이용하면 된다
- 자세히 살펴보려면 `git stash show 스태시 --patch` 옵션을 이용하면 된다
<p align = "center"><img src = "../imageFiles/068-git-stash-show.jpg?raw=true"/></p>

<br>
 <br>

### Stash 불러오기
- 저장한 `stash`를 불러오려면 `git stash apply 스태시` 명령어를 이용하면 된다
- 만약 `git stash apply`만 입력하면, `stack`처럼 가장 위에 있는 `stash`를 불러온다
- 참고로 `stash`는 저장한 `branch` 외의 다른 `branch`에서도 불러올 수 있다
<p align = "center"><img src = "../imageFiles/069-git-stash-apply.jpg?raw=true"/></p>

- 또는 `git stash pop`을 이용해서 `stash`를 가져옴과 동시에 삭제할 수도 있다
<p align = "center"><img src = "../imageFiles/070-git-stash-pop.jpg?raw=true"/></p>

<br>
 <br>

### Stash 삭제하기
- `stash`를 삭제하려면 `git stash drop 스태시`를 사용하면 된다
- 만약 모든 `stash`를 전부 삭제하려면, `git stahs clear`를 하면 된다
<p align = "center"><img src = "../imageFiles/071-git-stash-drop.jpg?raw=true"/></p>

<br>
 <br>

### Stash를 적용한 Branch 만들기
- 현재 상태에서 `stash`가 적용된 `branch`를 추가로 만들고 싶을 때가 있다
- `git stash branch 브랜치명` 명령어를 이용하면, `stash`가 적용이 된 `branch`를 만들 수 있다
<p align = "center"><img src = "../imageFiles/072-git-stash-branch.jpg?raw=true"/></p>









