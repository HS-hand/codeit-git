# Cancel 

## reset
  - git reset --soft HEAD~1
    - 브랜치 범위만 축소된다.
    - 커밋하기 직전으로 회귀
  - git reset --mixed HEAD~1
    - 브랜치 범위만 축소된다. + 스테이징 에어리어에서 리셋
    - 커밋하고 add 하기 직전으로 회귀
  - git reset --hard HEAD~1
    - 브랜치 범위만 축소된다. + 스테이징 에어리어에서 리셋 + 워킹 디렉토리 Tracked 리셋
    - 커밋하고 add 하고 작업하기 직전으로 회귀

  - 기타
    - git reset --hard HEAD~1 = git reset --hard HEAD^
    - git reset --hard HEAD~2 = git reset --hard HEAD^^
    - git reset --hard [커밋 아이디]