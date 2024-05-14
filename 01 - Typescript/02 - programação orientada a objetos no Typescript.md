## Resumo

## Exemplos

## Anotações
### O que é POO?
**Programação Orientada a Objetos - POO**, é um paradigma de estruturação de dados, que parte do conceito de "objetos": Uma capsula de dados que contém, em si, atributos e métodos.
No TypeScript, bem como no JavaScript, um objeto é representado por um bloco de código dentro de uma variável.
>[!example] Objeto simples
>```ts
 >const objeto = {
>	 idade : 1,
>	 nome : "Stallone"
 >}
> ```

Um objeto é, essencialmente, um conjunto de pares "**chave-valor**", onde a chave é uma variável que representará a informação a nível de chamada, e o valor é o dado em si
> [!example] Exemplo de objeto com método:
>```ts
>const meuMetodo = {
>	idade : 1,
>	nome : "Stallone",
>	metodo() => {
>		console.log(`Nome: ${this.nome}\nIdade: ${this.idade}`)
>	}
>}
>```

### Classes
Dentro do paradigma de POO, existe o conceito de "**classe**", um objeto especial que serve para "construir" outros objetos, servindo de molde.

>[!info] Uma classe é representada desta forma:
>```ts
>class Animal {
>	name: string;
>	age: number;
>
>	constructor(name:string, age:number){
>		this.name = name;
>		this.age = age;
>	}
>	
>	sayMyName = () => {
>		console.log(`My name is: ${this.name}, and I am ${this.age} years old`)
>	}
>}
>```

Uma classe por si só não gera valores ou elementos executáveis, ela serve apenas como um **molde** de um objeto que conterá esses valores.

Para modelar um objeto, basta utilizar o operador especial "**new**", desta forma:
>[!example] Instanciando uma classe
>```ts
>const cat = new Animal("gatinho", 4)
>```
 
E para utilizá-la agora, é necessário apenas "chamar" as propriedades através do operador " **.** " (ponto)
>[!example] Exemplo
>```ts
>const cat = new Animal("gatinho", 4);
>
>console.log(cat.name) // "gatinho"
>console.log(cat.age) // 4
>
>cat.sayMyName() // "My name is: gadinho, and I am 4 years old'
>```



