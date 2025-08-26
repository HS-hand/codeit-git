# Github

## 깃허브란?
 - 깃으로 관리되는 프로젝트를 저장하고 공유할 수 있는 클라우드 서비스

## 인증
  - 유저 아이디, 토큰

  - 토큰을 로컬에 저장하고 사용
    - 인증 초기화
      - git config --global --unset credential.helper

    - 인증 등록
      1. 보안에 취약한 방법
        - git config --global credential.helper store
        - 토큰을 암호화하지 않고 평문 그대로 저장
        - MAC : ~/.git-credentials 파일에 저장
        - Window : C:/Users/[사용자 이름]/.git-credentials 파일에 저장.

      2. 보안에 좋지만 귀찮은 방법
        - git config --global credential.helper cache --timeout=3600
        - 토큰을 메모리에 임시로 저장.

      3. 보안에 좋은 방법 => 결론은 이걸 쓰는거에요
        - 토큰을 암호화 하여 저장
        - MAC : git config --global credential.helper osxkeychain
        - Window : 자동으로 된다.. git config --global credential.helper manager

## 로컬과 원격의 연결
  - git remote add [원격 리포지토리 주소의 별명 : origin] [원격 리포지토리 주소]
  - git remote add origin https://github.com/HS-hand/codeit-git.git
  - git remote -v : 등록된 원격 리포지토리의 주소와 별명을 출력

## 업로드
  - git push [원격 리포지토리의 별명 : origin] [업로드 하고싶은 브랜치 이름]
    - git push origin chat
    - 리모트 리포지토리에 chat 브랜치가 업데이트
    - 로컬 리포지토리에 트래킹 브랜치 origin/chat이 리모트 브랜치와 동기화 된다.

## 다운로드
  - git fetch [원격 리포지토리의 별명 : origin] [다운로드 하고싶은 브랜치 이름]
    - git fetch origin dev
    - 로컬 리포지토리에 origin/dev 이름을 가진 트래킹 브랜치가 생성됨
    - 트래킹 브랜치는 그림자 브랜치 ( 체크아웃 X, 커밋 X )
