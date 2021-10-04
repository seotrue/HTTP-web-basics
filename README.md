#http 웹 기본 지식
## 색션1: 인터넷 네트워크
##### 인터넷통신
- 
##### IP
- 
##### TEC, UDP
- 인터넷 프로토콜 스택의 4계층
1. 애플리케이션 계층 - http, Ftp
2. 전송계층 - tcp, udp
3. 인터넷 계층- ip
4. 네트웨크(렌등등) 인터페이스 계층

- ex) 
1.프로그램이 헬로우 월드 메세지 생성
2. 소켓 라이브러리를 통해 전달
3. tcp정보가 해당 메세지 데이터롤 포함에서 감싼다
4. tcp 까지 감싸져 잇는걸 ip로 한번더 감싼 패킷으로 만들어서(ip+ tcp) 
5. 네트웨크를 통해 다른 서버로 보냄

- TEC:http/1

- UDP: http/3
##### PORT
- 같은 ip 내에서 프로세스 구분
- 패킷 보낼때 출발지, 목적지 ip + port 같이 보냄
- 한 아파트(서버)라면 호수가 포트 라고 비유

##### DNS
- ip는 기억하기 어렵다 => 길자나~ 그리고 변경 될수 잇다 그래서 도메인 네임 시스템사용
- 도메인명을 ip 주소로 변한 

## 색션2: URI와 웹 브라우저 요청 흐름
##### URI
- URI는 로케이터(locator), 이름(name) 또는 둘다 추가로 분료 될수 잇음
- 프로토콜: 어떤 자원에
##### 웹 브라우저 요청 흐름

### 색션3: 모든것이 http
##### 모든것이 http
- http 메세지에 모든것을 전송
- 현재 http/1.1 주로 사용

##### http 특징
클라이언트 서버구조
무상태 프로토콜 비연결성
http 메시지
단순한 확장가능

이벤트 페이지등

stateful: 상태유지
서버가 클라이언트 이전 상태를 보존
중간에 점원이 바뀌면 서버에러
로그인 상태를 서버에 유지 할 경우


비연결성
서버는 연결 유지x -> 현재 요청을 주고 받을때만 연결 요청할때만 연결 ->  최소한의 자원으로 서버 유지
단점은 tcp/ip 연결을새로 연결 맺어야함 -> 시간 추가
 http 지속 연결 :
 다 받을때까지 연결

스테리스리스를 기억하자

http 메세지
- http 메시지에 모든걸 보낼수 잇다
- 요청과 응답 구조가 다름
http 메시지 구조

시작 라인
요청 : http메서드(서버가 수행해야할 동작지정) + 요청대상(절대경로) + http 버전
응답 : http 버전 + http 상태(요청 성공, 실패를 나타냄

해더(http 전송에 필요한 부가 정보)
필드네임: 벨류

공배라인

메세지바디
실제 전송할 데이터
