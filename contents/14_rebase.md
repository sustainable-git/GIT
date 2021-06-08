## Rebase와 Cherry-Pick

### Rebase! 하나의 Branch로 병합하기
- GIT에서 한 `branch`에서 다른 `branch`로 합치는 방법은 2가지이다. 하나는 `merge`, 다른 하나는 `rebase`이다
- 아래와 같이 `master branch`위에 있지 않은 `branch`는 `fast-forward merge`할 수 없다
- 하지만 `git rebase 브랜치명` 명령어를 입력하면, 하나의 `branch`로 합쳐지면서 `fast-forward merge`가 가능해진다
-<>

<br>
 <br>

### Rebase --Onto
- `rebase`는 단순히 `branch`를 합치는 것만 아니라 다른 용도로도 사용할 수 있다
- `rebase --onto` 명령어를 이용하면 여러 `branch`가 섞여있는 와중에도, 특정 `branch`만 `rebase`가 가능하다
-<>

<br>
 <br>

### Cherry-Pick
- GIT에는 특정 `commit`만 미리 `rebase`할 수 있는 기능이 있다
- `git cherry-pick 해시태그`를 입력하면 해당 `commit`만 `rebase` 가능하다
- <>
