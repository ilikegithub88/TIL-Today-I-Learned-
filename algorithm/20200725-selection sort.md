# 선택 정렬

## 1. 정의
배열을 처음부터 끝까지 훑어서 가장 작은 수를 맨 앞으로 이동시킨다.

그리고 다시 배열을 처음부터 끝까지 스캔해서 두 번째로 제일 작은 수를 두번째 자리로 이동시킨다.

세번째로 제일 작은 수를 배열의 세번째 자리로 이동시키고 이 행동을 반복한다.

[10,5,3,7,12,9]에서 배열 맨 첫 요소부터 맨 끝 요소까지 훑어서 제일 작은 3을 앞으로 이동시킨다.

[3,10,5,7,12,9]에서 다시 배열 처음부터 끝까지 스캔해서 두번째로 제일 작은 5를 3 뒤로 이동시킨다.

[3,5,10,7,12,9]가 되고 이 행동을 반복해서 [3,5,7,9,10,12]로 정렬한다.

## 2. 코드
    var selectionSort = function(array) {

    var length = array.length;

    var minIndex, temp, i, j;


    for (i = 0; i < length - 1; i++) { 
        minIndex = i;

        for (j = i + 1; j < length; j++) { 

        if (array[j] < array[minIndex]) {

            minIndex = j;

        }

        }

        temp = array[minIndex]; 

        array[minIndex] = array[i];

        array[i] = temp; 

    }

    return array;

    };

## 3. 특징
사람들이 이해하기 쉬운 정렬이지만 성능이 좋지 않다.

***
참조한 블로그('https://www.zerocho.com/category/Algorithm/post/57f728c85141fc5fe4f4ca89')