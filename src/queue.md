스택과 큐는 완전 탐색에서 언급된 적이 있는 자료 구조입니다.

이 두 가지는 원소를 특정한 순서대로 삽입하고 제거할 수 있는 자료 구조로, 다음 연산을 제공합니다.

1. 원소 삽입
2. 원소 제거
3. 자료 구조가 비어 있는지 검사

두 자료 구조가 이 세 가지 연산을 어떻게 처리하는지 살펴봅시다.


큐(queue)는 스택과 비슷하게 생긴 자료 구조입니다.

스택이 긴 바구니였다면 큐는 긴 빨대입니다.

빨대는 양쪽이 뚫려 있기 때문에 한쪽으로는 원소가 삽입되고 다른 쪽으로는 빠져나가게 됩니다.

큐에서 원소가 제거되는 순서는 원소를 삽입한 순서와 동일합니다.

이와 같이 먼저 삽입한 원소가 먼저 나오는 구조를 FIFO(First In First Out : 선입선출)라고 합니다.

자바에서 큐는 스택과는 다르게 인터페이스로 작성되어 있습니다.

따라서 자바에서 큐를 이용하려면 인터페이스 Queue를 구현하는 클래스를 사용해야 합니다.

이를 위해 가장 많이 활용되는 클래스는 LinkedList입니다.

다음과 같이 LinkedList 클래스를 사용하여 Queue를 선언할 수 있습니다.

```java
Queue<Integer> queue = new LinkedList<>();
```

Queue 인터페이스가 제공하는 add()와 poll() 메서드를 사용하면 다음과 같이 원소를 삽입하고 제거할 수 있습니다.

```java
Queue<Integer> queue = new LinkedList<>();

queue.add(1);
queue.add(2);
queue.add(3);
System.out.println(queue.poll()); // 1
System.out.println(queue.poll()); // 2

queue.add(4);
System.out.println(queue.poll()); // 3
System.out.println(queue.poll()); // 4
```

또 Stack과 마찬가지로 isEmpty() 메서드를 사용하여 자료 구조가 비어 있는지 확인할 수 있습니다.

```java
Queue<Integer> queue = new LinkedList<>();

queue.add(1);
queue.add(2);
queue.add(3);
System.out.println(queue.poll()); // 1
System.out.println(queue.poll()); // 2

queue.add(4);
System.out.println(queue.poll()); // 3
System.out.println(queue.isEmpty()); // false

System.out.println(queue.poll()); // 4
System.out.println(queue.isEmpty()); // true
```