![Easynvest](https://camo.githubusercontent.com/c4ee611d69893fec43b903eb88a444530eaf8e7f/68747470733a2f2f7777772e656173796e766573742e636f6d2e62722f66617669636f6e2e69636f)

# Teste de Android Developer Easynvest
Este teste é apresentado aos candidatos as vagas de Android Developer para avaliar os quesitos técnicos.

### O Desafio

Seu objetivo é criar um app com duas telas, uma que exibe um formulário e outra que exibe o resultado de uma API.

### Telas

(ADICIONAR SCREENSHOT DAS TELAS)
![input](./images/input.png)
![result](./images/result.png)

Para o desenho das telas, não precisa se preocupar com a interface na horizontal;

## Consumindo o serviço de cálculo
A API que calcula o os valores futuros se encontram em [outro projeto Open Source, aqui](https://github.com/easynvest/api-simulator-calc). Abaixo segue algumas informações sobre como utilizamos esse serviço no nosso simulador.

 - **URL**: https://easynvestsimulatorcalcapi.azurewebsites.net/calculator/simulate
 - **Method**: GET
 - **URL Params**:
    ```javascript
        investedAmount = 32323.0                 // Valor a investir em reais
        index = "CDI"                            // Índice, por enquanto só CDI disponível
        rate = 123                               // Percentual do papel
        isTaxFree = false                        // Isento de IR, por enquanto só falso
        maturityDate = "2023-03-03"              // Data do vencimento, no formato ano-mes-dia
    
    ```
 - **Response**
    ```javascript
    {
        "investmentParameter": {
            "investedAmount": 32323.0,                      // O valor a ser investido
            "yearlyInterestRate": 9.5512,                   // Rentabilidade anual
            "maturityTotalDays": 1981,                      // Dias corridos
            "maturityBusinessDays": 1409,                   // Dias úteis
            "maturityDate": "2023-03-03T00:00:00",          // Data de vencimento
            "rate": 123.0,                                  // Percentual do papel
            "isTaxFree": false                              // Isento de IR
        },
        "grossAmount": 60528.20,                            // Valor bruto do investimento
        "taxesAmount": 4230.78,                             // Valor do IR
        "netAmount": 56297.42,                              // Valor líquido
        "grossAmountProfit": 28205.20,                      // Rentabilidade bruta
        "netAmountProfit": 23974.42,                        // Rentabilidade líquida
        "annualGrossRateProfit": 87.26,                     // Rentabilidade bruta anual
        "monthlyGrossRateProfit": 0.76,                     // Rentabilidade bruta mensal
        "dailyGrossRateProfit": 0.000445330025305748,       // Rentabilidade bruta diária
        "taxesRate": 15.0,                                  // Faixa do IR (%)
        "rateProfit": 9.5512,                               // Rentabilidade no período
        "annualNetRateProfit": 74.17                        // Rentabilidade líquida anual
    }
    ```

### Pré-requisitos: 
 - Versão mínima do SDK: 16
 - Tela deve ajustar em devices menores.

### Plus:
 - Utilizar Kotlin;
 - Construir layouts com Constraints.

### O que esperamos:
 - Testes, no mínimo testes unitários;
 - Padrão de Projeto e boas práticas de Orientação a Objetos. 


