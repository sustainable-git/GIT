## Staging Area에서 파일 Track 또는 Untrack 하기
- track 하려는 파일이 있다면 `git add 파일명`을 입력한다
- `one.txt`라는 테스트 파일을 만들고, `git add one.txt`하면 아래와 같다
<p align = "center"><img src = "https://github.com/sustainable-git/GIT/blob/main/imageFiles/08-git-add.jpg?raw=true"/></p>
 
- 현재 GIT의 상태를 확인하기 위해서는 `git status`를 이용하면 된다
- `git add`를 하기 전과 후의 `git status` 결과가 바뀌었다는 것을 알 수 있다
<p align = "center"><img src = "https://github.com/sustainable-git/GIT/blob/main/imageFiles/09-git-add-status.jpg?raw=true"/></p>

- 파일을 untrack 하기 위해서는 `git rm --cached 파일명`을 입력하면 된다
<p align = "center"><img src = "https://github.com/sustainable-git/GIT/blob/main/imageFiles/10-git-rm-cached.jpg?raw=true"/></p>

### gitignore를 이용해 특정 파일을 항상 Untrack 하기
- GIT에 포함하고 싶지 않는 파일들을 untrack 하기 위해서는 gitignore을 이용하는 것이 좋다
- `log.log`를 항상 untrack 하기 위해서는 `.gitignore`파일을 만들고, 그 내부에 `log.log`를 적어놓으면 된다
- `git status`를 통해 확인해 보면, `log.log`는 이제 확인할 수 없으며, 항상 untrack 된 상태로 존재하게 된다
<p align = "center"><img src = "https://github.com/sustainable-git/GIT/blob/main/imageFiles/11-git-ignore.jpg?raw=true"/></p>
