# 깃

## 버전 관리 시스템
- 프로젝트 폴더를 버전별로 저장할 수 있는 시스템
- 가장 대표적인 버전 관리 시스템 = 깃

## 깃 설치
- 윈도우 : 설치 프로그램 다운 받아서 설치
- 맥 : Homebrew를 이용해서 설치

## 깃 사용자 설정
- git config --global user.name "깃허브 사용자 이름"
- git config --global user.email "깃허브 계정 이메일"
- git config --global init.defaultBranch [기본 브렌치 이름]

## 깃 사용법
1. 프로젝트 디렉토리를 깃으로 관리하기 시작한다.
  - git init
  - .git 폴더 생성( 숨김폴더 )

2. 프로젝트 디렉토리는 아래의 3단계로 구분된다.
  - 워킹 디렉토리 (디렉토리)
    - Tracked : 스테이징 에어이러에 기록된 파일 및 폴더
    - Untracked : Tracked를 제외한 나머지 전부
  - 스테이징 에어리어 (장바구니)
  - 로컬 리포지토리 (구매내역)

3. 현재 프로젝트 폴더의 상태 파악
  - git status
    1. 로컬 리포지토리와 스테이징 에어리어의 차이를 보여줌
    2. 스테이징 에어리어와 워킹 디렉토리의 Tracked 의 차이를 보여줌
    3. untracked를 보여줌 이히히히히

4. 현재 프로젝트 폴더의 상태 저장
  - git commit -m "메세지"
  - 메시지는 팀에서 정한 규칙대로

5. 저장된 기록 확인
  - git log

6. 다른 저장 기록으로 돌아가기
  - checkout : Head를 이동시킨다.
  - git checkout [브랜치 이름] : 다시 원래 상태로 돌아오기
    - Head가 브랜치를 가리킨다.
  - git checkout [커밋 아이디] : head를 왔다 갔다 하는것
    - Head가 특정 커밋을 가리킨다.
    - Head가 브랜치에서 이찰(detached) 했다.


7. 브랜치 만들기
  - git branch
  - git branch [브랜치 이름]
  - git checkout [브랜치 이름]
  - git branch -d [브랜치 이름] : 브랜치 제거
  - git branch -r  : 트래킹 브랜치의 목록을 보여준다.
  - 브랜치가 갈라지는 지점 : *base commit*
  - 브랜치 범위
    - 브랜치 화살표가 가르키는 마지막 커밋으로부터 찾을 수 있는 모든 부모 커밋을 전부 포함한다.