### 2021.09.16. TIL (Network)

## Network

* 컴퓨터 사이의 리소스를 공유

* 네트워크로 연결된 다른 컴퓨터에 접근하여 파일을 생성, 수정, 삭제할 수 있다.

* 프린터와 스캐너, 팩스 등의 출력장치에 네트워크를 연결하여 여러 컴퓨터가 동시 접근 가능

<br>

## Requirements of Network

1. Network Cable

2. Distributor (Switch Hub)

3. Router

4. Network card

<br>


## 커버 범위에 따른 네트워크 구분

1. LAN

>: Local Area Network (근거리 통신망)

>: 학교, 회사 등 가까운 지역의 좁은 범위

2. WAN

>: Wide Area Network

3. MAN (LAN < MAN < WAN)

>: Metrpolitan Area Network

4. WLAN

>: Wireless LAN

<br>

## Network Topology

1. Ring

2. Mesh

3. Star (가장 많이 쓰이고 유지비용이 가장 적게 든다)

4. Fully Connected (비용이 많이 드므로 소규모일 때만)

5. Line

6. Tree

7. Bus

<br>

---

## OSI 7 Layer

* Open Systems Interconnection Reference Model

* 국제 표준화 기구에서 개발한 컴퓨터 네트워크 프로토콜 디자인과 통신을 계층으로 나누어 설명한 것

<br>

7. Application Layer

>: 사용자에게 네트워크 자원에 대한 접근을 제공

>: 네트워크 활동들에 대한 모든 기본적인 인터페이스를 제고

>: 사용자에게 보이는 유일한 계층

>: 크게 보면 웹 브라우저를 의미

<br>

6. Presentation Layer

>: 응용 계층으로 부터 전송받거나 전달되는 데이터의 인코딩과 디코딩

>: 안전하게 데이터를 사용하기 위해 몇 가지 암호화와 복호화 형식 보유

<br>

5. Session Layer

>: 두 대의 컴퓨터 사이의 세션이나 대화를 관리

>: 모든 통신 장비를 연결하고 관리하며 종료

>: 순간적으로 연결이 끊어지는 것을 막고 호스트 사이의 연결을 적절하게 종료

<br>

4. Transport Layer

>: 아래 계층에 신뢰성 있는 데이터를 전송할 수 있게 함

>: 흐름 제어, 분할, 재조립, 오류 관리 (정보의 순서가 전송과 일치하는지 체크)

>: 라우터 존재 -> 방화벽과 프록시 서버

<br>

3. Network Layer

>: 통신사가 주관하는 layer

>: 이더넷의 핵심

>: 가장 복잡한 OSI 계층 중 하나로, 물리적인 네트워크 사이의 라우팅을 담당하며, 라우터가 이 계층에서 동작

>: 네트워크 호스트의 논리적인 주소(IP 주소 같은)를 관리하고 패킬을 분할해 프로토콜을 식별하는 기능, 오류 탐지 같은 몇 가지 경우를 담당

>: 최단 거리 계산 및 전송

<br>

2. Data Link Layer

>: 물리적인 네트워크 사이의 데이터 전송을 담당

>: 물리적인 장비를 식별하는데 사용되는 주소 지정 체계 (Addressing Schema)와 데이터가 변조되지  않았음을 확증하기 위한 오류 확인을 제공

>: 브리지와 스위치가 이 계층에 있음

<br>

1. Physical Layer

>: 가장 아래 단계

>: 네트워크 데이터가 전송 될 때 사용되는 물리적 매개체

>: 전압, 허브, 네트워크 어댑터, 리피터 등 모든 HW의 물리적이고 전자적인 특성의 정의

>: 연결을 설정하고 종료하며, 공유된 통신 자원을 제공하고, 아날로그를 디지털화 한다.
>
