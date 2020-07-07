# 07. 오류 처리

- 오류 코드보다 예외를 사용하라.
코드를 사용하면 if else if ... 로 코드가 복잡해진다.
오류가 발생하면 예외를 던지는게 낫다.
비지니스 로직과 오류 처리 코드가 뒤섞이지 않는다.

- Try-Catch-Finally
예외가 발생할 코드를 짤 때는 try-catch-finally 문으로 시작하는 편이 낫다.
먼저 강제로 예외를 일으키는 테스트 케이스를 작성한 후 테스트를 통과하게 코드를 작성
try블록의 트랜잭션 범위부터 구현하게 됨

- 미확인 예외를 사용하라

- null을 리턴하지마라
if 직원이 없으면 {
  return Collections.emptyList();
}

- assert p1 != nill : "p1 should not be nill";

