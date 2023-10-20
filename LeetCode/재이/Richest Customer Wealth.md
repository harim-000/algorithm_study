## Problem
You are given an m x n integer grid accounts where accounts[i][j] is the amount of money the i​​​​​​​​​​​th​​​​ customer has in the j​​​​​​​​​​​th​​​​ bank. Return the wealth that the richest customer has.

A customer's wealth is the amount of money they have in all their bank accounts. The richest customer is the customer that has the maximum wealth.

## Example

Input: accounts = [[1,2,3],[3,2,1]] <br>
Output: 6<br>
Explanation:<br>
1st customer has wealth = 1 + 2 + 3 = 6<br>
2nd customer has wealth = 3 + 2 + 1 = 6<br>
Both customers are considered the richest with a wealth of 6 each, so return 6.<br>


## code
```
import java.util.*;

class Solution {
    public int maximumWealth(int[][] accounts) {
        int max = 0;
        for (int[] account : accounts) {
            int wealth = 0;
            for (int money : account) {
                wealth += money;
            }
            max = Math.max(wealth, max);
        }
        return max;
    }
}
```
