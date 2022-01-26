# 367.valid_perfect_square
java
class Solution {
    public boolean isPerfectSquare(int num) {
      if(num<=1) return true;  
     long start=0,end=num;
        while(start+1<end){
            long mid=start+(end-start)/2;
            if(mid*mid==num) return true;
            else if(mid*mid<num) start=mid;
            else end=mid;
            if(end*end==num) return true;
        }
        if(start*start==num) return true;
        else return false;
    }
}
