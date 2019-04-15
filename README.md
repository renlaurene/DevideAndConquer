# DevideAndConquer
BigOAnalysis


max_min(A, i, j, max, min)
{ 
   // The initial conditions in if are called 
   // termination conditions and do not 
   // determine complexity. 
   if (i==j)  // 0 comparisons  
   {
      max=min=A[i];  
      return (max,min);  
   } 
   if (i=j-1)  
   { 
      if (A[i]>A[j])   // 1 comparisons  
      { max=A[i];  min=A[j]; }  
      else   
      { max=A[j];   min=A[i]; }
   }
   else // Time complexity is determined 
        // for else part of the code.
   {  
      mid=(i+j)/2; // O(1)   
      (max1,min1)=max_min(A, i, mid, max, min);  // T(n/2)  
      // if T(n) is complexity for n elements
      (max2,min2)=max_min(A, mid+1, j, max. min); // T(n/2)     
      if (max1>max2) // 1 comparisons
         max=max1;
      else  
         max=max2; 
      if (min1>min2) // 2 comparisons  
         min=min2;   
      else  
         min=min1; 
   }  
   return(max,min);
}  
