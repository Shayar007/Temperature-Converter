# Temperature-Converter
Temperature Converter is  used to convert temperature in celcius to fahrenheit and vice versa



<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Temperature Converter</title>
    <style>
        body{
            padding: 50px 100px;
        }
        h1{
            text-align: center;
        }
        #container{
            text-align: center;
            background-color: #1abc9c;
            padding: 50px;
        }
        .input-div{
            display: inline-block;
        }
        .inp{
            padding: 5px 10px;
            margin: 10px;
            font-size: 35px;
            font-weight: bold;
            width: 250px;
            text-align: center;
        }
        label{
            font-size: 25px;

            color: black;
        }
    </style>
</head>
<body>
    <h1>Temperature Converter</h1>
    <div id="container">
        <div class="input-div">
            <label >Celcius</label><br>
            <input type="number" value="0" id="cel" class="inp"> 

        </div>
        <div class="input-div">
            <label >Fahrenheit</label><br>
            <input type="number" value="32" id="Fah" class="inp">
        </div>
    </div>
    <script>
        var cel = document.getElementById("cel");
        var Fah = document.getElementById("Fah");

        cel.addEventListener('input', function(){
            let c = this.value;
            let f = (c * 9/5) + 32;
            if(!Number.isInteger(f)){
                f = f.toFixed(4);
            }
            Fah.value = f;
        });
        Fah.addEventListener('input', function(){
           let f =  this .value;
           let c =  (f - 32)* 5/9;
           if(!Number.isInteger(f)){
                c = c.toFixed(4);
            }
           cel.value = c;
        });
    </script>
</body>
</html>
