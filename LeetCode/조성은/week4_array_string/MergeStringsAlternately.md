## Merge Strings Alternately 1768

```java

class Solution {
    public String mergeAlternately(String word1, String word2) {
        int num = word1.length() > word2.length() ? word2.length() : word1.length();
        StringBuilder builder = new StringBuilder();
        for (int i = 0; i < num; i++) {
            builder.append(word1.charAt(i));
            builder.append(word2.charAt(i));
        }
        String s = word1.length() > word2.length() ? word1.substring(num) : word2.substring(num);
        return builder.append(s).toString();
    }
}


```