#   JAVA:Collection framework

```java

//ArrayList 사용법

        import java.util.ArrayList;

        ArrayList al = new ArrayList();
		al.add("one"); //Object타입으로 저장됨
		al.add(2);
		for(int i=0;i<al.size();i++){
			String value = (String)al.get(0); //Object 값 -> String으로 형변환
			System.out.println(value);
			System.out.println(al.get(i));
		}

//요소를 꺼내올때 형변환 주의! -옛날방식
//GENERIC을 이용하자.

        import java.util.ArrayList;

        ArrayList<String> al = new ArrayList<String>();
		al.add("one"); //Object타입으로 저장됨
		for(int i=0;i<al.size();i++){
			String value = al.get(0); 
			System.out.println(value);
			System.out.println(al.get(i));
		}

        
//Set,List,Map

//Set- 하나의 값만 저장(중복제거 - 고유한 값 저장) 주로 집합관련
//list - 값 중복가능


//Map-Key값은 중복 X, Value값은 중복 O

