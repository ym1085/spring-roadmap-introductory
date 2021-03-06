## π λͺ©μ°¨

- λμμΈν¨ν΄ κ°μ
- λμμΈν¨ν΄ μ’λ₯
  - μ΄λν° ν¨ν΄
  - νλ‘μ ν¨ν΄
  - λ°μ½λ μ΄μ ν¨ν΄
  - μ±κΈν΄ ν¨ν΄
  - ννλ¦Ώ λ©μλ ν¨ν΄
  - `ν©ν°λ¦¬ λ©μλ ν¨ν΄`
  - μ λ΅ ν¨ν΄
  - ννλ¦Ώ μ½λ°± ν¨ν΄
  - μ€νλ§μ΄ μ¬λν λ€λ₯Έ ν¨ν΄λ€(λ§λ¬΄λ¦¬)

## 01. μ€νλ§μ΄ μ¬λν λμμΈν¨ν΄

![μ£Όλ°©λκ΅¬](./images/kitchen_utensils.jpg)

> νμ¬κΉμ§λ OOPμ 4λ νΉμ±κ³Ό 5λ μμΉμ λν΄ μ§ν νμμ΅λλ€

1. κ°μ²΄ μ§ν₯μ 4λ νΉμ±
2. SOLID 5λ μμΉ
3. `λμμΈν¨ν΄` π

**κ°μ²΄ μ§ν₯ νΉμ±**μ **λκ΅¬**, **μ€κ³ μμΉ**μ **λκ΅¬λ₯Ό μ¬λ°λ₯΄κ² μ¬μ©νλ λ°©λ²**μ΄λ€.  
κ·Έλ λ€λ©΄, λμμΈν¨ν΄μ λ¬΄μμ λΉμ ν  μ μμμ§ μλ νλ₯Ό μ΄ν΄λ³΄μ.

| μλ¦¬                                | κ°μ²΄ μ§ν₯ νλ‘κ·Έλλ°                   |
| ----------------------------------- | -------------------------------------- |
| **μλ¦¬λκ΅¬**                        | 4λ μμΉ(μμ, μΆμν, λ€νμ±, μΊ‘μν) |
| **μλ¦¬λκ΅¬ μ¬λ°λ₯΄κ² μ¬μ©νλ λ°©λ²** | 5λ μ€κ³ μμΉ(SOLID)                   |
| `λ μνΌ`                            | λμμΈ ν¨ν΄                            |

## 01-1. λμμΈν¨ν΄μ΄λ?

<img alt="curiosity" src="./images/curiosity.png" width=70%>

- νλμ μλ¦¬μ λν νμ€ν λ λ°©μμ΄ μ‘΄μ¬.
- νλ‘κ·Έλ¨μ μμ±νλ€λ³΄λ©΄ `λΉμ·ν μν©`μ μ§λ©΄νκ² λ¨
- μ΄λ¬ν μν©μμ μ΄μ μ λ§μ κ°λ°μλ€μ΄ κ³ λ―Όνκ³  μ μ ν `νμ€ μ€κ³ ν¨ν΄`λ₯Ό μλ―Έ

> μ¦, μ€μ  κ°λ° νμ₯μμ λ€μν μκ΅¬μ¬ν­μ νλ‘κ·Έλλ°μΌλ‘ μ²λ¦¬νλ©΄μ λ§λ€μ΄μ§ λ€μν ν΄κ²°μ± μ€  
> λ§μ μ¬λλ€μ΄ μΈμ ν **Best Practice**λ₯Ό μ λ¦¬ν κ².

## 01-2. μ€νλ§ νλ μμν¬(Spring Framework)

> μ€νλ§ νλ μμν¬λ₯Ό μ€λͺνλ κ³΅μμ μΈ μ μ

- μλ° μν°νλΌμ΄μ¦ κ°λ°μ νΈνκ² ν΄μ£Όλ **Open source application framework**
- **OOP νλ μμν¬**
- `μ€νλ§`μ `κ°μ²΄ μ§ν₯`μ `νΉμ±κ³Ό μ€κ³ μμΉ`μ `κ·Ήν`κΉμ§ μ μ©ν νλ μμν¬

## 02. μ΄λν° ν¨ν΄(Adapter Pattern)

![phone](./images/charger.jpg)

> π‘ κ°λ° νμ μμΉμ νμ©ν μ€κ³ ν¨ν΄, **κ°μ²΄λ₯Ό μμ±μΌλ‘ λ§λ€μ΄ μ°Έμ‘°νλ λμμΈ ν¨ν΄**

- μ΄λν°λ₯Ό λ²μ­νλ©΄ `λ³νκΈ°`
- **μλ‘ λ€λ₯Έ λ μΈν°νμ΄μ€ μ¬μ΄μ ν΅μ μ κ°λ₯νκ² ν¨**
- λνμ μΌλ‘λ `ν΄λν° μΆ©μ κΈ°`κ° μ‘΄μ¬
- λ€μν DataBaseλ₯Ό μ‘°μν  μ μλ μΈν°νμ΄μ€
  - ODBC(Open Database Connectivity), JDBC(Java Database Connectivity)
  - JRE

## 02-1. μ΄λν° ν¨ν΄

```java
// Before : Class ServiceA
public class ServiceA {
    void runServiceA() {
        System.out.println("ServiceA");
    }
}
```

```java
// Before : Class ServiceA
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
        ServiceA sa1 = new ServiceA(); // 1. κ°μ²΄ μμ±
        ServiceB sb1 = new ServiceB(); // 2. κ°μ²΄ μμ±

        sa1.runServiceA(); // 3. sa1.runServiceA() νΈμΆ
        sb1.runServiceB(); // 4. sa1.runServiceB() νΈμΆ
    }
}
```

- νμ¬ sa1, sb1 μ°Έμ‘° λ³μλ₯Ό ν΅ν΄ runServiceA(), runServiceB() λ©μλ νΈμΆ
- λΉμ·ν μΌμ νμ§λ§ λ©μλλͺλ§ λ€λ₯Έ κ²μ νμΈ κ°λ₯

### 02-2. μνΈμ€ λ€μ΄μ΄κ·Έλ¨(Sequence Diagram)

![before_adapter_diagram](./images/before_adapter_diagram.PNG)

### 02-3. μ΄λν° ν¨ν΄ μ μ© ν

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

        asa1.runService();
        asb1.runService();
    }
}
```

- ν΄λΌμ΄μΈνΈ(ClientWithAdapter)κ° λ³νκΈ°λ₯Ό ν΅ν΄ λμΌν λ©μλμΈ runService() νΈμΆ
- μ¦, μ§μ  ServiceA, ServiceBμ λ©μλλ₯Ό νΈμΆνλ κ²μ΄ μλ μ΄λν° κ°μ²΄λ₯Ό ν΅ν΄ μ κ·Ό

### 02-4. μνΈμ€ λ€μ΄μ΄κ·Έλ¨(Sequence Diagram)

![after_adapter_diagram](./images/after_adapter_diagram.PNG)

- μ΄λν° ν¨ν΄ `ν©μ±`, μ¦ κ°μ²΄λ₯Ό μμ±μΌλ‘ λ§λ€μ΄μ μ°Έμ‘°νλ λμμΈ ν¨ν΄
- νΈμΆ λΉνλ μͺ½μ λ©μλ(**runServiceA**)λ₯Ό μ€κ° λ³νκΈ°(**AdapterServiceA**)λ₯Ό ν΅ν΄ νΈμΆνλ ν¨ν΄

## 03. νλ‘μ ν¨ν΄(Proxy Pattern)

<img alt="proxy" src="./images/proxy.png" width=80%>

> κ°λ°© νμ μμΉκ³Ό μμ‘΄ μ­μ  λ²μΉμ΄ λΉμλ€μ΄ μλ νλ‘μ ν¨ν΄

- νλ‘μλ λλ¦¬μ, λλ³μΈμ λ»μ κ°μ§ λ¨μ΄
- λμμΈ ν¨ν΄μμλ λλ¦¬μ/λλ³μΈμ νλ‘μ ν¨ν΄μΌλ‘ νν

![before_proxy_pattern_diagram](./images/before_proxy_pattern_diagram.PNG)

![before_proxy_pattern_seq_diagram](./images/before_proxy_pattern_seq_diagram.PNG)

- ClientWithNoProxyκ° λλ¦¬μ(**νλ‘μ κ°μ²΄**)μμ΄ Service κ°μ²΄μ runSomething() μ§μ  νΈμΆ

### 03-1. νλ‘μ ν¨ν΄ μ μ© μ 

```java
// Before: Class Service
public class Service {

    public String runSomething() {
        return "μλΉμ€λ₯Ό μ€νν©λλ€.";
    }
}
```

```java
// Before: Class ClientWithNoProxy
public class ClientWithNoProxy {

    public static void main(String[] args) {
        // νλ‘μλ₯Ό μ΄μ©νμ§ μμ νΈμΆ
        Service service = new Service(); // κ²°ν©λ μ­μ μ¬λΌκ°
        System.out.println(service.runSomething);
    }
}
```

- ClientWithNoProxy ν΄λμ€μμ Service ν΄λμ€μ λ©μλλ₯Ό μ§μ  νΈμΆ
- μμ κ°μ μ½λλ₯Ό A(ClientWithNoProxy) κ° Bμ μμ‘΄νλ€ ν  μ μλ€

### 03-2. νλ‘μ ν¨ν΄

![after_proxy_pattern_diagram](./images/after_proxy_pattern_diagram.PNG)

> νλ‘μ ν¨ν΄μ μ¬μ©νκΈ° μν μ μ°¨

- νλ‘μ ν¨ν΄μ κ²½μ° **μ€μ  μλΉμ€ κ°μ²΄κ° κ°μ§ λ©μλμ κ°μ μ΄λ¦μ λ©μλ**λ₯Ό μ¬μ©
  - μ΄λ₯Ό μν΄μ μΈν°νμ΄μ€ μ¬μ©
- μΈν°νμ΄μ€λ₯Ό μ¬μ©νλ©΄ μλΉμ€ κ°μ²΄κ° λ€μ΄κ° μλ¦¬μ λλ¦¬μ κ°μ²΄κ° ν¬μλ¨
- **ν΄λΌμ΄μΈνΈλ μλΉμ€ κ°μ²΄λ₯Ό νΈμΆνλμ§, λλ¦¬μ κ°μ²΄λ₯Ό νΈμΆνλμ§ μ μκ° μλ€**

### 03-3. μνΈμ€ λ€μ΄μ΄κ·Έλ¨

![after_proxy_pattern_seq_diagram.PNG](./images/after_proxy_pattern_seq_diagram.PNG)

### 03-4. νλ‘μ ν¨ν΄ μ μ© ν

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
        return "μλΉμ€λ₯Ό μ€νν©λλ€.";
    }
}
```

```java
// After: Class Proxy
// @desc : π‘ μ€κ° λλ¦¬μμ μ­ν μ μν, νΈμΆμ λν λ³κ²½μ΄ μλ μ μ΄κ° μ£Ό λͺ©μ μ΄λ€
public class Proxy implements IService {
    IService service; // μΈν°νμ΄μ€ IServiceμ μ°Έμ‘° λ³μλ₯Ό λ§΄λ²λ‘ κ°λλ€

    @Overried
    public String runSomething() {
        System.out.println("νΈμΆμ λν νλ¦ μ μ΄κ° μ£Όλͺ©μ , λ°ν κ²°κ³Όλ₯Ό κ·Έλλ‘ μ λ¬")

        // Bussiness Logic μν κ°λ₯

        service = new Service();
        return service.runSomething();
    }
}
```

```java
// After: Class ClientWithProxy
public class ClientWithProxy {

    public static void main(String[] args) {
         // λ€νμ±, λΆλͺ¨ κ°μ²΄λ‘ μμ κ°μ²΄λ₯Ό λ°μ
         // ex) List<String> list = new ArrayList<>();
        IService proxy = new Proxy();
        System.out.println(proxy.runSomething());
    }
}
```

> λλ¦¬μμ μ­ν , μ¬κΈ°μλ Proxy ν΄λμ€κ° λλ€

1. μλΉμ€μ κ°μ μ΄λ¦μ λ©μλ κ΅¬ν, μ΄λ μΈν°νμ΄μ€ μ¬μ©
2. μ€μ  μλΉμ€μ λν μ°Έμ‘° λ³μλ₯Ό κ°μ(**ν©μ±**)
3. μ€μ  μλΉμ€μ κ°μ μ΄λ¦μ κ°μ§ λ©μλ νΈμΆ, κ·Έ κ°μ λ°ν
4. μ€μ  μλΉμ€μ **λ©μλ νΈμΆ μ νμ λ³λμ λ‘μ§ μν κ°λ₯**

### νμ€ μ λ¦¬

> β­ **μ μ΄ νλ¦μ μ‘°μ νκΈ° μν λͺ©μ μΌλ‘ μ€κ°μ λλ¦¬μλ₯Ό λλ ν¨ν΄**

## 04. λ°μ½λ μ΄ν° ν¨ν΄(Decorator Pattern)

<img alt="curiosity" src="./images/decorator_pattern_tree.jpg" width=70%>

- λ°μ½λ μ΄ν°λ **λμ₯**, **λλ°°μμ**, `μ₯μμ`μ λ»μ κ°μ§ λ¨μ΄
- μ¦, `μλ³Έμ μ΄λ ν μ₯μμ λνλ ν¨ν΄`μ΄λΌλ κ²μ΄ μ΄λ¦μμ λ€μ΄λ¨
- νλ‘μ ν¨ν΄κ³Ό κ΅¬ν λ°©λ²μ΄ κ°μΌλ, `ν΄λΌμ΄μΈνΈμ μ΅μ’ λ°νκ°μ μ‘°μ`

### 04-1. νλ‘μ ν¨ν΄κ³Ό λ°μ½λ μ΄ν° ν¨ν΄ λΉκ΅

- `νλ‘μ ν¨ν΄`
  - μ μ΄μ νλ¦μ λ³κ²½νκ±°λ λ³λμ λ‘μ§ μ²λ¦¬ λͺ©μ 
  - ν΄λΌμ΄μΈνΈμ λ°ν κ°μ νΉλ³ν κ²½μ°κ° μλλ©΄ λ³κ²½νμ§ μμ
- `λ°μ½λ μ΄ν° ν¨ν΄`
  - ν΄λΌμ΄μΈνΈκ° λ°λ λ°νκ°μ μ₯μμ λνλ€
  - μ¦, `return κ°μ νΈλ€λ§ νλ€λ μλ―Έ`

### 04-2. λ°μ½λ μ΄ν° ν¨ν΄ μ μ©

```java
// Interface Iservice
public Interface IService {
    public abstract String runSomething();
}
```

```java
// Class Service
public class Service implements IService {

    @Overried
    public String runSomething() {
        return "μΆμ λ©μλ runSomething νΈμΆ!";
    }
}
```

```java
// Class Decoreator
public class Decoreator implements IService {
    IService service; // interface ref variable

    public String runSomething() {
        // System.out.println("νΈμΆμ λν νλ¦ μ μ΄κ° μ£Όλͺ©μ , λ°ν κ²°κ³Όλ₯Ό κ·Έλλ‘ μ λ¬") // Proxy
        System.out.println("νΈμΆμ λν μ₯μμ΄ λͺ©μ , ν΄λΌμ΄μΈνΈμκ² λ°ν κ²°κ³Όμ μ₯μμ λνμ¬ μ λ¬");

        service = new Service();

        // μ μ μ λ°ν κ°μ λ°μ½λ μ΄ν° λ¨μμ νΈλ€λ§
        return "μ λ§" + service.runSomething();
    }
}
```

```java
// Class Decoreator
public class ClientWithDecorator {

    public static void main(String[] args) {
        // μμ μΈν°νμ΄μ€λ‘ νμ Decorator κ°μ²΄λ₯Ό λ°λλ€
        IService decorator = new Decoreator();

        // How to call method?
        //  γ΄ decorator.runSomthine
        //      γ΄ service.runSomthine
        System.out.println(decorator.runSomething());
    }
}
```

> Class : Decorator => 'μ₯μμ', Service => 'μλΉμ€'

1. μ₯μμλ μ€μ  μλΉμ€μ `κ°μ μ΄λ¦μ λ©μλ` κ΅¬ν, μ΄ λ μΈν°νμ΄μ€ μ¬μ©
2. μ₯μμλ μ€μ  μλΉμ€μ λν `μ°Έμ‘° λ³μ`λ₯Ό κ°λλ€(ν©μ±)
3. μ₯μμλ `μ€μ  μλΉμ€μ κ°μ μ΄λ¦μ κ°μ§ λ©μλ νΈμΆ, λ°νκ°μ μ‘°μ ν λ°ν`
4. μ₯μμλ μ€μ  μλΉμ€μ λ©μλ `νΈμΆ μ νμ λΉμ¦λμ€ λ‘μ§ μν` κ°λ₯

### νμ€ μ λ¦¬

> β­ λ©μλ νΈμΆμ λ°νκ°μ λ³νλ₯Ό μ£ΌκΈ° μν΄ μ€κ°μ μ₯μμ(Decorator)λ₯Ό λλ ν¨ν΄

## 05. μ±κΈν΄ ν¨ν΄(Singleton Pattern)

![connection_pool](./images/connection_pool.PNG)

- `μΈμ€ν΄μ€λ₯Ό νλλ§ λ§λ€μ΄ μ¬μ©νκΈ° μν ν¨ν΄. `
- **Connection pool**, **Thread pool**μ μΈμ€ν΄μ€λ₯Ό μ¬λ¬κ°λ₯Ό λ§λ€λ©΄ λΆνμν μμ μ¬μ©.
  - νλ‘κ·Έλ¨μ΄ μμμΉ λͺ»ν κ²°κ³Όλ₯Ό λ³μ μ μμ.

### 05-1. μ±κΈν΄ ν¨ν΄ μ μ©μ μν μ μ½

> μ±κΈν΄ ν¨ν΄μ μ€μ§ μΈμ€ν΄μ€λ₯Ό νλλ§ λ§λ€κ³  κ·Έκ²μ κ³μν΄μ μ¬μ¬μ©νλ€  
> μ±κΈν΄ ν¨ν΄μ μ μ©ν  κ²½μ° μλ―Έμ λ κ°μ κ°μ²΄κ° μ‘΄μ¬ν  μ μλ€

1. κ°μ²΄ μμ±μ μν **new ν€μλ**μ μ μ½μ κ±Έμ΄μΌ ν¨
2. μ μΌν λ¨μΌ κ°μ²΄λ₯Ό λ°νν  μ μλ μ μ  λ©μλ(**static method**) νμ
3. μ μΌν λ¨μΌ κ°μ²΄λ₯Ό μ°Έμ‘°ν  μ μ  μ°Έμ‘° λ³μ(**static variable**)κ° νμ

### 05-2. μ±κΈν΄ ν¨ν΄ μ μ©

```java
// Class Singleton
public class Singleton {
    static Singleton singletonObj; // static reference variable

    // private constructor
    private Singleton() { };

    // return singletonObj
    public static Singleton getInstance() {
        if (singletonObj == null) {
            singletonObj = new Singleton();
        }
        return singletonObj;
    }
}
```

```java
// Class Client
public class Client {

    public static void main(String[] args) {
        // The constructor Singleton() is not visible
        // Singleton singleton = new Singleton();

        Singleton s1 = Singleton.getInstance();
        Singleton s2 = Singleton.getInstance();
        Singleton s3 = Singleton.getInstance();

        System.out.println(s1);
        System.out.println(s2);
        System.out.println(s3);

        s1 = null;
        s2 = null;
        s3 = null;
    }
}
```

### 05-3. λ©λͺ¨λ¦¬ κ΅¬μ‘° νμΈ

![singleton_memory](./images/singleton_memory.PNG)

- 4κ°μ μ°Έμ‘°λ³μκ° νλμ λ¨μΌ κ°μ²΄λ₯Ό μ°Έκ³ 
- `λ¨μΌ κ°μ²΄`μΈ κ²½μ° κ³΅μ  κ°μ²΄λ‘ μ¬μ©λκΈ° λλ¬Έμ `μμ±μ κ°μ§ μλκ² μ μ`
  - νλμ μ°Έμ‘° λ³μκ° λ³κ²½ν μμ±μ΄ λ€λ₯Έ μ°Έμ‘° λ³μμ μν₯μ λ―ΈμΉ¨
  - μ΄λ₯Ό, μ μ­/κ³΅μ  λ³μλ₯Ό κ°λ₯ν μ¬μ©νμ§ λ§λΌλ μ§μΉ¨κ³Ό μΌλ§₯μν΅
  - final static λ³μλ μκ΄ μμ

### 05-4. μ±κΈν΄ ν¨ν΄ μ λ¦¬

1. `private μμ±μ`
2. `static μ°Έμ‘° λ³μ`
3. `static λ©μλ`

### νμ€ μ λ¦¬

> β­ ν΄λμ€μ μΈμ€ν΄μ€, μ¦ κ°μ²΄λ₯Ό νλλ§ λ§λ€μ΄ μ¬μ©νλ ν¨ν΄

## 06. ννλ¦Ώ λ©μλ ν¨ν΄(Template Method Pattern)

- `μμ ν΄λμ€μμ μ²λ¦¬μ νλ¦μ μ μ΄`
- `νμ ν΄λμ€μμ μ²λ¦¬μ λ΄μ©μ κ΅¬μ²΄ν νλ κ²`

### 06-1. ννλ¦Ώ λ©μλ ν¨ν΄ μ μ©(Template Method Pattern) μ μ© μ 

```java
// Before : Class Dog
public class Dog {
    public void playWithOwner() {
        System.out.println("κ·μΌλ₯μ΄ μ΄λ¦¬μ¨...");
        System.out.println("λ©! λ©! λ©!"); // μ€λ³΅
        System.out.println("κΌ¬λ¦¬ μ΄λ μ΄λ~");
        System.out.println("μνμ΄");
    }
}
```

```java
// Before : Class Cat
public class Cat {
    public void playWithOwner() {
        System.out.println("κ·μΌλ₯μ΄ μ΄λ¦¬μ¨...");
        System.out.println("μΌμΉ~ μΌμΉ~"); // μ€λ³΅
        System.out.println("κΌ¬λ¦¬ μ΄λ μ΄λ~");
        System.out.println("μνμ΄");
    }
}
```

- λλ²μ§Έ μ€μ λ³΄λ©΄ `μ€λ³΅λλ μ½λ`κ° μ‘΄μ¬
- OOPμ νΉμ± μ€ νλμΈ `μμ`μ ν΅ν΄ λ¬Έμ  ν΄κ²°

### 06-2. ννλ¦Ώ λ©μλ ν¨ν΄(Template Method Pattern) μ μ© ν

```java
// After : Class Animal
public abstract class Animal {
    // template Method
    public void playWithOwner() {
        System.out.println("κ·μΌλ₯μ΄ μ΄λ¦¬μ¨...");
        play();
        runSomething();
        System.out.println("μνμ΄");
    }

    // abstract method
    abstract void play();

    // Hook(κ°κ³ λ¦¬) λ©μλ, abstract ν€μλ μμ΄μΌν¨
    void runSomething() {
        System.out.println("κΌ¬λ¦¬ μ΄λ μ΄λ~");
    }
}
```

**ν(Hook) λ©μλλ?**

abstract ν€μλλ₯Ό ν΄λμ€μ λΆνλ©΄ μμλ°μ ν΄λμ€λ λ°λμ ν΄λΉ ν΄λμ€μ  
μΆμ λ©μλλ₯Ό κ΅¬νν΄μΌ νμ§λ§ ν(Hook) λ©μλλ‘ λ§λ€λ©΄ λ°λμ κ΅¬νν  νμκ° μλ€.  
μ¦, μ νμ  μ€λ²λΌμ΄λ©(Override)κ° κ°λ₯ν΄μ§λ€λ λ§μ΄λ€.

```java
// After : Class Dog
public class Dog extends Animal {

    // μΆμ λ©μλ μ€λ²λΌμ΄λ©
    @Override
    void play() {
        System.out.println("λ©! λ©!");
    }

    // Hook λ©μλ μ€λ²λΌμ΄λ©
    @Override
    void runSomething() {
        System.out.println("λ©! λ©!~ κΌ¬λ¦¬ μ΄λ μ΄λ~");
    }
}
```

```java
// After : Class Cat
public class Cat extends Animal {

    // μΆμ λ©μλ μ€λ²λΌμ΄λ©
    @Override
    void play() {
        System.out.println("μΌμΉ~ μΌμΉ~");
    }

    // Hook λ©μλ μ€λ²λΌμ΄λ©
    @Override
    void runSomething() {
        System.out.println("μΌμΉ~ μΌμΉ~ κΌ¬λ¦¬ μ΄λ μ΄λ~")
    }
}
```

```Java
// After : Class Driver
public class Driver {

    public static void main(String[] args) {
        Animal bolt = new Dog();
        Animal kitty = new Cat();

        bolt.playWithOwner(); // bolt μ°Έμ‘° λ³μλ‘ template method νΈμΆ

        System.out.println();
        System.out.println();

        kitty.playWithOwner(); // kitty μ°Έμ‘° λ³μλ‘ template method νΈμΆ
    }
}
```

### 06-2. μνΈμ€ λ€μ΄μ΄κ·Έλ¨

- `μμ ν΄λμ€ Animal`μλ `ννλ¦Ώ`μ μ κ³΅νλ `playWithOwner λ©μλ`κ° μ‘΄μ¬
  - play() μΆμ λ©μλ
  - runSomething() ν λ©μλ

> μ΄μ²λΌ **μμ ν΄λμ€**μ **κ³΅ν΅ λ‘μ§μ μννλ ννλ¦Ώ λ©μλ**μ **νμ ν΄λμ€**μ μ€λ²λΌμ΄λ©μ κ°μ νλ **μΆμ λ©μλ** λλ μ νμ  μ€λ²λΌμ΄λ©μ΄ κ°λ₯ν **ν λ©μλ**λ₯Ό λλ ν¨ν΄μ ννλ¦Ώ λ©μλ ν¨ν΄μ΄λΌ μ§μΉ­νλ€.

![template_method_seq_diagram](./images/template_method_seq_diagram.PNG)

![template_method_pattern_diagram](./images/template_method_pattern_diagram.PNG)

| ννλ¦Ώ λ©μλ ν¨ν΄ κ΅¬μ± μμ               | μμ ν΄λμ€ Animal | νμ ν΄λμ€ Dog, Cat | λΆμ° μ€λͺ                                                    |
| ------------------------------------------ | ------------------ | -------------------- | ------------------------------------------------------------ |
| ννλ¦Ώ λ©μλ                              | playWithOwner()    |                      | κ³΅ν΅ λ‘μ§μ μν, λ‘μ§ μ€ νμ ν΄λμ€μ μΆμ, ν λ©μλ νΈμΆ |
| ννλ¦Ώ λ©μλμμ νΈμΆνλ μΆμ λ©μλ     | play()             | μ€λ²λΌμ΄λ© νμ      | λΉκ³                                                          |
| ννλ¦Ώ λ©μλμμ νΈμΆνλ ν(Hook) λ©μλ | runSomething()     | μ€λ²λΌμ΄λ© μ ν      | λΉκ³                                                          |

### νμ€ μ λ¦¬

> β­μμ ν΄λμ€μ κ²¬λ³Έ λ©μλμμ νμ ν΄λμ€κ° μ€λ²λ¦¬μ΄λ©ν λ©μλλ₯Ό νΈμΆνλ ν¨ν΄

## 07. ν©ν°λ¦¬ λ©μλ ν¨ν΄(Factory Method Pattern)

<img alt="curiosity" src="./images/abstract_factory_pattern.PNG" width=70%>

- μ°μ , κ³΅μ₯μ΄λΌλ λ¨μ΄λ₯Ό μκ°ν΄λ³΄λ©΄, `λ¬΄μΈκ°λ₯Ό μμ°νλ€` λΌλ λ¨μ΄κ° λ μ€λ₯Έλ€
- κ°μ²΄μ§ν₯μμ `ν©ν°λ¦¬`λ κ°μ²΄λ₯Ό μμ±νλλ°, `ν©ν λ¦¬ λ©μλ`λ `κ°μ²΄λ₯Ό μμ± λ°ννλ λ©μλλ₯Ό μλ―Έ`
- **νμ ν΄λμ€μμ ν©ν°λ¦¬ λ©μλλ₯Ό μ€λ²λΌμ΄λ©νμ¬ κ°μ²΄λ₯Ό λ°ννλ κ²**

![ball_dog](./images/ball_dog.png)

> μμμ κ°μμ§ boltμ κ³ μμ΄ kittyκ° μ£ΌμΈκ³Ό λΈλ μ½λλ₯Ό μμ±ν΄ λ³΄μλλ°  
> μ΄λ²μλ boltμ kittyκ° **κ°μ κ°μ§κ³  λκ³  μΆμ΄νλ μ₯λκ°μ κ°μ Έμ€λ λͺ¨μ΅**μ μμν΄λ³΄μ

### 07-1 ν©ν°λ¦¬ λ©μλ ν¨ν΄ μ μ©

```java
// abstract class Animal
public abstract class Animal {

    // μΆμ ν©ν°λ¦¬ λ©μλ
    abstract AnimalToy getToy();
}
```

```java
// abstract class AnimalToy
// @desc ν©ν°λ¦¬ λ©μλκ° μμ±ν  κ°μ²΄μ μμ ν΄λμ€
public abstract class AnimalToy {

    abstract void identify();
}
```

```java
// class Dog
public class Dog extends Animal {

    // μΆμ ν©ν°λ¦¬ λ©μλ μ€λ²λΌμ΄λ©
    @Override
    AnimalToy getToy() {
        return new DogToy();
    }

}
```

```java
// class DogToy
public class DogToy extends AnimalToy {

    public void identify() {
        System.out.println("λλ νλμ€κ³΅! κ°μμ§μ μΉκ΅¬!");
    }
}
```

```java
// class Cat
public class Cat extends Animal {

    // μΆμ ν©ν°λ¦¬ λ©μλ μ€λ²λΌμ΄λ©
    @Override
    AnimalToy getToy() {
        return new CatToy();
    }

}
```

```java
// class CatToy
public class CatToy extends AnimalToy {

    public void identify() {
        System.out.println("λλ μΊ£νμ! κ³ μμ΄μ μΉκ΅¬!");
    }
}
```

```java
public class Driver {

    public static void main(String[] args) {
        // ν©ν°λ¦¬ λ©μλλ₯Ό λ³΄μ ν κ°μ²΄λ€ μμ±
        Animal bolt = new Dog();
        Animal kitty = new Cat();

        // ν©ν°λ¦¬ λ©μλκ° λ°ννλ κ°μ²΄λ€
        AnimalToy boltBall = bolt.getToy();
        AnimalToy kittyTower = kitty.getToty();

        // ν©ν°λ¦¬ λ©μλκ° λ°νν κ°μ²΄λ€μ μ¬μ©
        boltBall.identify();
        boltBall.identify();
    }
}
```

![factory_method_pattern_diagram](./images/factory_method_pattern_diagram.PNG)

![factory_method_patter_seq_diagram](./images/factory_method_patter_seq_diagram.PNG)

### νμ€ μ λ¦¬

> β­ μ€λ²λΌμ΄λλ λ©μλκ° κ°μ²΄λ₯Ό λ°ννλ ν¨ν΄

## 08. μ λ΅ ν¨ν΄(Strategy Pattern)

- μ λ΅ λ©μλλ₯Ό κ°μ§ μ λ΅ κ°μ²΄
- μ λ΅ κ°μ²΄λ₯Ό μ¬μ©νλ **μ»¨νμ€νΈ**(**μ λ΅ κ°μ²΄ μ¬μ©μ**)
- μ λ΅ κ°μ²΄λ₯Ό μμ±ν΄ μ»¨νμ€νΈμ μ£Όμνλ **ν΄λΌμ΄μΈνΈ**(**μ λ΅ κ°μ²΄ κ³΅κΈμ**)

![strategy_pattern](./images/strategy_pattern.PNG)

> `ν΄λΌμ΄μΈνΈλ λ€μν μ λ΅ μ€ νλλ₯Ό μ νν΄ μμ± ν μ»¨νμ€νΈμ μ£Όμ`

- λ³΄κΈ μ₯κ΅κ° κ΅°μΈμκ² λ¬΄κΈ°λ₯Ό μ§κΈνλ€.
  - **λ³΄κΈ μ₯κ΅** : ν΄λΌμ΄μΈνΈ
  - **κ΅°μΈ** : μ»¨νμ€νΈ
  - **λ¬΄κΈ°** : μ λ΅

### 08-1. μ λ΅ ν¨ν΄(Strategy Pattern) μ μ©

```java
// μ λ΅μ© μΈν°νμ΄μ€
public interface Strategy {
    public abstract void runStrategy(); // μ λ΅ λ©μλ μμ±
}
```

```java
public class StrategyGun implements Strategy {

    @Override
    public void runStrategy() {
        System.out.println("ν!, ν!, ν!, μ΄μΌλ‘ μλ μ λ΅!");
    }
}
```

```java
public class StrategySword implements Strategy {

    @Override
    public void runStrategy() {
        System.out.println("μ±!, μ±!, μ±!, κ²μ νλλ₯΄λ μ λ΅!");
    }
}
```

```java
public class StrategyBow implements Strategy {

    @Override
    public void runStrategy() {
        System.out.println("μμ°μ°μ°μμ~~~!, νμ μλ μ λ΅!");
    }
}
```

```Java
// κ΅°μΈμ μ­ν 
public class Soldier {

    void runContext(Strategy strategy) {
        System.out.println("μ ν¬ μμ");
        strategy.runStrategy();
        System.out.println("μ ν¬ μ’λ£");
    }
}
```

```java
// λ³΄κΈ μ₯κ΅μ μ­ν 
public class Client {

    public static void main(String[] args) {
        Strategy strategy = null;
        Soldier rambo = new Soldier();

        // μ΄μ λλ³΄μκ² μ λ¬, μ ν¬ μν
        strategy = new StrategyGun();
        rambo.runContext(strategy);

        System.out.println();

        // κ²μ λλ³΄μκ² μ λ¬, μ ν¬ μν
        strategy = new StrategySword();
        rambo.runContext(strategy);

        System.out.println();
        // νμ΄μ λλ³΄μκ² μ λ¬, μ ν¬ μν
        strategy = new StrategySBow();
        rambo.runContext(strategy);
    }
}
```

```
μ ν¬ μμ
ν!, ν!, ν!, μ΄μΌλ‘ μλ μ λ΅!
μ ν¬ μ’λ£

μ ν¬ μμ
μ±!, μ±!, μ±!, κ²μ νλλ₯΄λ μ λ΅!
μ ν¬ μ’λ£

μ ν¬ μμ
μμ°μ°μ°μμ~~~!, νμ μλ μ λ΅!
μ ν¬ μ’λ£
```

- μ λ΅ ν¨ν΄κ³Ό ννλ¦Ώ λ©μλ ν¨ν΄μ΄ λΉμ·ν κ°μ΄ μμ§λ§, λ¨μΌ μμλ§ κ°λ₯ν μλ° -> **μ λ΅ ν¨ν΄**

![strategy_pattern_diagram](./images/strategy_pattern_diagram.PNG)

![strategy_pattern_seq_diagram](./images/strategy_pattern_seq_diagram.PNG)

### νμ€ μ λ¦¬

> β­ ν΄λΌμ΄μΈνΈ μΈ‘μμ μ λ΅(κ°μ²΄)μ μμ±ν΄ μ λ΅μ μ€νν  μ»¨νμ€νΈμ μ£Όμνλ ν¨ν΄

## 09. ννλ¦Ώ μ½λ°± ν¨ν΄(Template Callback Pattern)

> κ²¬λ³Έ/νμ  ν¨ν΄

- μ λ΅ ν¨ν΄μ λ³νν λμμΈ ν¨ν΄
- `μ€νλ§μ 3λ νλ‘κ·Έλλ° λͺ¨λΈ` μ€ νλμΈ `DIμμ μ¬μ©λλ ννμ μ λ΅ ν¨ν΄`
- μ λ΅ ν¨ν΄κ³Ό λͺ¨λ  κ²μ΄ λμΌ, `μ λ΅μ μ΅λͺ λ΄λΆ ν΄λμ€λ‘ μ μνμ¬ μ¬μ©`

### 09-1. ννλ¦Ώ μ½λ°± ν¨ν΄(Template Callback Pattern) μ μ©

```java
// μ λ΅ : Strategy
public interface Strategy {
    public abstract void runStrategy();
}
```

```java
// μ»¨νμ€νΈ : κ΅°μΈ
public class Soldier {

    void runContext(Strategy strategy) {
        System.out.println("μ ν¬ μμ");
        strategy.runStrategy();
        System.out.println("μ ν¬ μ’λ£");
    }
}
```

```java
// ν΄λΌμ΄μΈνΈ : μ₯κ΅
public class Client {

    public static void main(String[] args) {
        Soldier rambo = new Soldier();

        rambo.runContext(new Strategy() {
            @Override
            public void runStrategy() {
                System.out.println("μ΄! μ΄μ΄μ΄μ΄μ΄ λ°μ¬!!");
            }
        });

        System.out.println();

        rambo.runContext(new Strategy() {
            @Override
            public void runStrategy() {
                System.out.println("μΉΌ! μΉ΄κ°κ° μΉΌ! μΉΌλ‘ μ°λ₯Έλ€!!");
            }
        });

        System.out.println();

        rambo.runContext(new Strategy() {
            @Override
            public void runStrategy() {
                System.out.println("λλΌ λλ.... λλΌλ‘ λ΄λ¦¬μΉλ€!!");
            }
        });
    }
}
```

### 09-2. ννλ¦Ώ μ½λ°± ν¨ν΄(Template Callback Pattern) λ¦¬ν©ν λ§

```java
// μ λ΅ : Strategy
public interface Strategy {
    public abstract void runStrategy();
}
```

```java
// μ»¨νμ€νΈ : κ΅°μΈ
public class Soldier {

    void runContext(String weaponSound) {
        System.out.println("μνμ¬μ νκ³‘μ μ€μ κ²μ νμν©λλ€.");
        executeWeapon(weaponSound).runStrategy();
        System.out.println("μ ν¬κ° μ’λ£λμμ΅λλ€.");
    }

    private Strategy executeWeapon(final String weaponSound) {
        return new Strategy() {
            @Override
            public void runStrategy() {
                System.out.println(weaponSound);
            }
        };
    }
}
```

```java
// ν΄λΌμ΄μΈνΈ : μ₯κ΅
public class Client {

    public static void main(String[] args) {
        Soldier rambo = new Soldier();

        rambo.runContext("μ΄! λ°μ¬!");
        rambo.runContext("μΉΌ! μ°λ₯Έλ€!");
        rambo.runContext("λλΌ! λ΄λ¦¬μΉλ€!");
    }
}
```

### νμ€ μ λ¦¬

> β­ μ λ΅μ μ΅λͺ λ΄λΆ ν΄λμ€λ‘ κ΅¬νν μ λ΅ ν¨ν΄

## 10. μ€νλ§μ΄ μ¬λν λ€λ₯Έ ν¨ν΄λ€(λμμΈν¨ν΄ λ§λ¬΄λ¦¬)

- μ 8κ°μ§ ν¨ν΄ λ§κ³ λ μ€νλ§μ λ€μν λμμΈ ν¨ν΄ νμ©
- λνμ μΌλ‘λ Spring MVC(Model, View, Controller) ν¨ν΄ μ‘΄μ¬

### μ°Έκ³  μλ£

- [[μ± λ§ν¬] μ€νλ§ μλ¬Έμ μν μλ° κ°μ²΄ μ§ν₯μ μλ¦¬μ μ΄ν΄](http://www.yes24.com/Product/Goods/22483294)
- [[μ¬μ§ μ°Έκ³ ] Spring μ΄λ‘  (POJO, Java Beans)](https://ksshlee.github.io/spring/spring/)
- [[μ¬μ§ μ°Έκ³ ] IStock](https://www.istockphoto.com/kr/%EB%B2%A1%ED%84%B0/%EB%91%90-%EB%B2%A1%ED%84%B0-%ED%81%AC%EB%A6%AC%EC%8A%A4%EB%A7%88%EC%8A%A4-%ED%8A%B8%EB%A6%AC%EC%9E%85%EB%8B%88%EB%8B%A4-%ED%81%AC%EB%A6%AC%EC%8A%A4%EB%A7%88%EC%8A%A4-%ED%8A%B8%EB%A6%AC-%EA%BE%B8%EB%AF%B8%EA%B8%B0-%EC%A0%84%ED%9B%84-%ED%81%AC%EB%A6%AC%EC%8A%A4%EB%A7%88%EC%8A%A4-%EC%9E%A5%EC%8B%9D-%ED%94%8C%EB%9E%AB-%EA%B3%A0%EB%A6%BD-%EB%90%9C-%EA%B7%B8%EB%A6%BC%EC%9E%85%EB%8B%88%EB%8B%A4-gm1064483898-284620235)
- [[μ¬μ§ μ°Έκ³ ] How Do I Setup A Proxy Server On Windows PC?](https://streamtelly.com/proxy-server-windows/)
- [[μ¬μ§ μ°Έκ³ ] Connection pool](https://hyuntaeknote.tistory.com/12)
- [[μ¬μ§ μ°Έκ³ ] μΆμ ν©ν λ¦¬ ν¨ν΄](https://heebeom.me/posts/abstract-factory-pattern/)
