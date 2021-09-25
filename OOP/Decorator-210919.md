### 2021.09.19. TIL (Decorator Pattern)

## 1. Decorator Pattern이란?

* Decorate는 장식하다, 꾸미다라는 의미를 가진 영단어이다.

* 데코레이터 패턴은 기존 뼈대(클래스)는 유지하되, 이후 필요한 형태로 꾸밀 때 사용한다.

* 확장이 필요한 경우 상속의 대안으로 활용한다.

* SOLID 중에서는 OCP와 DIP를 따른다.

* 데코레이터는 어떤 기능에 추가적으로 기능을 덧붙이고 싶은 경우, 그 기능들을 Decorator로 만들어서 덧붙이는 방식입니다.

* 데코레이터 패턴을 사용하면 기능이 딱 정해져있는 객체가 아닌, 동적으로 기능을 조합하여 객체를 만드는 것이 가능해집니다.

<br>

## 2. Decorator Example

* 커피

  * 에스프레소 + 물   -> 아메리카노

  * 에스프레소 + 우유 -> 카페라떼

* 빵

  * 빵 + 딸기잼 -> 딸기빵

  * 빵 + 포도잼 -> 포도빵

  * 빵 + 초코잼 -> 초코빵