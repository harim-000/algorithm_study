## Number of Employees Who Met the Target 2798


```java

class Solution {
    public int numberOfEmployeesWhoMetTarget(int[] hours, int target) {
        int answer = 0;
        for (int hour : hours) {
            if (hour >= target) {
                answer++;
            }
        }
        return answer;
    }
}

```