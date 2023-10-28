## Richest Customer Wealth 1672


```java

class Solution {
    public int maximumWealth(int[][] accounts) {
        int answer = 0;
        for (int i = 0; i < accounts.length; i++) {
            int temp = 0;
            for (int j = 0; j < accounts[i].length; j++) {
                temp += accounts[i][j];
            }
            if (temp > answer) {
                answer = temp;
            }
        }
        return answer;
    }
}

```