# Git-GitHub
![gitgithub](https://user-images.githubusercontent.com/83889135/193991354-5b8af519-a28b-4862-bdbb-169b01a190c8.png)

# Git을 배워야 하는 이유, 버전들을 만들어 시간과 차원을 제어하는 방법
 Git = VCS(Version Control System)
 시간과 차원을 종횡으로 넘나든다
 프로그래밍을 하면서 새기능을 만들고 오류를 고쳐가며 새로운 버전이 나온다 Git을 사용하면 
 코드파일을 따로 압축하고 저장  할 필요가 없다 
 예로 버전2에서 버전1으로 돌아가야하는 경우가 생기면 프로젝트의 내용들을 다른 폴더 인것처럼 변경사항을 자유롭게 이듕가능 
 여러 개발자들이 협업해서 함께 소프트웨어를 만들어가는데 있어 중요한 기능들을 지원한다.

## VCS..
### 로컬 VCS (Distributed VCS: DVCS)

<img width="447" alt="스크린샷 2022-10-05 오후 3 19 18" src="https://user-images.githubusercontent.com/83889135/193994006-594d84d9-9472-4480-b01e-eea71c905a10.png">

 + 사용하는 컴퓨터(local computer)에 간단한 데이터베이스를 만들어 파일 변경 정보를 기록 관리
 + 필요한 시점에 DB에서 특정 버전을 불러와서 사용
 + 다른 개발자들과 함께 사용하기에는 문제가 많음

### 중앙집중식 VCS (Centralized VCS: CVCS)

<img width="458" alt="스크린샷 2022-10-05 오후 3 21 11" src="https://user-images.githubusercontent.com/83889135/193994219-4a404a65-6d93-4dcb-bd84-df58ecc6445f.png">

 + 파일을 관리하는 서버(CVCS Server)가 별도로 있고 클라이언트가 중앙 서버에서 파일을 받아서 사용(Checkout).
 + 다른 개발자들과 함께 작업하기에 매우 편리함 ex) CVS, Subversion, Perforce...
 + 중앙 서버에 문제 발생시 작업 중단, 모든 자료 손실 등 치명적 한계가 있음

### 분산 VCS (Distributed VCS: DVCS)

<img width="458" alt="스크린샷 2022-10-05 오후 3 25 49" src="https://user-images.githubusercontent.com/83889135/193994916-5a3e655e-c899-408c-bd39-b8ba8652bae6.png">

 + Client는 단순히 파일의 마지막 스냅샷을 복사하지 않고 그냥 저장소를 전부 복제
 + 서버에 문제가 생겨도 local 또는 다른 client를 통해 완벽한 복원 가능
 + 동시에 다양한 그룹과 다양한 방법 으로 협업 가능
 + DVCS

## CLI VS GUI
 CLI(Command Line Interface) = 명령줄을 입력하여 사용하는 것 (Ex. cmd, 터미널)
 GUI(Graphical User Interface) = 그래픽 요소를 활용한 인터페이스

 Git에서 실행하기 위한 어떤 명령들을 사용할 때는 CLI를 사용 (명령어 사용)
  프로젝트의 상태를 Git상에서 자세히 살펴보아야 할 때는 GUI를 사용 (시각적)

## 매우중요 (⭐️⭐️⭐️) 
### Git 파일의 3가지 상태
 + Committed: 데이터가 로컬 데이터베이스에 안전하게 저장되었음
 + Modified: 수정했으나 아직 로컬 데이터베이스에 커밋(commit)하지 않은 것
 + Staged: 현재 수정한 파일을 곧 커밋 할 것이라고 표시한 상태를 의미
 
<img width="711" alt="스크린샷 2022-10-05 오후 3 05 33" src="https://user-images.githubusercontent.com/83889135/193992247-07217bd6-a3e9-42b4-8a26-98a2bc546a25.png">

### Git 디렉토리 
   + Working Director : 지금 작업하는 컴퓨터의 특정 디렉토리, 리모트 서버 등에서 특정 버전을 가져와(checkout) 만든 작업용 디렉토리
   + Git Directory: (Git의 핵심) : 보통 Working Directory의 sub directory (.git)로 생성됨 프로젝트의 메타데이터와 객체 데이터베이스를 저장 하는 곳
   + Staging Area: (←실제 directory가 아니고 특정 파일의 개념적 용도를 말함) Git directory에 저장된 단순 파일이며, 곧 커밋할 파일 정보를 저장
 
 ## 과거로 돌아가는 방법 2가지 Reset VS Revert

![git-reset-vs-git-revert](https://user-images.githubusercontent.com/83889135/194001933-8cc96054-0b46-4346-8704-e86afe2b60a2.jpeg)
 
 
  Reset = 시간을 과거로 되돌림, 과거로 돌아간 다음 이후 행적을 히스토리에서 지움 <br>
  Revert = 과거로 돌아간 다음 이후 행적을 히스토리에서 지우지 않고 이 때의 변화를 거꾸로 수행하는 캡슐을 하나 넣음으로써
  예시) 추가한 게 있으면 삭제하고, 변경이 있으면 수행
  *협업시 한번 공유된 코드는 Revert를 이용하여 되돌려야 충돌이 되지않는다.*
  
 ## Branch 가지 (다른 차원)
 ![git-branches-merge](https://user-images.githubusercontent.com/83889135/193998253-cc7aa72b-8248-40e4-81ba-c2fa328ae0c6.png)

  + 프로젝트를 하나 이상의 모습으로 관리해야 할 때
      + ex) 실배포용, 테스트서버용, 새로운 시도용 
  
  + 여러 작업들이 각각 독립되어 진행될 때
      + ex) 신기능1, 신기능2, 코드개선, 긴급수정...
      + 각각의 차원에서 작업한 뒤 확정된 것을 메인 차원에 통합한다. 
 ## Branch 사용법 
  추가예정.
 ![img](https://user-images.githubusercontent.com/83889135/193982874-52e1f987-a1b5-4625-b6da-ace9a0b54639.gif)

# What is GitHub
 + 코드 공유 및 협업 서비스
 + 깃허브는 영리적인 서비스와 오픈소스를 위한 무상 서비스를 모두 제공한다.
 + Git으로 관리하는 프로젝트들을 온라인 공간에 공유해서 프로젝트 구성원들이 함께 소프트웨어를 만들어갈 수 있도록 도와주는 서비스

## GitHub
 모든 업로드와 다운로드를 커밋 단위로 주고받는다.
 협업시 커밋을 함으로써 원활한 버전공유가 가능하다. (최신버전을 다운로드)
 
## 원격 저장소 
 Git Repository는 Git으로 관리하는 프로젝트 저장소
 + Local Repository : 본인의 컴퓨터에 저장된 로컬 버전의 프로젝트 저장소.
 + Remote Repository : 로컬이 아닌 외부 서버의 프로젝트 저장소.
 + 팀 단위의 작업을 진행할 때 유용합니다. 이 곳에서는 프로젝트 코드를 공유할 수 있고, 다른 사람의 코드를 확인할 수 있습니다. 또한, 
   로컬 버전 의 프로젝트와 병합, 변경 사항 등을 적용할 수 있습니다.

 ## 깃허브의 주요 지원 
  + 깃허브는 대부분 코드를 위해 사용된다.
  + 다른 사용자를 구독하는 옵션 (다른 사용자의 언급 알림).
  + 깃허브 페이지: 작은 웹사이트들은 깃허브의 공개 저장소의 호스팅을 받을 수 있다. URL 포맷은 https://username.github.io
  + 지형공간 분석 데이터 시각화
  + 파일 내의 중첩 작업 목록
  + 각기 다른 패키지에서 공통 취약점 및 노출로 알려진 보안 경보
  + README == MarkDown 프로젝트 소개글

## Git 최초 설정 
 + 깃허브 계정과는 별개.
 
 git config --global user.name "Your Name" 

 git config --global user.email "your@email.com"

## 프로젝트 생성 & Git 관리 
 git init = 로컬 Git 저장소를 설정합니다. 
 
 git status = 현재 상태 확인
 
 git add = 현재 상태 추적
 
 git commit = 현재 상태 저장
 
 git config = git 설정(사용자 정보 설정, 설정 확인 등)
 
 git diff = 이전 버전과 비교해 다른 점 나타냄
 
 git log = 로그 상태 보기

## Git 저장소 만들기 

프로젝트 디렉토리로 이동하여 다음 명령 실행
$ git init
  ... 아직 프로젝트 디렉토리의 어떤 파일도 버전 관리가 시작되지 않았음
### 버전 관리할 파일을 git 명령으로 추가하고 커밋해야 관리가 시작됨
 $ git add *.c // 관리할 파일 추가
 $ git add readme.txt // 관리할 파일 추가
 $ git commit -m 'first version' // 저장

<img width="208" alt="스크린샷 2022-10-05 오후 3 39 19" src="https://user-images.githubusercontent.com/83889135/193996707-c00e9eea-4715-4606-a18f-1d9a5033ae52.png">

### 기존 저장소를 복사하기
서버 등 다른 컴퓨터의 프로젝트를 로컬 컴퓨터로 복사
기존 저장소를 복사해 올 디렉토리로 이동 후 다음 명령 실행
$ git clone [url] 
  #### 예) userhome 디렉토리에서 다음 명령 실행
  #### $ git clone https://github.com/SeungJin051/project
  #### Userhome 디렉토리에 project 이름의 Git 저장소가 복사됨
  #### 다른 디렉토리 이름으로도 저장할 수 있다 
  #### $ git clone [url] newDirectory

> 출처 동의과학대학교 오픈소스소프트웨어실습 교수 윤혜정

# 직접 커밋 

<img width="1190" alt="스크린샷 2022-10-05 오전 10 45 32" src="https://user-images.githubusercontent.com/83889135/193997284-0025397b-3f23-4690-aafb-ee938606aa57.png">
----
<img width="668" alt="스크린샷 2022-10-05 오전 10 46 32" src="https://user-images.githubusercontent.com/83889135/193997324-ac0cf46f-1b55-4fe1-bcf7-a48b365d0d00.png">
----
<img width="668" alt="스크린샷 2022-10-05 오전 10 49 10" src="https://user-images.githubusercontent.com/83889135/193997362-4b246206-3303-4540-8666-dc2fe83db4c2.png">
