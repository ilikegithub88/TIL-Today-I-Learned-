# modified content, untracked content

1. 문제점
   
   리액트와 노드 혼합한 보일러플레이트를 커밋하려는데 리액트로 만든 client 폴더가 git add되지 않았다.

   에러 원인은 modified content, untracked content였다. 

2. 시도한 방법들

   2-1. 깃 배쉬에 git rm -rf --cached 문제폴더이름 입력하고 git add 문제폴더이름 했다.

   2-2. 깃 원격저장소 연결 해제하고 다시 연결했다.

   2-3. gitignore 파일이 리액트로 만든 client 폴더에는 없어서 만들고 git add 명령했다.

3. 해결책
   
   윈도우 탐색기에서 숨긴 항목을 보여지게 한 후 문제가 된 client 폴더에 있는 .git 폴더를 삭제했다.

   그리고나서 깃 배쉬에 git rm -rf --cached 문제폴더이름 입력했다. 이제 git add 문제폴더이름이 정상 작동된다.
