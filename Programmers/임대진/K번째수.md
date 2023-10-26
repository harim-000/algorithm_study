```java

package programmers;

import java.util.Arrays;

public class P42748 {

	public static void main(String[] args) {
		int[] result = solution(new int[] {3,5,6,8,10,12}, new int[][] {{1,5,3},{2,4,3}});
		System.out.println("결과값:" + Arrays.toString(result));
		
	}
	
	public static int[] solution(int[] array, int[][] commands) {
		//이차원 배열의 갯수만큼 길이 구하기.
	    int[] answer = new int[commands.length];
	    
	    //시작 인덱스, 종료 인덱스, 구하려는 값의 인덱스 초기화
	    int startNum = 0;
	    int endNum = 0;
	    int k = 0;
	    
	    //이차원 배열 관련 로직
	    for(int i = 0; i < commands.length; i++) {
	    	int[] arrTemp = commands[i];
			startNum = arrTemp[0];
			endNum = arrTemp[1];
			k = arrTemp[2];
			
			//Arrays.copyOfRange 메소드 이용해서 배열 자르기
			int[] arrSlice = Arrays.copyOfRange(array, startNum-1, endNum);
			//정렬
	    	Arrays.sort(arrSlice);
	    	//결과값에 넣기
	    	answer[i] = arrSlice[k-1];
    	}
	    
	    return answer;    	
	}
}


```
