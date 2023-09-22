```
class Solution {
    public int solution(int[] arr) {
        int answer = 0;
        
        if(arr.length==1){
            return arr[0];
        }
        
        int gcd=GCD(arr[0],arr[1]);
        answer=(arr[0]*arr[1])/gcd;
        
        if(arr.length>2){
            for(int i=2;i<arr.length;i++){
                gcd=GCD(answer,arr[i]);
                answer=(answer*arr[i])/gcd;
            }
        }
        
        return answer;
    }
    public int GCD(int x,int y){
        int r=x%y;
        if(r==0) return y;
        else return GCD(y,r);
    }
}
```
