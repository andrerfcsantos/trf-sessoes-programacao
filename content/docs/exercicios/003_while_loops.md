+++
date = '2025-11-06T19:33:10+01:00'
draft = false
title = 'While Loops'
+++

# Exercícios: While Loops

## Material de apoio

### Notas da sessão anterior

- [Notas sessão 6](../sessoes/006_202511103/) - Notas da sessão sobre while loops

### Lembrete de material anterior

- [Deno: Prompts](https://docs.deno.com/examples/prompts/) - Explica como usar a função `prompt()` no Deno
- [Deno.exit()](https://docs.deno.com/api/deno/~/Deno.exit) - Explica como usar `Deno.exit()`
- [MDN Web Docs - Number()](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Number) - Tem exemplos de como usar `Number()`
- [MDN Web Docs - isNaN()](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/isNaN) - Explica como funciona `isNaN()` e tem exemplos de uso

### Material sobre aleatoriedade

- [Deno: randomIntegerBetween()](https://jsr.io/@std/random/doc/~/randomIntegerBetween) - Explica como usar a função `randomIntegerBetween()` do módulo `random` do Deno
- [MDN Web Docs - Math.random()](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Math/random) - Explica como usar `Math.random()` em JavaScript
- [MDN Web Docs - Math.floor()](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Math/floor) - Explica como usar `Math.floor()` em JavaScript

### Material de loops

- [MDN Web Docs - while](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/while) - Docs da MDN sobre o while loop

## Exercícios

{{% hint tip %}}
Criar um ficheiro separado para a resolução de cada um destes exercícios.
{{% /hint %}}

1. **Contador decrescente**
   
   Escreve um programa que peça ao utilizador para inserir um número inteiro positivo `n` e imprima uma contagem regressiva de `n` até 1, seguida de "Descolagem!".
   
   Exemplo de output para `n = 3`:
   ```
   3
   2
   1
   Descolagem!
   ```
   
2. **Tabuada de multiplicação**
   
   Escreve um programa que peça ao utilizador para inserir um número inteiro `m` e imprima a tabuada de multiplicação desse número de 1 a 10.
   
   Exemplo de output para `m = 5`:
   ```
   5 x 1 = 5
   5 x 2 = 10
   5 x 3 = 15
   ...
   5 x 10 = 50
   ```

3. **Soma de números**
    
    Escreve um programa que peça ao utilizador para inserir números inteiros, um de cada vez, e mostre a sua soma.
    O programa deve continuar a pedir números até o utilizador inserir `0`.
    Quando o utilizador inserir `0`, o programa deve imprimir a soma total dos números inseridos.
    
    Exemplo de input/output:
    ```
    Insere um número (0 para terminar): 5
    Insere um número (0 para terminar): 10
    Insere um número (0 para terminar): 3
    Insere um número (0 para terminar): 0
    A soma dos números inseridos é: 18
    ```

## Mini-projecto: Jogo de adivinhar números

Neste mini-projecto, vamos fazer um jogo para o utilizador adivinhar um número aleatório gerado pelo computador.
Neste jogo, o computador vai escolher um número aleatório entre 1 e 20, e o utilizador vai tentar adivinhar esse número em tentativas sucessivas.

{{% hint tip %}}
O mini-projecto vai ser dividido em várias fases.
A ideia é em cada fase ir adicionando mais funcionalidades ao jogo, de forma gradual.
Dividir o mini-projecto em fases ajuda a tornar o problema mais gerível e permite focar em uma parte de cada vez.
Permite também ir testando o programa à medida que ele vai crescendo, para ir validando o nosso progresso.
{{% /hint %}}

### Fase 1: Geração de número aleatório e input do utilizador

Nesta fase queremos que o programa gere um número aleatório entre 1 e 20 e peça ao utilizador para inserir um palpite.
O programa deve imprimir o número aleatório gerado e o palpite do utilizador.

Nesta fase o programa deve converter o input do utilizador para número usando a função `Number()` e verificar se o valor inserido é um palpite válido.
Um palpite é válido se for um número válido e estiver entre 1 e 20.
Se o palpite inserido não for válido, o programa deve imprimir uma mensagem de erro e terminar imediatamente com um código de saída diferente de zero.

Exemplo de output:
```
Insire o teu palpite (número entre 1 e 20): 10
Número aleatório gerado: 15
O teu palpite: 10
```

{{% hint tip %}}
Nesta fase ainda não é necessário verificar se o palpite está correto ou não e não precisamos de fazer loops.
Na versão final do programa, não vamos querer imprimir o número aleatório gerado, mas nesta fase é útil para podermos testar o programa.
{{% /hint %}}


### Fase 2: Verificação do palpite

Nesta fase queremos que o programa verifique se o palpite do utilizador é igual ao número aleatório gerado.
Se o palpite estiver correto, o programa deve imprimir "Parabéns! Adivinhaste o número!".
Se o palpite estiver incorreto, o programa deve imprimir "Palpite incorreto. Tenta novamente.".

{{% hint tip %}}
Nesta fase não é necessário fazer loops.
A ideia é testar se a lógica de verificação do palpite está correta para 1 tentativa.
{{% /hint %}}

### Fase 3: Loop de tentativas

Nesta fase queremos que o programa continue a pedir palpites ao utilizador até que ele adivinhe o número correto.
O programa deve usar um loop `while` para continuar a pedir palpites enquanto o palpite estiver incorreto.
Quando o utilizador adivinhar o número correto, o programa deve imprimir "Parabéns! Adivinhaste o número!" e terminar.
O utilizador tem um número ilimitado de tentativas para adivinhar o número.

### Fase 4: Dicas de maior/menor

Nesta fase queremos adicionar dicas ao programa para ajudar o utilizador a adivinhar o número correto.
Se o palpite for um número válido, mas o palpite estiver incorrecto:
- Se o palpite for menor que o número aleatório, o programa deve imprimir "O número secreto é maior do que o teu palpite.".
- Se o palpite for maior que o número aleatório, o programa deve imprimir "O número secreto é menor do que o teu palpite.".

### Fase 5: Número de tentativas

Nesta fase queremos que o programa conte o número de tentativas que o utilizador fez para adivinhar o número correto.
Quando o utilizador adivinhar o número correto, o programa deve imprimir também o número de tentativas que foram necessárias para acertar o número.

Nesta fase, queremos também que se o utilizador inserir um valor inválido (não é um número ou não está entre 1 e 20), o programa deve imprimir uma mensagem de erro e pedir o palpite novamente.
Caso o número seja inválido, essa tentativa não deve ser contada.

### Fase 6: Permitir sair do jogo

Nesta fase queremos adicionar a funcionalidade de permitir ao utilizador sair do jogo a qualquer momento.
Para isso, o programa deve permitir que o utilizador insira a palavra "sair" quando lhe é pedido um número.
Se o utilizador escrever "sair" em vez de dar um número, o jogo deve terminar.

### Fase 7: Limite de tentativas

Nesta fase queremos adicionar um limite ao número de tentativas que o utilizador pode fazer para adivinhar o número correto.
O utilizador deve ter no máximo 6 tentativas para adivinhar o número.
Se o utilizador não conseguir adivinhar o número dentro dessas 6 tentativas, o programa deve imprimir "Fim de jogo! Tentativas esgotadas. O número era X." (onde X é o número aleatório)

### Fase Bónus: Escolher dificuldade

Depois das 7 fases anteriores, temos um jogo de adivinhação de números bastante completo e funcional!
Podemos parar de trabalhar no jogo aqui.

No entanto, para um desafio extra opcional, podemos adicionar uma fase bónus onde o utilizador antes de começar pode escolher um nível de dificuldade.

Os níveis de dificuldade podem ser:
- 1 - Fácil: número entre 1 e 10, 3 tentativas no máximo
- 2 - Médio: número entre 1 e 20, 6 tentativas no máximo
- 3 - Difícil: número entre 1 e 50, 15 tentativas no máximo

A forma como podemos pedir ao utilizador para escolher o nível de dificuldade é pedindo para inserir 1, 2 ou 3 no início do programa.
Com base na escolha do utilizador, o programa deve ajustar o intervalo do número aleatório e o número máximo de tentativas permitidas.