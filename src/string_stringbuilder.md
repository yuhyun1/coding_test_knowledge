반복문을 이용하여 String을 구성하는 예시 코드)

```java
String az = "";
for (char c = 'a'; c <= 'z'; c++) {
	az += c;
}
System.out.println(az);           //   "abcd..xyz"
```

이 코드는 비효율적인 코드. 단순히 “abc…xyz”를 만들기 위해 제곱의 시간 복잡도를 소요.

이를 해결하기 위해 StringBuilder 클래스 등장.

- StringBuilder 클래스에서 자주 사용하는 메서드

| 메서드 | 역할 | 시간 복잡도 |
| --- | --- | --- |
| StringBuilder.toString() | 지금까지 구성한 문자열을 String 형식으로 반환함. | O(N) |
| StringBuilder.append(char c) | 문자 c를 문자열 끝에 이어 붙임. | O(1) |
| StringBuilder.length() | 지금까지 구성한 문자열 길이를 반환함. | O(1) |
| StringBuilder.reverse() | 지금까지 구성한 문자열을 뒤집음. | O(N) |

‘a’부터’z’까지 이어 붙이는 앞의 예시 코드를 StringBuilder를 이용하여 바꾼 코드)

```java
StringBuilder azBuilder = new StringBuilder();
for (char c = 'a'; c <= 'z'; c++) {
	azBuilder.append(c);
}
String az = azBuilder.toString();
System.out.println(az);              //    "abcd...xyz"
```