## OX퀴즈

```java
class Solution {
    public String[] solution(String[] quiz) {
        String[] answer = new String[quiz.length];
        int count = 0;

        for (String x : quiz) {
            String[] str = x.split(" ");
            int a = 0;
            int b = 0;
            String op = "";
            int sum = 0;
            int result = 0;

            for (int i = 0; i < str.length; i++) {
                if (i == 0) {
                    a = Integer.parseInt(str[i]);
                } else if (i == 1) {
                    if ("+".equals(str[i])) {
                        op = "+";
                    }else {
                        op = "-";
                    }
                } else if (i == 2) {
                    b = Integer.parseInt(str[i]);
                } else if (i == 4) {
                    sum = Integer.parseInt(str[i]);
                }
            }

            if (op.equals("+")) {
                result = a + b;
                if (result == sum) {
                    answer[count] = "O";
                    count++;
                }else {
                    answer[count] = "X";
                    count++;
                }
            }else {
                result = a - b;
                if (result == sum) {
                    answer[count] = "O";
                    count++;
                }else {
                    answer[count] = "X";
                    count++;
                }
            }
        }
        return answer;
    }
}
```