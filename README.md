#Calculo do IMC
<!DOCTYPE html>
<html>
  <head>
  	<meta charset="utf-8">
    <script>
      function calcularIMC(){
      		function carregarNome(){
				    var nome = document.getElementById("nomeId").value;
				    return nome;
			    }	
        formulario = document.getElementById("formulario");		
        var kilos = parseInt(formulario.kilos.value);
		    var metros = parseInt(formulario.metros.value);
		    var centimetros = parseInt(formulario.centimetros.value);
        var altura = ((metros * 100) + centimetros) / 100;
        var imc = kilos / (altura * altura);
        formulario.imc.value = imc.toFixed(2);
        if(imc <= 20){
			    alert(""+carregarNome()+" você está abaixo do Peso!");
		    }else if (imc >= 20 && imc <= 25){
			    alert(""+carregarNome()+" você está no peso Ideal!");
		    }else if (imc > 25 && imc <= 30){
			    alert(""+carregarNome()+"  você está com Sobrepeso!");
		    }else if (imc > 30 && imc <= 35){
			    alert(""+carregarNome()+" você está com Obesidade Moderada!");
		    }else if (imc > 35 && imc <= 40){
		      	alert(""+carregarNome()+" você está com Obesidade Severa!");
		    }else if (imc > 40 && imc <= 50){
			    alert(""+carregarNome()+" você está com Obesidade Morbida!");
		    }else {
			    alert(""+carregarNome()+" você está com Super Obesidade!");
		    }
     }
    </script>
    <style type="text/css">
    	table#tab{
		    border:1px solid #606060;
		    box-shadow: 2px 2px 2px rgba(0,0,0,.5);
		    border-spacing: 0px;
		    margin-top: 10px;
		  }
    </style>
  </head>
  <body>
     <form id="formulario">
      <label for="nome">Nome:</label>
      <input type="text" name="nome" id="nomeId"  placeholder=" Informe seu Nome " onchange="carregarNome()">
      <label for="kilos">Kilos:</label>
      <input type="text" name="kilos" id="kilo" placeholder=" Informe seus Kilos">
      <label for="metros">Metros:</label>
      <input type="text" name="metros" id="metro" placeholder=" Informe seus Metros">
      <label for="centimetros">Cm:</label>
      <input type="text" name="centimetros" id="centimetro" placeholder=" Informe seus Centímetros">
      <label for="imc">IMC:</label>
      <input type="text" name="imc" disabled="disabled" id="im" placeholder=" Aguarde...">
      <a href="#" onclick="calcularIMC();"> Calcular</a>
    </form>
    <table id="tab">
      <tr><td class="colEsq">IMC</td><td class="colDir">Classificação</td></tr>
      <tr><td>Abaixo de 20</td><td>Abaixo do Peso</td></tr>
      <tr><td>20 a 25</td><td>Peso Ideal</td></tr>
      <tr><td>25 a 30</td><td>Sobrepeso</td></tr>
      <tr><td>30 a 35</td><td>Obesidade Moderada</td></tr>
      <tr><td>35 a 40</td><td>Obesidade Severa</td></tr>
      <tr><td>40 a 50</td><td>Obesidade Mórbida</td></tr>
      <tr><td>Acima de 50</td><td>Super Obesidade</td></tr>
    </table><br>
 <body>
</html
