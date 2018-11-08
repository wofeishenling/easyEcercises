**以下以10进制转16进制为例**

```c++
#include<iostream>
#include<string>
#include<map>
#include<set>
#include<cmath>
#include<queue>
#include<sstream>
#include<vector>
#include<algorithm>
using namespace std;

int main()
{
	int input,cnt=0;
	int radix;
	cin >> input >> radix;
	int bit[40] = { 0 };
	do {
		bit[cnt++] = input % radix;//除基取余
		input /= radix;
	} while (input != 0);
	for (int i = cnt - 1; i >= 0; i--)//倒序输出
	{
		if (bit[i] < 10) printf("%d", bit[i]);
		else printf("%c", char(bit[i] - 10 + 'A'));
	}
	system("pause");
	return 0;
}
```
