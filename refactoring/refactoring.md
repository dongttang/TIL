### 리팩토링 설계방법들

- 메서드 추출
```
1. 기존 메서드에서 추출할 내용을 복사해서 빼옴
2. 빼온 내용들 중에 지역변수를 찾아서 새로 만드는 메서드의 매개변수로 선언하기
3. 빼온 내용들 중에 임시변수가 있다면 이는 새로 만드는 메서드의 필드로 선언하기
4. 추출 코드에 의해 변경되는 지역변수가 있는지 파악하기
5. 원본 메서드 안에 빼낸 코드를 새로 생성한 메서드 호출로 수정하기
```

- 메서드 내용 직접 삽입
```
1. 메서드 기능이 너무 단순해서 메서드명이 기능의 대부분을 드러낼땐, 메서드를 삭제하고 해당 내용을 호출하는 부분에 직접 작성해주기
2. 하위클래스에서 해당 메서드가 재정의 되어 있지 않은지 먼저 확인
3. 해당 메서드를 호출하는 부분을 모두 찾기
4. 호출 부분을 메서드 내용으로 교체
5. 테스트 실시
6. 메서드 정의 삭제
```

- 임시 변수 내용 직접 삽입
```java
double basePrice = anOrder.basePrice();
return (basePrice > 1000)
```
```java
return (anOrder.basePrice() > 1000)
```




































