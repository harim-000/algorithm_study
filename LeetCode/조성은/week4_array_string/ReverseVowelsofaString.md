## Reverse Vowels of a String 345


```java

class Solution {
    public String reverseVowels(String s) {
        String vowels = "aeiouAEIOU";
        char[] chars = s.toCharArray();
        int start = 0;
        int end = s.length()-1;
        while (start < end) {
            while (start < end && !vowels.contains(s.charAt(start) + "")) {
                start++;
            }
            while (start < end && !vowels.contains(s.charAt(end) + "")) {
                end--;
            }
            chars[start] = s.charAt(end);
            chars[end] = s.charAt(start);
            start++;
            end--;
        }
        return new String(chars);
    }
}

```