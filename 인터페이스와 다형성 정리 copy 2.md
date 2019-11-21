# 다형성 정리

```java

//인터페이스와 다형성 정리
//클래스 타입,인터페이스 형태에 따라 필요한 메소드만 제한해서 사용가능하다.
interface father(){}
interface mother(){}
interface believer(){}
interface programmer(){
	public void coding();
}

//다중 상속가능
class Steve implements father,believer,programmer{
	public void coding(){
		System.out.println("남성스럽게 코딩중");
	}
	
}

class Rachel mother,programmer{
	public void coding(){
		System.out.println("여성스럽게 코딩중");
	}
}
//각각의 인터페이스에 맞는 메소드 사용가능
public class PolymorphismMemo {
	public static void main(String[] args) {
		
		programmer employee1 = new Steve();
		programmer employee2 = new Rachel();
		
		employee1.coding();
		employee2.coding();
		
	}
}

```