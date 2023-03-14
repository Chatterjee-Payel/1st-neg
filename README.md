# 1st-neg
vector<long long> printFirstNegativeInteger(long long int A[],
                                             long long int N, long long int K) {
 vector<long long>ans;
   deque<long long>dq;
  int i=0;
  int j=0;
  while(j<N)
  {
      if(A[j]<0)
      {
          dq.push_back(A[j]);    
      }
      if((j-i+1)<K)
      {
         j++;
      }
      else if((j-i+1)==K){
          if(dq.size()==0)
          {
              ans.push_back(0);
          }
          else{
              ans.push_back(dq.front());
             if(A[i]<0)
             {
                 dq.pop_front();   
             }
             
          }
          i++;
          j++;
      }
      
  }
  return ans;
  };
  
