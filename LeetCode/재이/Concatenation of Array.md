**문제설명**<br>
Given an integer array nums of length n, you want to create an array ans of length 2n where `ans[i] == nums[i]` and `ans[i + n] == nums[i]` for `0 <= i < n` (0-indexed).

Specifically, ans is the concatenation of two nums arrays.

Return the array ans.


**예제**<br>
Input: nums = [1,2,1]<br>
Output: [1,2,1,1,2,1]<br>
Explanation: The array ans is formed as follows:<br>
- ans = [nums[0],nums[1],nums[2],nums[0],nums[1],nums[2]]<br>
- ans = [1,2,1,1,2,1]<br>
<br>

**코드**
```
class Solution {
    public int[] getConcatenation(int[] nums) {
        int n = nums.length;
        int[] ans = new int[n * 2];
        for (int i = 0; i < n ; i++) {
            ans[i] = ans[i + n] = nums[i];
        }
        return ans;
    }
}
```
