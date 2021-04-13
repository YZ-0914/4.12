# 4.12
#define _CRT_SECURE_NO_WARNINGS 1
#include<iostream>

using namespace std;

//int main()
//{
//	int num[] = { 198, 98, 'c', 230 };
//	cout << num[2] << endl;
//}

//int main()
//{
//	const int N = 5;
//	double scores[N];
//	for (int i = 0; i < N;i++)
//	{
//		cout << "请输入第" << (i + 1) << "门课的成绩：";
//		cin >> scores[i];
//	}
//	for (int i = 0; i < N;i++)
//	{
//		cout << "第"<<(i+1)<<"门课的成绩:"<<scores[i] << endl;
//	}
//	return 0;
//}

//int main()
//{
//	const int N = 5;
//	int nums[N];
//	cout << "数组的大小：" << sizeof(nums) / sizeof(nums[0]) << endl;
//	for (int i = 0; i < sizeof(nums) / sizeof(int); i++)
//	{
//		cout << "请输入第" << (i + 1) << "个数组元素:";
//		cin >> nums[i];
//	}
//	for (int i = 0; i < N; i++)
//	{
//		cout << nums[i] << endl;
//	}
//}
//
//int main()
//{
//	int nums[]{8, 4, 2, 1, 23, 344, 12};
//	int numsLen = sizeof(nums) / sizeof(nums[0]);
//	int sum = 0;
//	for (int i = 0; i < numsLen; i++)
//	{
//		cout << nums[i] << '\t';
//	}
//	cout << endl;
//	for (int i = 0; i < numsLen; i++)
//	{
//		sum += nums[i];
//	}
//	cout << "数列的和为：" << sum<<'\t' << "平均值为：" << sum / numsLen << endl;
//	int max = nums[0];
//	int maxIndex = 0;
//	for (int i = 1; i < numsLen; i++)
//	{
//		if (nums[i] > max)
//		{
//			max = nums[i];
//			maxIndex = i;
//		}
//	}
//	cout << "最大值是：" << max << '/' << nums[maxIndex] << endl;
//	cout << "最大值的下标是：" << maxIndex << endl;
//	int min = nums[0];
//	int minIndex = 0;
//	for (int i = 0; i < numsLen; i++)
//	{
//		if (nums[i] < min)
//		{
//			min = nums[i];
//			minIndex = i;
//		}
//	}
//	cout << "最小值是：" << min << '/' << nums[minIndex] << endl;
//	cout << "最小值的下标是：" << minIndex << endl;
//
//	int jCount = 0, oCount = 0;
//	for (int i = 0; i < numsLen; i++)
//	{
//		if (nums[i] % 2 == 0)
//		{
//			oCount++;
//		}
//		else{
//			jCount++;
//		}
//	}
//	cout << "奇数个数：" << jCount << '\t' << "偶数个数：" << oCount << endl;
//
//	int searchNum;
//	int searchIndex = INT_MIN;
//	cout << "请输入要查找的数字：";
//	cin >> searchNum;
//	for (int i = 0; i < numsLen; i++)
//	{
//		if (nums[i] == searchNum)
//		{
//			searchIndex = i;
//			break;
//		}
//	}
//	if (searchIndex == INT_MIN)
//	{
//		cout << "数组中没有这个数字！" << endl;
//	}
//	else
//	{
//		cout << searchNum << "在数组中的下标为：" << searchIndex << endl;
//	}
//}

//数组排序
//循环录入5个整型数字，进行降序排列后输出结果
//冒泡排序：
//1、第一轮比较的次数：数组的总长度-1
//2、下一轮比上一轮比较的次数：少一次

//int main()
//{
//	int N = 5;
//	int temp;
//	int nums[] = { 15, 25, 90, 23, 9 };
//	//外层循环控制比较的轮数
//	for (int i = 0; i < N- 1; i++)
//		//内层循环控制每轮的比较和交换
//		for (int j = 0; j < N-1 - i; j++)
//		{
//		    if (nums[j] < nums[j + 1])
//		   {
//			//交换
//			temp = nums[j];
//			nums[j] = nums[j + 1];
//			nums[j + 1] = temp;
//		   }
//		
//		}
//	
//}
//
//int main()
//
//{
//	//选择排序
//	int nums[]{8, 4, 2, 1, 23, 23, 344,12};
//	//通过计算得到整型数组的实际长度（不能用于string数组）
//	int numsLen = sizeof(nums) / sizeof(int);
//	//擂台变量
//	int min = nums[0];   //假设最小值是数组的第一个元素
//	int minIndex = 0;    //最小值的初始下标设置为0
//	int temp;            //临时变量
//	for (int i = 0; i < numsLen-1 ; i++)
//	{
//		min = nums[i];//假设第i个元素是最小值了
//		minIndex = i;
//		for (int j = i + 1; j < numsLen;j++)
//			//打擂台
//			if (nums[j] < min)
//			{
//			min = nums[j];
//			minIndex = j;
//			}
//		//交换
//		if (minIndex > i)
//		{
//			//可以不写
//			temp = nums[minIndex];
//			nums[minIndex] = nums[i];
//			nums[i] = temp;
//		}
//	}
//	
//	cout << "排序后：" << endl;
//	for (int i = 0; i < numsLen; i++)
//	{
//		cout << nums[i] << endl;
//	}
//	//逆序
//	for (int i = 0; i < numsLen/2; i++)
//	{
//		temp = nums[i];
//		nums[i] = nums[numsLen - i - 1];
//		nums[numsLen - i - 1] = temp;
//	}
//	cout << "n逆序后：" << endl;
//	for (int i = 0; i < numsLen; i++)
//	{
//		cout << nums[i] << endl;
//	}
//}

int main()
{
	//实现数组元素的删除和插入
	double power[99];//数组的大小一旦确定了，就不能再更改了！！！
	int powerCount = 0;//当前数组中的元素个数
	double insertPower;//要插入的攻击力数值
	int insertIndex=0;//默认插入到第一个元素的位置
	power[powerCount++] = 45771;
	power[powerCount++] = 42322;
	power[powerCount++] = 40907;
	power[powerCount++] = 40706;

	double temp;
	for (int i = 0; i < powerCount; i++)
	{
		for (int j = 0; j < powerCount-i-1; j++)
		{
			if (power[j] < power[j + 1])
			{
				temp = power[j];
				power[j] = power[j + 1];
				power[j + 1] = temp;
			}
		}
	}
	cout << "排序后：" << endl;
	for (int i = 0; i < powerCount; i++)
	{
		cout << power[i] << '\t';
	}
	cout << endl;
	//插入
	cout << "请输入要插入的数字：";
	cin >> insertPower;
    //插入以后，保证数组仍然是有序的
	//1、把新数字放在数组的末尾，重新进行排序
	//2、找到第一个比插入数字大的位置insertIndex
	   //  从最后一个元素开始，将数字复制到后面一个元素中
	   //  将要插入的数字赋值给下标为insertIndex的元素
	//
	insertIndex = powerCount - 1;
	//1.找到第一个比插入数字大的位置insertIndex
	for (int i = 0; i < powerCount; i++)
	{
		if (insertPower>power[i])
		{
			insertIndex = i;
			break;
		}
	}
	//2.从最后一个元素开始，将数字复制到后面一个元素中
	for (int i = powerCount - 1; i >= insertIndex; i--)
	{
		power[i + 1] = power[i];
	}
	//3.将要插入的数字赋值给下标为insertIndex的元素
	power[insertIndex] = insertPower;
	//4.将数组的总长度+1
	powerCount++;
	cout << "插入后：" << endl;
	for (int i = 0; i < powerCount; i++)
	{
		cout << power[i] << '\t';
	}

	//删除
	//1.找到要删除的元素下标
	double deletePower;
	int deleteIndex = INI_MIN;
	cout << "请输入要删除的数字：";
	cin >> deletePower;
	for (int i = 0; i < powerCount; i++)
	{
		if (deletePower == power[i])
		{
			deleteIndex = i;
			break;
		}
	}
	//2.从找到的下标开始，后面一个元素赋值给前面一个元素
	for (int i = deleteIndex; i < powerCount - 1; i++)
	{
		power[i] = power[i + 1];
	}
	//3.总长度-1
	powerCount--;
	cout << "删除后：" << endl;
	for (int i = 0; i < powerCount; i++)
	{
		cout << power[i] << '\t';
	}
}






