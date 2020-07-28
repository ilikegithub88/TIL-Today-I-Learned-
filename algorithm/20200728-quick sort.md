# 퀵 정렬

## 1. 정의

배열의 맨 오른쪽 요소나 중간 요소를 기준(pivot)으로 잡고 그 기준보다 작거나 큰 수의 위치를 조정하고 재귀적으로 접근한다.

가장 왼쪽부터 값을 기준과 비교해서 기준보다 큰 값이 나타날 때까지 오른쪽으로 이동한다.

가장 오른쪽부터 값을 기준과 비교해서 기준보다 작은 값이 나타날 때까지 왼쪽으로 이동한다.

기준보다 큰 왼쪽 값과 기준보다 작은 오른쪽 값 위치를 서로 바꾼다.

## 2. 코드

배열의 제일 오른쪽 요소가 아니라 중간 요소를 기준(pivot)으로 잡는 코드를 인용했다.

        function quickSort (array, left = 0, right = array.length - 1) {

                if (left >= right) {

                return;
            }

            const mid = Math.floor((left + right) / 2);

            const pivot = array[mid];

            const partition = divide(array, left, right, pivot);

            quickSort(array, left, partition - 1);

            quickSort(array, partition, right);



            function divide (array, left, right, pivot) {

                while (left <= right) {

                    while (array[left] < pivot) {

                        left++;

                    }

                    while (array[right] > pivot) {

                        right--;

                    }

                    if (left <= right) {

                        let swap = array[left];

                        array[left] = array[right];

                        array[right] = swap;

                        left++;

                        right--;

                    }
                }

            return left;
        }

        return array;

        }

## 3. 특징

문제를 잘게 분해해 해결하는 분할 정복 알고리즘에 속하는 정렬이다.

아주 가끔 느리지만 평소에는 성능이 뛰어나다.

***
참조한 블로그('https://im-developer.tistory.com/135')