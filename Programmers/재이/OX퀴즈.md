**문제 설명**<br>
덧셈, 뺄셈 수식들이 'X [연산자] Y = Z' 형태로 들어있는 문자열 배열 quiz가 매개변수로 주어집니다. 수식이 옳다면 "O"를 틀리다면 "X"를 순서대로 담은 배열을 return하도록 solution 함수를 완성해주세요.
<br>

**입출력 예** <br>
quiz	result<br>
["3 - 4 = -3", "5 + 6 = 11"]	                                ["X", "O"]<br>
["19 - 6 = 13", "5 + 66 = 71", "5 - 15 = 63", "3 - 1 = 2"]	  ["O", "O", "X", "O"]

<br>

**다른 사람의 코드**
```
class Solution {
    public String[] solution(String[] quiz) {
        for(int i=0; i<quiz.length; i++){
            String[] text = quiz[i].split(" ");
            int result = Integer.parseInt(text[0]) + ( Integer.parseInt(text[2]) * ( text[1].equals("+") ? 1:-1) );
            quiz[i] = result == Integer.parseInt(text[4])? "O": "X";
        }
        return quiz;
    }
}
```
- 삼항연산자를 이용해 간단히 풀어낼 수 있다. 
<br>

**코드**
```
import java.util.*;
class Solution {
    
    public String[] solution(String[] quiz) {
        String[] answer = new String[quiz.length];
        for (int i = 0; i < quiz.length; i++) {
            String[] str = quiz[i].split(" ");

            // 계산 
            int ans = Integer.parseInt(str[0]);
            if (str[1].equals("+")) ans += Integer.parseInt(str[2]);
            else ans -= Integer.parseInt(str[2]);
            // ( x [연산자] Y ) == Z 
            if (Integer.parseInt(str[4]) == ans) answer[i] = "O";
            else answer[i] = "X";
        }

        return answer;
    }
}
```
