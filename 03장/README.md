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

<img alt="curiosity" src="./images/curiosity.png" width=70%>

- 프로그램을 작성하다보면 `비슷한 상황`을 직면하게 됨.
- 이러한 상황에서 이전의 많은 개발자들이 고민하고 정제한 `표준 설계 패턴`를 의미.

> 즉, 실제 개발 현장에서 다양한 요구사항을 프로그래밍으로 처리하면서 만들어진 다양한 해결책 중  
> 많은 사람들이 인정한 Best Practice를 정리한 것.

## 01-2. 스프링 프레임워크(Spring Framework)

> 스프링 프레임워크를 설명하는 공식정인 정의

- 자바 엔터프라이즈 개발을 편하게 해주는 **Open source application framework**
- **OOP 프레임워크**
- `스프링`은 `객체 지향`의 `특성과 설계 원칙`을 `극한`까지 적용한 프레임워크

## 01-1. 어댑터 패턴(Adapter Pattern)

![phone](./images/charger.jpg)

> 💡 개발 폐쇄 원칙()을 활용한 설계 패턴

- 어댑터를 번역하면 `변환기`
- **서로 다른 두 인터페이스 사이에 통신을 가능하게 함**
- 대표적으로는 `휴대폰 충전기`가 존재
- ODBC(Open Database Connectivity), JDBC(Java Database Connectivity), JRE

### 어댑터 패턴 적용 전

```java
// Before: Class ServiceA
public class ServiceA {
    void runServiceA() {
        System.out.println("ServiceA");
    }
}
```

```java
// Before: Class ServiceB
public class ServiceB {
    void runServiceB() {
        System.out.println("ServiceB");
    }
}
```

```java
// Before: Class ClientWithNoAdapter
public class ClientWithNoAdapter {

    public static void main(String[] args) {
        ServiceA sa1 = new ServiceA(); // 1. 객체 생성
        ServiceB sb1 = new ServiceA(); // 2. 객체 생성

        sa1.runServiceA(); // 3. sa1.runServiceA() 호출
        sb1.runServiceB(); // 4. sa1.runServiceB() 호출
    }
}
```

- 현재 sa1, sb1 참조 변수를 통해 runServiceA(), runServiceB() 메서드 호출
- 비슷한 일을 하지만 메서드명만 다른 것을 확인 가능

### 시퀸스 다이어그램(Sequence Diagram)

![before_adapter_diagram](./images/before_adapter_diagram.PNG)

### 어댑터 패턴 적용 후

```java
// After: Class AdapterServiceA
public class AdapterServiceA {
    ServiceA sa1 = new ServiceA();

    void runService() {
        sa1.runServiceA();
    }
}
```

```java
// After: Class AdapterServiceB
public class AdapterServiceB {
    ServiceA sb1 = new ServiceB();

    void runService() {
        sb1.runServiceB();
    }
}
```

```java
// After: Class ClientWithAdapter
public class ClientWithAdapter {

    public static void main(String[] args) {
        AdapterServiceA asa1 = new AdapterServiceA();
        AdapterServiceB asb1 = new AdapterServiceB();

        sa1.runService();
        sb1.runService();
    }
}
```

- 클라이언트(ClientWithAdapter)가 변환기를 통해 동일한 메서드인 runService() 호출
- 즉, 직접 ServiceA, ServiceB의 메서드를 호출하는 것이 아닌 어댑터 객체를 통해 접근

### 시퀸스 다이어그램(Sequence Diagram)

![after_adapter_diagram](./images/after_adapter_diagram.PNG)

- 어댑터 패턴 `합성`, 즉 객체를 속성으로 만들어서 참조하는 디자인 패턴
- 호출 당하는 쪽의 메서드(**runServiceA**)를 중간 변환기(**AdapterServiceA**)를 통해 호출하는 패턴

## 01-2. 프록시 패턴(Proxy Pattern)

> 개방 폐쇄 원칙과 의존 역전 법칙이 녹아들어 있는 프록시 패턴

- 프록시는 대리자, 대변인의 뜻을 가진 단어
- 디자인 패턴에서는 대리자/대변인을 프록시 패턴으로 표현

![before_proxy_pattern_diagram](./images/before_proxy_pattern_diagram.PNG)

![before_proxy_pattern_seq_diagram](./images/before_proxy_pattern_seq_diagram.PNG)

- ClientWithNoProxy가 대리자(**프록시 객체**)없이 Service 객체의 runSomething() 직접 호출

### 프록시 패턴 적용 전

```java
// Before: Class Service
public class Service {

    public String runSomething() {
        return "서비스를 실행합니다.";
    }
}
```

```java
// Before: Class ClientWithNoProxy
public class ClientWithNoProxy {

    public static void main(String[] args) {
        // 프록시를 이용하지 않은 호출
        Service service = new Service(); // 결합도 역시 올라감
        System.out.println(service.runSomething);
    }
}
```

- ClientWithNoProxy 클래스에서 Service 클래스의 메서드를 직접 호출.
- 위와 같은 코드를 A 가 B(ClientWithNoProxy)에 의존한다 할 수 있다.

### 프록시 패턴

![after_proxy_pattern_diagram](./images/after_proxy_pattern_diagram.PNG)

- 프록시 패턴의 경우 **실제 서비스 객체가 가진 메서드와 같은 이름의 메서드**를 사용
  - 이를 위해서 인터페이스 사용
- 인터페이스를 사용하면 서비스 객체가 들어갈 자리에 대리자 객체가 투입됨
- **클라이언트는 서비스객체를 호출하는지, 대리자 객체를 호출하는지 알 수가 없다.**

### 시퀸스 다이어그램

![](./images/after_proxy_pattern_seq_diagram.PNG)

1. ClientWithProxy 클래스에서 메서드 호출
2. BBB
3. CCC

### 프록시 패턴 적용 후

```java
// After: Interface IService
public interface IService {
    String runSomething();
}
```

```java
// After: Class Service
public class Service implements IService {

    @Overried
    public String runSomething() {
        return "서비스를 실행합니다.";
    }
}
```

```java
// After: Class Proxy
// @desc : 💡 중간 대리자의 역할을 수행, 호출에 대한 변경이 아닌 제어가 주 목적이다
public class Proxy implements IService {
    IService service; // 인터페이스 IService의 참조 변수를 맴버로 갖는다

    @Overried
    public String runSomething() {
        System.out.println("호출에 대한 흐름 제어가 주목적, 반환 결과를 그대로 전달")

        // Bussiness Logic 수행 가능

        service = new Service();
        return service.runSomething();
    }
}
```

```java
// After: Class ClientWithProxy
public class ClientWithProxy {

    public static void main(String[] args) {
         // 다형성, 부모 객체로 자식 객체를 받음
         // ex) List<String> list = new ArrayList<>();
        IService proxy = new Proxy();
        System.out.println(proxy.runSomething());
    }
}
```

> 대리자의 역할, 여기서는 Proxy 클래스가 된다

1. 서비스와 같은 이름의 메서드 구현, 이때 인터페이스 사용
2. 실제 서비스에 대한 참조 변수를 갖음(**합성**)
3. 실제 서비스와 같은 이름을 가진 메서도 호출, 그 값을 반환
4. 실제 서비스의 **메서드 호출 전후에 별도의 로직 수행 가능**

⭐ **제어 흐름을 조정하기 위한 목적으로 중간에 대리자를 두는 패턴**

## 01-3. 데코레이터 패턴(Decorator Pattern)

## 01-4. 싱글턴 패턴(Singleton Pattern)

## 01-5. 템플릿 메서드 패턴(Template Method Pattern)

## 01-6. 팩터리 메서드 패턴(Factory Method Pattern)

## 01-7. 전략 패턴(Strategy Pattern)

## 01-8. 템플릿 콜백 패턴(Template Callback Pattern - 견본/회신 패턴)

## 01-9. 스프링이 사랑한 다른 패턴들(디자인패턴 마무리)

- 위 8가지 패턴 말고도 스프링은 다양한 디자인 패턴 활용.
- 대표적으로는 Spring MVC(Model, View, Controller) 패턴 존재.

## 02. 스프링 삼각형과 설정정보

<img alt="spring_fw" src="./images/spring_fw.png" width=70%>

- **DI**(**Dependency Injection**)
- **AOP**(**Aspect Oriented Programming**)
- **PSA**(**Portable Service Abstractions**)

## 02-1. IOC/DI - 제어의 역전과 의존성 주입

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
