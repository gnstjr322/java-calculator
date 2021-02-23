## 계산기를 만들어 봅시다

### 목적

- 단위 테스트를 익혀봅시다.

### 단위 테스트는 무엇인가요?

- 단위 테스트는 실제 비즈니스 로직이 담겨져 있는 코드를 구현한 후 JUnit과 같은 도구를 활용해 **작은 단위를 테스트하는 것**입니다.
- Input과 Output이 명확한 클래스 메소드에 대한 단위 테스트를 연습해봅시다.

### 요구사항

- 사용자가 입력한 문자열 값에 따라 사칙연산을 수행할 수 있는 계산기를 구현해야 합니다.
- 문자열 계산기는 사칙연산의 계산 우선순위가 아닌 입력 값에 따라 계산 순서가 결정됩니다. 
즉, 수학에서는 곱셈, 나눗셈이 덧셈, 뺄셈 보다 먼저 계산해야 하지만 이를 무시합니다.
- 예를 들어 `2 + 3 * 4 / 2`와 같은 문자열을 입력할 경우
 `2 + 3 * 4 / 2` 실행 결과인 10을 출력해야 합니다. 
우리가 알고있는 사칙연산의 계산 우선순위로 인한 `3 * 4 / 2 + 2` 의 결과인 8은 오답입니다.

### 힌트

- 문자열을 입력받고 빈 공백 문자열을 기준으로 문자들을 분리해야 하겠죠?

    ```java
    String value = scanner.nextLine();
    String[] values = value.split(" ");
    ```

- 문자열을 정수로 변경하는 방법으로는 `Integer` 클래스의 `parseInt()` 메소드가 있습니다.

    ```java
    int number = Integer.parseInt("문자열");
    ```
