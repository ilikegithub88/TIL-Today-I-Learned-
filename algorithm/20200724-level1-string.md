# 프로그래머스 Level1. 문자열 다루기 기본

## 1. 문제 설명
문자열 s의 길이가 4 혹은 6이고, 숫자로만 구성돼있는지 확인해주는 함수, solution을 완성해야 한다. 

예를 들어 s가 a234이면 False를 리턴하고 1234라면 True를 리턴하면 된다.

제한 사항이 있는데  s는 길이 1 이상, 길이 8 이하인 문자열이어야 한다.
	


## 2. 내 풀이

function solution(s) { 

    const answer = true;

    let result;

    result=isNaN(s);  
    
        if(!result && s!==null && s!==true  && s.length===4

        || !result && s.length===6){

            return true;

        }else{

            return false;

        }

}


## 3. 다른 사람의 풀이 

function solution(s) {

    var answer = true;

    for(let i=0;i<s.length;i++){

        if(isNaN(Number(s[i]))===true){

            return false;

        }

        else if(s.length !== 4 && s.length !== 6){

            return false;

        }

    }

    return answer;

}

***


function solution(s) {

    var answer = true;

    if(s.length==4 || s.length==6){

        for(let c of s.split("")){

            let num = c*1;

            if(0<=num && num<=9) continue;

            answer = false;

            break;

        }

    }else answer = false;

    return answer;

}

***

function alpha_string46(s){

var regex = /^\d{6}$|^\d{4}$/;

return regex.test(s);

}

***

function alpha_string46(s){

var result = false;

if((s.length == 4 || s.length == 6) && /^[0-9]+$/.test(s)) {

    result = true;

}

return result;

}

