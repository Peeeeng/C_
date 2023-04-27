# 2023-04-27 9주차 C프로그래밍 수업

### 2주차 연습문제
```c
//덧셈 프로그램
#include <stdio.h>

int main(void)
{
  int x, y, sum;

  printf("첫 번째 숫자를 입력하시오 : ");
  scanf("%d", &x);
  printf("두 번째 숫자를 입력하시오 : ");
  scanf("%d", &y);
  
  sum = x + y;

  printf("두 수의 합: %d", sum);
  
  return 0;
}

//원의 면적 계산 프로그램
#include <stdio.h>

int main(void)
{
  float radius;
  float area;

  printf("반지름을 입력하시오 : ");
  scanf("%f", &radius);

  area = 3.14 * radius * radius;

  printf("원의 면적 : %f", area);
  
  return 0;
}

//환율 계산 프로그램
#include <stdio.h>

int main(void)
{
  double rate;
  double usd;
  int krw;

  printf("환율을 입력하시오 : ");
  scanf("%lf", &rate);
  printf("원화 금액을 입력하시오 : ");
  scanf("%d", &krw);
  
  usd = krw / rate;
  printf("원화 %d원은 %lf달러입니다.", krw, usd);
  
  return 0;
}

//평균 계산하기 프로그램
#include <stdio.h>

int main(void)
{
  double num1, num2, num3;
  double sum, avg;

  printf("3개의 실수를 입력하시오 : ");
  scanf("%lf %lf %lf", &num1, &num2, &num3);

  sum = num1 + num2 + num3;
  avg = sum / 3.0;
  
  printf("합계=%.2lf\n", sum);
  printf("평균=%.2lf\n", avg);
  
  return 0;
}

//사각형의 둘레와 면적
#include <stdio.h>

int main(void)
{
  double w, h, area, perimeter;

  w = 10.0;
  h = 5.0;
  area = w * h;
  perimeter = 2 * (w + h);
  
  printf("사각형의 넓이 : %lf\n", area);
  printf("사각형의 둘레 : %lf\n", perimeter);
  
  return 0;
}
```

### 3주차 연습문제
```c
//태양빛 도달 시간
#include <stdio.h>

int main(void)
{
  double light_speed = 300000;
  double distance = 149600000;
  double time;

  time = distance / light_speed;
  //time = time / 60.0;

  printf("빛의 속도는 %fkm/s \n", light_speed);
  printf("태양과 지구와의 거리 %fkm \n", distance);
  printf("도달 시간은 %f초\n", time); //?분 ?초
  
  return 0;
}
```
### 4주차 연습문제
```c
//거스름돈 계산하기
#include <stdio.h>

int main(void)
{
  int money, change;
  int price, c5000, c1000, c500, c100;

  printf("물건 값을 입력하시오 : ");
  scanf("%d", &price);

  printf("투입한 금액을 입력하시오 : ");
  scanf("%d", &money);
  change = money - price;

  c1000 = change / 1000;
  change = change % 1000;

  c500 = change / 500;
  change = change % 500;

  c100 = change / 100;
  change = change % 100;

  printf("\n천원권 : %d장\n", c1000);
  printf("오백원 동전 : %d개\n", c500);
  printf("백원 동전 : %d개\n", c100);
  
  return 0;
}
```
### 5주차 연습문제
### 6주차 연습문제
### 7주차 연습문제
