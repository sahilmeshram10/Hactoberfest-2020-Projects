# Add in your CPP codes here
#REPLACE X
#include <iostream>
#include<bits/stdc++.h>
using namespace std;

int main() {
int t;
cin>>t;
while(t--){
    int a,b,c,d;
    cin>>a>>b>>c>>d;
    int e[a];
    for(int i=0;i<a;i++)cin>>e[i];
    sort(e,e+a);
    if(c<=d&&e[c-1]>=b){int sum=0;
        for(int i=c-1;i>=0;i--){
            if(e[i]>b)sum++;
            else break;
        }cout<<sum<<"\n";
    }
    else if(c>=d&&e[c-1]<=b){int sum=0;
        for(int i=c-1;i<a;i++){
            if(e[i]<b)sum++;
            else break;
        }cout<<sum<<"\n";
    }
    else
    cout<<"-1\n";
    
}
	return 0;
}
