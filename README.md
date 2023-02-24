**UNIVERSIDADE LUSÓFONA, Programação Web, 22-23**

# Laboratório 2:  *Website com Quizz 🔘 e CSS 🖌* 

## Objetivo
* Estender o website criado no Laboratório 2 com mais algumas páginas.
* Explorar os vários tipos de entrada de formulário através da construção de um quizz sobre a cidade que escolheu.
* Praticar CSS, experimentando todos os seletores CSS aprendidos. O objetivo é conhecer os comandos de formatação, não fazer um website com super UX design! Isso aprenderá na disciplina Interação Humano Máquina.

## Prazo de Entrega
* Este laboratório deverá ser concluido até dia 26.2, sendo posteriormente avaliado. 

## Pré-requisitos
* Deve ter concluído o lab1
* VS Code com a extensão live server. Permitir-lhe-á visualizar a página, à medida que for editando. Basta clicar, no canto inferior direito, em `Go live`.
* Utilize `Shift+Alt+F` para indentar código
* Reveja se necessário os slides da aula teórica disponiveis no Moodle. É a fazer que aprenderá!
* Deverá ter instalado o git no seu computador.

# 1. [Git](https://github.com/ULHT-PW/git) para sincronizar **PythonAnyWhere &rarr; GitHub &rarr; PC**  

Consdideremos que tem o projeto no PythonAnywhere e está num PC da escola sem o seu projeto. Vamos criar um repositorio no PythonAnywhere, e sincronizar  **PythonAnyWhere &rarr; GitHub &rarr; PC**.

1. Crie um repositório no GitHub com nome pw-labs
2. Abra uma consola do PythonAnywhere e crie, dentro da pasta `web`, um repositorio git e sincronize-o com o GitHub:
   ```Bash
   > git init .
   > git add .
   > git commit -m "o meu lab1"
   > git branch -M main
   > git remote add origin https://github.com/<seu-username-no-github>/pw-labs
   > git push -u origin main
   ```
   
3. Vamos agora enviar o projeto do PythonAnywhere para o seu novo repositorio. Dê push do projeto que está no PythonAnyWhere para o GitHub. PAra tal, siga as instruções no GitHub. 

4. Clone (descarregue uma cópia) do GitHub para o seu computador, ficando com uma cópia do que tem até agora feito no PythonAnyWhere:
    1. abra um processador de comandos (prima a tecla Windows e escreva `cmd` ou `Powershell`)
    2. escolha a pasta onde quer colocar o repositório (navegando com o comando `cd nome-de-pasta` para entrar numa determinada pasta)
    3. clone o seu repositório com o comando:
    ```bash
    > git clone https://github/seuUserName/nome_do_repo .
    ```

# 2. Nova estrutura das páginas

1. Todas as suas páginas HTML deverão ser reestruturadas para integrar com elementos semânticos HTML5. No `body` deverá ter:

    1. dentro de um elemento `header` deverá incluir o cabeçalho, com o titulo do site e fotografia 
    
    3. o menu de navegação deverá estar dentro dum elemento `nav`
    
    5. o conteúdo dentro de um elemento `main`. Dentro do `main`, use elementos `section` caso existam várias secções (cada elemento `section` deverá ter dentro um elemento `h1` ou outro, e parágrafos `p`). Por exemplo, na página multimedia.html, utilize elementos `section` para dividir os vários conteúdos que tem (fotos, video e poema).
    
    7. um novo elemento `footer` com o seu nome, numero, universidade, e ano, tudo numa linha.
    
3. Nas imagens, vídeos e mapa, recorra a elemento `figure` e `figcaption`, tendo neste ultimo um elemento `details` para mostrar/esconder mais detalhes sobre a imagem.

Se visualizar no seu navegador as páginas HTML, verá que estes elementos nada mudaram em termos visuais. No entanto, estes permitirão aplicar estilos. Neste primeiro laboratório aplicará a esta estrutura estilizações simples. No entanto, no lab4 esta estruturação com elementos semânticos permitirá criar layouts dinâmicos, configurados pelo CSS.

<img src="https://user-images.githubusercontent.com/42048382/221050105-d8db51a6-7e51-4a2d-9a4a-09871035f87e.png" width="200px">

# 3. Página com Quizz 🤓

1. Crie uma nova página HTML `quizz.html` que tenha o mesmo cabeçalho das restantes.

1. Esta página irá ter um formulário com um quizz sobre a cidade. Deverá fazer perguntas de vários tipos sobre a cidade, o formulário sendo enviado para um endereço de email (quando desenvolvermos o back-end, poderá processar os dados enviados e apresentar ao utilizador uma resposta). Nesta página irá experimentar todos os tipos de entrada que foram falados na aula. Implemente os passos a seguir descritos.

1. Insira um elemento h3 com a palavra Quizz.

3. insira um parágrafo com um texto introdutório a explicar que nesta página será feito um quizz para testar se o utilizador conhece bem a cidade que a página apresenta.

1. Crie dentro do form um elemento `fieldset`, coma uma legenda (por exemplo, "Quizz sobre «cidade»", "City quizz", "Mostre que conhece «cidade»"

1. Crie outro elemento `fieldset` para inserção de dados pessoais, com o titulo "info" (`fieldset` dentro de `fieldset`, sim 🤩!):
   * Nome
   * apelido
   * email (input de tipo email)

1. Crie outro elemento `fieldset` para inserção das perguntas do quizz, com título "perguntas":

1. Crie um quiz com perguntas sobre a cidade, explorando de forma imaginativa elementos input. 
    * Deverá utilizar cada um dos seguintes tipos (atributo `type`):
        * `text`
        * `radio`
        * `checkbox`
        * `date`
        * `image`
        * `color`
        * `number`
        * `range`
 
    * Deverá garantir que utiliza pelo menos uma vez cada um dos seguintes atributos:
        * `value`
        * `placeholder`
        * `autocomplete`
        * `size`
        * `max` e `min`
        * `maxlength`
        * `form`
        * `multiple`
        * `autofocus`
        * `required`
        * `pattern`

1. Inclua também perguntas usando os seguintes elementos:
   * `select`
   * `datalist`
   * `label`

1. Inclua  um elemento `textarea` para inserir um comentário

1. Inclua um elemento do tipo `submit` para submeter o seu formulário.

1. No marcador form, inclua os seguintes atributos `<form method="POST" action="mailto: seuemail@gmail.com" enctype="multipart/form-data">`. Assim, quem abrir a sua página, ao submeter o formulário enviará por email para si este.  
   * Quando desenvolvermos o back-end, poderá processar os dados enviados e apresentar ao utilizador uma resposta.

 
# 4. Página HTML5 & CSS 😎

1. Crie uma nova página HTML intitulada `html5-css.html` que tenha o mesmo cabeçalho das restantes.
 
2. Insira um elemento `h3` com o título HTML5 e CSS. Esta página terá 3 secções, estruturadas com elementos `section`, onde cada uma terá um breve texto e uma tabela. 
 
3. Crie uma secção com o elemento intitulada HTML 5 onde deverá incluir:
    1. uma frase introdutória sobre o HTML5
    2. um tabela com 3 colunas:
       * na primeira coluna, os elementos semânticos HTML5 apresentados na aula, um por linha. 
       * na segunda coluna, para cada elemento HTML5 deverá indicar se o usou ou não nalguma página, recorrendo a um icon adequado (use icones Google, por exemplo ❌ e ✔, ou então 😀 e 🙄)
       * na terceira coluna deverá incluir uma breve descrição a explicar onde utilizou. 
 
4. Crie uma subsecção intitulada CSS onde deverá incluir:
    1. uma frase introdutória sobre CSS 
    2. uma tabela com todos os tipos de seletores CSS, um por linha. Na segunda coluna deverá indicar se o usou ou não nalguma página, recorrendo a um icon adequado (use os icones Google), e na terceira coluna deverá incluir um breve comentário a explicar como este funciona e onde o utilizou. 
    3. uma tabela com todos os combinadores de seletores apresentados na aula, um por linha. Na segunda coluna deverá indicar se o usou ou não nalguma página, recorrendo a um icon adequado (use os icones Google), e na terceira coluna deverá incluir um breve comentário a explicar como este funciona e onde o utilizou.

# 5. Estilização com CSS 🖌

Para a definição dos estilos será usado um único ficheiro estilos.css, que guardará todos os estilos usados nas páginas. Em cada ficheiro HTML deverá existir um link para este ficheiro, de modo a permitir usar os estilos.

1. crie o ficheiro estilos.css 
 
2. deverá utilizar todos os tipos de seletores (tipo, classe, id, atributo, pseudo-classe, pseudo-elemento, veja o slide 17 do PPT dos selectores), em pelo menos 3 sítios diferentes do seu HTML. A seguir sugere-se onde utilizar alguns destes. Não se esqueça de registar na tabela onde os utiliza!
 
3. Deverá utilizar pelo menos três composições de selectores (descendentes, filhos `>`, adjacentes `~`, imediatamente adjacentes `+`, agrupados `,`), veja o slide 32). 

5. Escolha e use uma [fonte Google](https://fonts.google.com/) no o seu website. Veja no [video](https://lh3.googleusercontent.com/-PO1uxMdsqoA/Xpmn6QDUKHI/AAAAAAAA2qg/l1B6uSjPRu0eg_3EZkjp04siUjJb1dQxQCK8BGAsYHg/s0/2020-04-17.gif) como se procede:
    1. escolha uma fonte que gosta
    2. selecione os estilo que quer usar (no caso de apresentar várias variantes)
    3. copie na janela direita o link e insira no head de cada uma das suas páginas HTML
    4. especifique no ficheiro CSS que quer usar essa fonte em todo o lado, usando o seletor universal * e a regra CSS para especificar a familia da fonte, por exemplo 
`* {font-family: 'Syne Mono', monospace;} `
 
6. Configure a cor de background do seu website, assim como de alguns elementos HTML5 usando seletores adequados. em particular, na pagina do Quizz, use cores diferentes para o fundo de cada umdos `fieldsets`.
 
7. Para os elementos do seu menu:
    * utilize selectores de pseudo-classe (`link`, `visited`, `hover`, `active`) para configurar cores para os links (veja o slide 27)
    * especifique com selectores `before` e `after` (slide 31) efeitos que acontecem quando passa com o rato por cima de cada elemento do menu (use `hover`). 
    * No HTML inclua, antes de cada palavra do menu, um icon adequado premindo no teclado em `Windows + .` (pode escolher por exemplo 🏡 para home, 📷 para multimédia,🗺 localizaçao, etc). Pode também explorar [aqui](https://www.w3schools.com/icons/icons_reference.asp) ícones Google, Awesome Font ou Bootstrap; clique em "try" para entender como se usam:
       * deve incluir no elemento head um link ao repositório de icons. 
       * veja como se especifica o icon que pretende inserir (depende do repositório). Estes icones são extremamente leves e variados.

8. Nas tabelas e no poema os selectores de pseudo-classe assim como os pseudo-elementos, explorando cores de fonte e fundos diferentes. Por exemplo, introduza variedades de cor nas linhas pares e impares das tabelas.
  
9. Recorra a seletores de atributo (slide 25) para configurar as cores e larguras das molduras em redor das imagens da página interesses.
 
10. No texto descritivo (por exemplo no parágrafo da introdução), use os pseudo-elementos first-letter, first-line para estilizá-lo.
 
11. nos seus formulários, remova o uso de quebras de linha `br` para colocar inputs em linhas diferentes. Em vez disso, transforme os elementos `input` em blocos através da propriedade `display`. 
 
13. estilize as molduras (border) das imagens e iframes usando seletores, sem recorrer a classes.
 
# 6. Menu
Garanta que o menu inclui hiperlinks para as 2 novas páginas criadas (semelhante a todas as páginas).


# 7. Página Multimédia 🎬

Na página `multimedia.html` atualize e crie:

1.	Um elemento `h3` intitulado Fotografias. Escolha no Google pelo menos 3 fotografias emblemáticas do lugar que escolheu.  	 	 
2. Utilize a aplicação Paint.Net para gravar duas versões das fotografias em tamanhos definidos (o comando Ctrl+R ou Ctrl+W permite abrir um interface que permite configurar o tamanho das imagens, consoante a aplicação; deverá igualmente recortar as fotografias com o comando "crop", para as proporções indicadas): 
    1. Grande, de 600x400 pixels de largura. Altere o nome, incluindo _grande no fim (e.g., lisboa_grande.jpg).
    2. Pequena, de 120x80 pixels de largura. Altere o nome, incluindo _pequena (e.g., lisboa_pequena.jpg).
    3. Guarde as 6 fotografias na pasta `imagens`. 
    4. Insira na página HTML as imagens de 100px de largura,dentro de um único parágrafo, uma ao lado da outra. Especifique o campo `alt`. Aninhe o elemento `img` dentro de um hiperlink `a`, com hiperligação para a fotografia grande correspondente e com o atributo `target="foto"`.
 ```bash
 <a href=""><img src="" alt=""></a>
 ```
    5. Crie um elemento `iframe` 800x600 com `name="foto"`, para visualizar em grande a fotografia que for clicada. Especifique na iframe,no atributo `src`, uma das imagens, para que apareça
    6. antes das fotografias, escreva um texto que apresente as fotografias em baixo.
3.	Um elemento `h3` intitulado Poema. Escolha um poema que de alguma forma associa ao lugar escolhido. Escreva, usando tamanhos diferentes, o título numa linha, o nome do poeta na seguinte, seguindo-se o poema, em itálico. Todo o texto deverá estar centrado. 
4. Defina identificadores `id` em cada título `h3`. Por baixo do elemento `h3` Multimédia, coloque hiperlinks "âncora" para cada uma das secções desta página (fotografias, video, poema). 


# 8. Página Informações ℹ

Na página `info.html`:
1. Altere a tabela do forma a integrar pelo menos um `colspan` e um `rowspan`

# 9. Site atualizado online!

1. Depois de verificar que tudo está operaciona, vamos enviar o seu projeto para o GitHuB e para o PythonAnyWhere.
2. Primeiro, envie para o GitHub com os comandos:
   * `git add .`
   * `git commit -m "lab2"`
   * `git push`
3. Depois, duma consola do PythonAnywhere (Console Bash), descarregue o seu projeto atualizado do GitHub com o comando  `git pull`
4. No menu superior, clique em "Web"
5. Clique no botão verde "Reload ...." para ativar as alterações
6. Clique no seu dominio. O seu site está online 🥳
    
 
# 9. Fim 🎉

Submeta o domínio da sua aplicação no Moodle até à sua próxima aula prática

Esperamos que tenha gostado de aplicar os conhecimentos de HTML5 e CSS no seu website &#127760;!

