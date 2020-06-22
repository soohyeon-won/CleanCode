# 06. 객체와 자료 구조

- 자료 추상화
아무 생각 없이 get, set 함수를 쓰지않는다.
interface (protocol) 정의 > 추상화하여 사용

- 자료 / 객체 비대칭
절차지향적 : Class Square, Rectangle, Circle > Geometry 안의 func getArea
객체지향적 : interface Shape (func getArea) > Class Square, Rectangle, Circle implements Shape
절차적인 코드는 새 함수를 추가하기 쉽다.
객체 지향 코드는 새 클래스를 추가하기 쉽다.

- 디미터 법칙
객체 + 자료 구조 > 잡종구조 > 양쪽의 단점만 모아지게 됨

- 자료 전달 객체
공개 변수만 있고 함수가 없는 클래스 : Data Transfer Object <DTO>
이 객체에 비지니스 로직을 적용하지마라
