# Exception
```java

// try{
//     예외의 발생이 에쌍되는 로직
// } catch(예외클래스 인스턴스){ //JVM이 호출함
//     예외가 발생했을 때 실행되는 로직
// }finally{
//     예외여부와 관계없이 실행되는 로직
// }

class A{
    private int[] arr = new int[3];
    A(){
        arr[0]=0;
        arr[1]=10;
        arr[2]=20;
    }
    public void z(int first, int second){
        try {
            System.out.println(arr[first] / arr[second]);
        } catch(Exception e){ //주의 - Exception이 먼저올 경우 이후의 예외처리를 모두 포함한 결과 이므로  후처리를 확인 할 수 없음
            System.out.println("Exception");
        } catch(ArrayIndexOutOfBoundsException e){
            System.out.println("ArrayIndexOutOfBoundsException");
        } catch(ArithmeticException e){
            System.out.println("ArithmeticException");
        }finally{
            System.out.println("finally");
        }
         
    }
}
 
public class ExceptionDemo1 {
    public static void main(String[] args) {
        A a = new A();
        a.z(10, 0);
        a.z(1, 0);
        a.z(2, 1);
    }
}


