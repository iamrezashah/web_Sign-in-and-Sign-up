<!DOCTYPE html>
<html ng-app>

<head>
    <title>Bootstrap Example</title>
    <meta charset="utf-8">
    <meta name="viewport" content="width=device-width, initial-scale=1">
    <link rel="stylesheet" href="https://maxcdn.bootstrapcdn.com/bootstrap/3.3.7/css/bootstrap.min.css">
    <script src="https://ajax.googleapis.com/ajax/libs/jquery/3.2.1/jquery.min.js"></script>
    <script src="https://maxcdn.bootstrapcdn.com/bootstrap/3.3.7/js/bootstrap.min.js"></script>
    <script src="https://ajax.googleapis.com/ajax/libs/angularjs/1.6.4/angular.min.js"></script>
    <script src="js/wow.min.js"></script>
    <style>
        body {
            background-image: url('../images/bkgrd.PNG');
        }
        
        .main_div {
            padding: 0;
        }
        
        .each_box {
            display: inline-block;
            visibility: hidden;
            float: left;
            width: 50%;
            padding: 20px;
            margin-top: 25px;
            display: none;
        }
        
        #left_box {
            border: 2px solid royalblue;
        }
        
        #right_box {
            float: right;
            border: 2px solid cadetblue;
        }
        
        input[type=text],
        input[type=password] {
            width: 100%;
            padding: 12px 20px;
            margin: 8px 0;
            display: inline-block;
            border: 1px solid #ccc;
            box-sizing: border-box;
        }
        
        button {
            background-color: #4CAF50;
            color: white;
            padding: 14px 20px;
            margin: 8px 0;
            border: none;
            cursor: pointer;
            width: 100%;
        }
        
        button:hover {
            opacity: 0.8;
        }
        
        .btns {
            text-align: center;
            font-size: 1.6em;
            margin-top: 70px;
        }
        
        .btns_in {
            width: 50%;
            padding: 10px 18px;
            background-color: royalblue;
            color: white;
            float: left;
        }
        
        .btns_up {
            width: 50%;
            padding: 10px 18px;
            background-color: cadetblue;
            color: black;
            float: right;
        }
        
        .cancelbtn {
            width: auto;
            padding: 10px 18px;
            background-color: #f44336;
        }
        
        .imgcontainer {
            text-align: center;
            margin: 24px 0 12px 0;
        }
        
        img.avatar {
            text-align: center;
        }
        
        span.psw {
            float: right;
            padding-top: 16px;
        }
        /* Change styles for span and cancel button on extra small screens */
        
        @media screen and (max-width: 300px) {
            span.psw {
                display: block;
                float: none;
            }
            .cancelbtn {
                width: 100%;
            }
        }
    </style>
</head>

<body class="container">
    <div class="btns">
        <button type="button" class="btns_in" id="sign_in">Sign-in</button>
        <button type="button" class="btns_up" id="sign_up">Sign-up</button>
    </div>
    <div class="main_div">
        <div class="each_box wow" id="left_box">
            <form action="#">
                <div class="imgcontainer"> <img src="/images/in.png" alt="Avatar" class="avatar"> </div>
                <div>
                    <label for="uname"><b>Username</b></label>
                    <input type="text" placeholder="Enter Username" name="uname" required>
                    <label for="psw"><b>Password</b></label>
                    <input type="password" placeholder="Enter Password" name="psw" required>
                    <button type="submit">Login</button>
                    <label>
                        <input type="checkbox" checked="checked" name="remember"> Remember me </label>
                </div>
                <div style="background-color:#f1f1f1">
                    <button type="button" class="cancelbtn">Cancel</button> <span class="psw">Forgot <a href="#">password?</a></span> </div>
            </form>
        </div>
        <div class="each_box wow" id="right_box">
            <form action="#">
                <div class="imgcontainer"> <img src="/images/up.png" alt="Avatar" class="avatar"> </div>
                <div>
                    <label for="uname"><b>Username</b></label>
                    <input type="text" placeholder="Enter Username" name="uname" required>
                    <label for="psw"><b>Password</b></label>
                    <input type="password" placeholder="Enter Password" name="psw" required>
                    <button type="submit">Submit</button>
                    <label>
                        <input type="checkbox" checked="checked" name="remember"> Remember me </label>
                </div>
                <div style="background-color:#f1f1f1">
                    <button type="button" class="cancelbtn">Cancel</button>
                </div>
            </form>
        </div>
    </div>
    <br style="clear:both;" />
    <script>
        new WOW().init();
        var btnHight = $('.btns_in').css('height')
        var winHight = window.innerHeight
        $("#sign_in").click(function () {
            $("#right_box").fadeOut(300)
            $("#left_box").fadeToggle(1000)
        });
        $("#sign_up").click(function () {
            $("#left_box").fadeOut(300)
            $("#right_box").fadeToggle(1000)
        });
    </script>
</body>

</html>
