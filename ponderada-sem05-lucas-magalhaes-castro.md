# Instruções

- Faça uma cópia deste arquivo .md para um repositório próprio
- Resolva as 6 questões objetivas assinalando a alternativa correta
- Resolva as 4 questões dissertativas escrevendo no próprio arquivo .md
  - lembre-se de utilizar as estruturas de código como ``esta aqui com ` `` ou
```javascript
//esta aqui com ```
let a = "olá"
let b = 10
print(a)
```
- Resolva as questões com uso do Visual Studio Code ou ambiente similar.
- Teste seus códigos antes de trazer a resposta para cá.
- Cuidado com ChatGPT e afins: entregar algo só para ganhar nota não faz você aprender e ficar mais inteligente. Não seja dependente da máquina!
- ao final, publique seu arquivo lista_01.md com as respostas em seu repositório, e envie o link pela Adalove. 

# Questões objetivas

**1)** O que o código a seguir faz?

![Uma imagem](assets/ex01.PNG)

Escolha a opção que responde corretamente:

~~a)~~ Imprime os números pares de 1 a 10.

b) Imprime os números ímpares de 1 a 10.

c) Imprime os números pares de 2 a 10.

d) Imprime os números ímpares de 2 a 10.

______

**2)** Identificar a linha que falta no código para criar uma classe Veiculo com atributo marca, e uma classe Carro que herda de Veiculo com um método ligar(). 

![Uma imagem](assets/ex02.PNG)

No lugar onde está escrito “// linha” qual das opções abaixo deve estar para funcionar corretamente o código?

~~A)~~ let carro = new Carro("Toyota");

B) let ligar = new ligar("Toyota");

C) class Moto extends Veiculo {};

D) carro1.ligar();

______

**3)** Qual é o valor de resultado após a execução deste código?

![Uma imagem](assets/ex03.PNG)

Escolha a opção que responde corretamente:

~~A)~~ 18

B) 16

C) 14

D) 12

______

**4)** Como você criaria um método `acelerar()` em uma classe `Carro`, que recebe um parâmetro `velocidade` e o adiciona a um atributo `velocidadeAtual`?

~~A)~~ ![Uma imagem](assets/ex04_1.PNG)

B) ![Uma imagem](assets/ex04_2.PNG)

C) ![Uma imagem](assets/ex04_3.PNG)

D) ![Uma imagem](assets/ex04_4.PNG)

______

**5)** Qual a forma correta de definir uma classe Carro em JavaScript, com um método ligar() e um atributo marca?

~~A)~~ ![Uma imagem](assets/ex05_1.PNG)

B) ![Uma imagem](assets/ex05_2.PNG)

C) ![Uma imagem](assets/ex05_3.PNG)

D) ![Uma imagem](assets/ex05_4.PNG)

______

**6)** Observe o código abaixo:

![Uma imagem](assets/ex06.PNG)

Qual será a saída do código acima?

~~A)~~ "Olá, meu nome é João. Olá, meu nome é Maria."

B) "Olá, meu nome é ."

C) "João Maria"

D) "undefined undefined"

______

# Questões dissertativas

**7)** Vamos criar um programa em JavaScript para entender classes, métodos e atributos!
Classe Animal:
- Crie uma classe chamada Animal.
- Adicione dois atributos: nome e idade.
- Adicione um método chamado descrever() na classe Animal.
  - Este método deve exibir no console uma descrição do animal com seu nome e idade.

Criando e manipulando Animais:
- Crie dois objetos da classe Animal: um chamado "cachorro" e outro "gato", com idades distintas.
- Para cada animal, chame o método descrever() para ver a descrição no console.

Dica: Utilize `console.log()` para exibir as informações!

Resposta:

```javascript
class animal {
    constructor (nome, idade) {
        this.nome = nome;
        this.idade = idade;
    }

    descrever() {
        console.log(`Este animal se chama ${this.nome} e ele tem ${this.idade} anos`);
    }

}

let cachorro = new animal('Cachorro', 7);
let gato = new animal('Gato', 5);

cachorro.descrever();
gato.descrever();
```

______

**8)** Nos últimos dias tivemos a oportunidade de ter contato com Programação Orientada a Objetos, e tivemos contato com o tema "herança". Herança é um princípio de orientação a objetos, que permite que classes compartilhem atributos e métodos. Ela é usada na intenção de reaproveitar código ou comportamento generalizado ou especializar operações ou atributos. Então vamos praticar esse conteúdo nessa questão.
Vamos criar um programa em JavaScript para entender classes, métodos, atributos e herança!

Classe Animal:
- Crie uma classe chamada Animal.
- Adicione dois atributos: nome e idade.
- Adicione um método descrever() que exiba no console uma descrição do animal com seu nome e idade.

Classe Gato (Herda de Animal):
- Crie uma classe chamada Gato que herda da classe Animal.
- Adicione um atributo extra cor específico para gatos.
- Adicione um método miar() que exiba no console o som que um gato faz.

Criando Animais:
- Crie dois objetos da classe Animal: um chamado cachorro e outro gato, com idades distintas.
- Para o gato, também defina a cor.

Chamando os Métodos:
- Para cada animal, chame o método descrever() para ver a descrição no console.
- Para o gato, chame o método miar() para "ouvir" o som que ele faz (é também para ver o som no console).

Dica: Utilize console.log() para exibir as informações!

Resposta: 

```javascript
class animal {
    constructor(nome, idade) {
        this.nome = nome;
        this.idade = idade;
    }

    descrever() {
        console.log(`Esse animal se chama ${this.nome} e ele tem ${this.idade} anos`);
    }

}

class Gato extends animal {
    constructor(nome, idade, cor) {
        super(nome, idade);
        this.cor = cor;
    }

    miar() {
        console.log('O som que o gato faz é miauuuu');
    }

    descrever() {
        console.log(`Esse animal se chama ${this.nome}, ele tem ${this.idade} anos e sua cor é ${this.cor}`);
    }

}

let cachorro = new animal('cachorro', 8);
let gato = new Gato('gato', 4, 'branca');

cachorro.descrever()
gato.descrever();
gato.miar();
```

______

**9)** Vamos criar um programa em JavaScript para somar notas!

Classe SomadorDeNotas:
- Crie uma classe chamada SomadorDeNotas.
- Adicione um atributo total inicializado com 0 para armazenar a soma das notas.

Método adicionarNota:
- Adicione um método chamado adicionarNota(nota) na classe SomadorDeNotas.
- Este método deve receber um parâmetro nota e somá-lo ao atributo total.

Criando o Somador e Adicionando Notas:
- Crie um objeto da classe SomadorDeNotas, chamado somador.
- Utilize o método adicionarNota(nota) para adicionar algumas notas ao somador.

Chamando o Método para Ver o Total:
- Após adicionar todas as notas, chame um método verTotal() para exibir o total das notas adicionadas.

Dica: Utilize console.log() para exibir as informações!

Resposta:
```javascript
class SomadorDeNotas {
    constructor(total = 0) {
        this.total = total;
    }

    adicionarNota(nota) {
        this.total += nota;
    }

    verTotal() {
        console.log(`Sua nota total é ${this.total}`);
    }

}

let somador = new SomadorDeNotas();
somador.adicionarNota(5);
somador.adicionarNota(9);

somador.verTotal();
```

______

**10)** Imagine que você está criando um programa em JavaScript para uma escola. Neste programa, existem diferentes tipos de funcionários, cada um com suas próprias características. Considere as seguintes classes:

Funcionário:
- atributo: Nome
- atributo: Idade
- atributo: Salário base
- método: calcularSalario() - Este método calcula o salário total do funcionário. Para cada tipo de funcionário, o cálculo será diferente.

Professor (herança de Funcionário):
- atributo: Disciplina
- atributo: Horas de aula por semana
- método: calcularSalario() - Para calcular o salário do professor, multiplicamos suas horas de aula pelo valor da hora/aula.

Agora, sua tarefa é escrever um código em JavaScript que crie as classes Funcionário e Professor, com suas características e métodos descritos acima. Depois de criar as classes, crie:
- Dois objetos do tipo Professor com informações fictícias.
- Para cada objeto, chame o método calcularSalario() e mostre o salário calculado no console.

Certifique-se de explicar cada parte do código utilizando comentários, explicando para que serve cada atributo e método, bem como a lógica por trás do cálculo de salário para o tipo de funcionário Professor.

Resposta:

```javascript
// criando a classe funcionário
class Funcionario {
  // adicionando os atributos pedidos
  constructor(nome, idade, salarioBase) {
    this.nome = nome;
    this.idade = idade;
    this.salarioBase = salarioBase;
  }

  // criando o método para calcular o salário, coloquei para retornar 0 porque o calculo é feito diferente para cada tipo de funcionário
  calcularSalario() {
    return 0;
  }
}

// criando a classe professor e herdando os atributos e métodos da classe funcionário
class Professor extends Funcionario {
  // adicionando os atributos novos e herdados
  constructor(nome, idade, salarioBase, disciplina, hAulaSemana) {
    super(nome, idade, salarioBase);
    this.disciplina = disciplina;
    this.hAulaSemana = hAulaSemana;
  }

  // criando o método para calcular o salário dos professores. adicionei o valor da hora e também já o salário total com a intenção de economizar trabalho e já adicionar no console.
  calcularSalario(valorHora, salarioTotal) {
    // calculando o salário total do professor. Multipliquei por 4 porque o salário é do mês inteiro e as horas de trabalho são as horas da semana, logo temos 4 semanas no mês.
    salarioTotal = valorHora * this.hAulaSemana * 4;

    // para guardar a informação do salário total e adicionar isso no console
    this.salarioTotal = salarioTotal;

    // comando para mostrar no console todas as informações necessárias sobre os professores
    console.log(
      `O salario de ${this.nome}, que é professor(a) de ${this.disciplina}, tem ${this.idade} anos e trabalha ${this.hAulaSemana} por semana é R$:${this.salarioTotal} por mês. O salário base para professores da área de ${this.nome} é de R$:${this.salarioBase}`
    );
  }
}

// criando dois objetos do tipo professor e colocando informações que inventei
let professor1 = new Professor("Marco", 30, 1500, "Matemática", 10);
let professor2 = new Professor("Martha", 47, 1200, "Geografia", 25);

// chamando o método para calcular o salário do professor e mostrar no console
professor1.calcularSalario(40);
professor2.calcularSalario(32);
```
