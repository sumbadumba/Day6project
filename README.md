# Day6project



//#include<stdio.h>
//#include<math.h>
//
//
//int main()
//{
//	int arr[3];//배열형 변수라고 한다.[0][1][2]를
//
//	arr[0] = 10; //이것이 index를 의미함 
//	arr[1] = 20;
//	arr[2] = 30;
//	//arr[3] = 30;
//
//	//printf("%d ", arr[3]);
//	//printf("arr의 index %d 의 값 = %d\n", 0, arr[0]);
//	//printf("arr의 index %d 의 값 = %d\n", 1, arr[1]);
//	//printf("arr의 index %d 의 값 = %d\n", 2, arr[2]);
//
//
//	//for (int i = 0; i < 3; i++)
//	//{
//	//	printf("arr의 index %d 의 값 = %d\n", i, arr[i]);
//	//}
//
//	int a = arr[0];
//	int b = arr[1];
//	int c = arr[2];
//	
//	const int t = 20;//배열에서 상수취급을 한다.
//
//	int arr2[t];//그래서 가능하다.
//
//	int arr3[] = { 1,2,3,4,5 };//이니셜라이저 = (영어로)초기화 한다.(initialize)
//
//	//arr3의 크기는 {에서}까지 내용물의 개수
//	printf("size of arr3 : %d\n", sizeof(arr3));//배열의 크기(4*?)를 파악한다.
//
//	printf("const of arr3 : %d\n", sizeof(arr3)/sizeof(int));//배열의 개수를 파악
//
//	int arr4[99]; //0~98
//
//	//pow 제곱을 구하는 함수
//
//	for (int i = 0; i < 99; i++)
//	{
//		arr4[i] = pow(i, 3);//컨트롤 + 시프트 + 스페이스 = 
//		printf("arr4[%d] : %d \n", i, arr4[i]);
//
//	}
//	
//	//방법
//	//1. 과제를 할 때 순서를 먼저 적는다.
//	//2. 순서도를 그린다.(마이크로 비지오(그림툴))
//
//	return 0; 
//}

//실습
//크기가 20인 배열에 0~50까지 의 랜덤한 숫자를 입력
// 20개 모두 입력이 되면 배열 전체를 출력

#include<stdio.h>
#include<time.h>
#include<stdlib.h>


//
//int main()
//{
//	int arr[20];
//
//	srand(time(NULL));
//
//	for (int i = 0; i < 20; i++)
//	{
//		arr[i] = rand() % 50;
//		printf("arr[%d] = %d\n", i, arr[i]);
//
//	}
//
//}

//2차원 배열
//int main()
//{
//	int arr[3][2];//세로가 먼저 입력된다고 생각하는게 좋다. 3 = y축 2 = x축
//	arr[0][0] = 10;
//	arr[0][1] = 10;
//	arr[1][0] = 20;
//	arr[1][1] = 20;
//	arr[2][0] = 30;
//	arr[2][1] = 30;
//
//
//	for (int i = 0; i < 3; i++)
//	{
//		for (int j = 0; j < 2; j++)
//		{
//			printf("arr[%d][%d] = %d \n", i, j, arr[i][j]);
//
//		}
//	}
//	return 0;
//
//}

//실습2
// 구구단이 들어 있는  2차월 배열을 만드시오.
// 구구단이 모두 들어가면 출력

//int main()
//{
//	int  arr[9][9];
//	
//
//
//	for (int i = 0; i < 9; i++)
//	{
//		for (int j = 0; j < 9; j++)
//		{
//			arr[i][j] = arr[i][j];
//		
//		}
//	}
//
//	for (int i = 2; i < 10; i++)
//	{
//		for (int j = 2; j < 10; j++)
//		{
//			printf("%d X %d = %d \t",i,j, i*j);
//
//		}
//		printf("\n");
//	}
//}
//썜코드 
//for (int i = 0; i < 8; i++)
//{
//	for (int j = 0; j < 9; j++)
//	{
//		arr[i][j] = (i + 2) * (j + 1);
//
//	}
//}


//pointer
#include<stdio.h>


//포인터 = 메모리에 주소 값을 저장하기 위함이다.

int main()
{
	int * ptr = nullptr;
	//char * charptr = nullptr;//캐릭터형 포인터(사용빈도 높음)
	int a = 10;
	ptr  = &a; //&가 a와 띄어져 있으면 단항연산자이다.(& a)XXXX

	//printf("ptr의 주소값 : %X\n", ptr);
	//printf("&a의 주소값 : %X\n", &a);

	//printf("ptr이 가르키는 곳의 실제 들어있는 값 %d\n", *ptr);//주소를 출력하려면
	////%x를 쓰고 값을 받으려면 %d를 쓴다.


	printf("ptr의 크기 : %d\n", sizeof(ptr));//sizeof에는 형을 집어 넣는데 배열도 가능하다.

	int arr[3];
	printf("arr의 크기 : %d\n", sizeof(arr));//배열 전체크기가 나옴
	ptr = arr;//<-주소 값을 가진다.(포인터도 변수이기 때문에 
	//포인터 형 변수
	printf("ptr의 크기 : %d\n", sizeof(ptr));//배열값 하나의 크기가 나온다.
}

//숙제1
// 짤짤이 게임 만들기
//- 랜덤하게 홀짝을 10회 결정 배열에 미리 저장
//- 결정된 홀짝이 어떤 값인지 사용자로부터 10회 입력받는다.
//- 각 회차에 입력된 값이 결정 된 값과 같으면 Win 아니면 Failed 출력
//- 출력메세지가 영어로 되야 하는 것은 아님.
//- 10회에 대한 최종 승률 출력 


