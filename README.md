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
