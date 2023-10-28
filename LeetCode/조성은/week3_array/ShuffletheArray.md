## Shuffle the Array 1470


```java

class Solution {
    public int[] shuffle(int[] nums, int n) {
        int[] ans = new int[nums.length];
        int place = 0;
        for (int i = 0; i < n; i++) {
            ans[place] = nums[i];
            ans[place + 1] = nums[n + i];
            place += 2;
        }
        return ans;
    }
}


```