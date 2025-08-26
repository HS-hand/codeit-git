# Cancel 

## reset : 이미 완료된 커밋을 취소
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

## Stash : 스테이징 에어리어에서 진행된 작업을 잠시 취소
- git stash : 현재 스테이징 에어리어의 상태를 잠시 옆으로 치워놓는다.
- git stash drop : 옆에 잠시 치워둔 상태를 제거해버린다.
- git stash pop : 옆에 잠시 치워둔 상태를 다시 스테이징 에어리어에 덮어쓴다.