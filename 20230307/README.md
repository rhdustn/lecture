# 20230307
<!--md 문서 작성  -->
<!-- #제목을 작성 -->
## 20230307

### 20230307


# git프로젝트

- git은?
1. 현상관리 도구중에 하나
현상관리 도구  : 버전 관리 시스쳄
작업하면서 작업의 리스츠응 관리할 수 있다

- git의 장점
-협업하는 단계에서 소스코드 파링로 주고
받을 필요가 없이 갗은 파일을 침원과 병렬로 작업이 가능하다

- 눈으로 보고 찾는것 보다 효율이 좋고 작업이 편하다코드의 다른 부분을 바로 찾을 수 있다

- git 설치

- git 사용자 설정

- git 사용
- git config --global user.name "본인 닉네임"
- git config --global uder.gmail

- 설정 정보 조회
- git config --global --list

- 경로 지정
- cd .. : 한폴더 뒤로 이동 
- ls -a : 경로의 파일을 전부 보고싶으면
- cd 폴더명 : 해당 폴더로 경로 이동
- cd 앞부분 폴더명 쓰고 기억이 안나면 tab 버츤 눌러서 비슷한 폴더명 확인 가능
gi
- git 저장소 초기화 저장소를 생성하는 명령어
- 해당 프로젝트의 경로에서
- git init

- 저장소와 파일의 내용이 다를 때 컬러로 표현 해준다

- 저장소 파일 스테이징
- 업로드 전 준비 업로드 할 파일들

- git add 해당 파일 이름
- git add .: 모든 파일 스테이징
- git commit -m "메세지 내용"
햣
-파일들을 업로드 할 준비가 끝
- git remot add origin "연결 할 준비 완료"

- 원격저장소에 업로드
- git push -u origin master
- 깃을 관리하면서 자리 이동 했을 때 커밋을 올렸는대 사용자 사용명이 다를 경우 제어판-> 사용자계정 ->자격증명 관리자 ->github.com ->아코디언 박스 열어서 제거 버튼 누르고 삭제한 후 다ㅣ 사용자 등록 진행 하면 된다

- 협업을 할 때 git push 부터 받으면 안되고 pull, 
- pull push 먼저 작업물을 병합하고 작업물을 올리자

- a 와 b가 있으면 a가 먼저 push b 가 계속 작업을 하다가 
- a의 작업물이 병합하지 않고 push를 하게되면 a의 작업물이 다 날아간다,

- git 파링을 잘못 만들었을 때 
- rm -rf : 폴저 삭제 ( ec)

- 새로운 환경에서 git 저장소를 연결 항때 따라하세요gti 
- git init
- git remote add origin "저장소 주소"
- 저장소의 주소는 해당 깃허브의 저장소에 접속하여 code,(초록색 버튼)
- cd 
- git pull origin master : 원격저장소에서 파일을 받아온다.

- 오늘 과제는 자굼까지 한 과제들이랑 수업자료들을 저잘소를 만들어서 업로드 하기git 