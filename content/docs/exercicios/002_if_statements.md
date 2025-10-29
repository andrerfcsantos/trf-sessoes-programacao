+++
date = '2025-10-28T20:06:10+01:00'
draft = false
title = 'If statements'
+++


# Exercícios de If statements

## Material de apoio

- [Notas sessão 2](../sessoes/002_20250926/#estrutura-condicional-if)
- [Notas sessão 3](../sessoes/003_20251010/#mais-sobre-condicionais)
- [Notas sessão 4](../sessoes/004_20251020/#exercícios-práticos-sobre-condicionais)
- [MDN Web Docs - Comparison operators](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/Comparison_Operators)
- [MDN Web Docs - if...else](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/if...else)
- [MDN Web Docs - Logical operators](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/Logical_Operators)
- [Deno Documentation - Prompts](https://docs.deno.com/examples/prompts/)
- [MDN Number()](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Number/Number)
- [MDN isNaN()](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/isNaN)

## Exercícios

{{% hint tip %}}
Criar um ficheiro separado para a resolução de cada um destes exercícios.
{{% /hint %}}

1. A lei portuguesa estabelece os critérios para uma pessoa poder ser candidata à presidência da república.
   Uma pessoa pode ser candidata se:
    - tiver pelo menos 35 anos
    - for cidadã portuguesa
    - tiver o direito de voto

   Criar um programa que com base nas variáveis `idade` (inteiro), `cidadania` (string) e `direitoVoto` (booleano), imprima se a pessoa pode ser candidata ou não à presidência da república.

   ```javascript
   let idade = 40; // exemplo de idade
   let cidadania = "portuguesa"; // exemplo de cidadania
   let direitoVoto = true; // exemplo de direito de voto
   
   // escrever o if statement aqui
   ```
   {{% hint tip %}}
   O programa pode assumir que os valores das variáveis vão estar corretos (por exemplo, `idade` será sempre um número inteiro, `cidadania` será sempre uma string, e `direitoVoto` será sempre um booleano).
   {{% /hint %}}
2. Modificar o programa anterior para receber inputs do utilizador usando a função `prompt()`.

   {{% hint tip %}}
   Lembrar de converter o input da idade para número usando a função `Number()`. 
   {{% /hint %}}
3. Modificar o programa anterior para validar os valores inseridos pelo utilizador
   Os requisitos de validação são:
    - A idade deve ser um número válido entre 0 e 120
    - A cidadania deve ser uma string não vazia
    - O direito de voto deve ser "sim" ou "nao" (e convertido para booleano)
   {{% hint tip %}}
   Usar a função `isNaN()` para verificar se o valor inserido é um número válido.
   {{% /hint %}}
4. O programa seguinte recebe como input uma idade dada pelo utilizador, converte-a para um número e a seguir mostra uma mensagem a dizer quantos anos o utilizador tem ou um erro caso a idade seja inválida:
   ```javascript
   let idadeString = prompt("Qual é a tua idade?");
   let idade = Number(idadeString);
   if (isNaN(idade)) {
    console.log("Por favor, insere um número válido para a idade.");
   } else {
    console.log("Tens " + idade + " anos.");
   }
   ```
   No entanto, se o utilizador disser que tem 1 ano, a mensagem vai estar no plural:
   ```bash
   $ Qual é a tua idade? 1
   Tens 1 anos.
   ```
   Neste caso "anos" está no plural, mas devia estar no singular "ano".
   Modifica o programa para que "anos" fique no singular quando o utilizador tiver 1 ano apenas.
   