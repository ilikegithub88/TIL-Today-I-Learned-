# 삽입 정렬

## 1. 정의
여러 숫자가 섞여있으면 작은 숫자부터 큰 숫자로 오름차순으로 정렬한다. 

어떤 숫자가 자신의 왼쪽에 있는 숫자보다 크면 가만히 있고, 더 작으면 왼쪽의 숫자의 왼쪽으로 이동한다.

예를 들어 [5,1,10,7]에서 1은 5보다 작으니 5의 왼쪽으로 이동시켜 [1,5,10,7]으로 만든다.

그리고 10은 5보다 크니 가만히 있는다. 7은 10보다 작으니 10의 왼쪽으로 이동한다.

결국 삽입정렬한 결과는 [1,5,7,10]이 된다.


## 2. 삽입 정렬 코드
숫자를 이동시킬 때 임시로 숫자를 보관하는 변수 temp가 중요하다.

             function insertSort(array){>
                var i, j, temp;>
                for(i=1; i<array.length; i++){>
                    temp=array[i];
                 
                    for(j=i-1; j>=0 && temp<array[j]; j--){
                    
                            array[j+1]=array[j];>
                            array[j]=temp;
                 
                    }>
                }>
                return array;>
             }

## 3. 삽입 정렬 특징
성능이 아주 뛰어나지는 않다. 반복문을 두 번 돌기 때문이다. 


참조한 블로그('https://www.zerocho.com/category/Algorithm/post/57e39fca76a7850015e6944a')