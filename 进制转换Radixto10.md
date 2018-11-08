**以下以16进制转10进制为例**

```c++
#include<iostream>
#include<string>
#include<algorithm>
using namespace std;

int main()
{
	string s;
	cin >> s;
	long long sum = 0;
	for (int i = 0; i < s.size(); i++)
	{
		if (s[i] >= 'A' && s[i] <= 'F')
			sum = sum * 16 + (s[i] - 'A' + 10);
		else
			sum = sum * 16 + (s[i] - '0');
	}
	cout << sum;
	system("pause");
	return 0;
}
```
