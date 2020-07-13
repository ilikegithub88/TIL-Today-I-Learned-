# 리액트 Component Life Cycle
    컴포넌트를 생성 할 때는 constructor -> componentWillMount -> render -> componentDidMount 순으로 진행된다.
    컴포넌트를 제거 할 때는 componentWillUnmount 메소드만 실행된다.
## 컴포넌트 생성 과정
1. constructor
 
    생성자 메소드로서 컴포넌트가 처음 만들어 질 때 실행된다.
    이 메소드에서 기본 state 를 정할 수 있다.
    >constructor(props){
    >    
    >   super(props);
    >
    >}  
3. componentWillMount
  
    컴포넌트가 DOM 위에 만들어지기 전에 실행된다.
    >componentWillMount(){
    >
    >   console.log("componentWillMount");
    >
    >}
4. render
 
    컴포넌트 렌더링을 담당한다.
5. componentDidMount
 
    컴포넌트가 만들어지고 첫 렌더링을 다 마친 후 실행되는 메소드이다.
    이 안에서 다른 JavaScript 프레임워크를 연동하거나,
    setTimeout, setInterval 및 AJAX 처리 등을 넣는다.
    >componentDidMount(){
    >
    >   console.log("componentDidMount");
    >
    >}


## 컴포넌트 제거 과정
1. componentWillUnmount
 
    컴포넌트가 DOM 에서 사라진 후 실행되는 메소드입니다.

    >componentWillUnmount(){
    >
    >    console.log("componentWillUnmount");
    >
    >}


참조한 블로그('https://velopert.com/1130')