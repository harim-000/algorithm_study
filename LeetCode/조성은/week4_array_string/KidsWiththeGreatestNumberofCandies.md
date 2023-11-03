## Kids With the Greatest Number of Candies 1431



```java

class Solution {
    public List<Boolean> kidsWithCandies(int[] candies, int extraCandies) {
        int greatest = 0;
        ArrayList<Boolean> answer = new ArrayList<>();
        for (int candy : candies) {
            if (candy > greatest) {
                greatest = candy;
            }
        }

        for (int candy : candies) {
            answer.add(candy + extraCandies >= greatest);
        }
        return answer;
    }
}

```