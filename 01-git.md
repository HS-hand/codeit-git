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

## 깃 사용법
1. 프로젝트 디렉토리를 깃으로 관리하기 시작한다.
  - git init
  - .git 폴더 생성( 숨김폴더 )

2. 프로젝트 디렉토리는 아래의 3단계로 구분된다.
  - 워킹 디렉토리 (디렉토리)
  - 스테이징 에어리어 (장바구니)
  - 리포지토리 (구매내역)

3. 현재 프로젝트 폴더의 상태 파악
  - git status
  1. 마지막 리포지토리와 스테이징 에어리어의 차이를 보여줌
  2. 스테이징 에어리어와 워킹 디렉토리의 Tracked 파일들의 차이를 보여줌
  3. untracked 파일들을 보여줌 이히히히히

4. 현재 프로젝트 폴더의 상태 저장
  - git commit -m "팀에서 정한 규칙대로"

5. 저장된 기록 확인
  - git log
  - 스크롤 : 화살표 키로 아래로 스크롤
  - q : 종료

6. 다른 저장 기록으로 돌아가기
  - git checkout [커밋 아이디] : head를 왔다 갔다 하는것
  - git checkout [브랜치 이름] : 다시 원래 상태로 돌아오기
  - git config --global init.defaultBranch [기본 브렌치 이름]

7. 브랜치 만들기
  - git branch
  - git branch [브랜치 이름]
  - git config --global init.defaultBranch [기본 브랜치 이름]
  - git checkout [브랜치 이름]
  - 브랜치가 갈라지는 지점 : *base*

8. 브랜치 병합
  - git merge sub : master 브랜치에서, 베이스와 sub 브렌치의 차이를 워킹디렉토리와 SA에 복사하고, 커밋. = 3-way-merge
  - 