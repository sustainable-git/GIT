## Merge Conflict와 Merge Tool

### Merge Conflict
- `merge`를 하려고 하는 과정에서, 두 `branch`가 동일한 `file`을 수정했다면, `conflict`가 발생한다
- 아래의 `test case`를 살펴보자. `master branch`와 `fix branch`가 동일한 파일을 수정한 경우이다
<p align = "center"><img src = "https://github.com/sustainable-git/GIT/blob/main/imageFiles/53-modify-same-file.jpg?raw=true"/></p>

- 이런 상황에서 `merge`를 하게 되면, `merge conflict`가 발생하게 된다
<p align = "center"><img src = "https://github.com/sustainable-git/GIT/blob/main/imageFiles/54-merge-conflict.jpg?raw=true"/></p>

- 만약 `merge` 를 취소하고 싶다면 `git merge --abort`명령어를 사용하면 된다
<p align = "center"><img src = "https://github.com/sustainable-git/GIT/blob/main/imageFiles/55-merge-abort.jpg?raw=true"/></p>

- 또는 `conflict`가 발생한 부분을 수정하고 `merge`를 완료할 수도 있다
- `merge conflict`가 발생한 `file`을 열어보면, 두 `branch`의 수정사항이 모두 적혀져 있는 것을 볼 수 있다
- 해당 파일을 직접 수정한 후, 저장하고 나서 `git add` 하고, `git merge --continue` 하면 `conflict`가 해결된다 
<p align = "center"><img src = "https://github.com/sustainable-git/GIT/blob/main/imageFiles/56-conflict-result.jpg?raw=true"/></p>
<p align = "center"><img src = "https://github.com/sustainable-git/GIT/blob/main/imageFiles/57-merge-continue.jpg?raw=true"/></p>
<p align = "center"><img src = "https://github.com/sustainable-git/GIT/blob/main/imageFiles/58-after-merge.jpg?raw=true"/></p>

<br>
 <br>

### Merge Tool 설정하고 사용해보기
- `merge conflict`가 발생했을 때, 직접 해당 파일을 직접 수정하지 않고, `editor`를 이용해 수정하는 방법이 있다
- `git config --global -e`에서 아래의 명령어를 기입하고 저장하자 (`visual studio code`가 있는 경우에 한함)
- `[merge] tool = vscode` `[mergetool "vscode"] cmd = code --wait $MERGED`
<p align = "center"><img src = "https://github.com/sustainable-git/GIT/blob/main/imageFiles/59-mergetool-setting.jpg?raw=true"/></p>

- `merge tool`을 설정하고 `merge conflict`가 발생했다면, `git mergetool` 명령어를 입력해보자
- `vs code`에서 제공하는 4가지 `option`들을 볼 수 있는데, 이를 활용하여 변경사항을 만든 후 저장하면 된다
<p align = "center"><img src = "https://github.com/sustainable-git/GIT/blob/main/imageFiles/60-mergetool.jpg?raw=true"/></p>
