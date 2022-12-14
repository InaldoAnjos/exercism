# Sobre o básico

JavaScript é uma linguagem dinâmica, suportando estilos orientados a objetos, imperativos e declarativos (por exemplo, programação funcional).

# (Re-)Atribuição

Existem algumas maneiras principais de atribuir valores a nomes em JavaScript - usando variáveis ​​ou constantes. No Exercism, as variáveis ​​são sempre escritas em **camelCase**; as constantes são escritas em **SCREAMING_SNAKE_CASE** . Não existe um guia oficial a seguir, e várias empresas e organizações têm vários guias de estilo. Sinta-se à vontade para escrever variáveis ​​da maneira que desejar . A vantagem de escrevê-los da maneira como os exercícios são preparados é que eles serão destacados de forma diferente na interface da Web e na maioria dos IDEs.

As variáveis ​​em JavaScript podem ser definidas usando a palavra-chave ```const```, ```let``` ou ```var```.

Uma variável pode fazer referência a diferentes valores ao longo de seu tempo de vida ao usar ```let``` ou ```var```. Por exemplo, ```myFirstVariable``` pode ser definido e redefinido várias vezes usando o operador de atribuição ```=```:

   ```let myFirstVariable = 1;```
   ```myFirstVariable = 'Some string';```
   ```myFirstVariable = new SomeComplexClass();```

Ao contrário de ```let``` e ```var```, as variáveis ​​definidas com ```const``` só podem ser atribuídas uma vez. Isso é usado para definir constantes em JavaScript.

```const MY_FIRST_CONSTANT = 10;```

``` // Can not be re-assigned.```
```MY_FIRST_CONSTANT = 20;```
```// => TypeError: Assignment to constant variable.```

>💡 Num Exercício de Aprendizagem posterior, é explorada e explicada a diferença entre atribuição/vinculação constante e valor constante .

# Declarações de função

 Em JavaScript, as unidades de funcionalidade são encapsuladas em funções , geralmente agrupando funções no mesmo arquivo se elas estiverem juntas. Essas funções podem receber parâmetros (argumentos) e podem retornar um valor usando a ```return``` palavra-chave. Funções são invocadas usando ```()``` sintaxe.

``` function add(num1, num2) {```
```     return num1 + num2;```
  ```}```

``` add(1, 3);```
```// => 4```

>💡 Em JavaScript existem diversas formas de declarar uma função. Essas outras formas parecem diferentes de usar a ```function``` palavra-chave. A faixa tenta apresentá-los gradualmente, mas se você já os conhece, fique à vontade para usar qualquer um deles. Na maioria dos casos, usar um ou outro não é melhor ou pior.

# Expor a outros arquivos

Para disponibilizar um __function__, uma constante ou uma variável em outros arquivos , eles precisam ser **exportados** usando a __export__ palavra-chave. Outro arquivo pode então **importá-los** usando a __import__ palavra-chave. Isso também é conhecido como sistema de módulos. Um ótimo exemplo é como todos os testes funcionam. Cada exercício possui pelo menos um arquivo, por exemplo __lasagna.js__, que contém a implementação . Além disso, há pelo menos um outro arquivo, por exemplo __lasagna.spec.js__, que contém os testes . Este arquivo importa as entidades públicas (ou seja, exportadas) para testar a implementação:

```// file.js```
```export const MY_VALUE = 10;```

```export function add(num1, num2) {```
  ```return num1 + num2;```
```}```

```// file.spec.js```
```import { MY_VALUE, add } from './file';```

```add(MY_VALUE, 5);```
```// => 15```