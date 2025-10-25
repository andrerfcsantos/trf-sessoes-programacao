+++
date = '2025-10-28T20:06:10+01:00'
draft = false
title = 'If statements (Parte 2)'
+++

# Exercícios de If statements

## Material de apoio

- [Notas sessão 5](../sessoes/005_20251103/) - Notas da última sessão
- [MDN Number()](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Number) - Tem exemplos de como usar `Number()` e qual o "algoritmo" usado para converter strings (ou outros valores!) para números.
- [MDN isNaN()](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/isNaN) - Explica como funciona `isNaN()` e tem exemplos de uso.
- [Deno Prompts](https://docs.deno.com/examples/prompts/) - Explica como usar a função `prompt()` no Deno, assim como algumas variantes para pedir input ao utilizador (ver `confirm()` por exemplo)
- [MDN Deno.exit()](https://docs.deno.com/api/deno/~/Deno.exit) - Explica como usar `Deno.exit()`.

## Exercícios

{{% hint tip %}}
Criar um ficheiro separado para a resolução de cada um destes exercícios.
{{% /hint %}}

1. **Validador de Login**

   Escreve um programa para simular o típico caso de login num sistema informático.
   
   O programa deve pedir ao utilizador para inserir um nome de utilizador e uma palavra-passe e deve validar se o nome de utilizador e a palavra-passe estão corretos.
   
   Neste momento o sistema apenas tem um utilizador cujo username é `admin` e a palavra-passe é `admin123`.
  
   Se o nome de utilizador e a palavra-passe estiverem corretos, o programa deve imprimir `"Login bem-sucedido!"`.
   Caso contrário, deve imprimir `"Nome de utilizador ou palavra-passe incorretos."`
2. **Maior de dois números**
   
   Escreve um programa que peça ao utilizador para inserir dois números e imprima qual dos dois números é maior. 
   Se os números forem iguais, o programa deve imprimir `"Os dois números são iguais."`

   Pontos a considerar neste exercício:
    - Validar se os inputs são números válidos.
    - Se algum dos inputs não for um número válido, o programa deve imprimir uma mensagem de erro e terminar imediatamente com um código de saída diferente de zero.
   