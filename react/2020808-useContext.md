# useContext

+ useContext 사용하기 전에는 아래처럼 여러 컴포넌트를 거쳐 prop이 전달되었다.

        import React, {createContext, useContext, useState} from 'react'

            function Child(){
                
                return <p>안녕하세요? {text} </p>
            }


            function Parent({text}){
                return <Child text={text}></Child>
            }

            function GrandParent({text}){
                return <Parent text={text}></Parent>
            }


            function ContextSample() {
                return (
                <>   
                        <GrandParent text='good'></GrandParent>
                </>
                )
                
            }

        export default ContextSample


+ 그 문제를 해결하기 위해 useContext 사용한 소스이다.
    
        import React, {createContext, useContext, useState} from 'react'

        const MyContext=createContext('defaultValue');

        function Child(){
            const text=useContext(MyContext);
            return <p>안녕하세요? {text} </p>
        }


        function Parent(){
            return <Child ></Child>
        }

        function GrandParent(){
            return <Parent ></Parent>
        }


        function ContextSample() {
            const [value, setValue]=useState(true);
            return (
            <>       
                <MyContext.Provider value={value ? 'good' : 'bad' }>
                    <GrandParent></GrandParent>
                    <button onClick={()=>setValue(!value)}>Click me</button>
                </MyContext.Provider>
            </>
            )
            
        }

        export default ContextSample


***
참조한 영상(velopert의 온라인 강의)