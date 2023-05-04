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
