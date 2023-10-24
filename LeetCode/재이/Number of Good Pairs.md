**문제 설명**<br>
Given an array of integers nums, return the number of good pairs.<br>

A pair (i, j) is called good if nums[i] == nums[j] and i < j.<br>

**예제**<br>
Input: nums = [1,2,3,1,1,3]<br>
Output: 4<br>
Explanation: There are 4 good pairs (0,3), (0,4), (3,4), (2,5) 0-indexed.<br>

**코드**
```
class Solution {
    public int numIdenticalPairs(int[] nums) {
    
        int ans = 0;
        for (int i = 0; i < nums.length; i++) {
            for (int j = i + 1; j < nums.length; j++) {
                if (nums[i] == nums[j]) ans++;
            }
        }
        return ans;
    }
}
```
