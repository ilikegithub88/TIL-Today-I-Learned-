# 계수 정렬

## 1. 정의

모든 숫자의 개수를 센 후, 누적 합을 구하고, 다시 숫자를 넣으면 된다.

[3,4,0,1,2,4,2,4], [개수를 저장할 공간], [결과]

개수를 저장할 공간을 정렬할 제일 큰 수의 갯수만큼 0으로 만든다.

[3,4,0,1,2,4,2,4], [0,0,0,0,0], [결과]

처음부터 개수를 세어 저장한다. 0은 1개, 1은 1개, 2는 2개, 3은 1개, 4는 3개이다.

[3,4,0,1,2,4,2,4], [1,1,2,1,3], [결과]

개수를 저장한 것을 누적합으로 바꾼다. 순서대로 1, 2, 4, 5, 8이 된다.

[3,4,0,1,2,4,2,4], [1,2,4,5,8], [결과]

누적합을 바탕으로 숫자를 결과에 넣는다. 0은 1에, 1은 2에, 2는 3,4에 3은 5에, 4는 6,7,8에 넣는다.

[3,4,0,1,2,4,2,4], [1,2,4,5,8], [0,1,2,2,3,4,4,4]

## 2. 코드
        var countingSort = function(array, k) {
        var count = [], result = [];
        for (var i = 0; i <= k; i++) { // 모든 숫자의 개수를 일단 0으로 초기화
            count[i] = 0;
        }
        console.log(count, result, array.length);
        for (var j = 0; j < array.length; j++) { // 숫자의 개수를 세어 저장
            count[array[j]] += 1;
        }
        console.log(count, result, k);
        for (i = 0; i < k ; i++) { // 누적합을 구합니다.
            count[i + 1] += count[i];
        }
        console.log(count, result);
        for (j = 0; j < array.length; j++) { // 누적합이 가리키는 인덱스를 바탕으로 결과에 숫자를 넣는다
            console.log(array[j], count[array[j]] - 1);
            result[count[array[j]] - 1] = array[j];
            count[array[j]] -= 1;
        }
        console.log(count, result);
        return result;
        };

## 3. 특징

적은 개수의 숫자를 정렬할 때 유용하다.

***
인용한 블로그('https://www.zerocho.com/category/Algorithm/post/58006da88475ed00152d6c4b')
