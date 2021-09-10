<!DOCTYPE html>
<html lang="pt-br">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Calculadora Honorário</title>
    <script>
        
    
        function calcular(){
            var economia = document.getElementById("economia");
            var contabil = parseFloat(document.getElementById("valorContabil").value.replace(/\./g,"").replace(",","."))
            
            
                if(contabil > 0){
                    var plano = parseInt(document.getElementById("plano").value);
                    var planoVisual = document.getElementById("plano"); // variavel para usar com o innerHMTL
                

                    var selectRegime = document.getElementById("regime");
                    var selectServico = document.getElementById("servico");
                
                
                    var opcaoReg = selectRegime.options[selectRegime.selectedIndex].value;
                    var opcaoSer = selectServico.options[selectServico.selectedIndex].value;


                    var calcularValorSocio = calcularSocio();
                    var calcularValorFun = calculcarFuncionario();
                

                
                        if(opcaoReg == 1 && opcaoSer == 1){
                            if(contabil < 379.99){
                                economia.innerHTML = "Entre em contato conosco, temos uma oferta especial para você =)" ;
                                var mensalidade = 380;
                                planoVisual.innerHTML = "R$" + mensalidade.toFixed(2).replace(/\B(?=(\d{3})+(?!\d))/g, ".") + " /Mês";
                                
                            }else{
                                plano = calcularValorSocio +calcularValorFun  + 380 ;
                                var converterNumero = plano.toFixed(2);
                                planoVisual.innerHTML = "R$" + converterNumero.replace(/\B(?=(\d{3})+(?!\d))/g, ".") + " /Mês";

                                let custoTotal = contabil * 12;
                                let planoEconomia = plano * 12;
                                let economiaTotal = custoTotal - planoEconomia;
                                var converterNumero1 = economiaTotal.toFixed(2);
                                economia.innerHTML = "R$ " + converterNumero1.replace(/\B(?=(\d{3})+(?!\d))/g, ",") + " /Ano";
                                
                                
                            }

                        }if(opcaoReg == 1 && opcaoSer == 2){
                            if(contabil < 166){
                                economia.innerHTML = "Entre em contato conosco, temos uma oferta especial para você =)" ;
                                var mensalidade = 166;
                                planoVisual.innerHTML = "R$" + mensalidade.toFixed(2).replace(/\B(?=(\d{3})+(?!\d))/g, ".") + " /Mês";
                            }else{
                                plano = calcularValorSocio +calcularValorFun + 166 ;
                                var converterNumero = plano.toFixed(2);
                                planoVisual.innerHTML = "R$" + converterNumero.replace(/\B(?=(\d{3})+(?!\d))/g, ".") + " /Mês";

                                let custoTotal = contabil * 12;
                                let planoEconomia = plano * 12;
                                let economiaTotal = custoTotal - planoEconomia;
                                var converterNumero1 = economiaTotal.toFixed(2);
                                economia.innerHTML = "R$ " + converterNumero1.replace(/\B(?=(\d{3})+(?!\d))/g, ",") + " /Ano";

                            }

                        }if(opcaoReg == 1 && opcaoSer == 3){
                            if(contabil < 379.99){
                                economia.innerHTML = "Entre em contato conosco, temos uma oferta especial para você =)" ;
                                var mensalidade = 380;
                                planoVisual.innerHTML = "R$" + mensalidade.toFixed(2).replace(/\B(?=(\d{3})+(?!\d))/g, ".") + " /Mês";
                            }else{
                                plano = calcularValorSocio +calcularValorFun  + 380 ;
                                var converterNumero = plano.toFixed(2);
                                planoVisual.innerHTML = "R$" + converterNumero.replace(/\B(?=(\d{3})+(?!\d))/g, ".") + " /Mês";

                                let custoTotal = contabil * 12;
                                let planoEconomia = plano * 12;
                                let economiaTotal = custoTotal - planoEconomia;
                                var converterNumero1 = economiaTotal.toFixed(2);
                                economia.innerHTML = "R$ " + converterNumero1.replace(/\B(?=(\d{3})+(?!\d))/g, ",") + " /Ano";

                            }

                        }if(opcaoReg==2 && opcaoSer ==1 ){
                            if(contabil < 219.89){
                                economia.innerHTML = "Entre em contato conosco, temos uma oferta especial para você =)";
                                var mensalidade = 219.90;
                                planoVisual.innerHTML = "R$" + mensalidade.toFixed(2).replace(/\B(?=(\d{3})+(?!\d))/g, ".") + " /Mês";
                            }else{
                                plano = calcularValorSocio +calcularValorFun  + 219.90 ;
                                var converterNumero = plano.toFixed(2);
                                planoVisual.innerHTML = "R$" + converterNumero.replace(/\B(?=(\d{3})+(?!\d))/g, ".") + " /Mês";

                                let custoTotal = contabil * 12;
                                let planoEconomia = plano * 12;
                                let economiaTotal = custoTotal - planoEconomia;
                                var converterNumero1 = economiaTotal.toFixed(2);
                                economia.innerHTML = "R$ " + converterNumero1.replace(/\B(?=(\d{3})+(?!\d))/g, ",") + " /Ano";

                            }
                            

                        }if(opcaoReg==2 && opcaoSer ==2 ){
                            if(contabil < 219.89){
                                economia.innerHTML = "Entre em contato conosco, temos uma oferta especial para você =)";
                                var mensalidade = 219.90;
                                planoVisual.innerHTML = "R$" + mensalidade.toFixed(2).replace(/\B(?=(\d{3})+(?!\d))/g, ".") + " /Mês";
                            }else{
                                plano = calcularValorSocio +calcularValorFun  + 219.90 ;
                                var converterNumero = plano.toFixed(2);
                                planoVisual.innerHTML = "R$" + converterNumero.replace(/\B(?=(\d{3})+(?!\d))/g, ".") + " /Mês";

                                let custoTotal = contabil * 12;
                                let planoEconomia = plano * 12;
                                let economiaTotal = custoTotal - planoEconomia;
                                var converterNumero1 = economiaTotal.toFixed(2);
                                economia.innerHTML = "R$ " + converterNumero1.replace(/\B(?=(\d{3})+(?!\d))/g, ",") + " /Ano";

                            }
                            
                        }if(opcaoReg==2 && opcaoSer ==3 ){
                            if(contabil < 219.89){
                                economia.innerHTML = "Entre em contato conosco, temos uma oferta especial para você =)";
                                var mensalidade = 219.90;
                                planoVisual.innerHTML = "R$" + mensalidade.toFixed(2).replace(/\B(?=(\d{3})+(?!\d))/g, ".") + " /Mês";
                            }else{
                                plano = calcularValorSocio +calcularValorFun  + 219.90 ;
                                var converterNumero = plano.toFixed(2);
                                planoVisual.innerHTML = "R$" + converterNumero.replace(/\B(?=(\d{3})+(?!\d))/g, ".") + " /Mês";

                                let custoTotal = contabil * 12;
                                let planoEconomia = plano * 12;
                                let economiaTotal = custoTotal - planoEconomia;
                                var converterNumero1 = economiaTotal.toFixed(2);
                                economia.innerHTML = "R$ " + converterNumero1.replace(/\B(?=(\d{3})+(?!\d))/g, ",") + " /Ano";

                            }
                            
                        }if(opcaoReg==3 && opcaoSer ==1 ){
                            if(contabil < 54.89){
                                economia.innerHTML = "Entre em contato conosco, temos uma oferta especial para você =)";
                                var mensalidade = 54.90;
                                planoVisual.innerHTML = "R$" + mensalidade.toFixed(2).replace(/\B(?=(\d{3})+(?!\d))/g, ".") + " /Mês";
                            }else{
                                plano = calcularValorSocio +calcularValorFun  + 54.90 ;
                                var converterNumero = plano.toFixed(2);
                                planoVisual.innerHTML = "R$" + converterNumero.replace(/\B(?=(\d{3})+(?!\d))/g, ".") + " /Mês";

                                let custoTotal = contabil * 12;
                                let planoEconomia = plano * 12;
                                let economiaTotal = custoTotal - planoEconomia;
                                var converterNumero1 = economiaTotal.toFixed(2);
                                economia.innerHTML = "R$ " + converterNumero1.replace(/\B(?=(\d{3})+(?!\d))/g, ",") + " /Ano";

                            }
                        }if(opcaoReg==3 && opcaoSer ==2 ){
                            if(contabil < 54.89){
                                economia.innerHTML = "Entre em contato conosco, temos uma oferta especial para você =)";
                                var mensalidade = 54.90;
                                planoVisual.innerHTML = "R$" + mensalidade.toFixed(2).replace(/\B(?=(\d{3})+(?!\d))/g, ".") + " /Mês";
                            }else{
                                plano = calcularValorSocio +calcularValorFun  + 54.90 ;
                                var converterNumero = plano.toFixed(2);
                                planoVisual.innerHTML = "R$" + converterNumero.replace(/\B(?=(\d{3})+(?!\d))/g, ".") + " /Mês";

                                let custoTotal = contabil * 12;
                                let planoEconomia = plano * 12;
                                let economiaTotal = custoTotal - planoEconomia;
                                var converterNumero1 = economiaTotal.toFixed(2);
                                economia.innerHTML = "R$ " + converterNumero1.replace(/\B(?=(\d{3})+(?!\d))/g, ",") + " /Ano";

                            }
                            
                        }if(opcaoReg==3 && opcaoSer ==3 ){
                            if(contabil < 54.89){
                                economia.innerHTML = "Entre em contato conosco, temos uma oferta especial para você =)";
                                var mensalidade = 54.90;
                                planoVisual.innerHTML = "R$" + mensalidade.toFixed(2).replace(/\B(?=(\d{3})+(?!\d))/g, ".") + " /Mês";
                            }else{
                                plano = calcularValorSocio +calcularValorFun  + 54.90 ;
                                var converterNumero = plano.toFixed(2);
                                planoVisual.innerHTML = "R$" + converterNumero.replace(/\B(?=(\d{3})+(?!\d))/g, ".") + " /Mês";

                                let custoTotal = contabil * 12;
                                let planoEconomia = plano * 12;
                                let economiaTotal = custoTotal - planoEconomia;
                                var converterNumero1 = economiaTotal.toFixed(2);
                                economia.innerHTML = "R$ " + converterNumero1.replace(/\B(?=(\d{3})+(?!\d))/g, ",") + " /Ano";

                            }
                        }
               }else{
                   alert("Por favor, coloque o valor pago na sua contabilidade.")
               }
            }
              
                
        
            function calcularSocio(){
                var selectSocio = document.getElementById("socio");
                var opcaoValor = selectSocio.options[selectSocio.selectedIndex].value // pegar valor dos selects

                if(opcaoValor ==0){
                    return 0;
                }else{
                    var valorSoc = opcaoValor * 28.90;
                    return valorSoc;
                }   
                
            }
        

            function calculcarFuncionario(){
                var selectFun = document.getElementById("funcionario");
                var opcaoFun = selectFun.options[selectFun.selectedIndex].value;

                if(opcaoFun !=""){
                    var valorFun = opcaoFun * 28.90;
                    return valorFun;
                }else{
                    return 0;
                }
            }



    </script>
    <style>
        
        .corpo{
            margin-top: 80px;
            color: #FF7B0D ;
           
            
            
        }

        .mostrar-valores{
            display: flex;
            align-items:center;
            flex-direction: row;
            margin-left: 300px;
            margin-right: 300px;
            box-sizing: border-box;
            border: solid 1px gainsboro;
            border-radius: 15px;
            
        }
        p{
            color: #FF7B0D;
        }
        .texto-calc{
            margin-left: 510px;
            font-family: Arial, Helvetica, sans-serif;
            font-size: 20px;
        }

        select{
            border: none;
            -webkit-appearance: none;
            -ms-appearance:none;
            -moz-appearance: none;
            appearance: none;
            background:  #f2f2f2;
            padding: 5px;
            border-radius: 10px;
            width: 150px;
            outline: none;
            box-shadow: 5px 5px 10px gray;
        }

        input{
            border: none;
            -webkit-appearance: none;
            -ms-appearance:none;
            -moz-appearance: none;
            appearance: none;
            background:  #f2f2f2;
            padding: 5px;
            border-radius: 10px;
            width: 150px;
            outline: none;
            box-shadow: 5px 5px 10px gray;
        }

        .economia{
            flex: 0.5;
            text-align: center;
            margin: 5px;
            color: #FF7B0D ;
            font-family: Arial, Helvetica, sans-serif;
            font-size: 15px;
            
        }
        .plano{
            flex: 0.4;
            text-align: center;
            margin: 5px;
            color: #FF7B0D ;
            font-family: Arial, Helvetica, sans-serif;
            font-size: 15px;
        }


        .entradas{
            
            display: flexbox;
            
            
        }
        .entrada-linha1{
            
            display: flex;
            
            padding-left: 250px;
            padding-top: 10px;
            padding-bottom: 10px;
        }
        .entrada-linha2{
            
            display: flex;
            padding-top: 10px;
            padding-left: 300px;
            padding-bottom: 10px;
            
                  
        }
        .entrada-linha3{
            display: flex;
            
            padding-top: 10px;
            padding-left: 300px;
            padding-bottom: 10px;
        }
        label{
            padding: 10px;
            
            text-align: center;
            font-family: Arial, Helvetica, sans-serif;
            font-size: 15px;
        }
        .entrada-linha4{
         display: flex;
         
         padding-top: 10px;
         padding-left: 300px;
         padding-bottom: 10px;
        }
        .entrada-linha5{
            display: flex;
            padding-top: 30px;
            padding-left: 550px;
            padding-bottom: 10px;
        }

        .btn-calcular{
            padding: 10px;
            margin-top: 3px;
            margin-left: 25px;
            margin-bottom: 20px;
            border-radius: 8px;
            background-color: white ;
            border-color: black;
            color: #FF7B0D;
        }

        .btn-calcular:active, .btn-novo:active{
            background-color: rgb(246, 240, 255);
            box-shadow: 0 5px #666;
            transform: translateY(4px);
}
    </style>
</head>
<body class="corpo">
    <div>
        <p class="texto-calc">Calculadora Honorário Otimizzei</p>
    </div> 
    <div class="mostrar-valores">
        <div class="economia">
            <p class="texto da economia">Você irá economizar: </p>
            <p class="valor da economia" id="economia">R$</p>
        </div>
        <div class="plano">
            <p class="texto do plano">Sua mensalidade será: </p>
            <p class="valor do plano" id="plano">R$</p>
        </div>
    </div>
    <div class="entradas">
        
        <div class="entrada-linha2">
            <div class="entrada-coluna">
                <label>Qual o serviço?</label>
                <select id="servico">
                    <option value="1">Comércio</option>
                    <option value="2">Serviço</option>
                    <option value="3">Comércio e Serviço</option>
                </select>
            </div>
            <div class="entrada-coluna">
                <label> Qual o seu tipo de regime?</label>
                <select id="regime">
                    <option value="1">Simples</option>
                    <option value="2">Presumido</option>
                    <option value="3">MEI</option>
                </select>
            </div>
            
            
        </div>
        <div class="entrada-linha3">
            <div class="entrada-coluna">
                <label>Quantos sócios?</label>
                <select id="socio">
                    <option value="0">Sou o único dono</option>
                    <option value="1">1</option>
                    <option value="2">2</option>
                    <option value="3">3</option>
                    <option value="4">4</option>
                    <option value="5">5</option>
                    <option value="6">6</option>
                    <option value="7">7</option>
                    <option value="8">8</option>
                    <option value="9">9</option>
                    <option value="10">10</option>
                    <option value="11">Mais sócios</option>
                </select>
        </div>
            
            <div class="entrada-coluna">
                <label>Qual faturamento mensal?</label>
                <select>
                    <option value="0">De R$ 0,00 até R$50.000,00</option>
                    <option value="50000">R$50.000.01 até R$100.000,00</option>
                    <option value="100000">R$100.000,01 até R$150.000,00</option>
                    <option value="150000">R%150.000,01 até R$200.000,00</option>
                    <option value="200000">R$200.000,01 até R$250.000,00</option>
                    <option value="250000">R$250.000,01 até R$300.000,00</option>
                    <option value="300000">R$300.000,01 até R$350.000,00</option>
                    <option value="350000">R$350.000,01 até R$400.000,00</option>
                </select>
            </div>
            
        </div>
        <div class="entrada-linha4">
            <div class="entrada-coluna">
                <label>Quantos funcionários?</label>
                <select id="funcionario">
                    <option value=''>Sem funcionários</option>
                    <option value="1">1</option>
                    <option value="2">2</option>
                    <option value="3">3</option>
                    <option value="4">4</option>
                    <option value="5">5</option>
                    <option value="6">6</option>
                    <option value="7">7</option>
                    <option value="8">8</option>
                    <option value="9">9</option>
                    <option value="10">10</option>
                    <option value="11">11</option>
                    <option value="12">12</option>
                    <option value="13">13</option>
                    <option value="14">14</option>
                    <option value="15">15</option>
                    <option value="16">16</option>
                    <option value="17">17</option>
                    <option value="18">18</option>
                    <option value="19">19</option>
                    <option value="20">Mais funcionários</option>
                </select>
            </div>
            <div class="entrada-coluna">
                <label>Quanto paga de contabilidade?</label>
                <input type="text"   id="valorContabil" >
            </div>
            
        </div>
        <div class="entrada-linha5">
            <button class="btn-calcular" title="Calcular minha economia" onclick="calcular()">Calcular minha economia</button>
        </div>
    </div>
</body>
</html>
