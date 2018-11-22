```c++
string to_String(int n)
{
	char s[10];
	char ss[10];
	int m=n;
	int i=0,j=0;
	if(n<0)
	{
		m=0-m;
		j++;
		ss[0]='-';
	}
	while(m>0)
	{
		s[i++]=m%10+'0';
		m/=10;
	}
	s[i]='\0';
	i--;
	while(i>=0)
	{
		ss[j++]=s[i--];
	}
	ss[j]='\0';
	return ss;
}
```
