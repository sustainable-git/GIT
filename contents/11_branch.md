## Branch를 이용해 독립된 공간에서 나만의 작업 공간을 만들자

### Branch 만들고 이동하기
- GIT에는 원래의 코드와 상관없이 "독립적"으로 개발을 진행하고, 해당 부분이 완성되면 "병합"하는 기능이 있다
- 바로 `branch` 기능을 이용한 것인데, 이는 여러 개발자들과 동시에 작업하기 위해 필수적인 기능이다
- `git checkout`을 사용해 `branch`를 만들고자 하는 `version`으로 이동해 보자
- <>

- `git branch 브랜치명`을 하면 `branch`를 만들 수 있고, `git switch 브랜치명`을 입력하여 `branch`로 이동할 수 있다
- <>

- 여기서 어떠한 작업을 하고 나서, `commit`을 하고 나면, 이제 가지가 생겨난 `log`를 관찰할 수 있다
- `alias` 설정이 안되어 있다면, `git log --oneline --graph --all` 을 사용하는 것을 추천한다
- <>

<br>
 <br>

- `ls`를 이용해서 `spanish`와 `master`을 비교해 보면 아래와 같다
- <>
- 
- `branch`를 만듦과 동시에 `switch`를 하기 위해서는 `git switch -C 브랜치명`을 이용하면 된다
- 간단한 작업을 하고 `commit`을 하고 나면, `master`에서도 `branch`가 생겨날 수 있음을 알 수 있다
- <>
- 
<br>
 <br>

### Branch 조회하고 수정하고 삭제하기
- `git log`를 이용해서 `branch`를 확인할 수 있지만, `commit`이 많아지면 식별성이 떨어진다
- `git branch` 옵션을 이용하면 `branch`만 따로 확인이 가능하다
- `git branch --all`을 이용하면 `server`에 저장된 `branch`도 함께 확인할 수 있다
- <>

- `branch`의 이름이 마음에 들지 않을 때에는 `git branch --move 브랜치명 바꿀브랜치명`을 이용하면 된다
- <>

- `branch`를 삭제하는 방법은 `git branch -d 브랜치명`을 이용하면 된다
- <>