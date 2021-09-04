# 2021.09.04. TIL (Serialization)

### 직렬화

>: 인스턴스의 상태를 그대로 파일에 저장하거나 네트워크로 전송하고 (Serialization) 이를 다시 복원하는 방식 (Deserialization)으로 많이 사용한다.

>: 자바에서는 보조 스트림을 활용하여 직렬화를 제공

<br>

---

### 직렬화 구현 방법

1. 직렬화 -> Serializable interface를 구현

: implements만 해주면 된다.

2. 역직렬화 -> Externalizable interface를 구현

: 역직렬화 같은 경우는 반드시 writeExternal()이랑 readExternal()을 오버라이딩 해줘야 한다.
