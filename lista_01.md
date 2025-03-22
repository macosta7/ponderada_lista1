# Instruções
- Faça uma cópia deste arquivo .md para um repositório próprio
- Resolva as 8 questões objetivas assinalando a alternativa correta e **justificando sua resposta.**
- Resolva as 2 questões dissertativas escrevendo no próprio arquivo .md
- Lembre-se de utilizar as estruturas de código como ``esta aqui com ` `` ou
```javascript
//esta aqui com ```
let a = "olá"
let b = 10
print(a)
```
- Resolva as questões com uso do Visual Studio Code ou ambiente similar.
- Teste seus códigos antes de trazer a resposta para cá.
- Cuidado com o uso de ChatGPT (e similares), pois entregar algo só para ganhar nota não fará você aprender. Não seja dependente da máquina!
- Ao final, publique seu arquivo lista_01.md com as respostas em seu repositório, e envie o link pela Adalove. 

# Questões objetivas
**1) Considerando a execução do código abaixo, indique a alternativa correta e justifique sua resposta.**
```javascript
console.log(x);
var x = 5;
console.log(y);
let y = 10;
```
``a) A saída será undefined seguido de erro``

b) A saída será 5 seguido de 10

c) A saída será undefined seguido de undefined

d) A saída será erro em ambas as linhas que utilizam console.log

```javascript
  //Primeiro vai aparecer undefined pois a variável x é declarada depois do console.log(x) e ela fica como undefined porque ela foi criada com var, que permite que o valor de x seja atualizado posteriormente. Já o erro acontece porque a variável y é declarada depois do console.log(y) e por y ser declarado com let, a variável y não pode ser declarada posteriormente, assim o código acaba em erro.
```

**2) O seguinte código JavaScript tem um erro que impede sua execução correta. Analise e indique a opção que melhor corrige o problema. Justifique sua resposta.**

```javascript
function soma(a, b) {
    if (a || b === 0) {
        return "Erro: número inválido";
    }
    return a + b;
}
console.log(soma(2, 0));
```

a) Substituir if (a || b === 0) por if (a === 0 || b === 0)

``b) Substituir if (a || b === 0) por if (a === 0 && b === 0)``

c) Substituir if (a || b === 0) por if (a && b === 0)

d) Remover completamente a verificação if (a || b === 0)

```javascript
  //Um número vai ser inválido caso some 0 + 0, para fazer essa lógica precisamos dizer que os valores de a E b precisam ser 0 e a alternativa que resolve esse problema é a alternativa B. No caso, o código apresenta erro porque no if a variável a não está fazendo nada, ela está atoa, então dá erro.
```

______
**3) Ao executar esse código, qual será a saída no console? Indique a alternativa correta e justifique sua resposta.**
```javascript
function calcularPreco(tipo) {
    let preco;

    switch(tipo) {
        case "eletrônico":
            preco = 1000;
        case "vestuário":
            preco = 200;
            break;
        case "alimento":
            preco = 50;
            break;
        default:
            preco = 0;
    }

    return preco;
}

console.log(calcularPreco("eletrônico"));
```

a) O código imprime 1000.

``b) O código imprime 200.``

c) O código imprime 50.

d) O código gera um erro.

```javascript
  //Mesmo que o tipo que está entrando no console.log seja "eletrônico" quando for para o switch, vai entrar na case "eletrônico" e o preco vai ser definido para 1000, porém, como não tem um break, o switch vai continuar rodando e vai entrar no case "vestuário" e vai redefinir a variável preco para 200 e como existe um break dentro desse case, o switch vai encerrar e o preco que vai ser retornado no console.log vai ser 200. 
```

______
**4) Ao executar esse código, qual será a saída no console? Indique a alternativa correta e justifique sua resposta.**
```javascript
let numeros = [1, 2, 3, 4, 5];

let resultado = numeros.map(x => x * 2).filter(x => x > 5).reduce((a, b) => a + b, 0);

console.log(resultado);
```
a) 0

b) 6

c) 18

``d) 24``

```javascript
  //Quando usamos numeros.map estamos pegando todos os numeros do array e fazendo o que está dentro do parênteses que no caso é multiplicar todos os números do array por 2, ficando (2, 4, 6, 8, 10). Quando usamos .filter estamos dizendo que vamos filtrar os números dentro da condição que no caso vai ser os números maiores do que 5, que vão ser (6, 8, 10). Quando usamos .reduce estamos somando todos os valores entre si, ou seja 6+8+10, resultando em 24.
```
______
**5) Qual será o conteúdo do array lista após a execução do código? Indique a alternativa correta e justifique sua resposta.**

```javascript
let lista = ["banana", "maçã", "uva", "laranja"];
lista.splice(1, 2, "abacaxi", "manga");
console.log(lista);
```

a) ["banana", "maçã", "uva", "abacaxi", "manga", "laranja"]

b) ["banana", "abacaxi", "manga"]

``c) ["banana", "abacaxi", "manga", "laranja"]``

d) ["banana", "maçã", "uva", "abacaxi", "manga"]

```javascript
  //O .splice altera os valores dentro daquela lista, então quando colocamos (1, 2, "abacaxi", "manga") estamos dizendo que a fruta a posição 1 da lista que no caso é "maçã" vai ser substituida por "abacaxi", o mesmo ocorre com a fruta na posição 2 que é "uva", com o splice a posição 2 vai ser alterada para "manga".
```
______
**6) Abaixo há duas afirmações sobre herança em JavaScript. Indique a alternativa correta e justifique sua resposta**

I. A herança é utilizada para compartilhar métodos e propriedades entre classes em JavaScript, permitindo que uma classe herde os métodos de outra sem a necessidade de repetir código.  
II. Em JavaScript, a herança é implementada através da palavra-chave `extends`.


``a) As duas afirmações são verdadeiras, e a segunda justifica a primeira.``

b) As duas afirmações são verdadeiras, mas a segunda não justifica a primeira.

c) A primeira afirmação é verdadeira, e a segunda é falsa.

d) A primeira afirmação é falsa, e a segunda é verdadeira.

```javascript
  //As afirmações estão corretas, pois a função da herança é reutilizar métodos ajudando a economizar trabalho, para fazer isso criamos a classe com: class Nome_da_Classe extends Nome_da_Classe_Herdada, dessa forma os métodos dentro da Nome_da_Classe_Herdada podem ser utilizados em Nome_da_Classe por conta da criação de classe utilizando o extends.
```
______
**7) Dado o seguinte código. Indique a alternativa correta e justifique sua resposta.**

```javascript
class Pessoa {
  constructor(nome, idade) {
    this.nome = nome;
    this.idade = idade;
  }

  apresentar() {
    console.log(`Olá, meu nome é ${this.nome} e tenho ${this.idade} anos.`);
  }
}

class Funcionario extends Pessoa {
  constructor(nome, idade, salario) {
    super(nome, idade);
    this.salario = salario;
  }

  apresentar() {
    super.apresentar();
    console.log(`Meu salário é R$ ${this.salario}.`);
  }
}
```


I) A classe Funcionario herda de Pessoa e pode acessar os atributos nome e idade diretamente.  
II) O método `apresentar()` da classe Funcionario sobrepõe o método `apresentar()` da classe Pessoa, mas chama o método da classe pai usando `super`.  
III) O código não funciona corretamente, pois Funcionario não pode herdar de Pessoa como uma classe, já que o JavaScript não suporta herança de classes.

Quais das seguintes afirmações são verdadeiras sobre o código acima?

``a) I e II são verdadeiras.``

b) I, II e III são verdadeiras.

c) Apenas II é verdadeira.

d) Apenas I é verdadeira.

```javascript
  // I) Quando a classe Funcionario é criada, ela extende a classe Pessoa, assim os atributos criados em Pessoa ficam acessíveis na classe Funcionário. Quando colocamos super(nome, idade); na classe Funcionario extendendo de Pessoa, estamos puxando as variáveis nome e idade que foram criadas em Pessoa para dentro da classe Funcionario permitindo que elas sejam criadas. II) Sim, o método apresentar() da classe Funcionaria sobrepõe o método apresentar() da classe Pessoa, porém, quando o método apresentar() da classe Funcionario é chamado, o super.apresentar() é chamado puxando o método apresentar() da classe pai, no caso a classe pessoa. Com isso, o retorno do código vai ser o método apresentar() da classe Pessoa aparecendo `Olá, meu nome é ${this.nome} e tenho ${this.idade} anos.` e logo em seguida `Meu salário é R$ ${this.salario}.` que está na função apresentar() da classe Funcionario. III) Afirmação falsa, pois o JavaScript suporta herança de classes.
```

______

**8) Analise as afirmações a seguir. Indique a alternativa correta e justifique sua resposta.**

**Asserção:** O conceito de polimorfismo em Programação Orientada a Objetos permite que objetos de diferentes tipos respondam à mesma mensagem de maneiras diferentes.  
**Razão:** Em JavaScript, o polimorfismo pode ser implementado utilizando o método de sobrecarga de métodos em uma classe.

a) A asserção é falsa e a razão é verdadeira.

``b) A asserção é verdadeira e a razão é falsa.``

c) A asserção é verdadeira e a razão é verdadeira, mas a razão não explica a asserção.

d) A asserção é verdadeira e a razão é verdadeira, e a razão explica a asserção.

```javascript
  // A asserção está correta pois em POO podemos crias diversas subclasses herdadas de uma classe pai e nessas subclasses podemos definir uma mesma função alterando apenas o que ela irá fazer em cada subclasse e no final podemos utilizar a herança para utilizar esse polimorfismo utilizando um mesmo método mas em cada classe filha ele faz algo  diferente. Já a Razão é falsa pois em JS não existe sobrecarga, mas caso criarmos dois métodos com o mesmo nome em uma classe mas sobrecarregarmos elas uma entrando um valor e na outro entrando dois valores, ao final o código vai acabar em erro, pois como não existe sobrecarga o último método criado irá substituir os outros criados anteriormente com o mesmo nome. 
```
______

# Questões dissertativas
9) O seguinte código deve retornar a soma do dobro dos números de um array, mas contém erros. Identifique os problema e corrija o código para que funcione corretamente. Adicione comentários ao código explicado sua solução para cada problema.

```javascript
function somaArray(numeros) {
    
    let soma = 0;

    for (let i = 0; i < numeros.length; i++) {
        soma = soma + (2 * numeros[i]);
    }
    return soma;
}
console.log(somaArray([1, 2, 3, 4]));
```

```javascript
  // numeros.size não funciona em JS, o correto para dizermos o tamanho do array é numero.length. Outra coisa que estava errada era que as variáveis soma e i não estvam sendo declaradas, para cosertar isso declarei a variável soma utilizando let soma = 0; e a variável i utilizando let i = 0; dentro do for. A variável soma estava armazenando os números da lista multiplicados por 2 mas ao invés de soma os números multiplicados por 2, ela estava armazendando o número e depois o outro número substituia o númeero anterior e assim por diante. Para consertar isso eu coloquei que soma vai ser igual ao valor anterior da soma + o numero da lista vezes dois, assim no final teremos como resposta 20, que é a soma do dobro dos números do array.
```
______
10) Crie um exemplo prático no qual você tenha duas classes:

- Uma classe `Produto` com atributos `nome` e `preco`, e um método `calcularDesconto()` que aplica um desconto fixo de 10% no preço do produto.
- Uma classe `Livro` que herda de `Produto` e modifica o método `calcularDesconto()`, aplicando um desconto de 20% no preço dos livros.

Explique como funciona a herança nesse contexto e como você implementaria a modificação do método na classe `Livro`.

```javascript
  class Produto {
    constructor (nome, preco) {
    this.nome = nome;
    this.preco = preco;
  }

    calcularDesconto() {
      return this.preco * 0,9; // Aplica um desconto de 10%
    }
  }

  class Livro extends Produto { // Cria a classe Livro herdando os atributos de Produto
    constructor (nome, preco) {
      super(nome, preco);
    }

    calcularDesconto() {
      return this.preco * 0.8; // Aplica um desconto de 20%
    }
  }

  // Criando instâncias e testando
  const produto = new Produto("Computador", 2000);
  console.log(`Preço do Produto com desconto: R$ ${produto.calcularDesconto()}`);

  const livro = new Livro("Programação", 100);
  console.log(`Preço do Livro com desconto: R$ ${livro.calcularDesconto()}`);
```
```javascript
  // A classe Livro herda os atributos (nome e preco) da classe Produto, assim a classe Livro pode utilizar essas variáveis dentro do escopo da classe, evitando a repetição de código. Quando o método calcularDesconto() dentro da classe Livro é chamado eu calculei o desconto multiplicando o preço do produto por 0.8, assim será aplicado um desconte de 20% em cima do Livro
```
