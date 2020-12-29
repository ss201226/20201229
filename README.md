# 20201229
package collection;


import java.util.ArrayList;
import java.util.Collections;

public class ArrTest {

	public static void main(String[] args) {
		ArrayList<String> arData=new ArrayList<>();
		
		//ArrayList 값 추가
		arData.add("하나");
		arData.add("둘");
		arData.add("셋");
		arData.add("넷");
		arData.add("다섯");
		//ArrayList 단순확인
		System.out.println(arData);
		
		//					ArrayList 크기
		for (int i = 0; i < arData.size(); i++) {
			//ArrayList 값 가져오기
			System.out.println(arData.get(i));
		}
		arData.remove(1);
		System.out.println(arData);
		
		ArrayList<Integer> arData2=new ArrayList<>();
		arData2.add(40);
		arData2.add(10);//오토박싱이 일어나서 10이 들어갈 수 있다
		arData2.add(50);
		arData2.add(20);
		arData2.add(30);
		
		arData2.remove(new Integer(30));
		//매개변수를 int형태로 받아오는 remove()가 호출되어 30이라는 값을 index로 처리하게 되어 오류 발생
		//'30' 이라는 값이 지우고 싶다면 내가 직접 박싱을 해서 넘겨준다.
		//현재 arData2.add(30); 이게 박싱되서 들어가 있기 때문에(integer타입(객체)으로 들어가 있는 상태) 제거할 때에도 언박싱을 해주어야 하는것!
		
		//정렬
		Collections.sort(arData2);
		System.out.println(arData2);
		//섞기
		Collections.shuffle(arData2);
		System.out.println(arData2);
		//뒤집기
		Collections.reverse(arData2);
		System.out.println(arData2);
	}

}
