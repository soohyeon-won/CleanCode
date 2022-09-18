## 14. 점진적인 개선
단순하게 돌아가는 코드에 만족하는 프로그래머는 전문가 정신이 부족하다.
시간에 대한 변명 X -> 코드를 썩어가게 방치하지말라

1. 초안을 만든다
2. TDD 기법을 이용해 테스트 코드를 작성한다.
3. 개선한다

## [ marshaler ]
한 객체의 메모리에서 표현방식을 저장 또는 전송에 적합한 다른 데이터 형식으로 변환하는 과정이다
직렬화된 객체를 바이트 단위로 분해한다

## [ serialization ]
직렬화
ex. xml, JSON -> 객체로 파싱
마샬링과 비슷한 개념, 직렬화는 마샬링이라고 할 수 있음.

## Iterator
protocol Collection: Sequence // protocol Sequence
- Array, Set, Dictionary

Collection프로토콜은 Sequence를 conform
for -> Iterator + while

struct Zedd: Sequence, IteratorProtocol {
    
    typealias Element = Int
    var current = 1
    
    mutating func next() -> Int? {
        if current > 10 { return nil }
        defer { current += 1 }
        return current
    }
}
💡 Iterator에서 nil을 리턴하는것은 완료를 의미합니다.

출처: https://zeddios.tistory.com/1340 [ZeddiOS:티스토리]
