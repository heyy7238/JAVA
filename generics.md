# 제네릭 사용이유

```java
자바와같은 언어에서 제공하는 컴파일 하는 과정 (코딩을 하는 과정에서)을 통해
사용자의 실수나 유발시킬수 있는 에러는 컴파일 단계에서 검출될 수 있도록 코딩을 작성

// -타입의 안정성
// -코드의 편의성
// -참조형 Data형만 가능(기본 Data형 쓸려면 Wrapper class를 써야함)
// Wrapper class = int -> int3eger , double -> Double
// -관습적으로 T 와 같이 T다음 대문자를 많이 씀
class Person<T,S>{
	public T info;
	public S id;
	Person(T info){ this.info = info;  }
}



