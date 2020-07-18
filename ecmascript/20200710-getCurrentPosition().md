# navigator.geolocation.getCurrentPosition(arg1, arg2)
1. 문제점

   사용자의 브라우저에 있는 navigator 객체를 이용해 사용자의 위치를 추적할 때 getCurrentPosition() 메서드를 사용하는데
   문제는 이 메서드가 timeout이 없이 무한대라고 한다. 그래서 가끔 작동 안 할 때가 있다고 한다.

2. 해결책
 
   2-1. navigator.geolocation.getCurrentPosition() 메서드 안에 timeout을 추가한다.
    > navigator.geolocation.getCurrentPosition(arg1, arg2, {timeout:7000})

   2-2. 위의 방법이 되지 않는다면 아래 방법을 사용한다.
    > navigator.geolocation.getCurrentPosition(arg1, arg2, {maximumAge:60000, timeout:5000, enableHighAccuracy:true});
