#include<stdio.h>
	//移位算乘法练习,递归；a<<1等价于a*2 ,b>>1等价于b/2
	//任何整数都可以表示为二进制，例如偶数6=110(二进制）=1*4+1*2+0*1 ，奇数7=111（二进制)=1*4+1*2+1*1 
	//故偶数a*6=a*(1*4+1*2+0*1)=a<<2 + a<<1 + 0  ，奇数a*7=a*(1*4+1*2+1*1)=a<<2 + a<<1 + a
	//递归：自我调用自我 , 终止条件 ，乘数被清空
	int multiply(int a,int b)
{
    if (b==0)
        return 0;//终止条件：乘数为0，返回0 
    if((b&1)==0)//b为偶数，b移被舍弃的数值为 0 
          return multiply(a<<1 ,b>>1);
          else //b为奇数,b右移被舍弃的数值为1
          return  a+multiply(a<<1,b>>1);//右移a+ multiply(左移a,b)
}
int main(int argc, char* argv[])
{
	int a,b;
	printf("请输入两个整数：");
	scanf("%d%d",&a,&b);
	printf("%d*%d=%d",a,b,multiply(a,b));
	return 0;	
}
