# __선형 검색__
선형검색은 원하는 원소가 발견될 때까지 처음부터 마지막 자료까지 차례대로 검색한다.

이렇게 하여 선형 검색은 찾고자 하는 자료를 찾을 때까지 모든 자료를 확인해야 한다.<br><br>

## __효율성 그리고 비효율성__

선형 검색 알고리즘은 정확하지만 아주 효율적이지 못한 방법이다.

리스트의 길이가 n이라고 했을 때, 최악의 경우 리스트의 모든 원소를 확인해야 하므로 n번만큼 실행된다.

여기서 최악의 상황은 찾고자 하는 자료가 맨 마지막에 있거나 리스트 안에 없는 경우를 말한다.

만약 100만 개의 원소가 있는 리스트라고 가정해본다면 효율성이 매우 떨어짐을 느낄 수 있다.

반대로 최선의 상황은 처음 시도했을 때 찾고자 하는 값이 있는 경우이다.

평균적으로 선형 검색이 최악의 상황에서 종료되는 것에 가깝다고 가정할 수 있다.

선형 검색은 자료가 정렬되어 있지 않거나 그 어떤 정보도 없어 하나씩 찾아야 하는 경우에 유용하다.

이러한 경우 무작위로 탐색하는 것보다 순서대로 탐색하는 것이 더 효율적이다.

이제 여러분은 왜 검색 이전에 정렬해줘야 하는지 알 수 있을 것이다.

정렬은 시간이 오래 걸리고 공간을 더 차지한다.

하지만 이 추가적인 과정을 진행하면 여러분이 여러 번 리스트를 검색해야 하거나 매우 큰 리스트를 검색해야 할 경우 시간을 단축할 수 있을 것이다.
```
#include <cs50.h>
#include <stdio.h>

int main(void)
{
    // numbers 배열 정의 및 값 입력
    int numbers[] = {4, 8, 15, 16, 23, 42};

    // 값 50 검색
    for (int i = 0; i < 6; i++)
    {
        if (numbers[i] == 50)
        {
            printf("Found\n");
            return 0;
        }
    }
    printf("Not found\n");
    return 1;
}
```