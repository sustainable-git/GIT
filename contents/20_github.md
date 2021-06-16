## GitHub - Remote 저장소 활용하기

- `remote` 저장소는 인터넷이나 네트워크 어딘가에 있는 저장소를 말한다
- GIT을 사용하는 목적은 대부분 다른 사람들과 함께 일하기 위해서이고, 그러려면 서로의 작업물을 공유할 수 있어야 한다
- 이럴 때 `GitHub`와 같은 온라인 `remote` 저장소를 활용하면, 쉽고 편리하게 작업내용을 공유할 수 있다

### GitHub Repository 만들기
- GitHub를 이용하기 위해서는, 계정을 만든 뒤 `repository`를 만들어야 한다
<p align = "center"><img src = "https://github.com/sustainable-git/GIT/blob/main/imageFiles/100-github-new.jpg?raw=true"/></p>

<br>
 <br>

### Remote 저장소 확인하고 등록하기
- `git remote` 명령어를 사용하면, `remote` 저장소가 있는지 확인할 수 있다
- 저장소를 등록하지 않았다면, 아무것도 나오지 않는다
<p align = "center"><img src = "https://github.com/sustainable-git/GIT/blob/main/imageFiles/101-git-remote-v.jpg?raw=true"/></p>

- 저장소를 등록하려면 `repository`의 주소를 알아야 한다
- `repository` 창으로 돌아가 오른쪽의 클립보드에 복사 버튼을 누른 후 `terminal`로 돌아온다
- `git clone 주소` 명령어를 이용해서 `remote` 저장소의 내용을 복사해주자
<p align = "center"><img src = "https://github.com/sustainable-git/GIT/blob/main/imageFiles/102-git-remote-address.jpg?raw=true"/></p>
<p align = "center"><img src = "https://github.com/sustainable-git/GIT/blob/main/imageFiles/103-git-clone.jpg?raw=true"/></p>

<br>
 <br>

### Remote 저장소에 commit 저장하기
- `remote` 저장소에 `commit`을 저장하려면 `git push` 명령어를 이용하면 된다
- `push`가 완료되었다면, GitHub `repository`에 `commit`이 저장된 것을 확인할 수 있다
<p align = "center"><img src = "https://github.com/sustainable-git/GIT/blob/main/imageFiles/104-git-push.jpg?raw=true"/></p>
<p align = "center"><img src = "https://github.com/sustainable-git/GIT/blob/main/imageFiles/105-git-push-result.jpg?raw=true"/></p>

<br>
 <br>

### Remote 저장소에서 commit 가져오기
- `remote` 저장소에 저장된 사항을 불러오려면 `git pull` 명령어를 이용하면 된다
- 만약 변경사항이 없다면 아래와 같이 나타난다
<p align = "center"><img src = "https://github.com/sustainable-git/GIT/blob/main/imageFiles/106-git-pull.jpg?raw=true"/></p>

- `README.MD` 파일을 추가하는 변경사항을 만들고, `git pull`을 사용해보자
<p align = "center"><img src = "https://github.com/sustainable-git/GIT/blob/main/imageFiles/107-git-readme.jpg?raw=true"/></p>
<p align = "center"><img src = "https://github.com/sustainable-git/GIT/blob/main/imageFiles/108-git-readme2.jpg?raw=true"/></p>

- `git log`를 통해 확인해보면, `remote` 저장소로부터 `README.MD`의 `commit`을 가져온 것을 알 수 있다
<p align = "center"><img src = "https://github.com/sustainable-git/GIT/blob/main/imageFiles/109-pull-log.jpg?raw=true"/></p>

- `git pull` 이외에도, `git fetch` 명령어를 사용할 수 있다
- 이 경우에는 추가된 부분이 `merge`가 되지 않았기 때문에 추후에 `merge`해 주어야 한다
<p align = "center"><img src = "https://github.com/sustainable-git/GIT/blob/main/imageFiles/110-git-fetch.jpg?raw=true"/></p>
