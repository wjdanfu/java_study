# 4주차
## CHAPTER 2
### 생각해보기 
#### 1) 코드를 재사용하게 된다면 어떤 장점이 있을까요
코드의 재사용은 장황한 작업에 소비하는 시간과 에너지를 절약하는 전형적 기법입니다. 
라이브러리는 추상화가 좋은 예입니다. 
프로그래머는 프로그램의 일부를 재사용가능하게 하기 위해서 내부에 추상화 포인트를 작성하거나 자기 부담으로 사용하기 위해서 커스텀 라이브러리를 만들거나 합니다. 
소프트웨어를 보다 재사용하기 쉽게 하는 특성을 모듈성, 저결합도, 고응집도, 캡슐화, 관심의 분리 등으로 부릅니다.
기존 코드를 사용하여 새로운 코드를 만드는 경우, 하등의 인터페이스 혹은 액세스 수단이 정의되어 있지 않으면 안 됩다. 
이것에는 서브루틴 호출, 오브젝트, 클래스, 프로토 타입 등이 포함되는 것이 일반적입니다. 기업에서는 이것들을 정식화, 표준화해두는 것이 일반적입니다.
#### 2) 파라미터와 아규먼트는 무엇을 가리키는 용어인가요?
Parameter는 함수 혹은 메서드 정의에서 나열되는 변수 명입니다. 
반면 Argument는 함수 혹은 메서드를 호출할 때, 전달 혹은 입력되는 실제 값입니다. 
Argument의 실체는 변수이고 Argument의 실체는 값입니다.
#### 3) 메소드가 파라미터로 값을 받아 들인다면 어떤 이점이 있을까요?
검색을 하다가 정말 좋은예가 있어서 가져와봤습니다.

출처) https://jojoldu.tistory.com/232
#### 4) 공통된 작업을 추출해서 하나의 메소드로 만들게 되면 어떤 장단점이 있을까요?
장점) 같은작업을 할때 코드를 두번,세번 쓰지않고 메소드를 이용해 해결할수 있습니다.

#### 5) 왜 static 메소드가 필요할까요?
![static](https://t1.daumcdn.net/cfile/tistory/99AAAC405CEC82C032)

[ Static 변수 특징 ]
- Static 변수는 클래스 변수이다.
- 객체를 생성하지 않고도 Static 자원에 접근이 가능하다.

Static Method는 객체의 생성 없이 호출이 가능하며, 객체에서는 호출이 가능은 하지만 지양하고 있습니다. 
일반적으로는 유틸리티 관련 함수들은 여러 번 사용되므로 static 메소드로 구현을 하는 것이 적합한데, 
static 메소드를 사용하는 대표적인 Util Class로는 java.uitl.Math가 있습니다.
```java
public class Test {
    private String name1 = "MangKyu";
    private static String name2 = "MangKyu";
 
    public static void printMax(int x, int y) {
        System.out.println(Math.max(x, y));
    }
         
    public static void printName(){
       // System.out.println(name1); 불가능한 호출
       System.out.println(name2);
    }
}
```
 두 수의 최대값을 구하는 경우에 Math클래스를 사용하는데, static 메소드로 선언된 max 함수를 초기화 없이 사용합니다. 
 하지만 static 메소드에서는 static이 선언되지 않은 변수에 접근이 불가능한데, 메모리 할당과 연관지어 생각해보면 당연합니다. 
 우리가 Test.printName() 을 사용하려고 하는데, name1은 new 연산을 통해 객체가 생성된 후에 메모리가 할당됩니다. 
 하지만 static 메소드는 객체의 생성 없이 접근하는 함수이므로, 할당되지 않은 메모리 영역에 접근을 하므로 문제가 발생하게 됩니다. 
 그러므로 static 메소드에서 접근하기 위한 변수는 반드시 static 변수로 선언되어야 합니다.
 
 출처) https://mangkyu.tistory.com/47
