# Rebase

## git rebase []
  - 3-way-merge가 예상되는 상황인 경우, commit 히스토리를 깔끔하게 유지하기 위해서 사용.
  - sub 브랜치에서 git rebase main 명령어를 실행
    - sub 브랜치가 main 브랜치를 잡아먹는(?) 느낌
  - base 커밋을 기준으로 sub 브랜치와 차이를 차례대로 계산해서 순차적으로 실행.
  - main 브랜치로 이동한 후 sub 브랜치를 fast-forward-merge한다.

