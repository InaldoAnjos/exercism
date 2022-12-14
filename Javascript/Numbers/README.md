# Sobre números

Muitas linguagens de programação possuem tipos numéricos específicos para representar diferentes tipos de números, mas o JavaScript possui apenas dois:

* __number__: um tipo de dados numéricos no formato de ponto flutuante de 64 bits de precisão dupla (IEEE 754). Exemplos são __-6, -2.4, 0, 0.1, 1, 3.14, 16.984025, 25, 976 e 1024.0.500000__
* __bigint__: um tipo de dado numérico que pode representar números inteiros no formato de precisão arbitrária. Exemplos são __-12n, 0n, 4n e 9007199254740991n.__

Se você precisar de precisão arbitrária ou trabalhar com números extremamente grandes, use o __bigint__. Caso contrário, o tipo __number__ provavelmente é a melhor opção.

# arredondamento

Existe um objeto global interno chamado __Math__ que fornece várias **funções de arredondamento** . Por exemplo, você pode arredondar para baixo (__floor__) ou arredondar para cima (__ceil__) números decimais para os números inteiros mais próximos.

```Math.floor(234.34);```
```// => 234```

```Math.ceil(234.34);``` 
```// => 235```