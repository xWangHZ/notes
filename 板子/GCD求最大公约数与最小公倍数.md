## 思路

> 辗转相除法，又名欧几里德算法，是求**最大公约数**的一种方法，具体做法是用较大的数除较小的数，再用出现的余数，做除数。再用一开始较小的数做被除数，如此反复，直到除数变成零，被除数就是两个数的最大公约数。
>
> 
>
> |  a   |  b   | a mod b |
> | :--: | :--: | :-----: |
> |  36  |  24  |   12    |
> |  24  |  12  |    0    |
> |  12  |  0   |         |
>
> 此时**12即是36和24的最大公约数**
>
> **两数相乘 除以 最大公约数 即是 最小公倍数**





## 代码

```cpp
#include<bits/stdc++.h>
using namespace std;
//递归算法
int gcd(int a,int b){
	return b==0?a:gcd(b,a%b);
}
/*循环算法 
int gcd(int a,int b)
{
	while(b^=a^=b^=a%=b);
	return a;
}*/
int main(){
	int a,b;
	cin>>a>>b;
	cout<<gcd(a,b)<<endl;//最大公约数
    cout<<a*b/gcd(a,b)<<endl;//最小公倍数
	return 0;
}
```



