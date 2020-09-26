# rock-and-liver
#include <bits/stdc++.h>
using namespace std;
#define ll long long

int main()
{

    int t;
    cin>>t;
    while(t--){
        int n;
        cin>>n;
        vector<ll> H(32,0);
        vector<int> A(n);
        for(int i=0;i<n;i++){
            cin>>A[i];
        }
        for(int i=0;i<n;i++){
            H[ceil(log2(A[i]+1))]++;
        }
        ll sum=0;
        for(int i=0;i<32;i++){
          sum+=((H[i]*(H[i]-1))/2);
        }
        cout<<sum<<endl;
    }

}
