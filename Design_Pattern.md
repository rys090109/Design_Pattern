# 방과후 A 디자인 패턴 정리

## 1. 디자인 패턴 vs 아키텍처

- **디자인 패턴 (Design Pattern)**  
  - 설계: 그룹과 관계 중심  
  - 코드 레벨에서의 구조 설계

- **아키텍처 (Architecture)**  
  - 전체 시스템 구조 설계  
  - 큰 단위의 구조와 흐름을 설계

---

## 2. 함수 vs 메소드 차이

- **함수 (Function)**  
  - 독립적으로 존재  
  - 객체에 속하지 않음

- **메소드 (Method)**  
  - 클래스 내부에 존재  
  - 객체와 연관됨

---

## 3. 생성자의 불편함

- 객체 강제 생성 문제  
- 초기화 과정이 불편함  
- 유연성이 떨어짐

---

## 4. 디자인 패턴 23개

### 생성 패턴 (Creational Patterns)
1. Singleton (싱글톤) — 1개 재사용  
2. Flyweight (플라이웨이트) — 여러 개 재사용  
3. Prototype (프로토타입) — 객체 복제  
4. Builder (빌더)

### 구조 패턴 (Structural Patterns)
5. Template Method (템플릿 메서드)  
6. Strategy (전략)  
7. Bridge (브릿지)  
8. Composite (컴포지트)  
9. Decorator (데코레이터)  
10. Proxy (프록시)  
11. Adapter (어댑터)  
12. Facade (퍼사드)

### 행동 패턴 (Behavioral Patterns)
13. Observer (옵저버)  
14. Command (커맨드)  
15. Iterator (이터레이터)  
16. Visitor (비지터)  
17. State (상태)  
18. Memento (메멘토)  
19. Interpreter (인터프리터)  
20. Chain of Responsibility (책임 연쇄)

### 기타
21. Future

---

## 5. 핵심 개념

- **1, 2, 3 패턴**
  - 미리 생성하여 재사용하는 방식

- **4, 5, 6, 7 패턴**
  - 생성 방식이 불편하거나 복잡한 경우에 사용

---

## 6. SOLID 원칙

1. **SRP (Single Responsibility Principle)**  
   - 단일 책임 원칙

2. **OCP (Open/Closed Principle)**  
   - 개방-폐쇄 원칙  
   - 확장에는 열려 있고 수정에는 닫혀 있어야 함

---

## (1). Singleton (싱글톤 패턴)

- **특징**
  - 객체를 1개만 생성
  - 재사용 가능
  - 전역적으로 접근 가능

- **사용 목적**
  - 공통 리소스 관리
  - 설정 객체
  - 로깅 시스템 등

### Java 예제 코드

```java
class Singleton {
    static Singleton s = new Singleton();

    private Singleton() {}

    static Singleton getInstance() {
        if (s == null)
            return new Singleton();
        return s;
    }
}