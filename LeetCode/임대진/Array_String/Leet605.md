605. Can Place Flowers

```java

package leetcode;

public class Leet605 {
	public static void main(String[] args) {
		boolean result = canPlaceFlowers(new int[] {0,0, 0, 0, 1}, new Integer(3));
		System.out.println("결과값:" + result);

	}
     public static boolean canPlaceFlowers(int[] flowerbed, int n) {   	 
		if (flowerbed == null || flowerbed.length == 0) {
		      return false;
	    }
		
	    int count = 0;
	    
	    for (int i = 0; i < flowerbed.length; i++) {
	      if (flowerbed[i] == 0 && (i == 0 || flowerbed[i - 1] == 0) && (i == flowerbed.length - 1 || flowerbed[i + 1] == 0)) {
	        flowerbed[i] = 1;
	        count++; 
	      }
	      
	      if (count >= n) { 
	        return true;
	      }
	    }
	    return false;
	  }

}



```
