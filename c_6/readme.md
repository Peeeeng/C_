# 2023-04-06 6주차 C프로그래밍 수업
```c
#include <stdio.h>

//백준 10950번

int main()
{
  int a, b, T;
  int i = 1;
  
  scanf("%d", &T); //케이스 개수 입력
  
  while(i<=T)
    {
      scanf("%d %d", &a, &b);
      printf("%d\n", a+b); //printf("Case #%d : %d + %d = %d\n", i, a, b, a+b); -> Case #i : a + b = a+b
      i++;
    }

  return 0;
}
```
