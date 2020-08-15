# 노드 기초 

+ 노드의 기초를 몰라서 찾아보았다.

        var express=require('express');

        var http=require('http');


        var app=express();

        //set은 포트 속성 지정

        app.set('port', process.env.PORT || 3000);

        //use는 미들웨어를 등록할 때 사용. 미들웨어는 리퀘스트, 리스판스, 넥스트 객체를 파라미터로 받는 함수

        app.use(function(req,res,next){

            console.log('첫번째 미들웨어 호출');

            //res.writeHead는 리스판스에 헤더 정보 넣는 것이다. 서버 응답을 200 즉 정상 응답으로 넣고 컨텐츠 유형을 객체로 설정한다.

            res.writeHead(200, {"Content-Type":"text/html;charset=utf8"});

            //end 함수에 스트림에 보낼 데이터의 마지막 비트를 선택적으로 전달할 수 있다.

            //res.write(헤더), res.write(<html>),res.write(<body>)순서 지나고 res.end()를 작성한다.

            res.end('<h3>서버에서 응답한 결과입니다</h3>');

        })

        //createServer 통해 웹 서버 객체를 만든다. 이 서버로 오는 http 요청마다  createServer에 전달된 함수가 한 번씩 호출

        var server=http.createServer(app).listen(app.get('port'), function(){

            console.log('익스프레스로 웹 서버 실행' +app.get('port'));

***
참조한 영상(Do it! Node.js 프로그래밍 강의)