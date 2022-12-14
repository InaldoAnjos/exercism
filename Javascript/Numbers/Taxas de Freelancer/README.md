# Instruções

Neste exercício, você escreverá um código para ajudar um freelancer a se comunicar com seus clientes sobre os preços de determinados projetos. Você escreverá algumas funções de utilidade para calcular rapidamente os custos para os clientes.

## 1. Calcule a taxa diária dada uma taxa horária

Um cliente entra em contato com o freelancer para perguntar sobre suas taxas. O freelancer explica que eles trabalham **8 horas por dia**. No entanto, o freelancer conhece apenas suas taxas horárias para o projeto. Ajude-os a estimar uma taxa diária dada uma taxa horária.

```dayRate(89);```
```// => 712```

A taxa diária não precisa ser arredondada ou alterada para uma precisão "fixa".

## 2. Calcule o número de dias úteis com um orçamento fixo

Outro dia, um gerente de projeto oferece ao freelancer para trabalhar em um projeto com orçamento fixo. Dado o orçamento fixo e a taxa horária do freelancer, ajude-o a calcular o número de dias que trabalharia até que o orçamento se esgote. O resultado deve ser **arredondado** para o número inteiro mais próximo.

```daysInBudget(20000, 89);```
```// => 28```

## 3. Calcule a taxa de desconto para grandes projetos

Freqüentemente, os clientes do freelancer os contratam para projetos que duram vários meses. Nesses casos, o freelancer decide oferecer um desconto para cada mês inteiro, e os dias restantes são cobrados à taxa diária. **Cada mês tem 22 dias faturáveis**. Ajude-os a estimar o custo de tais projetos, considerando uma taxa horária, o número de dias que o projeto abrange e uma taxa de desconto mensal. O desconto é sempre passado como um número, onde __42%__ se torna __0.42__. O resultado deve ser arredondado para o número inteiro mais próximo.

```priceWithMonthlyDiscount(89, 230, 0.42);```
```// => 97972```