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
  

## 업로드
  - 

## 다운로드