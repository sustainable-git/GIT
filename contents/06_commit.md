## Commit하여 GIT에 저장하고, 불러오기
### Staging Area에서 Commit하여 GIT에 저장하기
- `commit`을 하고 싶은 파일이 있다면 해당 파일만 `git add 파일명`를 이용해 `Staging Area`로 옮겨주면 된다
- 현재 폴더에는 `one.txt`와 `.gitignore`이 저장되어 있고, `git add .`을 이용해 모든 파일을 옮겨줬다
- 이후 `git commit -m "커밋 메시지"`를 입력하면 `Staging Area`의 파일들이 `GIT`에 저장된다
<p align = "center"><img src = "../imageFiles/017-git-commit.jpg?raw=true"/></p>

- `git log`명령어를 입력하면, `commit`의 이력을 알 수 있다
<p align = "center"><img src = "../imageFiles/018-git-commit-log.jpg?raw=true"/></p>

<br/><br/>

### 저장된 GIT version 불러오기
- 여러개의 `commit`이 만들어져 있다면, 언제든지 각각의 `version`으로 되돌아갈 수 있다
- 테스트를 위해 `two.txt`와 `three.txt`를 추가해 각각 `commit`하여 총 3개의 `version`을 만들었다
<p align = "center"><img src = "../imageFiles/019-git-commit-3.jpg?raw=true"/></p>
 
 - `git log` 를 이용해 되돌아가고 싶은 `version`의 `hash code`를 7자리 이상 복사해 준다
   - `git log --oneline`을 이용하면 더 간단하게 볼 수 있다
- `git checkout 해시코드`를 입력하면 해당 `version`으로 되돌아갈 수 있다
- 아래와 같이 `second commit`으로 돌아가게 되면 `three.txt`가 흔적도 없이 사라진 것을 확인할 수 있다
<p align = "center"><img src = "../imageFiles/020-git-checkout.jpg?raw=true"/></p>
<p align = "center"><img src = "../imageFiles/021-git-checkout-result.jpg?raw=true"/></p>

- 현재 `thrid commit`이 화면에 나타나고 있지 않은데, `git log --all` 명령어를 사용하면 확인이 가능하다
  - `git log --oneline --graph --all`처럼 여러 옵션을 병렬로 사용하면 가독성을 높일 수 있다
- 다시 `third commit` 상태로 돌아가려면 `git checkout master` 또는 `git checkout 해시코드`를 사용하자
<p align = "center"><img src = "../imageFiles/022-git-checkout-master.jpg?raw=true"/></p>
