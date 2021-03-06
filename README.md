<h1 align = "center">๐GIT ์ฌ์ฉ๋ฒ๐ฐ</h1>

<p align = "center"><img src = "https://git-scm.com/images/logo@2x.png"/></p>

## Contents
- [GIT์ ์ฌ์ฉํ๊ธฐ ์ํ ์ค๋น๐พ](./contents/01_preparation.md)
  - `git --version`
#
- [GIT ์ค์ ํ๊ธฐ๐ ](./contents/02_setting.md)
  - `git config --global user.name "์ด๋ฆ"`
  - `git config --global user.email "์ด๋ฉ์ผ"`
  - `git config --global --edit"`
    - `git config --global core.autocrlf input`(Mac)
    - `git config --global core.autocrlf true`(Window)
    - `git config --global core.editor "xed --wait"`(Xcode)
    - `git config --global core.editor "code --wait"`(Visual Studio Code)
#
- [GIT ์์ฑํ๊ณ  ์ญ์ ํ๊ธฐ๐](./contents/03_init.md)
  -  `git init`
  -  `rm -rf .git`
#
- [Working Directory์์ ํ์ผ Track ๋๋ Untrack ํ๊ธฐ๐โจ](./contents/04_add.md)
  -  `git add ํ์ผ๋ช`
     -  `git add .`
  -  `git rm --cached ํ์ผ๋ช`
  -  `echo ํ์ผ๋ช > .gitignore`
     - `echo *.log > .gitignore`
  -  `git status`
     -  `git status -s`
#
- [Staging Area์์ Track๋ ํ์ผ์ ๋ณ๊ฒฝ์ฌํญ ํ์ธํ๊ธฐ๐](./contents/05_diff.md)
  - `git diff`
    - `git diff --staged`
  - `git difftool`
    - `[diff] tool = vscode` `[difftool "vscode"] cmd = code --wait --diff $LOCAL $REMOTE`
#
- [Commitํ์ฌ GIT์ ์ ์ฅํ๊ณ , ๋ถ๋ฌ์ค๊ธฐ๐ฅ๐ค](./contents/06_commit.md)
  - `git commit -m "์ปค๋ฐ ๋ฉ์์ง"`
  - `git log`
    - `git log --oneline --graph --all`
  - `git checkout ํด์์ฝ๋`
#
- [Alias๋ฅผ ์ด์ฉํ์ฌ ๋๋ง์ ๋จ์ถ ๋ช๋ น์ด๋ฅผ ์ฌ์ฉํ์โ](./contents/07_alias.md)
  - `git config --global alias.๋ช๋ น์ด "๋จ์ถํ  ๋ช๋ น์ด"`
  - `git log --pretty=๋ช๋ น์ด`
#
- [Log๋ฅผ ์ด์ฉํด ํ์คํ ๋ฆฌ ์กฐํํ๊ธฐ(์ฌํ)๐](./contents/08_log.md)
  - `git log ๋ช๋ น์ด`
    - `git log -์ซ์`
    - `git log --before="๋ ์ง"`
    - `git log --author="์ด๋ฆ"`
    - `git log --grep="์ปค๋ฐ ๋ฉ์์ง"`
    - `git log -S "ํ์ผ๋ช"`
#
- [[Control-Z] ๋๋๋ฆฌ๊ธฐโฉ](./contents/09_undo.md)
  - `git commit --amend`
  - `git restore -- ํ์ผ๋ช`
#
- [Tag๋ฅผ ์ด์ฉํด ๊ฐ๋จํ๊ฒ ๋ฒ์  ํ์ํ๊ธฐโ](./contents/10_tag.md)
  - `git tag`
    - `git tag -l ํ๊ทธ๋ช`
    - `git tag -d ํ๊ทธ๋ช`
  - `git tag ํ๊ทธ๋ช`
    - `git tag ํ๊ทธ๋ช ํด์์ฝ๋ -a -m "ํ๊ทธ ๋ฉ์์ง"`
  - `git show ํด์์ฝ๋`
    - `git show head --name-only` 
#
- [Branch๋ฅผ ์ด์ฉํด ๋๋ฆฝ๋ ๊ณต๊ฐ์์ ๋๋ง์ ์์ ๊ณต๊ฐ์ ๋ง๋ค์๐](./contents/11_branch.md)
  - `git branch`
    - `git branch -v`
    - `git branch -all`
    - `git branch --merged`
    - `git branch --no-merged`
  - `git branch ๋ธ๋์น๋ช`
    - `git switch -C ๋ธ๋์น๋ช`
  - `git branch --move ๋ธ๋์น๋ช ๋ฐ๊ฟ๋ธ๋์น๋ช`
  - `git branch -d ๋ธ๋์น๋ช`
#
- [Merge! ํ๋์ Branch๋ก ๋ณํฉํ๊ธฐ๐](./contents/12_merge.md)
  - `git merge ๋ธ๋์น๋ช`
    - `git merge --no-ff`

#
- [Merge Conflict์ Merge Tool๐งท](./contents/13_conflict.md)
  - `git merge --abort`
  - `git merge --continue`
  - `git mergetool`
    - `[merge] tool = vscode` `[mergetool "vscode"] cmd = code --wait $MERGED`
#
- [Rebase์ Cherry-Pick๐](./contents/14_rebase.md)
  - `git rebase ๋ธ๋์น๋ช`
    - `git rebase ๋ธ๋์น๋ช ๋ธ๋์น๋ช`
    - `git rebase --onto ๋ธ๋์น๋ช ๋ธ๋์น๋ช ๋ธ๋์น๋ช`
    - `git rebase --abort`
    - `git rebase --continue`
  - `git cherry-pick ํด์์ฝ๋`
#
- [GIT ๋๊ตฌ - Stash, Cleanโ](./contents/15_stash.md)
  - `git stash push -m "์คํ์ ๋ฉ์์ง"`
    - `git stash`
    - `git stash -u`
    - `git stash --keep-index`
  - `git stash list`
    - `git stash show ์คํ์`
    - `git stash show ์คํ์ --patch`
  - `git stach apply ์คํ์`
    - `git stash pop ์คํ์`
  - `git stash drop ์คํ์`
    - `git stash clear`
  - `git stash branch ๋ธ๋์น๋ช`
  - `git clean`
    - `git clean -fd`
    - `git clean -x`
    - `git clean -d -n`
#
- [Reset์ผ๋ก ๋๋์๊ฐ๊ธฐโฎ](./contents/16_reset.md)
  - `git reset`
    - `git reset --soft ํด์์ฝ๋`
    - `git reset --hard ํด์์ฝ๋`
  - `git restore --source=ํด์์ฝ๋ ํ์ผ๋ช`
  - `git revert ํด์์ฝ๋`
#
- [GIT ๋๊ตฌ - RefLog๐](./contents/17_reflog.md)
  - `git reflog`
    - `git reflog expire --expire=์๊ฐ --all`
  - `git show HEAD@{์ซ์}`
  - `git show ๋ธ๋์น๋ช@{์๊ฐ}`
#
- [Rebase -i ์ต์์ผ๋ก Commit ์์ ํ๊ธฐโ](./contents/18_rebase_i.md)
  - `git rebase -i`
    - `git rebase --abort`
    - `git rebase --continue`
#
- [GIT ๋๊ตฌ - GIT์ผ๋ก ๋ฒ๊ทธ์ฐพ๊ธฐ(Blame, Bisect)๐](./contents/19_debug.md)
  - `git blame ํ์ผ๋ช`
    - `git blame -C -L ์ซ์,์ซ์ ํ์ผ๋ช`
  - `git bisect start`
    - `git bisect good`
    - `git bisect bad`
#
- [GitHub - Remote ์ ์ฅ์ ํ์ฉํ๊ธฐโ](./contents/20_github.md)
  - `git remote`
    - `git remote -v`
    - `git remote add origin ์ฃผ์`
    - `git remote remove ์ฃผ์`
  - `git clone ์ฃผ์`
  - `git push`
  - `git pull`
  - `git fetch`

#
- [์๋๋ฆฌ์ค - Pull request](./contents/22_scenario1.md)

#
- [Git๊ณผ Terminal ์ปค์คํ ์ธํโ๏ธ](./contents/21_custom.md)
  - `git config --global`  
