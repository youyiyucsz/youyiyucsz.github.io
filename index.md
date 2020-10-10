### 王超逸卒了
```cpp
  #include<iostream>
  #define w int main{
  #define c cout<<
  #define y "wcyzl";
  #define z return 0;
  #define l }
  using namespace std;
  wcyzl
```
### kmp
```cpp
#include<bits/stdc++.h>
using namespace std;
string s,s1;
int next[1000];
int kmp(string a,string b)
{
	int i=0,j=0;
	while(i<a.size()&&j<b.size())
	{
		if(a[i]==b[j]||j==-1)
		{
			i++;
			j++;
		}
		else
		{
			j=next[j];
		}
	}
	if(j==b.size())
	{
		return i-j;
	}
	else
	{
		return -1;
	}
	return -1;
}
void getnext(string a)
{
	next[0]=-1;
	int i=1,j=-1;
	while(i<a.size())
	{
		if(j==-1||a[i]==a[j])
		{
			i++;
			j++;
			next[i]=j;
		}
		else
		{
			j=next[j];
		}
	}
}
int main()
{
	cin>>s>>s1;
	int ans;
	getnext(s1);
	ans=kmp(s,s1);
	cout<<ans;
}
```
# 座位号
~ JS-00105	陈思哲	江苏省锡山高级中学	41
