### 2.2.7 도커 네트워크
#### 2.2.7.1 도커 네트워크 구조
 - 도커는 컨테이너에 내부 IP를 순차적으로 할당하며, 이 IP는 컨테이너를 재시작할 때 변경될 수 있음.
 - 도커는 컨테이너를 위한 veth 디바이스를 host에 생성 (host에는 vethXXXXXXX, docker에서는 eth로 보임)
 - host에는 docker0 라는 bridge 가 하나 생기고 이는 각 docker의 veht와 연결됨.
    > brctl show docker0
    > bridge name     bridge id               STP enabled     interfaces
    > docker0         8000.0242e3383aa5       no              veth6802cff    
