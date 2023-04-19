스택과 큐는 완전 탐색에서 언급된 적이 있는 자료 구조입니다.

이 두 가지는 원소를 특정한 순서대로 삽입하고 제거할 수 있는 자료 구조로, 다음 연산을 제공합니다.

1. 원소 삽입
2. 원소 제거
3. 자료 구조가 비어 있는지 검사

두 자료 구조가 이 세 가지 연산을 어떻게 처리하는지 살펴봅시다.

스택은 LIFO(Last In First Out: 후입선출) 특징이 있는 자료 구조입니다.

스택을 쉽게 이해하기 위해 좁고 긴 바구니를 생각해봅시다.

이 바구니는 좁고 길기 때문에 원소를 집어넣으면 그대로 쌓입니다.

이렇게 쌓인 원소들을 다시 스택에서 꺼낼 때는 넣은 순서의 반대로 꺼냅니다.

이렇듯 스택은 전혀 어려운 개념의 자료 구조가 아닙니다.

자바에서는 스택은 내장 제네릭 클래스로 지원합니다.

정수를 담을 수 있는 스택은 다음과 같이 선언할 수 있습니다.

```java
Stack<Integer> stack = new Stack<>();
```

이 Stack 클래스는 방금 살펴본 스택 기능을 모두 지원하고, 다음 패키지를 선언하면 사용할 수 있습니다.

```java
import java.util.Stack;
```

원소 추가는 add() 메서드, 삭제는 pop() 메서드로 할 수 있는데, pop() 메서드를 호출하면 제거된 원소가 반환됩니다.

```java
Stack<Integer> stack = new Stack<>();
        
        stack.add(1);
        stack.add(2);
        stack.add(3);

        System.out.println(stack.pop()); // 3
        System.out.println(stack.pop()); // 2
        
        stack.add(4);
        stack.add(5);

        System.out.println(stack.pop()); // 5
        System.out.println(stack.pop()); // 4
        System.out.println(stack.pop()); // 1
```

주의해야 할 점은 스택이 비어 있는 상태에서 원소를 제거하는 pop() 메서드를 호출하면 EmptyStackException이 발생한다는 것입니다.

따라서 스택이비어 있지 않을 때만 pop() 메서드를 호출하는 것이 중요합니다.

스택이 비어 있는지 여부는 isEmpty() 메서드로 확인할 수 있습니다.

```java
Stack<Integer> stack = new Stack<>();
        
        stack.add(1);
        stack.add(2);
        stack.add(3);

        System.out.println(stack.pop()); // 3
        System.out.println(stack.pop()); // 2
        
        stack.add(4);
        stack.add(5);

        System.out.println(stack.pop()); // 5
        System.out.println(stack.pop()); // 4

        System.out.println(stack.isEmpty()); // false

        System.out.println(stack.pop()); // 1

        System.out.println(stack.isEmpty()); // true
```

마지막으로 peek() 메서드로 스택에서 값을 재거하지 않고도 스택의 가장 위에 있는 값을 얻을 수 있습니다.

peek() 메서드 또한 스택이 비어 있을 때 호출하면 EmptyStackException을 발생시킵니다.

```java
Stack<Integer> stack = new Stack<>();
        
        stack.add(1);
        stack.add(2);
        stack.add(3);

        System.out.println(stack.pop()); // 3
        System.out.println(stack.pop()); // 2
        
        stack.add(4);
        stack.add(5);

        System.out.println(stack.pop()); // 5
        System.out.println(stack.pop()); // 4

        System.out.println(stack.isEmpty()); // false

        System.out.println(stack.peek()); // 1
        System.out.println(stack.pop()); // 1

        System.out.println(stack.isEmpty()); // true
```

스택을 활용하는 문제에서는 주로 짝을 찾는 용도로 스택을 활용합니다.

## 짝을 찾는 경우

짝이 맞는지 검사하는 것 이외에 짝이 되는 인덱스를 알아야 하는 상황이라고 합시다.

이때는 스택에 여는 괄호 자체를 넣는 대신 여는 괄호의 인덱스 정보를 넣어 주면 됩니다.

그렇게 하면 닫는 괄호를 검사할 때 스택에서 짝이 되는 여는 괄호의 인덱스를 알 수 있습니다.

```java
private void findPair(char[] str) {
    Stack<Integer> stack = new Stack<>();
    for (int i = 0; i < str.length; i++) {
        switch (str[i]) {
                case '(' -> stack.push(i);
                case ')' -> {
                    if (stack.isEmpty()) return;
                    
                    // 짝이 되는 괄호의 인덱스 출력
                    System.out.println(stack.pop() + ", " + i);
                }
        }
    }
}
```
