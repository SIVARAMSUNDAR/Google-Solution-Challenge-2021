// # Google-Solution-Challenge-2021
// C++ Programming
#include<bits/stdc++.h>
using namespace std;
int main()
{
	int n,count=0;
	cin>>n;
	int a[n],b[n];
	for(int i=0;i<n;i++)
	{
		cin>>a[i]>>b[i];
		b[i]=a[i]+b[i];
	}
	sort(a,a+n);
	sort(b,b+n);
	int p=1,r=1,i=1,j=0;
	while(i<n && j<n)
	{
		if(a[i]<=b[j])
		{
			p++;
			i++;
		}
		else if(a[i]>b[j])
		{
			p--;
			j++;
      count=count+1;
		}
		if(p>r)
			r=p;
	}
	cout<<r;
  cout<<count;
}
