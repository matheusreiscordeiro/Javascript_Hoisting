# Javascript_Hoisting

<br/>

Hoisting é um comportamento no JavaScript em que as declarações de variáveis e funções são movidas para o topo de seu escopo atual antes da execução do código. Isso significa que você pode chamar uma variável ou função antes de declará-la e ainda assim ela será executada corretamente, devido ao hoisting.

No entanto, é importante notar que apenas a declaração da variável ou função é movida para o topo, não a atribuição de valor ou a definição de função.

Aqui estão alguns exemplos de como o hoisting funciona em JavaScript:

<br/>

> Variáveis:

<br/>

```
console.log(x); // undefined
var x = 5;
```

<br/>

Neste exemplo, a variável x é declarada após a chamada console.log(), mas ainda assim não ocorre um erro. Isso acontece porque a declaração da variável x é movida para o topo do escopo atual, deixando-a como undefined no momento em que console.log(x) é chamado.

<br/>

> Funções:

<br/>

```
myFunction(); // "Hello World!"
function myFunction() {
  console.log("Hello World!");
}
```

<br/>

Neste exemplo, a função myFunction() é chamada antes de sua declaração, mas ainda assim é executada corretamente. Isso ocorre porque a declaração da função é movida para o topo do escopo atual antes da execução do código.

No entanto, é importante lembrar que apenas a declaração da função é movida para o topo, não a definição da mesma, como no exemplo abaixo:

<br/>

```
myFunction(); // Erro: myFunction não está definida
var myFunction = function() {
  console.log("Hello World!");
}
```

<br/>

Neste exemplo, myFunction() é chamada antes de sua definição, e como ela foi atribuída a uma variável, não é hoisted para o topo do escopo.
