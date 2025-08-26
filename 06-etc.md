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

## pull
  - git pull origin develop --rebase
    - git fetch origin develop
    - git rebase origin/develop : 충돌이 날수있다.

  - git pull origin develop --no-rebase
    - git fetch origin develop
    - git merge origin/develop
      - 3-way-merge 가 되거나 : 충돌이 날수있다.
      - fast-forward-merge 가 되거나 : 충돌 X

  - git pull origin develop --ff-only
    - git fetch origin develop
    - git merge origin/develop : 반드시 fast- forward merge만 진행한다.
      - 3-way-merge 가 되거나 : 충돌이 날수있다.
      - fast-forward-merge 가 되거나 : 충돌 X

  - git pull origin develop 명령어를 입력하면
    - 옵션을 쓰는 경우에도 동일 커밋 히스토리가 만들어 지는 경우 문제없이 진행된다.
    - 옵션을 쓰는 경우에 따라서 다른 커밋 히스토리가 만들어 지는 경우 어떤 옵션을 사용하고 싶은지 개발자에게 질문한다.
    - 근데, 이러한 질문도 받기 싫어? 그러면 config에서 미리 등록해두면 됨.
      - git config pull.rebase true : 선택의 순간이 오면 무조건 rebase
      - git config pull.rebase false : 선택의 순간이 오면 무조건 merge
      - git config pull.ff only : 선택의 순간이 오면 무조건 fast forward only