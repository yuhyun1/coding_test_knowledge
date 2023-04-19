- 숫자를 표현하는 문자의 아스키 코드

| 문자 | ‘0’ | ‘1’ | ‘2’ | ‘3’ | ‘4’ | ‘5’ | ‘6’ | ‘7’ | ‘8’ | ‘9’ |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| 아스키 코드 | 48 | 49 | 50 | 51 | 52 | 53 | 54 | 55 | 56 | 57 |

숫자를 표현하는 문자에서 ‘0’의 아스키코드를 빼면 해당 문자가 표현하는 정수 값이 나옴.

예를 들어 ‘5’가 표현하는 정수 값을 알아내기 위해’5’ - ‘0’ = 53 - 48 = 5처럼 계산함.

예시 코드)

```java
char digit = '9';
int digitToInt = digit - '0';
```

내장 라이브러리를 이용한 예시 코드)

```java
char digit = '9';
int digitToInt = Character.getNumbericValue(digit);
```

- 영문 소문자를 대문자로 바꾸는 법

아스키 코드표에서는 소문자는 소문자끼리, 대문자는 대문자끼리 연속해서 등장함.

대문자 ‘A’ ~ ‘Z’는 65~90의 값, 소문자 ‘a’ ~ ‘z’는 97~122의 값을 가짐.

예시 변환 코드)

```java
char lower = 'e';
char upper = (char) (lower + ('a' - 'A'));
```

char끼리 연산하면 정수형으로 취급되어 int형으로 형 변환이 일어남.

따라서 다시 문자로 취급하기 위해서는 char형으로 강제 형 변환을 시켜줘야 함.

내장 라이브러리를 이용한 예시 코드)

```java
char lower = 'e';
char upper = Character.toUpperCase(lower);
```

대문자를 소문자로 변환하는 코드)

```java
char upper = 'G';
char lower = (char) (upper - ('a' - 'A'));
```

내장 라이브러리를 이용한 예시 코드)

```java
char upper = 'G';
char lower = Character.toLowerCase(upper);
```