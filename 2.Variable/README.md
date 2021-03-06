변수(Variable)
====   

- 하나의 데이터를 저장하기 위해 프로그램에 의해 이름을 **할당받은 메모리공간**   
- 변수에 저장된 값은 변경가능   
- **초기화** : 변수에 초기값을 주는 행위. 즉, 변수에 값을 저장하는 행위   

## 변수의 종류  

- 기본타입 (primitive type)
    + 정수형, 실수형, 논리형
- 참조타입 (reference type)
    + 문자열, 배열 등

## 변수의 선언   

- 변수의 선언만 하는 방법 (데이터타입 변수명;)   
     ```int num;```
- 변수의 선언과 동시에 초기화하는 방법 (데이터타입 변수명 = 저장할 값;)   
     ```int num = 17;```

## 변수의 이름 작성 규칙   

- 첫번째 글자는 문자, $, _로 시작해야하며 **숫자로 시작 불가**
- 영어 대소문자가 구분되며 $, _를 제외한 **특수문자 사용 불가**
- 자바에서 미리 정의된 **예약어 사용불가** (int, String 등)
- 변수의 이름 사이에 **공백 포함 불가**
- **카멜표기법**(Camel case) - 첫 글자는 소문자로 작성하되 다른 단어가 붙을 경우 대문자로 작성 (ex. kakaoTalk)

## 변수 값 읽기   

- 변수는 초기화가 되어야 읽을 수 있음
- 초기화되지 않은 변수는 프로그램 안정성을 위해 사용불가 ~(만약 사용할경우 컴파일에러 발생)~

```java
public class Study {
    public static void main(String[] args){
        // 변수 초기화
        int num = 8;

        // 변수(num)의 값에 5를 더하는 연산 수행 후 result에 결과저장
        int result = num + 5;   // result = 13
    }
}
```

## 변수의 범위

- 선언된 블록 내에서만 사용가능
```java
public class Study2 {
    public static void main(String[] args){
        int a = 10;

        if(a < 15){
            int b = a + 5;  // b 변수는 if 블록에서만 유효, 실행이 끝나면 사라짐
        }

        int c = a + b + 10; // b 변수를 사용할 수 없어 컴파일 에러 발생 
    }
}
```