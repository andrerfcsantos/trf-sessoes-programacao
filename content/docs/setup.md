+++
date = '2025-09-22T19:11:17+01:00'
draft = false
title = 'Setup do ambiente de desenvolvimento'
+++

# Setup do ambiente de desenvolvimento

{{< image src="images/logos/js_logo.png" alt="Javascript logo" title="Javascript logo" class="img-small" >}}
{{< image src="images/logos/ts_logo.png" alt="Typescript logo" title="Typescript logo" class="img-small" >}}

Aqui encontras os passos para configurar um ambiente de desenvolvimento no teu computador que permite programar em Javascript e Typescript.

O editor de texto escolhido é o Visual Studio Code (VSCode) e para executar Javascript (JS) e Typescript (TS) usaremos Deno.

## Instalar o Deno

{{< image src="images/logos/deno_logo.png" alt="Deno logo" title="Deno logo" class="img-small" >}}

Para instalar o Deno visita a página oficial:
 - [Instruções de instalação do Deno](https://deno.land/manual@v1.36.4/getting_started/installation)

Para Windows, os passos são:

1. Abrir uma Powershell. Procurar no windows por "Powershell" e clicar na aplicação que aparece.
2. Copiar e colar o seguinte comando na Powershell:
   ```powershell
   iwr https://deno.land/install.ps1 -useb | iex
   ```
3. Carregar enter para executar o comando e esperar que acabe
4. Depois disto o `deno` deve ficar instalado. 
5. Para verificar que a instalação correu bem, na mesma Powershell, copiar e colar o seguinte comando e carregar enter:
   
   ```powershell
   deno --version
   ```
    - O comando deve mostrar a versão do Deno instalada. Se isto acontecer, o Deno está instalado corretamente e não é preciso fazer mais nada.
    - Se houver um erro a dizer que o comando `deno` não foi reconhecido, algo correu mal na instalação. Tenta repetir os passos anteriores.

### Porque precisamos do Deno?
É muito comum o Javascript ser executado no browser, dentro de páginas web.
No entanto, é também possível usar Javascript fora da web e criar programas que correm diretamente no computador.

O Deno permite executar Javascript e Typescript fora do browser e fora de uma página web, o que é ideal para aprender a linguagem.
Além de suportar Jaascript, o Deno suporta também Typescript sem precisar de grande configuração adicional!


{{% hint info %}}
**Node.js**

[Node.js](https://nodejs.org/en) é outra plataforma muito popular para executar Javascript fora do browser.
No entanto, o Deno é mais simples de instalar e usar, o que o torna ideal para aprender a linguagem.
{{% /hint %}}

## Instalar o Visual Studio Code (VSCode) com extensões

{{< image src="images/logos/vscode_logo.png" alt="Visual Studio Code logo" title="Visual Studio Code logo" class="img-small" >}}

Para instalar o VSCode visita a página de downloads oficial:
 - [Instruções de instalação do VSCode](https://code.visualstudio.com/download)

Para Windows, os passos são:
1. Abrir o browser e ir à [página de downloads do VSCode]((https://code.visualstudio.com/download))
2. Fazer download do instalador para Windows
3. Correr o instalador e seguir os passos

Depois de instalado, abre o VSCode para instalar as extensões necessárias para programar em Javascript e Typescript com Deno:

1. Para aceder às extensões, clicar no ícone de quadrados no lado esquerdo do VSCode ({{< image src="images/icons/vscode_ext_icon.png" alt="Javascript logo" title="Javascript logo" class="img-tiny" >}})
2. Na barra de pesquisa, procurar por "Deno" e instalar a extensão com mais downloads (deverá ser [esta](https://marketplace.visualstudio.com/items?itemName=denoland.vscode-deno))
3. Procurar por "Prettier" e instalar a mais popular (deverá aparecer [esta](https://marketplace.visualstudio.com/items?itemName=esbenp.prettier-vscode))
4. Procurar por "Code Runner" e instalar a mais popular (deverá aparecer [esta](https://marketplace.visualstudio.com/items?itemName=formulahendry.code-runner))

### Porque precisamos do VSCode e destas extensões?

O Visual Studio Code (VSCode) é um editor de texto simples e rápido, o que o torna bastante popular entre programadores.
 
Atráves da instalação de extensões, suporta várias linguagens de programação e ferramentas, o que o torna um editor muito completo e versátil.

Uma explicação breve das extensões recomendadas anteriormente:
- **Deno**: Esta extensão faz com que o VSCode reconheça coisas específicas do Deno. Também adiciona funcionalidades para Javascript e Typescript ao VSCode que tornam mais agradável programar nestas linguagens dentro do VSCode.
- **Prettier**: Esta extensão formata o código automaticamente, tornando-o mais fácil de ler e entender. Também ajuda a manter um estilo consistente no código. No fundo, como o nome sugere, torna o código mais bonito!
- **Code Runner**: Esta extensão permite correr código diretamente no VSCode através de um botão de play. Faz com que não seja preciso usar linha de comandos e dá uma forma fácil e rápida de correr ficheiros JS e TS.

### Preparar VSCode para programar o VSCode

Agora que temos o VSCode instalado e Deno instalados, já podemos começar a programar!

Como sugiro que faças isso:

1. Cria uma pasta no teu computador onde queres começar a guardar os projectos de programação.
   Podes-lhe chamar `programacao` por exemplo, ou outro nome que faça sentido para ti.
2. Dentro dessa pasta, cria uma nova pasta para o teu primeiro projecto.
   Podes-lhe chamar `introducao` por exemplo.
3. Abre o VSCode e clica em "File" > "Open Folder..." e escolhe a pasta do projecto que acabaste de criar.
4. Com a pasta aberta, podes agora começar a criar ficheiros Javascript e Typescript!
   {{% hint %}}
   Ficheiros javascript devem ter a extensão `.js` e ficheiros Typescript devem ter a extensão `.ts`.
   Começa por criar um ficheiro chamado `hello.js` e escreve o seguinte código dentro:
   ```javascript
   console.log("Hello, world!");
   ```
   {{% /hint %}}

Para ser mais fácil trabalhar com o código, recomendo também que faças uma configuração adicional ao VSCode:

1. Vai a este repositório do GitHub ([andrerfcsantos/vscode-deno](https://github.com/andrerfcsantos/vscode-deno)) e faz download dos conteúdos como zip:
   
   {{< image src="images/screenshots/vscode_conf_folder_download.png" alt="Image with arrows on how to download a repository as .zip from the Github interface" title="Dowload repo as .zip" class="img-medium" >}}
2. Extrai o conteúdo do zip para uma pasta no teu computador
3. Dentro da pasta extraída, deves ver uma pasta chamada `.vscode`
4. Copia essa pasta `.vscode` para dentro da pasta do teu projecto (a que abriste no VSCode)
5. Reinicia o VSCode (fecha e volta a abrir)

{{% hint tip %}}
Sempre que quiseres usar outra pasta para programar, volta a fazer o passo 3 (abrir a nova pasta no VSCode) e o passo 4 (copiar a pasta `.vscode` para dentro da nova pasta do projecto).
{{% /hint %}}

#### O que faz a pasta `.vscode`?

Esta pasta contém configurações específicas para o VSCode que tornam a experiência de programar em Javascript e Typescript com Deno mais agradável dentro do Visual Studio Code.
Estas configurações incluem:

- Dizer ao VSCode para:
  - Sugerir instalar as extensões que foram sugeridas anteriormente (Deno, Prettier, Code Runner).
    Com isto, o VSCode vai detectar se as extensões estão instaladas e, se não estiverem, sugere a instalação.
  - Usar o Prettier para formatar ficheiros JS e TS.
- Dizer à extensão "Code Runner":
  - Para usar o Deno para correr ficheiros JS e TS
  - Para guardar os ficheiros automaticamente antes de os correr (previne que haja erros por o ficheiro não estar guardado).
- Configurar o Prettier para formatar o código automaticamente ao guardar ficheiros JS e TS.

Usar estas configurações no teu projecto torna a experiência de programar mais fluida e agradável.
Evita também que tenhas que usar linha de comandos para correr os teus ficheiros JS e TS, e que tenhas que configurar a formatação de código manualmente.
