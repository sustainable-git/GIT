<h1 align = "center">🚀GIT 사용법🛰</h1>

<p align = "center"><img src = "https://git-scm.com/images/logo@2x.png"/></p>

## Contents
- [GIT을 사용하기 위한 준비💾](https://github.com/sustainable-git/GIT/blob/main/contents/01_preparation.md)
  - `git --version`
#
- [GIT 설정하기🛠](https://github.com/sustainable-git/GIT/blob/main/contents/02_setting.md)
  - `git config --global user.name "이름"`
  - `git config --global user.email "이메일"`
  - `git config --global --edit"`
    - `git config --global core.autocrlf input`(Mac)
    - `git config --global core.autocrlf true`(Window)
    - `git config --global core.editor "xed --wait"`(Xcode)
    - `git config --global core.editor "code --wait"`(Visual Studio Code)
#
- [GIT 생성하고 삭제하기🗑](https://github.com/sustainable-git/GIT/blob/main/contents/03_init.md)
  -  `git init`
  -  `rm -rf .git`
#
- [Working Directory에서 파일 Track 또는 Untrack 하기👀✨](https://github.com/sustainable-git/GIT/blob/main/contents/04_add.md)
  -  `git add 파일명`
     -  `git add .`
  -  `git rm --cached 파일명`
  -  `echo 파일명 > .gitignore`
     - `echo *.log > .gitignore`
  -  `git status`
     -  `git status -s`
#
- [Staging Area에서 Track된 파일의 변경사항 확인하기🔍](https://github.com/sustainable-git/GIT/blob/main/contents/05_diff.md)
  - `git diff`
    - `git diff --staged`
  - `git difftool`
    - `[diff] tool = vscode` `[difftool "vscode"] cmd = code --wait --diff $LOCAL $REMOTE`
#
- [Commit하여 GIT에 저장하고, 불러오기📥📤](https://github.com/sustainable-git/GIT/blob/main/contents/06_commit.md)
  - `git commit -m "커밋 메시지"`
  - `git log`
    - `git log --oneline --graph --all`
  - `git checkout 해시코드`
#
- [Alias를 이용하여 나만의 단축 명령어를 사용하자✈](https://github.com/sustainable-git/GIT/blob/main/contents/07_alias.md)
  - `git config --global alias.명령어 "단축할 명령어"`
  - `git log --pretty=명령어`
#
- [Log를 이용해 히스토리 조회하기(심화)📑](https://github.com/sustainable-git/GIT/blob/main/contents/08_log.md)
  - `git log 명령어`
    - `git log -숫자`
    - `git log --before="날짜"`
    - `git log --author="이름"`
    - `git log --grep="커밋 메시지"`
    - `git log -S "파일명"`
