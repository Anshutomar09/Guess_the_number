# Guess_the_number

class Solution {
public:
    int solving(int s, int e){
        int mid= s+(e-s)/2;
        if(guess(mid)==0){
            return mid;
        }
        else if(guess(mid)==-1){
            e=mid-1;
        }
        else{
            s=mid+1;

        }
        return solving(s,e);
        
    }
    int guessNumber(int n) {
        return solving(1, n);
        
    }
};
