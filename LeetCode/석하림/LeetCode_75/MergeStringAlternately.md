## Merge String Alternately
\```java
class Solution {
    public String mergeAlternately(String word1, String word2) {
        char[] word1CharArray = word1.toCharArray();
        char[] word2CharArray = word2.toCharArray();
        char[] result = new char[word1.length() + word2.length()];
        int idx = 0;
        for(int i = 0; i < word1.length() || i < word2.length(); i++) {
             if (i < word1.length()) {
                result[idx++] = word1CharArray[i];
            }
            if (i < word2.length()) {
                result[idx++] = word2CharArray[i];
            }
        }
        return new String(result);
    }
}
```
