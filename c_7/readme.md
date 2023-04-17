# 2023-04-12 7주차 C프로그래밍 수업

```c
#include <stdio.h>

//백준 10952번

int main()
{
  int a, b;
  
  while (1)
  {
    scanf("%d %d", &a, &b); //a와 b가 모두 0이면 중지
    if (a==0 && b==0)
    {
      break;
    }
      printf("%d\n", a+b);
    }
    return 0;
 }
