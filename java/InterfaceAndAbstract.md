# **Interface와 abstract의 차이**

## 작성자
[![rlatjdwo555](https://avatars0.githubusercontent.com/u/28692938?s=100&v=4)](https://github.com/rlatjdwo555)

## Interface?
- 인터페이스란 일종의 추상클래스이다. 추상화의 정도가 높기 때문에 일반 메소드나 멤버 변수를 가질 수 없고 오직 **추상메소드와 상수만**을 멤버로 가질 수 있다.

- 인터페이스 자체만으로 새로운 인스턴스(객체)를 생성할 수 없다. 

- 인터페이스를 쓰는 이유
    - 완벽한 추상화를 이루기 위해(메소드 구현 목적)
    - 다중 상속
    - 다형성

## Abstract?
- 상속을 강제하는 일종의 규제이다.
- 일반적인 추상화 및 상속에 초점을 둔다.
    - 예를 들어 냉장고, TV, 커피머신, 전자렌지등의 클래스를 만들어야할 일이 있을 때 가전제품이라는 추상클래스로 추상화 시켜서 사용하면 좋을 때 사용한다. 

    - 가전제품은 공통적으로 (on(), off(), 전기소모(), 기타등) 사용되는 메서드들을 적고, 구체적인 가전제품별로 별도의 동작(메서드)을 나눠서 적는다. 냉장고는 차갑게하고 전자렌지는 물분자 운동을 시키는 동작 등

    - 이렇듯 상속 받아서 기능을 확장시키는 목적으로 사용한다.


### 1. 추상 메소드
- 메소드의 정의만 되어있는 비어있는 메소드
- body가 있는 메소드는 abstract 키워드를 가질 수 없다.
```java
public abstract int show(); 
// public abstract int show(){System.out.println("hello")} <-- 불가능
```

### 2. 추상 클래스
- 추상 메소드를 하나라도 포함하고 있는 클래스는 추상 클래스가 된다.
- 추상 클래스만으로 새로운 인스턴스(객체)를 생성할 수 없다.
- 멤버 변수와 구현된 메소드가 존재 가능
- 다중 상속 불가