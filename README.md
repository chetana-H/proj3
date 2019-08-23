#include<bits/stdc++.h>
using namespace std;

main()
{
ios_base::sync_with_stdio(false);
cin.tie(NULL);

int n;
cin>>n;
int a[n];
int sum=0;

for(int i=0; i<n; i++)
{
	cin>>a[i];
}
sort(a,a+n);
for(int i=1; i<n; i++)
{
  for(int j=i-1; j>=0; j--)
  {
  	if(a[i]>a[j]&&a[j]!=0)
	{

		a[j]=0;
		break;
}
}
}
sum=0;
for(int i=0; i<n; i++)
{
	sum+=a[i];
}
cout<<sum;

}
