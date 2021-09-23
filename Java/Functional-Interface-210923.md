### 2021.09.23. TIL (Functional Interface)

## 함수형 인터페이스

>: 단 하나의 추상 메서드만 선언된 인터페이스

>: @FunctionalInterface를 안붙여줘도 에러는 안나지만 붙여줘야 컴파일러가 함수형 인터페이스가 잘 작성되었는지 확인을 할 수 있다.

>: 함수형 인터페이스 타입의 참조변수로 람다식을 참조할 수 있다. (재사용이 가능해진다.)

<br>

### Example Code

```java

Myfunction f = (a, b) -> a > b ? a : b
: 이 코드는 내부적으로 익명 클래스 선언 및 객체 생성을 동시에 하는 코드이다.


위의 코드를 뜯어보면 아래와 동일하다.

@FunctionalInterface
interface Myfunction {
    public abstract int max(int a, int b);
}

Myfunction f = new Myfunction() {
    public int max(int a, int b) {
        return a > b ? a : b;
    }
}
```

