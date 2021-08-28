## GIT 설정하기
- `git config --global user.name "이름" && git config --global user.email "이메일"`을 설정해준다. GitHub 아이디가 있는 경우 동일하게 기입하자
<p align = "center"><img src = "../imageFiles/003-window-git-user.jpg?raw=true"/></p>

- `git config --global core.autocrlf input`(Mac), `git config --global core.autocrlf true`(Window)를 기입한다
  - 위는 운영체제에 따른 개행(Mac : LF / Window : CR, LF)의 차이를 처리하기 위함이다
- `git config --global --edit`를 이용해 해당 내용을 확인하거나 수정할 수 있다
<p align = "center"><img src = "../imageFiles/004-window-git-global.jpg?raw=true"/></p>

- 설정을 마친 경우 상황에 따라 `:q`(변경 없이 나가기) `:q!`(변경을 저장하지 않고 나가기) `:wq`(변경을 저장하고 나가기)를 해준다

## Editor에서 GIT 설정하기
Terminal에서 수정하는 것이 불편하다면 다른 Editor를 사용하도록 수정할 수 있다.
- Visual Studio Code를 사용하는 경우
  - `git config --global core.editor "code --wait"`
- Xcode를 사용하는 경우
  - `git config --global core.editor "xed --wait"`
<p align = "center"><img src = "../imageFiles/005-window-editor.jpg?raw=true"/></p>
