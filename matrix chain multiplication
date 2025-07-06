#include<bits/stdc++.h>
using namespace std;
#define ll long long int
vector<vector<ll>>dp;
vector<vector<int>>kSplit;

ll matrix_multiplication ( int  i, int j, vector<int>&v)
{
    if(i==j)
    {
        return 0;

    }
     if (dp[i][j] != -1) return dp[i][j]; 

     ll MinCost=LLONG_MAX;
     for(int k=i;k<j;k++)
     {
       ll  cost=matrix_multiplication(i,k,v)+matrix_multiplication(k+1,j,v)+v[i-1]*v[k]*v[j];

       if(MinCost>cost)
       {    MinCost = cost;
        kSplit[i][j]=k;

       }
     
     }
      return dp[i][j] = MinCost;
}





ll solve(vector<int>&v)
{int n=v.size();
dp.assign(n,vector<ll>(n,-1));
kSplit.assign(n,vector<int>(n,-1));
 return matrix_multiplication(1,n-1,v);

}


 
int main()
{
    int MatrixNumber;
    cout<<"How much Matrices take you want !"<<endl;cin>>MatrixNumber;
vector<int>v;
cout<<"give rows and columns number"<<endl;
        
    for(int i=0;i<MatrixNumber;i++)
    {
        int a,b;cin>>a>>b;
        if(i==0)
        {
  v.push_back(a);
  v.push_back(b);
        }else v.push_back(b);
      

    }
   ll cost= solve(v);
   cout<<cost<<endl;

   /*for(int i=0;i<v.size();i++)
   {
    for(int j=0;j<v.size();j++)
    
    {
        cout<<dp[i][j]<<' ';
    }cout<<endl;
   }cout<<endl;
    for(int i=0;i<v.size();i++)
   {
    for(int j=0;j<v.size();j++)
    
    {
        cout<<kSplit[i][j]<<' ';
    }cout<<endl;
   }
*/
dp.clear();
kSplit.clear();


}