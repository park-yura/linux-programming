# Linux Programmin 최종 과제

## 1. Apache와 Tomcat 연동, webserver활용 및 app에 따른 요청 분배
### 로드 밸런스란?
- 서버에 가해지는 부하(=로드)를 분산(=밸런싱)해주는 장치 또는 기술
- 클라이언트와 서버풀(Server Pool, 분산 네트워크를 구성하는 서버들의 그룹) 사이에 위치하며, 한 대의 서버로 부하가 집중되지 않도록 트래픽을 관리해 각각의 서버가 최적의 퍼포먼스를 보일 수 있도록 함
- apache가 tomcat에게 url을 기반으로 요청을 분배 <br>
<iframe width="1062" height="597" src="https://www.youtube.com/embed/1GHWLkZf0Gs" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

## 2. Oracle Weblogic 설치 및 app deploy
### Domain, DAS, MS, Cluster 란?
- Domain :  웹로직 도메인이란 하나의 논리적인 관리 단위
- DAS(Domain Administration Server) : 도메인 관리 서버라고 하며, 관리자를 인증하고 관리 도구의 요청을 수락하며 도메인의 서버 인스턴스와 통신하여 요청을 수행
- MS(Managed Server) : Admin Server를 제외한 모든 서버
실제 서비스를 제공하는 서버로서 비즈니스 로직을 포함하고 있는 어플리케이션과 컴포넌트들은 거의 대부분 Managed Server에 배포
- Cluster : 여러 대의 웹로직 서버 인스턴스를 묶어 부하분산과 장애 복구 기능을 제공하여 클라이언트에게 중단없는 서비스를 제공하는 기능 <br>
<iframe width="1062" height="597" src="https://www.youtube.com/embed/zrMCb916ibk" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe><br>

## 3. Google Cloud Platform Compute engine 위에서 Apache-Tomcat  설치, 연동, App deploy
### 방화벽 해제 방법
- Google Cloud Platform Console에서 VPC 네트워크 메뉴에서 '방화벽' 선택
- '방화벽 규칙 만들기' 선택
- 방화벽 이름 지정
- 트래픽 방향: 수신 (Inbound) 또는 송신 (Outbound) 허용, 외부에서 GCP 서버에 접근하기 위해서는 '수신'을 선택
- 소스 범위 선택: 특정 IP 선택 또는 모든 IP를 허용.  모든 IP를 허용하는 경우에는 '0.0.0.0/0' 입력
- 프로토콜과 포트 선택: TCP, UDP의 포트를 지정 (Flask와 같은 경우에는 TCP에 5000번 입력)<br>
<iframe width="1062" height="597" src="https://www.youtube.com/embed/d2qXA7uTb2Y" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe><br>
