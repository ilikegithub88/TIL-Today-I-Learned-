# css 연습

        <!DOCTYPE html>
        <html lang="en">
        <head>
            <meta charset="UTF-8">
            <meta name="viewport" content="width=<device-width>, initial-scale=1.0">
            <title>Document</title>
            <style>
                *{
                    margin:0;
                    padding:0;
                    box-sizing:border-box;
                    /* -moz-box-sizing:border-box는 익스플로러 8 버전에서만 사용 */
                    -moz-box-sizing:border-box;
                    -webkit-box-sizing:border-box;
                }

                body{
                    background:url('https://source.unsplash.com/random/?nature/1600*900') 
                    no-repeat right top fixed;
                    background-size:cover;
                    /* cover이므로 화면 전체에 가득찬다  */
                }
                a:link, a:hover, a:visited{
                    color:#fff;
                    text-decoration:none;
                    text-shadow:1px 1px 0 #283744;
                }

                nav{
                    width:100%;
                    height:auto;
                    background:#34495e;
                    font-size:1.2em;
                    font-weight:bold;
                    position:relative;
                }

                nav ul{
                    /* 모바일 화면에서 메뉴가 안 보이다가 클릭했을 때만 보이도록 none으로 설정 */
                    display:none;
                    height:auto;
                }

                nav ul li{
                    display:block;
                    width:120%;
                    text-align:center;
                    /* border-bottom은 밑줄 그어주기 */
                    border-bottom:1px solid #576979;
                }

                nav ul li a{
                    line-height:50px;
                }

                nav a#trigger {
                    display:block;
                    background-color:#283744;
                    width:100%;
                    padding-left:15px;
                    line-height:40px;
                    position:relative;
                }

                nav a#trigger::after{
                    content:"";
                    background:url('small3.png') no-repeat;
                    /* background-size:100% 안 하면 이미지가 잘려 일부만 보인다 */
                    background-size:100%;
                    /* 가상 엘리먼트는 꼭 너비와 높이를 지정한다 */
                    width:30px; height:30px; display:inline-block;
                    position:absolute; right:15px; top:5px;
                }

                @media screen and (min-width:721px){
                    nav{
                        height:40px;
                        border-bottom:2px solid #34495e;
                    }

                    nav ul{
                        display:block;
                        width:850px; height:40px; padding:0;
                        margin: 0 auto;
                    }


                    nav ul li{
                        display:inline-block;
                        width:140px; border-bottom:0; border-right:1px solid #576979;
                        margin-right:-6px;
                    }

                    /* 맨 오른쪽 메뉴는 오른쪽에 줄이 있을 필요가 없다 */
                    nav ul li:last-child{
                        border-right:0;
                    }

                    nav ul li a{
                        font-size:1em;
                        line-height:40px;
                    }

                    nav a#trigger{
                        display:none;
                    }
                }
            </style>
        </head>
        <body>
            <nav>
                <!-- 에밋 코딩인 ul>(li>a[href="#"])*6 입력해서 아래 완성 -->
                <ul>
                    <li><a href="#">HOME</a></li>
                    <li><a href="#">BOARD</a></li>
                    <li><a href="#">LOGIN</a></li>
                    <li><a href="#">SIGNUP</a></li>
                    <li><a href="#"> GUESTBOOK </a></li>             
                    <li><a href="#">CONTACT</a></li>
                </ul>
                <a href="#" id="trigger">MENU</a>
            </nav>

        <script
        src="https://code.jquery.com/jquery-3.5.1.min.js"
        integrity="sha256-9/aliU8dGd2tb6OSsuzixeV4y/faTqgFtohetphbbj0="
        crossorigin="anonymous"></script>
            <script>
                $(function(){
                    var trigger=$('#trigger');
                    var menu=$('nav ul');
                    $(trigger).on('click',function(e){
                        e.preventDefault();
                        menu.slideToggle();
                    });
                    $(window).resize(function(){
                        var w=$(window).width();
                        if(w>320 && menu.is(':hidden')){
                            menu.removeAttr('style');
                        }
                    })
                })
            </script>
        </body>
        </html>