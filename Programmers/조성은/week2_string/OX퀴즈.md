## OX퀴즈 120907

```java
public static String[] solution(String[] quiz) {
        String[] answer = new String[quiz.length];

        for (int i = 0; i < quiz.length; i++) {
            String[] actual = quiz[i].split("\\ = ");
            String[] exp = actual[0].split(" \\- | \\+ ");
            int result = quiz[i].contains("+") ?
                    Integer.parseInt(exp[0]) + Integer.parseInt(exp[1]) :
                    Integer.parseInt(exp[0]) - Integer.parseInt(exp[1]);

            answer[i] = result == Integer.parseInt(actual[1]) ? "O" : "X";
        }

        return answer;
    }
```