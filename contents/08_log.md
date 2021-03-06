## Log를 이용해 히스토리 조회하기(심화)
- `git log`에는 유용한 기능이 정말 다양하다
- `git log --patch`는 각 커밋의 `diff`결과를 보여준다. 최근 2개의 결과만 보려면 `-2`를 붙이면 된다
<p align = "center"><img src = "../imageFiles/027-log-patch.jpg?raw=true"/></p>

- `git log --stat`은 각 커밋의 통계 정보를 조회할 수 있다
<p align = "center"><img src = "../imageFiles/028-log-stat.jpg?raw=true"/></p>
<br>
 <br>
 
### 조회 범위를 제한하는 옵션
- `git log`에는 특정한 조건의 버전만 검색해서 조회하는 기능이 있다

| 옵션 | 설명 |
|---|:---:|
| `-n` | 최근 n 개의 커밋만 조회 |
| `--since`, `--after` | 명시한 날짜 이후의 커밋만 조회 |
| `--until`, `--before` | 명시한 날짜 이전의 커밋만 조회 |
| `--author` | 입력한 저자의 커밋만 조회 |
| `--committer` | 입력한 커미터의 커밋만 조회 |
| `--grep` | 커밋 메시지 안의 텍스트를 검색 |
| `-S` | 커밋 변경 내용 안의 텍스트를 검색 |

<br>

<p align = "center"><img src = "/imageFiles/029-log-options.jpg?raw=true"/></p>

- `git log`를 하면서 두 커밋 사이의 변경사항을 확인할 때에는 아래처럼 `git diff`를 이용하면 된다
<p align = "center"><img src = "../imageFiles/030-correct-typos.jpg?raw=true"/></p>
