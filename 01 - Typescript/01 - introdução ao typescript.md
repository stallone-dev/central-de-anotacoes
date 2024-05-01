#typescript

## Resumo do módulo

## Exemplos

## Anotações
### Professora
> [!note] [Nathally Souza](github.com/nathyts)
 > Dev plena Itaú
> LGBTQIA+
> 10 anos de experiência 

> [!abstract] Objetivo geral
> Conhecer a sintaxe do Typescript + conceitos de OPP

### Etapa 1 - O que é typescript
> Typescript é um [[superset]] do Javacript, o qual adiciona funcionalidade extras que permitem um desenvolvimento mais fluido, através de ferramentas como tipagem estática, Generics e linting otimizado.
> ![[superset_typescript.excalidraw|400]]

#### Instalação básica 
Para o ambiente **NodeJS** (com o **Vs Code**), basta utilizar o comando: 
- `npm i -g typescript` -> Instalar globalmente o typescript
- `npm i -D typescript` -> Instalar localmente como dependência de desenvolvimento
Os arquivos do typescript terminam em `.ts` e depende de transpilar o código para javascript puro através do comando `npx tsc app.ts` e em seguida executar o novo arquivo `app.js`.

>[!tip] Executar instantaneamente
>É possível executar o arquivo `.ts` diretamente através da biblioteca "**tsx**"
>- `npm i -D tsx` -> Instalar biblioteca
>- `npx tsx app.ts` -> Executar arquivo

#### Uso básico
Comparando funções de **soma**:
```js
const soma = ( n1, n2 ) => { console.log( n1 + n2 ) }
soma(11, 22) // output: 33
soma("11",22) // output: 1122
soma("abc", "def") // output: abcdef
```

```ts
const soma = ( n1:number, n2:number ) => { console.log( n1 + n2 ) }
soma(11, 22) // output: 33
soma("11", 22) // output: TIPO INCORRETO (não compila)
soma("abc", "def")  // output: TIPO INCORRETO (não compila)
```

### Etapa 2 - Fundamentos e sintaxe

#### Sintaxe básica - Tipos primitivos
No Typescript existe a definição de tipos estáticos, que são representados através da sintaxe:`[variável] : [tipo]`, onde uma variável passa a ter um tipo estático que deve ser respeitado durante o desenvolvimento
> [!warning] Observação
> Essa restrição de tipo só existe, **de fato**, durante o desenvolvimento, após o código ser compilado essa sintaxe é excluída e o JS volta ao seu funcionamento natural

##### Tipos primitivos que o TS considera:

| Tipo / Sintaxxe                  | Descrição                         | Exemplos                    |
| -------------------------------- | --------------------------------- | --------------------------- |
| String / `[variável] : string`   | Aceita valores do tipo [[string]] | `name : string = 'Shie'`    |
| Number / `[variável] : number`   | Aceita valores do tipo numérico   | `idade : number = 23`       |
| Boolean / `[variável] : boolean` | Aceita valores booleanos          | `aprovado : boolean = true` |

Há também como sinalizar que uma mesma variável pode receber mais de um tipo, através da sintaxe: `[variável] : ( [tipo1] | [tipo2] )`
	Exemplo: `keyboardOnly: ( string | boolean ) = "new keybord"`

##### Tipagem para :
