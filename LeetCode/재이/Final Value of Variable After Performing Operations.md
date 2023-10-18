**문제 설명** <br>
There is a programming language with only four operations and one variable X:

++X and X++ increments the value of the variable X by 1.<br>
--X and X-- decrements the value of the variable X by 1.<br>
Initially, the value of X is 0.<br>

Given an array of strings operations containing a list of operations, return the final value of X after performing all the operations.

**예제**<br>
Input: operations = ["--X","X++","X++"]<br>
Output: 1<br>
Explanation: The operations are performed as follows:<br>
Initially, X = 0.<br>
--X: X is decremented by 1, X =  0 - 1 = -1.<br>
X++: X is incremented by 1, X = -1 + 1 =  0.<br>
X++: X is incremented by 1, X =  0 + 1 =  1.<br>


**코드**
```
class Solution {
    public int finalValueAfterOperations(String[] operations) {
        int ans = 0;
        for (String operation : operations) {
            if(operation.charAt(1)=='+') ans++;
            else ans--;
        }
        return ans;
    }
}
```
