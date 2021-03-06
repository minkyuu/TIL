2021.10.14. TIL (Memory Hierarchy)

## 1. 메모리 계층 구조 (Memory hierarchy)

> : 메모리를 필요에 따라 여러가지 종류로 나누어 두는 것을 의미

> (여기서 필요란 대부분의 경우 CPU가 메모리에 더 빨리 접근하기 위한 것)

<br>

## 2. 메모리 계층 구조 특징

1. 레지스터와 캐시는 CPU내부에 존재. 당연히 CPU는 아주 빠르게 접근할 수 있다.

2. 메모리는 CPU 외부에 존재한다. 레지스터와 캐시보다 더 느리게 접근할 수 밖에 없다.

3. 하드 디스크는 CPU가 직접 접근할 방법조차 없다.

    >: CPU가 하드 디스크에 접근하기 위해서는 하드 디스크의 데이터를 메모리로 이동시키고, 메모리에서 접근해야 한다.

    >: 따라서 아주 느린 접근만 가능하다


<br>

## 3. 컴퓨터 메모리 종류

### 1. 레지스터 (Register)

>: 컴퓨터에서 제일 빠른 메모리

>: 프로세서에 위치한 고속 메모리로 극히 소량의 데이터나 처리 중인 중간 결과와도 같은 프로세서가 바로 사용할 수 있는 데이터를 담고 있는 영역

>: 프로세서 레지스터 or 단순히 레지스터는 컴퓨터의 프로세서 내에서 자료를 보관한다.

>: 일반적으로 현재 계산을 수행중인 값을 저장하는데 사용

<br>

### 2. 캐시 (Cache)

>: 레지스터 다음으로 빠른 메모리

>: CPU 내부에 존재한다.

>: 용량은 비교적 작지만 가장 자주 사용되는 데이터를 복사해와 가지고 있으면서 CPU 메모리 접근시간을 줄여 속도를 향상시킬 수 있다.

>(대부분의 메모리 접근은 특정한 위치의 근방에서 자주 일어나는 경향이 있기 때문에)

>: CPU와 주기억장치간의 속도 차이로 인한 성능 저하를 막기 위해 사용

* L1 Cache
* L2 Cache
* L3 Cache

<br>

### 3. 주기억장치 (메인 메모리 - RAM, ROM)

>: CPU나 메인보드와 분리되어 있는 메모리 중에서 최상위 메모리

>: CPU에서 직접 접근이 가능한 메모리

>: 캐시에 비해 훨씬 느리지만, HDD, SSD에 비해서는 차원이 다르게 빠르다

>: 보통 DRAM으로 구성된다

<br>

### 4. 보조기억장치 (하드 디스크 - HDD, SSD)

>: CPU에서 직접 접근이 불가능한 메모리

>: 접근하려면 디바이스 드라이버와 시스템 콜을 통하여 기억장치의 특정 위치의 내용을 주기억장치로 로드한 뒤 읽어야 한다.
