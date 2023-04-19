- 포함 여부를 검사하는 메서드

| 메서드 | 반환형 | 내용 |
| --- | --- | --- |
| contains(CharSequence s) | boolean | 전달받은 문자열이 원본 문자열에 있는지 검사 |
| stratsWith(String prefix) | boolean | 원본 문자열이 전달받은 문자열로 시작하는지 검사 |
| endsWith(String suffix) | boolean | 원본 문자열이 전달받은 문자열로 끝나는지 검사 |
| indexOf(String str) | int | 전달받은 문자열이 원본 문자열에서 몇 번째 인덱스에 있는지 검사 |

- 문자열 치환 메서드

| 메서드 | 반환형 | 내용 |
| --- | --- | --- |
| replace(char oldChar, char newChar) | String | 원본 문자열의 oldChar 문자들을 newChar 문자로 치환한 문자열을 반환 |
| replace(CharSequence target, CharSequence replacement) | String | 원본 문자열에서 등장하는 target문자열을 replacement 문자열로 치환해서 반환 |

CharSequence는 문자열을 나타내는 인터페이스입니다. String 클래스도 CharSequence 인터페이스를 구현하고 있기 때문에 일반적인 문자열과 같다고 생각해도 무방합니다.