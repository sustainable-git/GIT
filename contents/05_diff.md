## Staging Area에서 track된 파일의 변경사항 확인하기
- `one.txt`에 `firstLine`이라는 글자가 들어있는 채로 `git add`가 되어 있다
- 때문에 `one.txt`는 `Working Directory`에서 `Staging Area`로 위치가 변경된 상태이다
- `git add` 전 후의 파일의 변경사항을 확인하기 위해서는 `git diff --staged`를 입력하면 된다
- `+firstLine`에서 `firstLine`이라는 글자가 추가되었음을 알 수 있다
- <>

- 이 상태에서 `echo secondLine > one.txt`를 입력하여 `firstLine`을 지우고, `secondLine`을 추가해 보았다
- `git status -s`로 확인하면 `one.txt`에 변경사항이 발생했음을 알 수 있다
  - 한 번 `git add`가 된 파일은 GIT에서 해당 파일을 지속해서 `track`하게 되기에 변경사항을 확인할 수 있다
- 이 상태에서 `git diff`를 하게 되면 `-firstLine`에서 해당 내용이 지워졌고, `+secondLine`에서 해당 내용이 추가되었음을 알 수 있다
- <>

### difftool 설정하기
- `diff`를 좀 더 가시적으로 확인하는 방법이 있다
- `git difftool`을 입력하게 되면 `vimdiff`에서 확인이 가능하다
- <>
- <>

- `editor`에서 확인하는 방법도 있다
- `git config --global -e`에서 아래의 명령어를 기입하고 저장하자
- `[diff] tool = vscode` `[difftool "vscode"] cmd = code --wait --diff $LOCAL $REMOTE`
- <>
