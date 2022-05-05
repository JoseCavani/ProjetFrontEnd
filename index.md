<html>
   <head>
  <title>Calculadora</title>
  <style>
    html {  
  display: flex;
  align-items: center;  
  justify-content: center;  
  background-color: gray;
  
}  
input[type=button] {  
  width: 30px;  
  height: 30px;   
  margin: 5px;   
  border :none;
  background: lightblue;  
  font-size: 30px;  
  line-height: 30px;    
  font-weight: 700;  
  color: green;  
  cursor: pointer;    
}  
#display {  
  height: 40px;  
  text-align: center;  
  background-color: white;  
  border: 3px solid black;  
  font-size: 18px;
  color: red;   
     margin-left: auto;
    margin-right: auto;
    display: block;
}  
.title {  
margin-bottom: 10px;  
padding: 5px 0;  
font-size: 40px;  
font-weight: lighter;  
text-align: center;  
color: black;  
font-family: 'Ariel', Arial, Helvetica, sans-serif;  
}  
     
   .allActions{  margin-bottom: 10px;  
padding: 5px 0;  
font-weight: lighter;  
text-align: center;  
     }
  </style>
 
   </head>
   <body>
       <div class="title">Calculadora</div>
    <input type="text" name="Input" Size="15" id="display">
      <div class = "allActions">
       <div class = "actions0">
  <input type="button" value="0" onclick="FuncaoNumeros('0')">
  <input type="button" value="1" onclick="FuncaoNumeros('1')">
  <input type="button" value="2" onclick="FuncaoNumeros('2')">
  <input type="button" value="*" onclick="FuncaoOperador('*')">
</div>
<div class = "actions1">
   <input type="button" value="4" onclick="FuncaoNumeros('4')">
   <input type="button" value="5" onclick="FuncaoNumeros('5')">
   <input type="button" value="6" onclick="FuncaoNumeros('6')">
   <input type="button" value="+" onclick="FuncaoOperador('+')">
  </div>
  <div class = "actions2">
   <input type="button" value="7" onclick="FuncaoNumeros('7')">
   <input type="button" value="8" onclick="FuncaoNumeros('8')">
   <input type="button" value="9" onclick="FuncaoNumeros('9')">
   <input type="button" value="-" onclick="FuncaoOperador('-')">
  </div>
  <div class = "actions4"> 
   <input type="button" value="C" onclick="FuncaoOperador('C')">
   <input type="button" value="," onclick="FuncaoOperador(',')">
   <input type="button" value="/" onclick="FuncaoOperador('/')">
   </div>
   </div>
   
   <script>
     var op = null;
  var FuncaoOperador = function(operador) 
      {
        op = operador;
        if (op == 'C'){
        op = null;
        document.getElementById('display').value = "";
        }
      }


      var FuncaoNumeros = function(value) 
      {
      
        
        if ( op == null)
        document.getElementById('display').value = value;
        else
        var numero2 = value;

        switch(op){
          case '*': 
          document.getElementById('display').value = (document.getElementById('display').value * numero2);
          break;

          case '+' :
          document.getElementById('display').value = (+document.getElementById('display').value + +numero2);
          break;

          case '-' :
          document.getElementById('display').value = (document.getElementById('display').value - numero2);
          break;

          case '/' :
          document.getElementById('display').value = (document.getElementById('display').value / numero2);
          break;

          case ',' :
          document.getElementById('display').value = (+document.getElementById('display').value + +(numero2/10)).toFixed(2);
          break;
        }
    
      }
   </script>
   </body>
</html>   
