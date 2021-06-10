## Reset으로 되돌아가기
### 전체 `file` 되돌리기
- GIT을 사용하다 보면, 이전 `commit` 상태로 돌아가야 할 경우가 있다
- 이런 경우에는 `checkout` 명령어나 `reset` 명령어를 이용해서 돌아가게 된다
- `reset`의 경우에는 `log`에 `commit`을 남기지 않고, 완전히 삭제하면서 돌아갈 때에 주로 사용된다
- (아래의 예시는 `branch`를 남겨둔 상태에서 `reset`을 했기에 `checkout`과 동일하게 `log`에 남겨진다)

### `git reset --soft` : 수정사항을 `Staging Area`에 저장한 채로 `reset`
- `git reset --soft 해시코드` 또는 `git reset --soft HEAD~숫자`를 이용하자
- <>

### `git reset --mixed` : 수정사항을 `Working Directory`에 저장한 채로 `reset`
- `git reset`의 `default` 옵션이 바로 `--mixed` 옵션이다
- `git reset --mixed 해시코드` 또는 `git reset HEAD~1` 등의 방법으로 이용하면 된다
-<>

- `--mixed` 옵션은 수정사항을 `Working Directory`로 옮겨서 저장해 준다
- `git reset HEAD`는 이를 응용한 방법으로, `git restore --staged .`과 동일하게 작동한다
-<>

### `git reset --hard` : 해당 `commit` 상태로 완전히 `reset`
-  `git reset --hard 해시코드` 또는 `git reset --hard HEAD~숫자`를 이용하자
- 완벽히 해당 `commit` 상태로 돌아가기에, `git status`에도 아무런 `file`이 나타나지 않는다
- <>

<br>
 <br>

### 특정 `file`만 되돌리기
- 전체 `file`을 되돌리지 않고, 몇몇 `file`만 이전 `commit`의 상태로 되돌리고 싶을 때가 있다
- 이럴 때에는 `git restore --source=해시코드 파일명` 명령어를 이용하자
- 아래와 같이 `2.txt`가 없는 상태로 `restore` 하게 되면, `2.txt`가 삭제된다
- <>