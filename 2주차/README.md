# 2주차
## CHAPTER 11,12
### 생각해보기 
#### 1) 입력값을 사용했을 때의 장점과 어떤 입력값이 존재할 수 있을까요
입력값을 사용했을때의 가장 장점은 사용자가 직접 필요할 정보를 입력할 수 있다는점 같습니다. 입력값으로는 어떤 데이터 형이든지 상관없을거 같습니다.
#### 2) 다른 방법으로도 자바에서 입력값을 받을 수 있을까요?
이 강의를 보기 이전에는 Scanner를 통한 입력, BufferedReader를 통한입력을 알고 있었는데 joptionpane은 처음 접해봤습니다. 
#### 3) argument와 parameter에 대해서 토론해 보세요
Parameter는 함수 혹은 메서드 정의에서 나열되는 변수 명입니다. 반면 Argument는 함수 혹은 메서드를 호출할 때, 전달 혹은 입력되는 실제 값입니다. Parameter의 실체는 변수이고 Argument의 실체는 값입니다
#### 4) 컴파일하고 실행하는 과정에서 어떤 일이 일어나는지 댓글로 토론해 보세요
![컴파일과정](https://img1.daumcdn.net/thumb/R1280x0/?scode=mtistory2&fname=https%3A%2F%2Fblog.kakaocdn.net%2Fdn%2FbpZT7s%2FbtqA2OXCTqK%2FnkV7pgjkSGG01pMSIjnynK%2Fimg.png)
빌드 시, 자바 파일(*.java)을 자바 컴파일러(javac.exe)를 이용하여 JVM이 이해할 수 있는 중간단계의 언어 바이트 코드(*.class)로 바꿔줍니다. 런타임 시, 바이트코드를 기계어로 바꿔주는데 이 역할을 JVM에서 합니다. Class Loader를 통해 바이트코드를 JVM내로 로드하고, Runtime Data Areas를 거쳐 Execution Engine으로 갑니다. Execution Engine에서 바이트코드로 변환하는 두 가지 방식이 있습니다. 인터프리터와 JIT컴파일러(Just-In-Time) 방식이 있습니다. 인터프리터 방식은 위에서 설명한 인터프리터 방식이며, JIT 컴파일러는 인터프리터 방식을 사용하다가 적정한 때에 바이트코드 전체를 기계어로 바꾸는 방식을 취합니다. 이 때 기계어는 캐싱을 이용하기 때문에 인터프리터의 단점을 극복할 수 있습니다.


출처)https://ttuk-ttak.tistory.com/38
#### 5) 라이브러리와 패키지는 무슨 차이점이 있을까요?
라이브러리가 더 상위 개념이다 쉽게말해 라이브러리안에 다양한패키지가 있고 패키지안에 클래스의 모음이있다.
#### 6) 명령어로 앱을 실행할 때 입력값을 주면 어떤 점이 좋은지 댓글로 토론해 보세요
cmd에서 argumant를 입력해서 바로 쓰는 것이 바로바로 실행할 수 있기 때문에 시간이 절약된다.
___
## CHAPTER 13
### 생각해보기 
#### 1) 자바 API는 무엇인가요?
API란 자바 시스템을 제어하기 위해서 자바에서 제공하는 명령어들을 의미한다. Java SE(JDK)를 설치하면 자바 시스템을 제어하기 위한 API를 제공한다. 자바 개발자들은 자바에서 제공한 API를 이용해서 자바 애플리케이션을 만들게 된다
#### 2) API와 UI의 차이점은 무엇인가요?
![API와 UI의 차이](https://img1.daumcdn.net/thumb/R1280x0/?scode=mtistory2&fname=https%3A%2F%2Fblog.kakaocdn.net%2Fdn%2FbtU1d2%2FbtqxTLqoWn6%2FatPkPvhrkA39XL4Q1LDAZ0%2Fimg.png)
UI는 사용자(User)입장에서 대화를 위한 접점(Interface)를 의미합니다. 마찬가지로 API란 앱(Application Programming)입장에서의 대화를 위한 접점(Interface)라고 할 수 있습니다. 


출처)https://gamsunghacker.tistory.com/2
#### 3) 클래스가 무엇인지 댓글로 토론해 보세요
객체를 만들어 내기 위한 설계도 혹은 틀,
연관되어 있는 변수와 메서드의 집합이라고 할 수 있습니다.
#### 4) 인스턴스와 클래스는 무슨 관계인가요?
설계도를 바탕으로 소프트웨어 세계에 구현된 구체적인 실체,
즉, 객체를 소프트웨어에 실체화 하면 그것을 ‘인스턴스’라고 부릅니다다. 실체화된 인스턴스는 메모리에 할당됩니다.
#### 5) 상속이란 무엇인지 댓글로 적어 보세요
Java에서 상속은 부모 클래스의 변수/메소드를 자식 클래스가 물려받아 그대로 사용 가능하게 해줍니다.

여기서 부모클래스를 superclass, 자식클래스를 subclass라 부릅니다.
자식클래스에서 A라는 기능을 처리하는데 부모클래스에서 이미 똑같은 A라는 기능을 처리하고 있다면

자식클래스는 이를 상속받아 그대로 사용할 수 있으며, 코드의 중복을 막아줍니다.


출처)https://gangnam-americano.tistory.com/23
