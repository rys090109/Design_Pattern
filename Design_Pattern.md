방과후 A 디자인 패턴

디자인 패턴 - 23개								설계(디자인) <====> 아키텍쳐(구조) 

생성자의 불편함 -객체 강제 생성 
			-초기화 불편함

1.Singleton (싱글톤) —1개 재사용
2.Flyweight (플라이웨이트) —여러개 재사용(n개)
3.Prototype (프로토타입) —복재 
4.Builder (빌더)
5.Template Method (템플릿 메서드)
6.Strategy (전략)
7.Bridge (브릿지)
8.State (상태)
9.Composite (컴포지트)
10.Command (커맨드)
11.Decorator (데코레이터)——나
12.Proxy (프록시)
13.Adapter (어댑터)
14.Observer (옵저버)
15.Iterator (이터레이터)
16.Visitor (비지터)
17.Memento (메멘토)
18.Interpreter (인터프리터)
19.Facade (퍼사드)
20.Chain of Responsibility (책임 연쇄)
21.Future

1.2.3 미리생성
언제 재사용 하고 언제 생성할 것 인가 : 
4,5,6,7
불리


Singleton (싱글톤) —미리 만들고 재사용(1개) 

class Singleton {
    static Singleton s = new Singleton(); 
    private Singleton() {}

    static Singleton getInstance() {
        if(s==null)
            return new Singleton();
        return s;
    }
}
