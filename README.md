# 자바 디자인 패턴

### 1. 객체지향 원리

- **추상화**

  > 어떤 영역에서 필요로 하는 **속성(변수)**이나 **행동(메소드)**을 추출하는 작업

  - **인간이 세상을 인식하는 방법**
  - **클래스 설계 시 변수와 메소드를 정의**하는 과정

- **캡슐화**

  > **높은 응집도**와 **낮은 결합도**를 유지하기 위한 객체지향 원리

  - ~~(개발자의 숙명인)~~**요구사항 변경에 의한 코드 수정을 최소화**
  - **응집도(↑): 가족(클래스 내부)** 구성원 간 얼마나 화목한지?
  - **결합도(↓): 이웃(클래스-클래스)** 간 얼마나 사이가 좋은지?
  - ~~팔은 안으로 굽는다~~

- **일반화**

  > 여러 개체들이 가진 **공통된 특성**을 부각시켜 하나의 개념이나 법칙으로 성립시키는 과정

  - **공통된 특성은 부모 클래스로** 모으고 자식 클래스의 특수한 기능은 각각 따로 정의(**상속**)

- **다형성**

  > 서로 다른 클래스의 객체가 **같은 메시지**를 받았을 때 **각자의 방식으로 동작**하는 능력

  - (동물에게 인사를 건넨다) 강아지: 멍멍! / 고양이: 야옹~ / 소: 음메~ 

  ​

- **코드에 적용하기**

  ```java
  public abstract class Pet {
    private String name;
    public Pet(String name){
      this.name = name;
    }
    public abstract void talk();
  }

  public class Cat extends Pet{
    public void talk(){
      System.out.println("야옹~");
    }
  }

  public class Dog extends Pet {
    public void talk(){
      System.out.println("멍멍!");
    }
  }

  public class Cow extends Cow {
    public void talk(){
      System.out.println("음메~");
    }
  }

  public class Main {
    public static void groupTalk(Pet[] p){
      int i;
      
      for(i = 0 ; i < 3; ㅑ++){
        p.talk();
      }
    }
  }

  public static void main(String[] args){
    Pet[] p = {new Cat(), new Dog(), new Cow()};
    groupTalk(p);
  }
  ```
