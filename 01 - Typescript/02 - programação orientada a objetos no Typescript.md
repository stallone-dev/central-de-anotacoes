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
 