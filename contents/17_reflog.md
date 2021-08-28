## GIT 도구 - RefLog
- GIT은 자동으로 `branch`와 `head`가 지난 몇 달 동안 가리켰던 커밋을 모두 `reflog`에 기록한다
- 만약 `reset --hard` 옵션으로 몇몇 `commit`들을 잃어버리더라도, `reflog`를 이용해 다시 돌아올 수 있다
- `git reflog` 는 `git log -g --abbrev-commit --pretty=oneline` 과 동일한 결과를 보여준다
<p align = "center"><img src = ../imageFiles/080-git-reflog.jpg?raw=true"/></p>

- `reflog`는 모두 `local`에서 저장되기 때문에, `sever`에 올리더라도 다른사람이 확인할 수 없다
- `local`에서 `HEAD`가 `n`번 전에 가리켰던 것을 보려면, `git show HEAD@{숫자}`를 입력하면 된다
- 동일하게 특정 시간에 대해서도 조회할 수 있는데, `git show 브랜치명@{시간}`을 입력하면 된다
<p align = "center"><img src = "../imageFiles/081-git-reflog-show.jpg?raw=true"/></p>

- `reflog`에는 3가지 `option`이 있다. `expire`, `delete`, `exists` 이다
- `expire` 옵션은 해당 기간 이전의 모든 `reflog`를 삭제한다
- `delete` 옵션은 하나의 `reflog`를 삭제한다
- `exists` 옵션은 `reflog`가 있는지 점검한다
<p align = "center"><img src = "../imageFiles/082-git-reflog-options.jpg?raw=true"/></p>
<p align = "center"><img src = "../imageFiles/083-git-reflog-expire.jpg?raw=true"/></p>
