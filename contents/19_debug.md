## GIT 도구 - GIT으로 버그찾기(Blame, Bisect)

- GIT에는 `version` 관리 기능 말고도 `project`를 `debugging`하기 위해 사용할 좋은 기능도 갖고 있다
- 개별 `file`에 생긴 모든 변화를 알아낼 수 있기에 `debugging`에 매우 편리하다

### File Annotation(Blame)
- 코드 한 줄 마다 누가, 언제 코드를 작성했는지 확인하려면 `git blame`을 사용하면 된다
- `git blame 파일명`을 입력하면 이를 확인할 수 있고, `git blame -L` 옵션을 활용하면 범위를 제한하여 확인이 가능하다
- `git blame -C -L` 옵션을 활용하면 `file` 이름을 변경한 이력도 확인이 가능하다
- <>

<br>
 <br>

### 이진 탐색(Bisect)
- 문제가 생겼을 때에 확인해야 할 `commit`이 엄청 많다면, 매우 고통스러울 것이다
- 이런 경우에 `bisect`를 이용하면 이진 탐색 `algorithm`으로 문제가 생긴 지점을 빠르게 알 수 있다
- 우선, 문제가 발생하지 않았던 확실한 `version`으로 `checkout` 해야한다
- <>

- 여기서 `git bisect start`를 하고, 문제가 없는 `commit`이니, `git bisect good`을 입력한다
- 이후 문제가 발생한 `commit`으로 다시 `checkout`한 후, `git bisect bad`를 입력한다
- <>

- `bisect`에 의해서 `commit` 사이를 계속 탐색하게 되고, 직접 프로그램을 확인하면서 문제가 발생하는지 확인한다
- 문제가 없으면 `git bisect good` / 문제가 있으면 `git bisect bad`를 사용하자
- `bisect`를 끝까지 따라가다 보면, 문제가 발생한 `version`에 도착할 수 있다
- <>