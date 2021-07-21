## netstat

  - ### 기능 
    - 현재 시스템에서 사용하고 있는 네트워크 포트를 확인하는 명령어
  - ### 형식
    - netstat [option] 
  - ### 옵션
    - -a : 모든 네트워크 상태 출력
    - -l : 열려있는 네트워크 포트 풀력(listen, 포트의 소켓이 열린 상태)
    - -n : 도메인 주소를 숫자로 출력
    - -p : PID와 사용중인 프로그램명 출력
    - -r : 라우팅 테이블 출력
    - -s : 프로토콜 요약 정보 출력
    - -t : TCP 프로토콜만 출력
    - -u : UDP 프로토콜만 출력
    - -v : 버전 출력
    - -A : 프로토콜별로 출력

<br>

## ss (socket statistics)

  - ### 기능
    - 시스템의 소켓 상태를 조회할 수 있는 명령이다. 
    - netstat와 비슷한 역할을 수행한다.
    - 최근에는 netstat보다 ss 사용을 권장하고 있다.
  - ### 형식
    - ss [option] [src :PortNumber | dst :PortNumber]
  - ### 속성
    - Netid : 소켓의 유형
      - u_str : IPv6의 ICMP 소켓
      - Unix 스트림
      - udp
      - icmp6
    - State : 소켓의 상태
    - Recv-Q : 수신된 패킷 개수
    - Send-Q : 전송된 패킷 개수
    - Local Address : Port : 프로그램이나 IP 주소에 할당된 Port가 표시
    - Peer Address : Port : 외부 서버나 클라이언트의 IP 주소 및 Port 표시
  - ### 옵션
    - -a : 열려있는(listen 또는 대기중) 소켓을 포함한 모든 소켓을 표시한다. 
    - -l : 열려있는(listen 또는 대기중) 소켓만 표시한다.
    - -t : TCP 유형의 소켓만 표시
    - -u : UDP 유형의 소켓만 표시
    - -w : RAW 유형의 소켓만 표시
    - -x : Unix 유형의 소켓만 표시
    - src : 로컬 서버의 특정 포트에 연결된 외부 IP 및 포트 표시
    - dst : 외부 서버에 연결한 로컬 서버 및 외부 서버의 IP 및 포트 표시
  - ### 사용 예
    - ss -t src :443 : 로컬 서버의 443 포트에 TCP 소켓으로 연결된 외부 IP 및 포트 효시
    - ss -t dst :443 : 로컬 서버가 443 포트에 TCP 소켓으로 연결한 외부 서버의 IP 및 포트 표시