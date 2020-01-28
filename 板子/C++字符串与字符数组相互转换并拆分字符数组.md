## 字符数组转换为字符串

```cpp
#include<bits/stdc++.h>
using namespace std;
int main(){
	char a[] = "123456789";
	string s(&a[0],&a[strlen(a)]);//起始位置的地址，结束位置的地址 
	cout<<s<<endl;
	return 0;
}
```



## 字符串转换为字符数组

```cpp
#include<bits/stdc++.h>
using namespace std;
int main(){
	string s = "123456789";
	char a[20];
	//s.c_str()返回指向字符串首地址的字符指针 
	strcpy(a,s.c_str());//将地址复制到字符数组 
	//strncpy(a,s.c_str(),s.length()+1) //第三个参数指定长度，最后+1为'\0'留出位置 
	return 0;
}
```




## 拆分字符数组

```cpp
#include<bits/stdc++.h>
using namespace std;
int main(){
	char a[] = "Hello World ACM Test";
	char* p;
	char* b = " ,*";
	//strtok(a,b);//可以指定多个参数进行拆分 
	p = strtok(a," ");//按照第二个参数进行拆分,标记第一次拆分结束的位置 
	while(p){
		cout<<p<<endl;
		p = strtok(NULL," ");//第一个参数为NULL代表从第一次拆分位置继续拆分 
	}
	return 0;
} 
```



