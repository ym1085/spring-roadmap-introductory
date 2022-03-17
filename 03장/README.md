## 📌 목차

1.  **디자인패턴**
2.  **스프링 삼각형과 설정정보**

## 01. 스프링이 사랑한 디자인패턴

![주방도구](./images/kitchen_utensils.jpg)

> 현재까지 진행한 OOP의 개념

1. 객체 지향의 4대 특성
2. SOLID 5대 원칙
3. `디자인패턴`

**객체 지향 특성**은 **도구**, **설계 원칙**은 **도구를 올바르게 사용하는 방법**으로 비유.

| 요리                | 객체 지향 프로그래밍                   |
| ------------------- | -------------------------------------- |
| **요리도구**        | 4대 원칙(상속, 추상화, 다형성, 캡슐화) |
| **요리도구 사용법** | 5대 설계 원칙(SOLID)                   |
| `레시피`            | 디자인 패턴                            |

## 01-1. 디자인패턴이란?

![curious](./images/curiosity.png)

- 프로그램을 작성하다보면 비슷한 상황을 직면.
- 이전의 많은 개발자들이 고민하고 정제한 `표준 설계 패턴`.

> 즉, 실제 개발 현장에서 다양한 요구사항을 프로그래밍으로 처리하면서 만들어진 다양한 해결책 중  
> 많은 사람들이 인정한 Best Practice를 정리한 것.

## 01-2. 스프링 프레임워크(Spring Framework)

> 스프링 프레임워크를 설명하는 공식정인 정의

- 자바 엔터프라이즈 개발을 편하게 해주는 **Open source application framework**
- **OOP 프레임워크**
- `스프링`은 `객체 지향`의 `특성과 설계 원칙`을 `극한`까지 적용한 프레임워크.

## 01-1. 어댑터 패턴(Adapter Pattern)

![phone](./images/charger.jpg)

> 💡 개발 폐쇄 원칙()을 활용한 설계 패턴

- 어댑터를 번역하면 `변환기`
- **서로 다른 두 인터페이스 사이에 통신을 가능하게 함**
- 대표적으로는 `휴대폰 충전기`가 존재
- ODBC(Open Database Connectivity), JDBC(Java Database Connectivity), JRE

### 어댑터 패턴 예제(Before)

```java
// ServiceA 클래스 생성
public class ServiceA {
    void runServiceA() {
        System.out.println("ServiceA");
    }
}
```

```java
// ServiceB 클래스 생성
public class ServiceB {
    void runServiceB() {
        System.out.println("ServiceB");
    }
}
```

```java
// main
public class ClientWithNoAdapter {

    public static void main(String[] args) {
        ServiceA sa1 = new ServiceA(); // 1. 객체 생성
        ServiceB sb1 = new ServiceA(); // 2. 객체 생성

        sa1.runServiceA(); // 3. sa1.runServiceA() 호출
        sb1.runServiceB(); // 4. sa1.runServiceB() 호출
    }
}
```

- 현재 sa1, sb1 참조 변수를 통해 runServiceA(), runServiceB() 메서드 호출.
- 비슷한 일을 하지만 메서드명만 다른 것을 확인 가능.

### 시퀸스 다이어그램(Sequence Diagram)

![before_adapter_diagram](./images/before_adapter_diagram.PNG)

### 어댑터 패턴 예제(After)

```java
public class AdapterServiceA {
    ServiceA sa1 = new ServiceA();

    void runService() {
        sa1.runServiceA();
    }
}
```

```java
public class AdapterServiceB {
    ServiceA sb1 = new ServiceB();

    void runService() {
        sb1.runServiceB();
    }
}
```

```java
// main
public class ClientWithAdapter {

    public static void main(String[] args) {
        AdapterServiceA asa1 = new AdapterServiceA();
        AdapterServiceB asb1 = new AdapterServiceB();

        sa1.runService();
        sb1.runService();
    }
}
```

- 클라이언트(ClientWithAdapter)가 변환기를 통해 동일한 메서드인 runService() 호출.
- 어댑터 패턴 `합성`, 즉 객체를 속성으로 만들어서 참조하는 디자인 패턴.

> 💡 호출당하는 쪽의 메서드를 호출하는 쪽의 코드에 대응하도록 중간에 변환기를 통해 호출하는 패턴

### 01-2. 프록시 패턴(Proxy Pattern)

### 01-3. 데코레이터 패턴(Decorator Pattern)

### 01-4. 싱글턴 패턴(Singleton Pattern)

### 01-5. 템플릿 메서드 패턴(Template Method Pattern)

### 01-6. 팩터리 메서드 패턴(Factory Method Pattern)

### 01-7. 전략 패턴(Strategy Pattern)

### 01-8. 템플릿 콜백 패턴(Template Callback Pattern - 견본/회신 패턴)

### 01-9. 스프링이 사랑한 다른 패턴들(디자인패턴 마무리)

- 위 8가지 패턴 말고도 스프링은 다양한 디자인 패턴 활용.
- 대표적으로는 Spring MVC(Model, View, Controller) 패턴 존재.

## 02. 스프링 삼각형과 설정정보

![spring_framework](./images/spring_fw.png)

- DI(**Dependency Injection**)
- AOP(**Aspect Oriented Programming**)
- PSA(**Portable Service Abstractions**)

### 02-1. IOC/DI - 제어의 역전과 의존성 주입

> 프로그래밍에서 의존성이란 무엇일까?  
> 그렇다면 어떠한 것에 의존 한다는게 어떤 의미일까?

### 의사 코드

- 운전자가 자동차를 생산한다.
- 자동차는 내부적으로 타이어를 생산한다.

### 자바로 표현

```java
// Car 객체 생성자에서 new Tire();

public class Test {

    public static void main(String[] args) {
        Car car = new Car(); // Car 생성자 호출
    }
}
```

```java
public class Car {
    Tire tire = null;

    public Car() {
        this.tire = new Tire();
    }
}
```

### 참고 자료

- [[책 링크] 스프링 입문을 위한 자바 객체 지향의 원리와 이해](http://www.yes24.com/Product/Goods/22483294)
- [[사진 참고] Spring 이론 (POJO, Java Beans)](https://ksshlee.github.io/spring/spring/)
