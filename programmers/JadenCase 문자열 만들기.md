```
import java.util.*;
class Solution {
    public String solution(String s) {
        String answer = "";
        
        String[] ss=s.split(" ");
        
        for(int i=0;i<ss.length;i++){
            if(ss[i].length()==0){
                answer+=" ";
            }else{
                String start=ss[i].substring(0,1);
                String end=ss[i].substring(1);
                answer+=start.toUpperCase()+end.toLowerCase()+" ";
            }
        }
    	
        if(s.substring(s.length()-1, s.length()).equals(" ")){
    		return answer;
    	}
        
        return answer.substring(0, answer.length()-1);
    }
}
```
