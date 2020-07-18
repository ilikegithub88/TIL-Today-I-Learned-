# 노드 에러 : code ELIFECYCLE 

1. 문제점
   
    npm start 명령할 때마다 npm ERR! code ELIFECYCLE  npm ERR! errno 1 에러 메세지

2. code ELIFECYCLE에만 초점 맞춰서 해결하려고 시도한 방법들
 
   2-1. 
      
      터미널에 npm cache clean --force 

      ->  node_modules 폴더와 package-lock.json 파일 삭제 
    
      -> 터미널에 npm install 

   2-2. package-lock.json 파일만 삭제
   
   2-3. package.json 파일에서 start:"node ."로 바꾸었다

   2-4. Visual Studio Code 내 터미널이 아니라 윈도우 명령 프롬프트에서 실행

   2-5. 터미널에 npm audit fix
   
   2-6. 터미널에 npm install -g node-pre-gyp
   
   2-7. 포트 번호 변경
   
   2-8. node 12버전 완전히 삭제한 후 10버전으로 설치

3. code ELIFECYCLE 자체보다는 코드에 초점 맞춰서 시도한 방법들
 
   3-1. 스키마 역할하는 User.js 파일에서 type:number 을 type:Number로 수정

   3-2. User.js 파일에서 맨 아랫줄 변수 설정을 수정

   3-3. index.js에서 app.use(bodyParser.urlencoded({extended:true})) 등을 수정

4. 해결책
  
   윗 방법 중 3-3 시도 방법이 성공. 
  
   index.js 파일 코드 중

   >app.user(bodyParser.urlencoded({extended:true}));
   >app.user(bodyParser.json());

   app.user을 app.use로 수정해서 해결

   >app.use(bodyParser.urlencoded({extended:true}));
   >app.use(bodyParser.json());
