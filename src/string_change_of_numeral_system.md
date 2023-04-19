- 문자열과 정수를 변환하는 메서드

| 메서드 | 반환형 | 내용 |
| --- | --- | --- |
| Integer.parseInt(String s) |  int | 숫자를 표현하는 문자열 s를 정수로 변환 |
| Integer.toString(int v) | String | 정수 v를 문자열로 변환 |
| Long.parseLong(String s) | long | 숫자를 표현하는 문자열 s를 정수로 변환 |
| Long.toString(long v) | String | 정수 v를 문자열로 변환 |

이 메서드들은 모두 10진수를 기준으로 합니다. `parseInt()` 나 `parseLong()` 메서드는 전달받는 문자열이 10진수로 표현되었을 때 정상적으로 동작하며, `toString()` 메서드는 해당 정수를 10진수로 표현된 문자열로 구성하여 반환합니다.

그런데 여기서 하나의 매개변수만 추가하면 아주 쉽게 진법을 변환할 수 있습니다.

- 문자열과 정수를 진법에 따라 변환하는 메서드

| 메서드 | 반환형 | 내용 |
| --- | --- | --- |
| Integer.parseInt(String s, int radix) |  int | radix진법으로 숫자를 표현하는 문자열 s를 정수로 변환 |
| Integer.toString(int v, int radix) | String | 정수 v를 radix진법의 문자열로 변환 |
| Long.parseLong(String s, int radix) | long | radix진법으로 숫자를 표현하는 문자열 s를 정수로 변환 |
| Long.toString(long v, int radix) | String | 정수 v를 radix진법의 문자열로 변환 |

2진수로 표현된 문자열을 16진수로 변경하는 예시 코드)

```java
String binary = "1010";
int value = Integer.parseInt(binary, 2);
String hex = Integer.toString(value, 16);
```

2진법 문자열 “1010”이 파싱되어 value 변수에는 정수 10이 들어갑니다. hex 변수에는 이 값을 16진수로 변환한 문자열 “a”가 들어갑니다. 대문자로 표현된 16진수를 얻고 싶다면 String.toUpperCase()를 사용합니다.

```java
String hex = Integer.toString(value, 16).toUpperCase();
```
