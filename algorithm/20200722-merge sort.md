# 병합 정렬(합병 정렬)

## 1. 정의
병합 정렬은 정렬할 대상인 배열과 별도의 빈 배열 총 2개를 준비한다. 

빈 배열말고 정렬할 배열을 재귀 함수를 통해서 두 개로 나눈다.

나누면서 각 배열의 첫번째 요소끼리 크기 비교해서 작은 값을 텅 빈 배열로 이동시켜 저장한다.

예를 들어 배열 [10,5,3,7,9,15,2,1]과 텅 빈 배열 []을 준비한다. 정렬할 배열을 둘로 나눠서 [10,5,3,7], [9,15,2,1]가 된다.

각 배열을 다시 나눠서 [10,5], [3,7],[9,15],[2,1]가 된다. 그리고 [10,5]를 [10],[5]로 [3,7]을 [3],[7]로 쪼갠다.

[10],[5] 배열의 첫번째 요소에서 더 작은 값은 5이므로 [5,10]으로 정렬하고 [3], [7]에서 더 작은 첫번째 요소는 3이므로 [3,7]로 정렬한다.

이런 식으로 잘게 쪼갠 후 정렬한 뒤 병합해서 [3,5,7,10],[1,2,9,15]처럼 되면 두 배열의 첫 번째 요소 중 작은 값을 빈 배열로 이동시킨다. 

3과 1 중 1이 더 작으므로 1을 빈 배열로 이동시킨다. 정렬할 배열은 [3,5,7,10],[2,9,15]이 되고 빈 배열은 [1]이 된다.

[3,5,7,10],[2,9,15] 각각에서 첫번째 요소는 3과 2이므로 더 작은 2가 별도의 배열로 이동해서 원래 배열은 [3,5,7,10],[9,15]가 되고 별도의 배열은 [1,2]가 된다.

[3,5,7,10],[9,15] 배열의 각 첫번째 요소는 3과 9이므로 더 작은 3이 이동한다. 그래서 [5,7,10],[9,15]가 되고 별도의 배열은 [1,2,3]이 된다.

이렇게 빈 배열에 작은 값들을 이동시켜 결과적으로 [1, 2, 3, 5, 7, 9, 10, 15]가 된다.

## 2. 코드

        var mergeSort = function(array) {

            if (array.length < 2) return array; // 원소가 하나일 때는 병합정렬을 실시하지 않는다.

            var middle = Math.floor(array.length / 2); 

            var left = array.slice(0, middle); 

            var right = array.slice(middle, array.length); 

            return merge(mergeSort(left), mergeSort(right)); // 재귀 알고리즘에 의거해 쪼개고 정렬한다.

        }


        function merge(left, right) {

            var result = [];

            while (left.length && right.length) {
                
                if (left[0] <= right[0]) { 

                result.push(left.shift()); 

                } else {

                result.push(right.shift());  

                }

            }

            while (left.length) result.push(left.shift()); 

            while (right.length) result.push(right.shift()); 

            return result;

        };



## 3. 특징
병합 정렬은 분할 정복 알고리즘에 속한다. 큰 문제를 작은 문제로 잘게 쪼개서 풀기 때문이다. 

삽입 정렬보다 성능이 좋아 자주 쓰인다.



참조한 블로그('https://www.zerocho.com/category/Algorithm/post/57ee1fc107c0b40015045cb4')