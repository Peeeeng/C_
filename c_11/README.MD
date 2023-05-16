# 2023-05-11 11주차 C프로그래밍 과제
```c
//동전 던지기 게임
#include <stdlib.h>
#include <stdio.h>
#include <time.h>
int coin_toss (void);
int main(void)
{
  int toss;
  int heads = 0;
  int tails = 0;
  srand((unsigned)time(NULL));
  
  for (toss = 0; toss < 100; toss++) {
    if (coin_toss() == 1)
      heads++;
    else
      tails++;
  }

  printf("동전의 앞면: %d \n", heads);
  printf("동전의 뒷면: %d \n", tails);
  return 0;
}

int coin_toss( void )
{
  int head = rand() % 2;
  return head;
}
```
```c
//자동차 게임
#include <stdlib.h>
#include <stdio.h>
#include <conio.h>
#include <time.h>
void disp_car(int car_number, int distance)
{
  int i;
  printf("CAR #%d:", car_number);
  for( i = 0; i < distance/10; i++ )
  {
    printf("*");
  }
  printf("\n");
}
int main(void)
{
  int i;
  int car1_dist=0, car2_dist=0;
  srand( (unsigned)time( NULL ) );
  for( i = 0; i < 6; i++ )
  {
    car1_dist += rand() % 100;
    car2_dist += rand() % 100;
    disp_car(1, car1_dist);
    disp_car(2, car2_dist);
    printf("---------------------\n");
    _getch();
  }
return 0;
}
```
```c
//삼각함수 라이브러리
#include <math.h>
#include <stdio.h>
int main(void)
{
  double pi = 3.1415926535;
  double x, y;
  
  x = pi / 2;
  y = sin( x );
  printf( "sin( %f ) = %f\n", x, y );
  y = cos( x );
  printf( "cos( %f ) = %f\n", x, y );
}
```
```c
//시간맞추기 게임
#include <stdio.h>
#include <time.h>
int main(void)
{
  time_t start, end; // time_t는 unsigned long과 동일하다.
  start = time(NULL);
  printf("10초가 되면 아무 키나 누르세요\n");
  while (1)
  {
    if (getchar())
    break;
  }
  printf("종료되었습니다.\n");
  end = time(NULL);
  printf("경과된 시간은 %ld 초입니다. \n", end - start);
  return 0;
}
```
```c
//나무 높이 측정
#define _CRT_SECURE_NO_WARNINGS
#include <math.h>
#include <stdio.h>
int main(void)
{
  double height, distance, tree_height, degrees, radians;
  
  printf("나무와의 길이(단위는 미터): ");
  scanf("%lf", &distance);
  
  printf("측정자의 키(단위는 미터): ");
  scanf("%lf", &height);
  
  printf("각도(단위는 도): ");
  scanf("%lf", &degrees);
  
  
  radians = degrees * (3.141592 / 180.0);
  tree_height = tan(radians) * distance + height;
  printf("나무의 높이(단위는 미터): %lf \n", tree_height);
  
  return 0;
}
```
```c
//삼각함수 그리기
#include <stdio.h>
#include <math.h>
#define PI 3.141592

double rad(double degree)
{
  return PI * degree / 180.0;
}
void drawbar(int height)
{
  for (int i = 0; i < height; i++)
  {
    printf("*");
  }
  printf("\n");
}
int main(void)
{
  int degree, x, y;
  for (degree = 0; degree <= 90; degree += 10)
  { 
    // 싸인값은 -1.0에서 1.0이므로 정수로 반올림하여서 증폭한다.
    y = (int)(60 * sin(rad((double)degree)) + 0.5);
    drawbar(y);
  }
return 0;
}
```
```c
//공학용 계산기 프로그램
#include <stdio.h>
#include <math.h>
int menu(void)
{
	int n;
	printf ("1.팩토리얼\n");
	printf ("2.싸인\n");
	printf ("3.로그(base 10)\n");
	printf ("4.제곱근\n");
	printf ("5.순열(nPr)\n");
	printf ("6.조합(nCr)\n");
	printf ("7.종료\n");
	printf ("선택해주세요: ");
	scanf ("%d", &n);
	return n;
}
void factorial()
{
	long long n, result=1, i;
	printf ("정수를 입력하시오: ");
	scanf ("%lld", &n);

	for (i = 1; i <= n; i++)
	result = result * i;
	printf ("결과 = %lld\n\n", result);
}

void sine()
{
	double a, result;
	printf ("각도를 입력하시오: ");
	scanf ("%lf", &a);
	result = sin(a);
	printf ("결과 = %lf\n\n", result);
}

void logBase10()
{
	double a, result;
	printf("실수값을 입력하시오: ");
	scanf("%lf", &a);
	if (a <= 0.0)
	{
		printf("오류\n");
	}
	else
	{
		result = log10(a);
		printf("결과 = %lf\n\n", result);
	}
}

int main(void)
{
	while (1)
  {
	   switch (menu())
     {
		      case 1:
			            factorial();
			             break;
		      case 2:
			            sine();
			            break;
		      case 3:
			            logBase10();
			            break;
		      case 7:
			            printf("종료합니다.\n");
			            return 0;
		      default:
			            printf("잘못된 선택입니다.\n");
			            break;
		}  
  }
}
```
