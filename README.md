<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Document</title>
    <style>
        *{
            padding: 0;
            margin: 0;
            font-family: cursive;
        }
        body{
            position: absolute;
            width: 100%;
            height:  100vh;
            display: flex;
            justify-content: center;
            align-items: center;
            background: #fff;
        }
        h1{
            text-transform: uppercase;
            font-weight: 800;
            font-size: 19vw;
            color: #000;
            text-shadow: 1px 1px 10px #999;
        }
        .wrapper{
            position: absolute;
            width: 100%;
            height: 100vh;
             background: rgba(0,55,0,.6);
            perspective: 550px;
        }
        .ink{
            position: absolute;
            width: 50px;
            height: 50px;
            border: 10px solid;
            box-shadow: 2px 2px 10px 10px #009900;
            border-radius: 50%;
            transition: 5s;
            z-index: -1;
            transform: rotate(20deg);
        }
    </style>
</head>
<body>
   
    <div id="wrapper"><h1>Bubbles</h1></div>
    
    <script type="text/javascript">
        let wrapper = document.getElementById('wrapper');
        const circle = 50;
            
          for(let i=0; i < circle; i++)
            {
                let div = document.createElement('div');
                div.classList = 'ink';
                wrapper.appendChild(div);
            }
        
        let ink = document.getElementsByClassName('ink');
       
           setInterval(function(){ 
               for(let i=0; i < ink.length; i++){
                ink[i].style.top = Math.floor(Math.random() * 90) + 'vh';
                ink[i].style.left = Math.floor(Math.random() * 90) + 'vw';
            }
           },2000);  
    
    
        
    </script>
</body>
</html>
