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
- Cuidado com ChatGPT e afins: entregar algo só para ganhar nota não faz você aprender e ficar mais inteligente. Não seja dependente da máquina! (E não se envolva em plágio!)
- ao final, publique seu arquivo lista_02.md com as respostas em seu repositório, e envie o link pela Adalove. 

# Questões objetivas

**1)** Considere o seguinte código JavaScript:

```javascript
//EX01
let p = 10;
let q = 3;
let r = 6;

let resultado = (p % q === 1) && (r * 2 > p) || (q + r < p);
console.log(resultado);

const valores = [3, 6, 9, 12, 15];
let produto = 1;

for (let j = 0; j < valores.length; j++) {
  produto *= valores[j];
}

console.log("O produto dos valores é:", produto);


```
Qual das seguintes alternativas melhor descreve o que o código faz?

A) O código avalia a expressão booleana, imprime `true`, calcula o produto dos números na lista e imprime o resultado no console. **X - A alternativa A é a correta, pois 10/3 tem resto 1 e 2*6 = 12>10, 
além de que 9<10, ou seja, todas as condições foram atendidas e, independentemente da presença do operador ou "||", o retorno será true. O produto da lista valores também é calculado através da operação
1*= cada valor da lista, provocando uma repetição que inclui todos os valores dentro dela multiplicados entre si, sendo imprimidos ao final com o comando console.log.**

B) O código avalia a expressão booleana, imprime `false`, calcula o produto dos números na lista e imprime o resultado no console.

C) O código avalia a expressão booleana, imprime `true` e, em seguida, verifica se o número 6 está na lista.

D) O código avalia a expressão booleana, imprime `false` e ordena os valores em ordem crescente.


______

**2)** O código a seguir contém duas funções que calculam o limite de crédito de um cliente com base nos seus gastos e na renda mensal.

```javascript
// Versão 1 da função de análise de crédito
function analisarCredito1() {
    var compras = [2500, 1200, 800, 100];
    var totalCompras = compras[0];
    var limite = 5000;
    var status = 'aprovado';
    var saldoDisponivel = 0;
    var i = 1;

    do {
        totalCompras += compras[i];
        i++;
    } while (limite >= totalCompras && i < compras.length);

    saldoDisponivel = limite - totalCompras;

    if (saldoDisponivel < 0) {
        status = 'negado';
    }
    console.log(`Seu crédito foi ${status}. Saldo disponível: ${saldoDisponivel}.`);
}
```

```javascript
// Versão 2 da função de análise de crédito
function analisarCredito2() {
    var compras = [2500, 1200, 800, 100];
    var totalCompras = compras[0];
    var limite = 5000;
    var status = 'aprovado';
    var saldoDisponivel = 0;
    var i = 1;

    while (limite >= totalCompras && i < compras.length) {
        totalCompras += compras[i];
        i++;
    }

    saldoDisponivel = limite - totalCompras;

    if (saldoDisponivel < 0) {
        status = 'negado';
    }
    console.log(`Seu crédito foi ${status}. Saldo disponível: ${saldoDisponivel}.`);
}
```
Se ambas as funções forem executadas com os valores fornecidos, qual será a saída exibida no console?

A) Ambas as funções exibirão: 'Seu crédito foi aprovado. Saldo disponível: 400.' **X = A alternativa correta é a A, pois após as somas dos valores de todos os elementos da lista compras (4600), e a subtração deste novo valor do limite, resta 400.**

B) analisarCredito1() exibirá: 'Seu crédito foi negado. Saldo disponível: -600.', enquanto analisarCredito2() exibirá: 'Seu crédito foi negado. Saldo disponível: -200.'

C) analisarCredito1() exibirá: 'Seu crédito foi negado. Saldo disponível: -200.', enquanto analisarCredito2() exibirá: 'Seu crédito foi aprovado. Saldo disponível: 100.'

D) Ambas as funções exibirão: 'Seu crédito foi aprovado Saldo disponível: 500.'
______

**3)** Considere o seguinte trecho de código em JavaScript:
```javascript
//EX03
const idade = 21;

if (idade >= 18 && idade < 60) {
  console.log("Você é um adulto!");
} else if (idade < 18) {
  console.log("Você é menor de idade!");
} else {
  console.log("Você está na melhor idade!");
}
```
Qual das seguintes alternativas melhor descreve o comportamento do código?

A) O código verifica se a idade indica um adulto ou um idoso e exibe a mensagem correspondente.

B) O código verifica se a idade pertence à faixa adulta. Se for, exibe "Você é um adulto!". Caso contrário, verifica se é menor de idade e exibe "Você é menor de idade!". Se nenhuma das condições anteriores for verdadeira, exibe "Você está na melhor idade!". **X = 
A alternativa correta é a B, pois a primeira condição a ser verificada é se o "usuário" está entre as faixas de 18 até 60 anos, e se esta não for verificada, a condição de menor de idade é percorrida, e caso nenhuma das duas sejam dadas como true, o código apresenta
que você está na melhor idade.**

C) O código verifica se a idade está entre 18 e 60 anos e, se for, imprime "Você é um adulto!". Se não estiver nesse intervalo, imprime "Você está na melhor idade!".

D) O código verifica se a idade é menor de 18, entre 18 e 60 ou acima de 60, imprimindo uma mensagem específica para cada caso.
______

**4)** Qual será o resultado impresso no console após a execução do seguinte código?
```javascript
//EX04
var energiaDisponivel = 1200;
var bateriaExtra = 400;
var consumoDispositivos = [300, 600, 500, 200, 400];

for (var i = 0; i < consumoDispositivos.length; i++) {
    var consumo = consumoDispositivos[i];

    if (consumo <= energiaDisponivel) {
        console.log("Dispositivo " + (i+1) + " ligado. Energia restante: " + (energiaDisponivel - consumo));
        energiaDisponivel -= consumo;
    } else if (consumo <= energiaDisponivel + bateriaExtra) {
        console.log("Dispositivo " + (i+1) + " ligado com bateria extra. Energia restante: " + ((energiaDisponivel + bateriaExtra) - consumo));
        energiaDisponivel = 0;
        bateriaExtra -= (consumo - energiaDisponivel);
    } else {
        console.log("Dispositivo " + (i+1) + " não pode ser ligado. Energia insuficiente.");
    }
}
```

Escolha a opção que responde corretamente:

A)
Dispositivo 1 ligado. Energia restante: 900

Dispositivo 2 ligado com bateria extra. Energia restante: 700

Dispositivo 3 ligado. Energia restante: 200

Dispositivo 4 ligado com bateria extra. Energia restante: 0

Dispositivo 5 ligado. Energia restante: -200

B)
Dispositivo 1 ligado. Energia restante: 900

Dispositivo 2 ligado com bateria extra. Energia restante: 700

Dispositivo 3 ligado. Energia restante: 200

Dispositivo 4 não pode ser ligado. Energia insuficiente.

Dispositivo 5 não pode ser ligado. Energia insuficiente.

C)
Dispositivo 1 ligado. Energia restante: 900

Dispositivo 2 ligado com bateria extra. Energia restante: 700

Dispositivo 3 ligado. Energia restante: 400

Dispositivo 4 não pode ser ligado. Energia insuficiente.

D) **X = A alternativa D é a correta, pois o valor da energia disponível (1200) - o primeiro valor da lista consumoDispositivos (300) deixa 900 de energia restante,
com a segunda verificação, já considerando o segundo valor da lista e o restante da operação anterior, resulta em 300, levando em conta que a conta realizada agora é 900 - 600.
A terceira verificação demonstra a utilização da bateria extra, pois o valor restante da energiaDisponível se tornou negativo (-200) a partir da operação 300 - 500, levando agora à 
compensação pela bateria. Considerando que a partir deste momento as operações serão nula e negativa (200 - 200 = 0 e 0 - 400 = -400), o status será de energia insuficiente nos
dispositivos 4 e 5.**

Dispositivo 1 ligado. Energia restante: 900

Dispositivo 2 ligado. Energia restante: 300

Dispositivo 3 ligado com bateria extra. Energia restante: 200

Dispositivo 4 não pode ser ligado. Energia insuficiente.

Dispositivo 5 não pode ser ligado. Energia insuficiente.

______

**5)** Qual é a principal função do método update() em um jogo desenvolvido com Phaser.js?

Escolha a opção que melhor descreve seu propósito:

A) O método update() é responsável por carregar os assets do jogo antes da cena ser exibida.

B) O método update() é chamado continuamente a cada quadro (frame) do jogo, sendo usado para atualizar a lógica, movimentação e interações dos objetos na cena. **X = A alternativa
correta é a B, pois o método update é utilizado para a constante atualização das ações do player ao longo do jogo, sempre considerando cada passo dado por este no 
cenário e com o que interage em um minigame ou diálogo, por exemplo.**

C) O método update() renderiza todos os sprites na tela e garante que a física do jogo seja processada corretamente.

D) O método update() é chamado apenas uma vez após a criação da cena, sendo utilizado para configurar variáveis iniciais do jogo.
______

**6)** Qual é o principal objetivo do módulo Matter.js Physics em Phaser.js?

Escolha a opção que responde corretamente:

A) Simular física avançada, incluindo corpos rígidos, colisões complexas e interação entre objetos com gravidade e forças. **"X = A alternativa correta é a A, pois o módulo 
matter.js é capaz de estabelecer, por exemplo, a colisão entre um player e um objeto ou a ação da gravidade sobre um que esteja em uma altura mais elevada e se coloca suspenso
no cenário, sendo levado ao chão.**

B) Gerenciar eventos de entrada do usuário, como cliques e toques na tela, permitindo movimentação de personagens.

C) Renderizar gráficos otimizados para jogos 2D e garantir uma taxa de quadros estável.

D) Criar animações automáticas para sprites e objetos interativos sem necessidade de programação de movimentação.

______

# Questões dissertativas

**7)** Uma loja online deseja implementar um sistema de classificação de pedidos com base no valor total da compra. O sistema deve determinar a categoria de um pedido com as seguintes regras:

```

Pedidos abaixo de R$50,00 → "Frete não disponível!"

Pedidos entre R$50,00 e R$199,99 (inclusive) → "Frete com custo adicional!"

Pedidos de R$200,00 ou mais → "Frete grátis!"
```
Implemente um pseudocódigo que receba o valor total da compra e exiba a classificação correta do frete para o cliente.

**RESPOSTA**

```javascript

var criterios = [50, 199, 200]
var compra = 0

function calcFrete(compra) {
    if (compra < criterios[0]) {
        console.log('Frete não disponível!');
    }
    else if (compra >= criterios[0] && compra < criterios[1]) {
        console.log('Frete com custo adicional!');
    }
    else { console.log('Frete grátis!'); }
}
//Exemplo em que o resultado é 'Frete grátis!'
calcFrete(350)

```
______

**8)** Considere a implementação da classe base Veiculo em um sistema de modelagem de veículos. Sua tarefa é implementar, utilizando pseudocódigo, as classes derivadas
Carro e Moto, que herdam da classe Veiculo, adicionando atributos específicos e métodos para calcular o consumo de combustível de um carro e de uma moto, respectivamente.

```
Classe Veiculo:
Atributos:

modelo
ano
Método Construtor(modelo, ano):

Define os valores dos atributos modelo e ano com os valores passados como parâmetro.
Método CalcularConsumo():
```
Implementação genérica para cálculo de consumo, a ser sobrescrita pelas subclasses.
Agora, implemente as classes Carro e Moto, garantindo que ambas herdem de Veiculo e possuam métodos específicos para calcular o consumo de combustível com base na 
quilometragem e eficiência do veículo.

**RESPOSTA**

```javascript
class Veiculo {
  constructor() {
    this.km = 0;
    this.eficiencia = 30; // km/l
    this.modelo = "modelo";
    this.ano = 1;
  }

  CalcularConsumo(km) {
    var calculo = km / this.eficiencia;
    return calculo;
  }
}

class Carro extends Veiculo {
  constructor() {
    super();
      this.eficiencia = 10;
      this.modelo = "Fusca";
      this.ano = 2000;
  }
}

class Moto extends Veiculo {
  constructor() {
    super();
    this.eficiencia = 20;
    this.modelo = "Motocross";
    this.ano = 2002;
  }
}

console.log(new Carro().CalcularConsumo(100));
console.log(new Moto().CalcularConsumo(400));


```
______

**9)** Você é um cientista da NASA e está ajudando no desenvolvimento de um sistema de pouso para sondas espaciais em Marte. Seu objetivo é calcular o tempo necessário para que a sonda reduza sua velocidade até um nível seguro para pouso, considerando uma velocidade inicial de entrada na atmosfera marciana e uma taxa de desaceleração constante causada pelo atrito atmosférico e retrofoguetes.

Entretanto, a sonda não pode ultrapassar um tempo máximo de descida para evitar desvios orbitais, nem pode desacelerar além de um limite mínimo, pois isso poderia causar instabilidade no pouso.

Implemente a lógica dessa simulação em pseudocódigo, considerando a seguinte equação para atualização da velocidade:

Considere a fórumla de atualização velocidade:
``` velocidade = velocidadeInicial - desaceleracao * tempo```

Seu programa deve determinar quanto tempo será necessário para que a sonda atinja uma velocidade segura de pouso, sem ultrapassar os limites estabelecidos.


**RESPOSTA**

```javascript


var velocidadeInicial = 0 //m/s
var desaceleracao = 0 
var tempo = 0 
var nivelSeguro = 0 
var limiteTempo = 0 //segundos
var limiteDesaceleracao = 0 

function desacelerarNave(velocidadeInicial, desaceleracao, nivelSeguro, limiteTempo, limiteDesaceleracao) {
    while (velocidadeInicial > nivelSeguro) {
        tempo += 1;
        let velocidade = velocidadeInicial -= (desaceleracao * tempo);
        if (tempo > limiteTempo) {
            console.log('Operação de pouso falha');
            break
        }
        else if (desaceleracao > limiteDesaceleracao) {
            console.log('Instabilidade no pouso');
            break
        }
        else {
            console.log(`A velocidade atual é: ${velocidade} e o tempo passado é: ${tempo} segundos`)
        }
    }
}

desacelerarNave(80, 2, 10, 15, 5) //teste


```
______

**10)** Em um sistema de análise financeira, as operações de investimento de uma empresa podem ser representadas por matrizes, onde cada linha representa um tipo de investimento e cada coluna representa um período de tempo.

A seguir, é fornecida a implementação da função SomarMatrizesInvestimento(matrizA, matrizB), que soma os valores de duas matrizes de investimento. Sua tarefa é implementar uma função semelhante, porém que realize a multiplicação das matrizes de investimento, determinando como os investimentos afetam os resultados ao longo do tempo.

```
Função SomarMatrizesInvestimento(matrizA, matrizB):  
    # Verifica se as matrizes têm o mesmo número de linhas e colunas  
    Se tamanho(matrizA) ≠ tamanho(matrizB) então:  
        Retornar "As matrizes não podem ser somadas. Elas têm dimensões diferentes."  
    Senão:  
        linhas <- tamanho(matrizA)  
        colunas <- tamanho(matrizA[0])  
        matrizResultado <- novaMatriz(linhas, colunas)  

        # Loop para percorrer cada elemento das matrizes e calcular a soma  
        Para i de 0 até linhas-1 faça:  
            Para j de 0 até colunas-1 faça:  
                matrizResultado[i][j] <- matrizA[i][j] + matrizB[i][j]  

        Retornar matrizResultado  

# Exemplo de uso da função  
investimentosAno1 <- [[1000, 2000], [1500, 2500]]  
investimentosAno2 <- [[1200, 1800], [1300, 2700]]  

totalInvestimentos <- SomarMatrizesInvestimento(investimentosAno1, investimentosAno2)  
Escrever("Total de investimentos acumulados:")  
ImprimirMatriz(totalInvestimentos)  
```
Agora, implemente a função MultiplicarMatrizesInvestimento(matrizA, matrizB), que multiplica as duas matrizes, simulando o efeito de diferentes fatores de crescimento e impacto financeiro nos investimentos ao longo do tempo.

**RESPOSTA**
```javascript

function multiplicarMatrizesInvestimento(matrizA, matrizB) {
    if (matrizA[0].length !== matrizB.length) {
        return "O número de colunas da matriz A deve ser igual ao número de linhas da matriz B."
    }
    else {
      let linhas = matrizA.length;
      let colunas = matrizB[0].length;
      let matrizResultado = [0];

      //Atribuir valores iniciais à matriz resultado e calcular com linhas/colunas iguais

      for (let i = 0; i < linhas; i++) {
        matrizResultado[i] = [0];
        for (let j = 0; j < colunas; j++) {
            matrizResultado[i][j] = 0;
            for (let k = 0; k < matrizA[1].length; k++) {
              matrizResultado[i][j] += matrizA[i][k] * matrizB[k][j];
            }
        }
      }

      return matrizResultado;
    }
}

var investimentosAno1 = [[1000, 2000], [1500, 2500]];
var investimentosAno2 = [[1200, 1800], [1300, 2700]];

var totalInvestimentos = multiplicarMatrizesInvestimento(investimentosAno1, investimentosAno2);
console.log("Total de investimentos acumulados:" + totalInvestimentos);

```
