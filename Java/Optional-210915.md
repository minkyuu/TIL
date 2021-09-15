### 2021.09.15. TIL(Optional)

## Optional

* Java8부터 Optional<T>클래스를 사용해 NullPointerException(이하 NPE)를 방지할수 있도록 했다.

* Optional<T>는 null이 올 수 있는 값을 감싸는 Wrapper 클래스로, 참조하더라도 NPE가 발생하지 않도록 도와준다.
 
  (Integer나 Double 클래스처럼 T 타입의 객체를 포장)

* 즉, 예상치 못한 NPE예외를 제공되는 메소드로 간단히 회피할 수 있어 복잡한 조건문 없이도 null값으로 인해 발생하는 예외를 처리할 수 있다.

