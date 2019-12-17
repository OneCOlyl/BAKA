##include<iostream>
#include<clocale>
using namespace std;
int main()
{
	setlocale(LC_ALL, "rus");
	cout<<"Введите натуральное число";
	int a, b(0), c(1), n, d(10), e(10), f, sum;
	cin >> n;
	while (n)
	{
		a = n % 5;
		b += a * c;
		c *= 10;
		n /= 5;
	}
	while(b>=d)
	{
		e = d;
		d *= 10;
	}
	f = b;
	b /= e;
	f %= 10;
	sum = b + f;
	cout << sum;
	return 0;
}
