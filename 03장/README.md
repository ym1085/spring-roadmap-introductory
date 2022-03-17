## 목차

- 스프링이 사랑한 디자인패턴
- 스프링 삼각형과 설정정보

## ⚡ 01. 스프링이 사랑한 디자인패턴

![주방도구](./images/kitchen_utensils.jpg)

It is a long established fact that a reader will be distracted by the readable content of a page when looking at its layout. The point of using Lorem Ipsum is that it has a more-or-less normal distribution of letters, as opposed to using 'Content here, content here', making it look like readable English.

| 요리                | 객체 지향 프로그래밍                   |
| ------------------- | -------------------------------------- |
| **요리도구**        | 4대 원칙(상속, 추상화, 다형성, 캡슐화) |
| **요리도구 사용법** | 5대 설계 원칙(SOLID)                   |
| **레시피**          | 디자인 패턴                            |

디자인 패턴은 실제 개발 현장에서 ~~~~~~~~

> 자바 엔터프라이즈 개발을 편하게 해주는 오픈소스 경량급 애플리케이션 프레임워크  
> OOP 프레임워크

### 01-1. 어댑터 패턴(Adapter Pattern)

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

## ⚡ 02. 스프링 삼각형과 설정정보

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

- [[블로그] Spring 이론 (POJO, Java Beans)](https://ksshlee.github.io/spring/spring/)
