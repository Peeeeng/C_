# 2023-05-04 10주차 C프로그래밍 수업
```c
#include <stdio.h>

//백준 2439

int main() {
  
  int N;
  int j=0;
  scanf("%d", &N);
  
  for (int i=1; i<=N; i++)
  {
    for (j=1; j<=N-i; j++)
    {
      printf(" ");
    }
    for (j=1; j<=i; j++)
    {
      printf("*");
    }
    printf("\n");
  }
  return 0;
}
```
```c
#include <stdio.h>

int get_integer();
int add(int x, int y);
int minus(int x, int y);
int multi(int x, int y);
int div(int x, int y);

int get_integer()
{
  int value;
  printf("정수를 입력하시오 : ");
  scanf("%d", &value);
  return value;
}

//add
int add(int x, int y)
{
  return x+y;
}

int main(void)
{
  int x, y;

  int x = get_integer();
  int y = get_integer();

  int sum = add(x, y);
  printf("두 수의 합은 : %d", x+y);

  return 0;
}
//minus
int minus(int x, int y)
{
  return x-y;
}

int main(void)
{
  int x, y;

  int x = get_integer();
  int y = get_integer();

  int sum = minus(x, y);
  printf("두 수의 차는 : %d", x-y);

  return 0;
}
//multi
int multi(int x, int y)
{
  return x*y;
}

int main(void)
{
  int x, y;

  int x = get_integer();
  int y = get_integer();

  int sum = multi(x, y);
  printf("두 수의 곱은 : %d", x*y);

  return 0;
}
//div
int div(int x, int y)
{
  return x-y;
}

int main(void)
{
  int x, y;

  int x = get_integer();
  int y = get_integer();

  int sum = div(x, y);
  printf("두 수의 나눗셈은 : %d", x/y);

  return 0;
}
```
```c
#include <stdio.h>

int factorial(int n)
{
  if(n==1)
  {
    return 1;
  }
  else
  {
    return n * factorial(n-1);
  }
}
int main(void)
{
  int n;
  printf("알고 싶은 팩토리얼의 값은? ");
  scanf("%d", &n);
  printf("%d!의 값은 %d입니다.\n", n, factorial(n));
  return 0;
}
```
