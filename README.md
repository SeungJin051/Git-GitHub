# Git-GitHub

![git](https://user-images.githubusercontent.com/83889135/193983137-4fe8dd95-7fa2-4407-8b87-a75ddb604ef1.png)
![github](https://user-images.githubusercontent.com/83889135/193983166-89321ac1-8e48-4e29-afbd-643b72148567.png)


# Git을 배워야 하는 이유!
 Git = VCS(Version Control System)
 시간과 차원을 종횡으로 넘나든다
 프로그래밍을 하면서 새기능을 만들고 오류를 고쳐가며 새로운 버전이 나온다 Git을 사용하면 
 코드파일을 따로 압축하고 저장  할 필요가 없다 
 예로 버전2에서 버전1으로 돌아가야하는 경우가 생기면 프로젝트의 내용들을 다른 폴더 인것처럼 변경사항을 자유롭게 이듕가능 
 여러 개발자들이 협업해서 함께 소프트웨어를 만들어가는데 있어 중요한 기능들을 지원한다.

# CLI VS GUI
 CLI(Command Line Interface) = 명령줄을 입력하여 사용하는 것 (Ex. cmd, 터미널)
 GUI(Graphical User Interface) = 그래픽 요소를 활용한 인터페이스

 Git에서 실행하기 위한 어떤 명령들을 사용할 때는 CLI를 사용 (명령어 사용)
  프로젝트의 상태를 Git상에서 자세히 살펴보아야 할 때는 GUI를 사용 (시각적)

# Git 최초 설정 
 + 깃허브 계정과는 별개.
 
 git config --global user.name "Your Name" 

 git config --global user.email "your@mail.com"

# 프로젝트 생성 & Git 관리 
 git init = 로컬 Git 저장소를 설정합니다.

 git status = 현재 상태 확인
 
 git add = 현재 상태 추적
 
 git commit = 현재 상태 저장
 
 # 과거로 돌아가는 방법 2가지 Reset VS Revert
  Reset = 시간을 과거로 되돌림, 과거로 돌아간 다음 이후 행적을 히스토리에서 지움
  Revert = 과거로 돌아간 다음 이후 행적을 히스토리에서 지우지 않고 이 때의 변화를 거꾸로 수행하는 캡슐을 하나 넣음으로써
  예시) 추가한 게 있으면 삭제하고, 변경이 있으면 수행
  *협업시 한번 공유된 코드는 Revert를 이용하여 되돌려야 충돌이 되지않는다.*
  
 # Branch 가지 (다른 차원)
  + 프로젝트를 하나 이상의 모습으로 관리해야 할 때
      + ex) 실배포용, 테스트서버용, 새로운 시도용 
  
  + 여러 작업들이 각각 독립되어 진행될 때
      + ex) 신기능1, 신기능2, 코드개선, 긴급수정...
      + 각각의 차원에서 작업한 뒤 확정된 것을 메인 차원에 통합한다. 
 # Branch 사용법 
 ![img](https://user-images.githubusercontent.com/83889135/193982874-52e1f987-a1b5-4625-b6da-ace9a0b54639.gif)

# What is GitHub
 + 깃허브는 루비 온 레일스로 작성된 분산 버전 관리 툴인 깃 저장소 호스팅을 지원하는 웹 서비스이다.
 + 깃허브는 영리적인 서비스와 오픈소스를 위한 무상 서비스를 모두 제공한다.
 ## 깃허브의 주요 지원
  + 깃허브는 대부분 코드를 위해 사용된다.
  + 다른 사용자를 구독하는 옵션 (다른 사용자의 언급 알림).
  + 깃허브 페이지: 작은 웹사이트들은 깃허브의 공개 저장소의 호스팅을 받을 수 있다. URL 포맷은 https://username.github.io
  + 지형공간 분석 데이터 시각화
  + 파일 내의 중첩 작업 목록
  + 각기 다른 패키지에서 공통 취약점 및 노출로 알려진 보안 경보
  + README == MarkDown 프로젝트 소개글


