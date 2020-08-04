# useEffect

+ useEffect 리액트 훅을 연습하는 중이다.

+ 아래는 useEffect 이용해 브라우저 페이지의 타이틀 엘리먼트를 바꾸는 소스이다.


        import React, {useState, useEffect} from 'react'

        function HookSeven() {
            const [count, setCount]=useState(0);
            useEffect( ()=>{
                document.title=`You clicked ${count} times`;
            })
            return (
                <div>
                    <button onClick={()=>{
                        setCount(count=>count+1);
                    }}>Click {count} times </button>
                </div>
            )
        }

        export default HookSeven
        

+ 다음은 마우스 움직일 때마다 위치 좌표가 출력되는 소스이다.

        import React, {useState, useEffect} from 'react'

        function HookTen() {
            const [x, setX]=useState(0)
            const [y, setY]=useState(0)

            const logMousePosition=e=>{
                console.log('Mouse event');
                setX(e.clientX)
                setY(e.clientY)
            }

            useEffect(()=>{
                console.log('useEffect called');
                window.addEventListener('mousemove', logMousePosition)

                return ()=>{
                    console.log('Component unmount');
                    window.removeEventListener('mousemove',logMousePosition)
                }
            }, [])
            return (
                <div>
                    Hooks X-{x} Y-{y}
                </div>
            )
        }

        export default HookTen


***
참조한 유튜브('https://www.youtube.com/watch?v=nAuWOnFMlOw', ' https://www.youtube.com/watch?v=DTlmk6QeOHY')
