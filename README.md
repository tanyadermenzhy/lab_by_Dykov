#include <iostream>
#include <stdio.h>
#include <cmath>
using namespace std;
int main() {
int x;
const float eps=pow(10,-6);
double sum=0;
cin>>x;
float t=-x/2;//при k=1;
int k=1;
printf("%3c%9c%15c\n",'k','t','s');
printf("%3d%c%15e%12.5f\n",k,' ',t,sum);
do{
	t*=-(pow(x,2))/(2*k*(2*k-1));
	sum+=t;//sum=sum+t
	k++;
	printf("%3d%c%15e%12.5f\n",k,' ',t,sum);
}while(fabs(t)>eps);
cout<<"Конечная сумма="<<sum<<endl;
	return 0;
}
