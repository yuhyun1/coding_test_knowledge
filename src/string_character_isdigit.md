- `Character.isDigit(char ch)` - ch가 숫자인지 검사하여 boolean값을 반환


- if (!Character.inDigit(c)) return false;
    
이 코드는 입력된 문자 `c`가 숫자인지 검사하는 코드입니다.
    
`!Character.isDigit(c)`는 입력된 문자 `c`가 숫자가 아니라면 `true`를 반환합니다. 
    
`!`는 논리 부정 연산자로, `true`를 `false`로, `false`를 `true`로 변경합니다.
    
따라서, `if (!Character.isDigit(c))`는 입력된 문자 `c`가 숫자가 아니면 `true`가 되어, `return false;`를 실행하여 `false`를 반환합니다.
    
즉, 이 코드는 문자열에서 숫자가 아닌 문자가 포함되어 있는 경우 `false`를 반환하며, 이를 통해 숫자로만 이루어진 문자열인지를 확인할 수 있습니다.
    
- `Character.inDigit`
    
**`Character.isDigit(char ch)`** 메소드는 매개변수로 전달된 문자 `ch`가 숫자인지를 검사하여, 숫자이면 `true`를 반환하고, 아니면 `false`를 반환합니다.
    
반면에 **`Character.inDigit(char ch)`** 메소드는 `isDigit()`와 비슷하지만, `Unicode`의 10진수 범주(0~9)에 있는 숫자인지를 검사합니다. 
    
`inDigit()`는 `isDigit()`와 같은 역할을 하지만, 더 넓은 범위의 숫자(예를 들어, 한자의 숫자 등)도 인식할 수 있습니다.
    
그러므로, 대부분의 경우 `isDigit()`를 사용하는 것이 적절합니다.
    
- `Character`는 변수가 아니라 클래스?
    
네, 맞습니다. `Character`는 자바에서 제공하는 클래스이며, `char`값에 대한 작업을 수행하는 정적 메서드와 상수를 제공합니다. 
    
`isDigit()`메서드는 `Character`클래스에 속한 정적 메서드 중 하나입니다.

---
**`Character.isAlphabetic(char ch)`** 메서드는 해당 문자가 알파벳인지 아닌지를 판별해주는 Java 내장 메서드입니다.

인자로 받은 **`char`** 타입의 문자가 알파벳이면 **`true`**를, 알파벳이 아니면 **`false`**를 반환합니다.

예를 들어, **`Character.isAlphabetic('a')`**의 결과는 **`true`**이며, **`Character.isAlphabetic('1')`**의 결과는 **`false`**입니다.

이를 이용해 문자열에서 알파벳인 문자를 판별하거나, 알파벳이 아닌 문자를 제외하고 문자열을 처리할 수 있습니다.


---

**`Character.isSpaceChar(char ch)`** 메서드는 인자로 전달된 **`char`** 값이 공백 문자인지 여부를 판별하는 메서드입니다.

공백 문자는 스페이스( ), 탭(**`\t`**), 개행(**`\n`**), 캐리지 리턴(**`\r`**) 등 다양한 문자를 포함합니다.

이 메서드는 이러한 공백 문자를 모두 판별합니다.

만약 해당 문자가 공백 문자라면 `true`를 반환하고, 그렇지 않다면 `false`를 반환합니다.

아래는 **`isSpaceChar()`** 메서드를 사용한 예시입니다.

```java
char c = ' ';
if (Character.isSpaceChar(c)) {
    System.out.println("The character is a whitespace.");
} else {
    System.out.println("The character is not a whitespace.");
}
```

위 예시에서 `c`는 공백 문자를 나타내는 스페이스( )입니다. `isSpaceChar()`메서드는 이를 공백 문자로 판별하므로, 출력 결과는 `The character is a whitespace.`가 됩니다.