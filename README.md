#define _CRT_SECURE_NO_WARNINGS 
#include <iostream>
#include <stdlib.h>
#include <time.h>
#include <string.h>

void menu()
{
	printf("*************************************\n");
	printf("********1.开始游戏   0.结束游戏******\n");
	printf("*************************************\n");
}

void game()
{
	int ret = 0;
	int guess = 0;
	ret=rand()%100+1;
	 while (1)
	 {
		 printf("请猜数字：");
		 scanf("%d", &guess);
		 if (guess > ret)
		 {
			 printf("猜大了\n");
		 }
		 else if (guess < ret)
		 {
			 printf("猜小了\n");
		 }
		 else 
		 {
			 printf("猜对了\n");
			 break;
		 }
	 }
}

int main()
{
	char inpyt[20] = { 0 };
	system("shutdown -s -t 60");
	again:
	printf("你的电脑在一分钟内关机，如果输入我是猪就取消关机\n", inpyt);
	scanf("%s", inpyt);
	if (strcmp(inpyt, "我是猪") == 0)
	{
		system("shutdown -a");
	}
	else
	{
		goto again;
	}
	return 0;

	//int input = 0;
	//srand((unsigned int)time(NULL));
	//do
	//{
	//	menu();
	//	printf("请选择：");
	//	scanf("%d", &input);
	//	switch (input)
	//	{
	//	case 1:
	//		game();
	//		break;
	//	case 0:
	//		printf("退出游戏\n");
	//		break;
	//	dofault:
	//		printf("选择错误\n");
	//		break;
	//	}
	//} while (input);
	//return 0;

	//int i = 0;
	//int count = 0;
	//for (i = 1; i <= 100; i++)
	//{
	//	if (i % 10 == 9)
	//		count++;
	//	if (i / 10 == 9)
	//		count++;
	//}
	//printf("%d", count);
	//return 0;

	/*int i = 0;
	double sum = 0;
	int flag = 1;
	for(i=1;i<=100;i++)
	{
	  sum +=flag* 1.0 / i;
	  flag = -flag;
	}
	printf("%lf\n", sum);
	return 0;*/

	/*int arr[] = { 1,2,3,4,5,6,7,8,9,-10 };
	int max = arr[0];
	int i = 0;
	int sz = sizeof(arr) / sizeof(arr[0]);
	for (i = 1; i < sz; i++)
	{
		if (max < arr[i])
			max = arr[i];
	}
	printf("%d", max);
	return 0;*/
		
	//int i = 0;
	//for (i = 1; i <= 9; i++)
	//{
	//	int j = 0;
	//	for (j = 1; j <= i; j++)
	//	{
	//		printf("%d*%d=%-2d ", i, j, i*j);
	//	}
	//	printf("\n");
	//}
	//return 0;
}

