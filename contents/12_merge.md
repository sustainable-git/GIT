## Merge! 하나의 Branch로 병합하기

### Fast-Forward Merge
- `branch`에서의 작업이 완료하였다면, `merge`를 이용하여 `branch`들을 병합할 수 있다
- `master branch` 위에 있는 `branch`를 빠르게 병합하려면 `git merge 브랜치명`을 입력하면 된다
- <>

### no-ff
- `fast-forward merge`를 하고 `branch` 지워버리면, 해당 `branch`의 존재 자체를 알 수가 없다
- `merge`한 흔적을 `history`로 남기고 싶을 때에는 `--no-ff` 옵션을 이용하면 된다
- 테스트를 위해 `branch` 하나를 더 만들어 보자
- <>

- `merge`를 위해 `master branch`로 이동한 후 `git merge 브랜치명 --no-ff`를 입력하면 된다
- 이렇게 하면 `fast-forward merge`와는 다르게 `log`에 `merge`한 흔적이 남게 된다
- <>

### Three-Way Merge
- `master branch` 위에 있지 않은 `branch`와 병합을 하려면 어떻게 해야할까?
- 위와 마찬가지로 `git merge 브랜치명`을 입력하면 `three-way merge`가 된다
- <>