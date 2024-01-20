# practice-question;
***********************************************************************************************************************************************
 Power of Two
Solved
Easy
Topics
Companies
Given an integer n, return true if it is a power of two. Otherwise, return false.

An integer n is a power of two, if there exists an integer x such that n == 2x.
***********************************************************************************************************************************************

**MY CODE**
class Solution {
public:
    bool isPowerOfTwo(int n) {
      int temp=0;
      if(n<=0)
      return false;
      while(n>1)
      {
          if(n%2==1)
          {
              temp=1;
              break;
          }
          else n=n/2;
      }  
      if(temp==0)
      return true;
      else return false;
    }
};
**OPTIMIZED CODE**
***********************************************************************************************************************************************
class Solution {
public:
    bool isPowerOfTwo(int n) {
        return (n <= 0) ? false: (n & (n-1)) == 0;
    }
};
***********************************************************************************************************************************************
# The complement of an integer is the integer you get when you flip all the 0's to 1's and all the 1's to 0's in its binary representation.

For example, The integer 5 is "101" in binary and its complement is "010" which is the integer 2.
Given an integer n, return its complement
*******************************************************************************************************************************************
**SOLUTION**......
class Solution {
public:
    int bitwiseComplement(int n) {
        int m=n,mask=0;
        if(n==0)
        return 1;
        while(m!=0)
        {
            mask=(mask<<1) | 1;
            m=m>>1;
        }
        int ans=(~n) & mask;
        return ans;
    }
};
*******************************************************************************************************************************************

