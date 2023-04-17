# 2023-03-23 4주차 C프로그래밍 수업

```c 
#include <stdio.h>

int main()
{
    int x, y;

    printf("두 개의 정수를 입력하시오 : ");
    scanf("%d %d", &x, &y);

    printf("%d\n", x * (y%10));
    printf("%d\n", x * (y/10%10));
    printf("%d\n", x * (y/100));
    printf("%d\n", x*y);

    return 0;
 }
 ```
