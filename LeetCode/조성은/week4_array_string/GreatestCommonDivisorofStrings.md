## Greatest Common Divisor of String 1071


```java

class Solution {
    public String gcdOfStrings(String str1, String str2) {
        if (!(str1 + str2).equals(str2 + str1)) {
            return "";
        }
        int shorter = str2.length();
        int longer = str1.length();
        if (str2.length() > str1.length()) {
            shorter = str1.length();
            longer = str2.length();
        }
        
        int answer = 0;
        while (shorter != 0) {
            answer = shorter;
            shorter = longer % shorter;
            longer = answer;
        }
        return str1.substring(0, answer);
    }
}


```