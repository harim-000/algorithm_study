## Count Pairs Whose Sum is Less than Target 2824


```java

class Solution {
    public int countPairs(List<Integer> nums, int target) {
        int count = 0;
        for (int i = 0; i < nums.size()-1; i++) {
            for (int j = i +1; j < nums.size(); j++) {
                if (target > nums.get(i) + nums.get(j)) {
                    count++;
                }
            }
        }
        return count;
    }
}


```