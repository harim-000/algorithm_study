**문제 설명**<br>
Given the array nums consisting of 2n elements in the form [x1,x2,...,xn,y1,y2,...,yn].<br>

Return the array in the form [x1,y1,x2,y2,...,xn,yn].<br>

**예제**<br>
Input: nums = [2,5,1,3,4,7], n = 3<br>
Output: [2,3,5,4,1,7] <br>
Explanation: Since x1=2, x2=5, x3=1, y1=3, y2=4, y3=7 then the answer is [2,3,5,4,1,7].<br>
<br>

**코드**
```
import java.util.*;

class Solution {
    public int[] shuffle(int[] nums, int n) {
        int[] answer = new int[nums.length];
        for (int i = 0; i < n; i++) {
            answer[i * 2] = nums[i];
            answer[i * 2 + 1] = nums[n + i];
        }
        return answer;
    }
}
```
