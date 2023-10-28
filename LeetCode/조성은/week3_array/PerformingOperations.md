## Final Value of Variable After Performing Operations 2011


```java

class Solution {
    public int finalValueAfterOperations(String[] operations) {
        int count = 0;
        for (String operation : operations) {
            if (operation.contains("+")) {
                count++;
            } else {
                count--;
            }
        }
        return count;
    }
}


```