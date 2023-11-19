```
class Solution {
    public int solution(int n, int k) {
        int answer = 0;
        String sum="";
        while(n>0){
            sum=Integer.toString(n%k)+sum;
            
            n/=k;
        }
        
        String[] arr=sum.split("0");
        
        for(String data: arr ){
            if(data.equals(""))continue;
            Long Longdata=Long.parseLong(data);
            if(isPrime(Longdata)){
                answer++;
            }
        }
        
        return answer;
    }
    public boolean isPrime(Long data){
        if(data<2){
            return false;
        }

        for(int i=2;i<=Math.sqrt(data);i++){
            if(data%i==0){
                return false;
            }
        }
        return true;
    }
}
```
