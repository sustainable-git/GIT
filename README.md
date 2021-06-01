<h1 align = "center">🚀GIT 사용법🛰</h1>

<p align = "center"><img src = "https://git-scm.com/images/logo@2x.png" width="240"/></p>

## GIT을 사용하기 위한 준비
- 본인의 PC에 GIT이 있는지 먼저 확인할 것
  - Terminal(Mac) 또는 CMD(windows)에서 git --version 명령어 입력하기

- Mac을 사용하는 경우
  - Apple Git이 탑재된 상태로 출고되기 때문에 다운받을 필요가 없다
  - 단, 최신버전으로 업데이트할 필요가 있을 수도 있다

- Windows를 사용하는 경우
  - GIT이 없다면 [CMDER](https://cmder.net/)을 다운받자(GIT을 포함해 다운받기 위해 Download Full을 클릭)
  - CMD에서는 git의 버전이 나오지 않지만, CMDER에서는 잘 나오는 것을 볼 수 있다
<p align = "center"><img src = "https://github.com/sustainable-git/git/blob/main/imageFiles/01-window-gitversion.jpg?raw=true"/> <img src = "https://github.com/sustainable-git/git/blob/main/imageFiles/02-window-gitversion2.jpg?raw=true" /></p>

## GIT 설정하기
- git config --global user.name "이름" && git config --global user.email "이메일"을 설정해준다. GitHub 아이디가 있는 경우 동일하게 기입하자
<p align = "center"><img src = ""/></p>

- git config --global core.autocrlf input(Mac), git config --global core.autocrlf true(Window)를 기입한다
  - 위는 운영체제에 따른 개행(Mac : LF / Window : CR, LF)의 차이를 처리하기 위함이다
- git config --global --edit를 이용해 해당 내용을 확인하거나 수정할 수 있다
<p align = "center"><img src = "https://github.com/sustainable-git/GIT/blob/main/imageFiles/04-window-git-global.jpg?raw=true"/></p>

- 설정을 마친 경우 상황에 따라 :q(변경 없이 나가기) :q!(변경을 저장하지 않고 나가기) :wq(변경을 저장하고 나가기)를 해준다

## Editor에서 GIT 설정하기
Terminal에서 수정하는 것이 불편하다면 다른 Editor를 사용하도록 수정할 수 있다.
- Visual Studio Code를 사용하는 경우
  - git config --global core.editor "code --wait"
- Xcode를 사용하는 경우
  - git config --global core.editor "xed --wait"
<p align = "center"><img src = "https://github.com/sustainable-git/GIT/blob/main/imageFiles/05-window-editor.jpg?raw=true"/></p>
