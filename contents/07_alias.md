## Alias를 이용하여 나만의 단축 명령어를 사용하자
- `git log --oneline --graph --all`처럼 명령어가 매우 길어져 타이핑하기 어려운 경우가 있다
- 이런 경우에는 `alias` 기능을 활용하면, 명령어를 짧게 만들 수 있다
- `git config --global alias.명령어 "단축할 명령어"`를 사용하면 된다
- 또는 `git config --global -e`를 이용해 `editor` 내에서 설정한 후 저장해도 된다
<p align = "center"><img src = "https://github.com/sustainable-git/GIT/blob/main/imageFiles/23-alias.jpg?raw=true"/></p>
<p align = "center"><img src = "https://github.com/sustainable-git/GIT/blob/main/imageFiles/24-alias-try.jpg?raw=true"/></p>
<br>
 <br>
 
### Log를 이쁘게 만들어 보자
- `git log`에는 가시성과 정보성을 향상시킬 수 있는 다양한 기능들이 있다
- 그 중에 하나는 `git log --oneline --graph --all`과 같이 여러개의 `--명령어`를 병렬로 사용하는 것이다
- 또는 `git log --pretty=명령어`구문을 활용하여 사용자가 원하는 정보를 정확하고 눈에 잘 보이게 나타낼 수 있다
<p align = "center"><img src = "https://github.com/sustainable-git/GIT/blob/main/imageFiles/25-log-pretty.jpg?raw=true"/></p>

- 사용 가능한 다양한 `format`은 [GIT](https://git-scm.com/docs/git-log/en) 사이트에서 확인할 수 있다
- 마찬가지로 `alias`를 이용해서 이 `format`을 저장해 차후에도 쉽게 이용 가능하도록 설정하자
- 인터넷에서 다양한 `format`을 검색한 후 본인에게 맞도록 수정해 사용해도 된다. 아래는 예시이다
-  `history = log --color --graph --pretty=format:'%C(yellow)[%ad]%C(reset) %Cred%h%Creset -%C(brightyellow)%d%Creset %C(white)%s %Cgreen(%cr)%C(bold blue)<%an>%Creset' --abbrev-commit --date=short`
<p align = "center"><img src = "https://github.com/sustainable-git/GIT/blob/main/imageFiles/26-log-alias.jpg?raw=true"/></p>
 
