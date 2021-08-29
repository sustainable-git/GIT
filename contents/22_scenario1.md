## 시나리오 - Pull request
- 협업을 하다 보면, 타인 또는 조직의 repository를 공용으로 작업해야 할 때가 있다
- 이런 경우, 나에게 권한이 주어지지 않아 `pull request`를 이용해 작업을 하게 되는 경우가 생긴다
- 또한, main이 아닌 특정한 `branch`에서만 개발하도록 강제하는 경우도 있다
- 예상되는 시나리오를 따라서 문제를 해결해보자

<br>
 <br>

## 예상되는 에러
- `git push -f` 옵션을 사용할 수 없다
    - 나에게 repository를 변경할 권한이 없기 때문에, forced push가 불가능하다
    - 때문에 한 번 실수를 하게 되면, 매우 난감해진다
- `pull request`에서 발생하는 문제 [[참고 사이트](https://meetup.toast.com/posts/122)]
    - github에서 `pull request`를 `merge`하는 데에는 `Merge`, `Squash and merge`, `Rebase and merge` 세 가지 방법을 지원한다
    - 각각의 방법에 따라 다양한 conflict가 발생할 수 있다
- `branch`에 익숙하지 않아서 발생하는 문제
    - `branch`를 제대로 사용하지 않으면, origin 또는 upstream의 모든 변경사항을 `fetch`받는 실수를 할 수 있다
    - `git log --oneline --graph --all`을 이용해 바라보면 쓸모없는 commit까지 모두 받아버려 수정이 어려워졌다는 것을 알 수 있다

<br>
 <br>

## 시나리오
### Repository fork
- 가장 먼저 우리가 해결해야 하는 repository를 fork해야 한다
- 우리는 이 repository를 `upstream` 이라고 부른다
- upstream에서 Fork 버튼을 누르면 Repositories에 동일한 repository가 하나 생긴다
- 우리는 이 repository를 `downstream` 또는 `origin` 이라고 부른다

|upstream|origin|
|:-:|:-:|
|<img 114>|<img 115>|

<br>
 <br>

### Origin clone branch
- 작업을 하기 위해서 `origin`에서 `local`로 `clone`해야 한다
- 하지만, 우리에게 배정된 특정 `branch`가 있을 경우에는 옵션을 더 적용해야 한다
- 때문에 `git clone -b 브랜치명 --single-branch 주소` 명령어를 이용해야 한다
- 여기서 `git branch -v`를 해보면 main도 없이 우리가 받고자 했던 `branch`만 존재한다는 것을 알 수 있다

<img 116>
<br>
 <br>

### 작업 branch 생성
- 우리만의 `branch` 이더라도 해당 `branch`를 바로 사용하지는 않는다
- 조직에서 우리에게 부여한 `branch`가 우리의 `main`이기 때문에, 여기서 새로운 `branch`를 추가로 만들어 추후에 `merge`하는 것이 옳다
- 대부분 `dev branch`를 만들어 작업한다

<img 117>
<br>
 <br>


### 작업후 origin에 push
- 어떠한 작업을 마치고 `origin`에 `push`할 때에도 옵션이 붙는다
- 이 때, 우리에게 배정된 `FrontPage` `branch`에 적용하면 안된다
- 신중하게 우리가 만든 `dev` `branch`로 `git push origin 브랜치명`을 반드시 입력해주자

<img 118><img 119>
<br>
 <br>

### Upstream로 pull request
- `origin`의 repository로 오면 2가지 변화가 생긴다
    - `dev` `branch`가 생겼다
    - `pull request`를 보낼 수 있다
- 여기서 `Compare & pull request`를 눌러주자
- 이 부분에서 가장 중요한 것은 `base`와 `compare`가 잘 적용되었는지 확인하는 것이다
- `Create pull request`를 보내고 나면, 끝이다

<img 120>
<img 121>
<br>
 <br>
 
### Upstream에서 pull
- 이 부분은 `upstream`의 관리자가 보는 내용이다
- `downstream`이 `pull request`를 잘 보내었는지 확인하고, 이를 수용하거나 거절할 수 있다
- 여기서 `upstream`은 3가지 방식으로 `merge`할 수 있는데, `Rebase and merge` 방식으로 한다고 가정하겠다

<img 122>
<img 123>
<br>
 <br>
 
### Origin에 필요 없어진 branch 삭제
- 이제 `dev` `branch`는 필요 없으므로 삭제해 주어야 한다
- `git branch -D 브랜치명`을 입력해서 `local`에서 삭제해 준다
- 이후 `git push origin -d 브랜치명`을 입력해서 `origin`에서 삭제해 준다

<img 124>
<br>
 <br>
 
### Local에서 upstream 가져오기
- 현재 `local`에는 `upstream`이 등록되어 있지 않기에 먼저 `git remote add upstream`을 해야 한다
- 이후 `git fetch upstream 브랜치명`을 이용해 `upstream`의 특정 `branch`만 `fetch`하자
- 여기서 `git rebase upstrea/브랜치명`으로 `local`을 `upstream`과 동기화 해주면 된다

<img 125>
<br>
 <br>
 
### Local에서 origin 동기화
- `git log`를 보면 origin만 따로 있는 것을 볼 수 있다
- 여기서 `git push -f origin 브랜치명` 명령으로 동기화하면 모든 작업이 완료된다

<img 126><img 127>
