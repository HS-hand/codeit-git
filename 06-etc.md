# 기타

## clone
  - git clone [리모트 리포지토리 주소] 
  : 위 명령어는 다음 명령어를 차례대로 실행한 결과와 같다.
    - 상황 : 내가 처음 팀에 합류한 상황.
    - 작업
      - 프로젝트 폴더를 생성한다.
      - git init, git remote add origin [리모트 리포지토리 주소]
      - git fetch : 리모트 리포지토리에 있는 모든 브랜치의 트래킹 브랜치를 생성.
        - 현재 시점의 브랜치 상태 : origin/main , origin/develop
      - git checkout -t origin/develop
        - origin/develop 과 동일한 범위를 가지는 develop 브랜칠르 생성하고 checkout
      - 작업을 진행한다.

  => 그니까 처음 팀에 합류했다? 그러면 저거 git clone [리모드 리포지토리 주소] 하면 됨.