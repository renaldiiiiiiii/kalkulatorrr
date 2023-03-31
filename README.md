# kalkulatorrr
<!DOCTYPE html>
<html>
<head>
    <title>calculator renaldi</title>
    <link rel="stylesheet" type="text/css" href="style.css">
    <script type="text/javascript">
        function insert(num) {
            document.form.textView.value = document.form.textView.value+num;
            // body...
        }

        function c(){
            document.form.textView.value = "";
        }

        function del(){
            var x = document.form.textView.value;
            document.form.textView.value = x.substring(0,x.length-1)
        }

        function equal(){
            var x = document.form.textView.value;
            if(x == ""){
                alert("MASUKIN ANGKA NYA DULU BROOO");
            }

            if(x){
                document.form.textView.value = eval(x);
            }
            // body...
        }
    </script>
</head>
<body>
    <div class="wrapper">
        <div class="calculator">
            <form name="form">
                <input type="text" id="result" readonly class="textView" name="textView">
          </form>
                <table>
                    <tr>
                        
                    <td><input type="button" class="button" value="C" onclick="c()"></td>
                    <td><input type="button" class="button" value="del" onclick="del()"></td>
                    <td><input type="button" class="button" value="+" onclick="insert('+')"></td>
                    <td><input type="button" class="button" value="&#247" onclick="insert('/')"></td>
                </tr>
                <tr>
                    <td><input type="button" class="button" value="7" onclick="insert(7)"></td>
                    <td><input type="button" class="button" value="8" onclick="insert(8)"></td>
                    <td><input type="button" class="button" value="9" onclick="insert(9)"></td>
                    <td><input type="button" class="button" value="*" onclick="insert('*')"></td>
                </tr>
                <tr>
                    <td><input type="button" class="button" value="4" onclick="insert(4)"></td>
                    <td><input type="button" class="button" value="5" onclick="insert(5)"></td>
                    <td><input type="button" class="button" value="6" onclick="insert(6)"></td>
                    <td><input type="button" class="button" value="-" onclick="insert('-')"></td>
                </tr>
                <tr>
                    <td><input type="button" class="button" value="1" onclick="i
                    nsert(1)"></td>
                    <td><input type="button" class="button" value="2" onclick="insert(2)"></td>
                    <td><input type="button" class="button" value="3" onclick="insert(3)"></td>
                    <td rowspan="2"><input type="button" class="button equal" value="=" onclick="equal()"></td>
                </tr>
                <tr>
                    <td><input type="button" class="button" value="," onclick="insert(',')"></td>
                    <td colspan="2"><input type="button" class="button zero" value="0" onclick="insert('0')"></td>
                    
                </tr>
               <table>
            </div>
            </div>
            </div>
</body>
</html>


*{
            padding: 0;
            margin: 0;
        }

        body{
          background-color: purple;
          background-image: white;
        }
        .wrapper{
            position: absolute;
            top: 50%;
            left: 50%;
            transform: translate(-50%,-50%);
        }

        .calculator{
            background: black;
            padding: 3px;
            box-shadow: blue;
            position: relative;
            height: auto;
            width: auto;
            border-radius: 20px;
            padding: 10px;

        }

        .textView{
            background-color: white;
            width: 345px;
            font-weight: 35px;
            font-weight: bold;
            padding: 5px;
            font-family: cooper black;
            font-size: 28px;
            text-align: right;
            color: black;
            background-color: white;
            border-width: 10px;
            height: 80px;
            border-radius: 15px;
            border: none;
            border-radius: 50px;

        }

        .button{
            width: 80px;
            height: 70px;
            font-size: 23px;
            font-family: cooper black;
            margin: 4px;
            border-color: white;
            border-width: 0px;
            cursor: pointer;
            color: white ;
            box-shadow: purple;
            background-color: black;
            border-radius: 50px;

        }

        .equal{
            height: 149px;
        }

        .equal:hover{
            background-color: cyan;
            color: black;
        }

        .zero{
            width: 170px;
        }

        .button c{
            background-color: red;
        }
