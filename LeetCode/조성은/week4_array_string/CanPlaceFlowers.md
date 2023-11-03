## Can Place Flowers 605


```java

class Solution {
    public boolean canPlaceFlowers(int[] flowerbed, int n) {
        int count = 0;

        if (flowerbed.length == 1) {
            if (flowerbed[0] == 0 && n ==1) {
                return true;
            }
        }

        for (int i = 1; i < flowerbed.length; i++) {
            if (i ==1){
                if (flowerbed[i-1] == 0 && flowerbed[i] == 0) {
                    count++;
                }
            } else if (i == flowerbed.length-1) {
                if (flowerbed[i - 1] == 0 && flowerbed[i] == 0) {
                    count ++;
                }
            } else if (flowerbed[i - 1] == 0 && flowerbed[i] == 0 && flowerbed[i + 1] == 0) {
                count++;
                flowerbed[i] = 1;
            }
        }

        return count >= n;
    }
}

```