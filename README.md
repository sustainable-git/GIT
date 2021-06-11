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
#
- [[Control-Z] 되돌리기↩](https://github.com/sustainable-git/GIT/blob/main/contents/09_undo.md)
  - `git commit --amend`
  - `git restore -- 파일명`
#
- [Tag를 이용해 간단하게 버전 표시하기✒](https://github.com/sustainable-git/GIT/blob/main/contents/10_tag.md)
  - `git tag`
    - `git tag -l 태그명`
    - `git tag -d 태그명`
  - `git tag 태그명`
    - `git tag 태그명 해시코드 -a -m "태그 메시지"`
  - `git show 해시코드`
#
- [Branch를 이용해 독립된 공간에서 나만의 작업 공간을 만들자🏗](https://github.com/sustainable-git/GIT/blob/main/contents/11_branch.md)
  - `git branch`
    - `git branch -v`
    - `git branch -all`
    - `git branch --merged`
    - `git branch --no-merged`
  - `git branch 브랜치명`
    - `git switch -C 브랜치명`
  - `git branch --move 브랜치명 바꿀브랜치명`
  - `git branch -d 브랜치명`
#
- [Merge! 하나의 Branch로 병합하기🔗](https://github.com/sustainable-git/GIT/blob/main/contents/12_merge.md)
  - `git merge 브랜치명`
    - `git merge --no-ff`

#
- [Merge Conflict와 Merge Tool🧷](https://github.com/sustainable-git/GIT/blob/main/contents/13_conflict.md)
  - `git merge --abort`
  - `git merge --continue`
  - `git mergetool`
    - `[merge] tool = vscode` `[mergetool "vscode"] cmd = code --wait $MERGED`
#
- [Rebase와 Cherry-Pick🍒](https://github.com/sustainable-git/GIT/blob/main/contents/14_rebase.md)
  - `git rebase 브랜치명`
    - `git rebase 브랜치명 브랜치명`
    - `git rebase --onto 브랜치명 브랜치명 브랜치명`
  - `git cherry-pick 해시코드`
#
- [GIT 도구 - Stash, Clean⛏](https://github.com/sustainable-git/GIT/blob/main/contents/15_stash.md)
  - `git stash push -m "스태시 메시지"`
    - `git stash`
    - `git stash -u`
    - `git stash --keep-index`
  - `git stash list`
    - `git stash show 스태시`
    - `git stash show 스태시 --patch`
  - `git stach apply 스태시`
    - `git stash pop 스태시`
  - `git stash drop 스태시`
    - `git stash clear`
  - `git stash branch 브랜치명`
  - `git clean`
    - `git clean -fd`
    - `git clean -x`
    - `git clean -d -n`
#
- [Reset으로 되돌아가기⏮](https://github.com/sustainable-git/GIT/blob/main/contents/16_reset.md)
  - `git reset`
    - `git reset --soft 해시코드`
    - `git reset --hard 해시코드`
  - `git restore --source=해시코드 파일명`
  - `git revert 해시코드`
#
- [GIT 도구 - RefLog📜](https://github.com/sustainable-git/GIT/blob/main/contents/17_reflog.md)
  - `git reflog`
    - `git reflog expire --expire=시간 --all`
  - `git show HEAD@{숫자}`
  - `git show 브랜치명@{시간}`
