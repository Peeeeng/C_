# 2023-03-30 5주차 C프로그래밍 수업

```c
#include <stdio.h>

//백준 1330번

int main(void)
{
  int A, B;

  
  scanf("%d %d", &A, &B);
  
  if (A > B)
  {
    printf(">\n");
  }
  else if (A < B)
  {
    printf("<\n");
  }
  else
  {
    printf("==\n");
  }
  return 0;
}
```
