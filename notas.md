# Notas

Estas são as anotações que fiz do curso [Curso Desenvolvedor Web Completo + 10 Projetos](https://www.udemy.com/course/curso-desenvolvedor-web-completo/) da Udemy.

Meu objetivo com essas anotações não é ensinar nada. Só quero registrar o meu aprendizado. Sendo assim, o material vai ficar parecido com o jeito que foi ensinado no curso. Se o curso pula etapas, também pularei, e se ele detalha outras, talvez eu não detalhe se eu já souber.

## Curso I - HTML5

O que iremos aprender:

* Introdução à linguagem;
* Conceitos básicos;
* Adicionar imagens;
* Adicionar links;
* Novos elementos estruturais.

### Breve História do HTML5

Em 2004, a W3C iniciou o desenvolvimento do XHTML 2.0. Frustrados com os rumos do HTML 2.0, um grupo de profissionais e corporações iniciaram o desenvolvimento do HTML5. Este grupo é chamado de Web Hipertext Application Technology Working Group, ou a WHATWG. O grupo iniciou as especificações do que eles chamaram de Web Applications 1.0. Em 2007, a W3C adotou as especificações do WHATWG e o renomeou para HTML5. Desde então, o XHTML 2.0 foi revogado, deixando apenas o HTML5 como substituto do HTML 4.0

**O que tem de especial no HTML 5**

* Ele mantém a compatibilidade com as versões anteriores do HTML;
* Contém muitas características que facilitam o desenvolvimento de aplicações;
* Foco no desenvolvimento de Web Application;
* Inclui melhores campos de formulário e suporte a vários tipos de API's.

Essas características ajudam a profissionais a criarem web e mobile applications, disponibilizar vídeos e áudios, além de um conteúdo mais interativo.

### Primeira Página HTML

Toda linguagem baseada em *tags* tem tags que abrem e *tags* que fecham. Uma *tag* é um nome entre os símbolos `<` e `>`. Para criar uma página HTML precisamos criar um arquivo e salvá-lo com a extensão `.html`. Dentro do arquivo precisamos das *tags* `<html></html>`. A barra indica que a *tag* está sendo fechada.

```html
<html>
</html>
```

Dentro da *tag* HTML colocaremos uma *tag* chamada `<head>` e outra chamada `<body>`. Essas são as *tags* mais importantes do HTML. Na *head* fica todo o cabeçalho do documento, enquanto que na *body* fica o corpo da página. 

```html
<html>
    <head>
        
    </head>
    <body>
        
    </body>
</html>
```

Algumas coisas nas páginas estão expostas para as pessoas lerem, mas outras coisas estão expostas somente para as máquinas. No início do nosso arquivo nós temos que mostrar que tipo de arquivo ele é para que a máquina entenda. Para isso, é necessário digitar uma *tag* no início do arquivo. Esta é a *tag*: `<!DOCTYPE html>`. Essa *tag* não precisa ser fechada.

```html
<!DOCTYPE html>

<html>
    <head>

    </head>
    <body>
        
    </body>
</html>
```

As *tags* HTML podem ter atributos. A *tag* principal HTML, por exemplo, tem o atributo `lang=""`, que indica o idioma usado na página. Utilizaremos o português do Brasil.

```html
[...]
<html lang="pt-BR">
[...]
```

Os `[...]` indicam que há código antes e depois. Eles foram colocados ali para que todo o código não precisasse ser repetido.

#### Mais *tags*

**`<title></title>`**

Esta *tag* define o título da página. O título é o que aparece lá em cima, na aba do navegador.

Esta *tag* deve ser colocada entre as *tags* `<head>`.

```html
<head>
    <title>Primeira Página</title>
</head>
```

**`<meta>`**

Esta *tag* tem vários atributos. Entre eles, há um chamado "charset", que é a configuração de caracteres. Geralmente utilizamos o "utf-8", que abrange uma grandíssima parte dos caracteres das línguas do mundo.

Esta *tag* deve ser colocada entre as *tags* `<head>`.

```html
<head>
    <meta charset="utf-8">
</head>
```

**`<p></p>`**

Esta *tag* cria parágrafos. Entre elas podemos escrever o que quisermos, e o texto que escrevermos será mostrado para o leitor da página.

Esta *tag* deve ser colocada entre as *tags* `<body>`.

```html
<body>
    <p>Até manhã!</p>
</body>
```

#### Como Ver Seus Sites

Para ver os sites que você criou, basta abrir os arquivos HTML no seu navegador. Você pode fazer isso arrastando o arquivo para o seu navegador. Todas as mudanças que você fizer podem ser vistas na página se você recarregá-la.

#### Espaços Vazios e Comentários

Se você adicionar múltiplos espaços em branco nos seus parágrafos, eles não serão vistos e ficará como se você tivesse colocado somente um espaço:

```html
<p>Até                                       amanhã!</p>
```

Todos esses espaços não serão vistos.

Para adicionar espaços em branco, você vai precisar usar um código. Este é o código do espaço em branco: `&nbsp;`. Usando ele você pode adicionar quantos espaços em branco você quiser.

```html
<p>Até &nbsp;&nbsp;&nbsp;&nbsp; amanhã!</p>
```

Usando esse mesmo e comercial juntamente com o ponto e vírgula no final é possível adicionar vários símbolos. Pesquise por "HTML entities" e você vai ver uma lista com todas eles. Aqui vão alguns:

```html
<p>Algumas entidades:</p>

<p>Mostrando euro: 15.99 &euro;</p>
<p>Mostrando libra: 15.99 &pound;;</p>

<p>Mostrando o sinal de maior que: 3 &gt; 2</p>
<p>Mostrando o sinal de menor que: 2 &lt; 3</p>
```

**Comentários**

Os comentários podem ser colocados dentro destes símbolos: `<!-- -->`. Comentários não são mostrados para os leitores. Você pode usá-los para explicar uma parte difícil do seu código ou para se lembrar de algo mais tarde. Não guarde segredos nesses comentários, pois um usuário consegue ter acesso a ele se ele vir o código fonte da página, que pode ser facilmente acessado através da opção "inspecionar elemento" quando se clica com o botão direito na página.

```html
<body>
    <!--Este é um comentário de uma linha-->
    <!--
        Este comentário
        tem várias
        linhas
    -->
    <p>Até &nbsp;&nbsp;&nbsp; manhã!</p>
</body>
```

### Explorando o *head*

O *head* é a parte pensante da página. Nela ficam algumas partes importantes da página, como os metadados, estilos, scripts e etc. Como analogia, o *head* é a cabeça, o *body* é o corpo, e o *html* é o conjunto dos dois.

Estes são os 5 elementos do *head*:

* *title element*;
* *base element*;
* *link element*;
* *meta element*;
* *style element*;

#### Aplicando CSS ao Documento HTML

Crie um arquivo como o da seção anterior, mas cujo título seja "Unidade 02 - Elemento Head".

Existem várias maneiras de aplicar estilos em uma página HTML. Vamos mostrar só uma por enquanto. O estilo serve para personalizar a aparência de uma página.

Abra e feche a *tag* `<style>` dentro do *head* do arquivo.

```html
<head>
    <meta charset="utf-8">
    <title>Unidade 02 - Elemento Head</title>

    <style>
    </style>
</head>
```

Dentro dela, mudaremos a cor de fundo de nosso site. Para isso, precisamos modificar o *body*.

```html
<head>
    [...]
    <style>
        body {}
    </style>
</head>
```

As cores podem ser definidas pelo formato hexadecimal ou outros formatos, como RGB ou ainda o nome das cores em inglês. Se quiser saber como são as cores no formato hexadecimal, pesquise online por "hex color picker".

Utilize o atributo "background" para mudar a cor de fundo.

```html
<head>
    [...]
    <style>
        body {
            background: #f0f0f0;
        }
    </style>
</head>
```

**Alterando a Fonte**

Vamos escrever um texto no *body*:

```html
<body>
    <p>Esta é a segunda unidade.</p>
</body>
```

Utilize o atributo "font-family" para alterar a fonte do *body*, que consequentemente irá alterar a fonte de toda a página:

```html
<head>
    [...]
    <style>
        body {
            background: #f0f0f0;
            font-family: Arial, Helvetica, sans-serif;
        }
    </style>
</head>
```

Demos três fontes diferentes como opção para o navegador. A fonte só é selecionada se ela estiver instalada no navegador do usuário. Assim, se a fonte "Arial" não estiver presente, o navegador irá usar a "Helvetica", mas se ela não estiver presente, então o navegador irá utilizar a "sans-serif". É sempre bom indicar mais de uma fonte.

**Alterando a Cor do Texto**

Utilize o atributo "color" para alterar a cor da fonte. Você pode usar cores hexadecimais também.

```html
<head>
    [...]
    <style>
        body {
            background: #f0f0f0;
            font-family: Arial, Helvetica, sans-serif;
            color: #747474;
        }
    </style>
</head>
```

#### Aplicando o JavaScript

Para adicionar código JavaScript na sua página, abra e feche a *tag* `<script>` dentro da *tag* *head*.

```html
<head>
    [...]
    <script></script>
</head>
```

Vamos criar um parágrafo no nosso *body*. Dentro da *tag* inicial do parágrafo vamos colocar um atributo chamado "id" com o valor chamado "nome" para que possamos acessá-lo utilizando JavaScript:

```html
<body>
    <p>Esta é a segunda unidade.</p>
    <p id="nome"></p>
</body>
```

Agora, entre as nossas *tags* `<script>` iremos escrever uma função:

```html
<head>
    <script>
        function escreverNome() {
            nome.innerHTML = "Paulo de Tarso";
        }

        window.onload = escreverNome;
    </script>
</head>
```

Com essa função, assim que a página for carregada o nome será escrito na página.

### Texto do Documento

Iremos aprender a trabalhar com o texto do documento. 

#### Cabeçalhos

Adicionaremos um texto de cabeçalho. O cabeçalho é o texto que tem maior destaque na página, como o título. Não é o título que fica lá em cima, na aba do navegador, mas o título da página que o leitor irá ler. Para isso, utilizaremos a *tag* `<h1>`.

```html
<body>
    <h1>Baleia jubarte presa em rede ganha a ajuda de pescadores no litoral de SP</h1>
</body>
```

Existem seis *tags* de cabeçalho. Elas vão de 1 a 6. Quanto maior for o número, menor é será a fonte. Quanto menor o número, mais destaque o texto dentro da *tag* terá.

**`<hgroup>`**

Esta *tag* agrupa *tags* de cabeçalho para deixar tudo mais organizado.

```html
<body>
    <hgroup>
        <h1>Baleia jubarte presa em rede ganha a ajuda de pescadores no litoral de SP</h1>
        <h2>Animal estava a cerca de 4 km da praia de Mongaguá. Segundo biólogos, espécie migra para águas tropicais nesta época do ano.</h2>
    </hgroup>
</body>
```

#### Parágrafos

Para adicionar parágrafos, utilize a *tag* `<p>`. Entre elas digite o texto que você deseja. Cada parágrafo é separado por padrão em um bloco diferente na página.

```html
<body>
    [...]

    <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Magni, nemo iusto laudantium assumenda fuga fugit, blanditiis doloribus nobis, enim ipsa quo? Ducimus vel reprehenderit a odit ipsum facere voluptate fuga?</p>

    <p>Lorem ipsum dolor sit, amet consectetur adipisicing elit. In culpa vel mollitia voluptas fugit, eum exercitationem nulla cum nobis cumque. Doloremque iste fuga consectetur placeat blanditiis recusandae nihil esse facere!</p>
</body>
```

#### Quebrando Linhas

Da mesma maneira que é necesário um código para mostrar mais do que um espaço em branco seguido, há também uma *tag* usada para quebrar linhas, já que na página, o texto não vai pra linha de baixo se você der ENTER.

```html
<body>
    <p>
        Nome: Chaves;
        Endereço: 8;
        País: México;
        Profissão: Criança.
    </p>
</body>
```

Todo o texto do parágrafo acima é mostrado em uma única linha. Podemos criar um parágrafo para cada uma dessas informações, entretanto, porque há um espaço padrão entre cada parágrafo, essas informações ficariam bastante separadas.

Para adicionar quebras de linha precisamos utilizar a *tag* `<br>`. Esta *tag* não precisa ser fechada. "br" significa "break row", ou "quebrar linha" em português.

```html
<body>
    <p>
        Nome: Chaves;<br>
        Endereço: 8;<br>
        País: México;<br>
        Profissão: Criança.
    </p>
</body>
```

#### Usando Marcações

Aqui vão algumas *tags* de marcação:

```html
<body>
    <p>Texto em <b>negrito</b></p>
    <p>Texto em <i>itálico</i></p>
    <p>Texto em <u>sublinhado</u></p>
    <p>Texto em <sub>subscrito</sub></p>
    <p>Texto em <sup>superescrito</sup></p>
    <p>Texto em <s>riscado</s></p>
</body>
```

#### Trabalhando com Lista

Em HTML existem três tipos listas, a sem ordem, a ordenada e a descritiva:

```html
<body>
    <h1>Listas</h1>

    <h2>Listam sem Ordem</h3>
    <ul>
        <li>Brasil</li>
        <li>Argentina</li>
        <li>Uruguai</li>
        <li>Venezuela</li>
    </ul>

    <h2>Lista em Ordem</h2>
    <ol>
        <li>Alonso</li>
        <li>Vettel</li>
        <li>Massa</li>
        <li>Button</li>
    </ol>

    <h2>Lista Descritiva</h2>
    <!--Definindo a lista-->
    <dl>
        <!--Definindo um termo-->
        <dt>Unidade 01</dt>
        <!--Descrevendo o termo-->
        <dd>
            Apresentação do Curso<br>
            Melhores softwares para usar neste curso
        </dd>

        <!--Definindo outro termo-->
        <dt>Unidade 02</dt>
        <!--Descrevendo-o-->
        <dd>
            Uma breve história do HTML5<br>
            Especificações do HTML5<br>
            HTML5 VS HTML4<br>
        </dd>
    </dl>
</body>
```

* ul: "unordered list" ou "lista não ordenada";
* li: "list item" ou "item da lista";
* ol: "ordered list" ou "lista ordenada";
* dl: "description list" ou "lista descritiva";
* dt: "description term" ou "termo da descrição";
* dd: "description definition" ou "definição da descrição".

Uma lista não ordenada é apresentada com pontos antes de cada item. Uma lista ordenada é apresentada com números antes de cada item. Uma lista descritiva é uma lista de termos com uma descrição para cada um dos termos.

**Tipos**

É possível editar os pontos de uma lista também. Para a lista não ordenada, podemos utilizar os tipos `square`, `cricle` e `none`.

```html
<ul type="circle">
        <li>Brasil</li>
        <li>Argentina</li>
        <li>Uruguai</li>
        <li>Venezuela</li>
    </ul>
```

Para a lista ordenada, podemos utilizar:

* `a`: Mostra os itens em ordem alfabética com letras minúsculas;
* `A`: Mostra os itens em ordem alfabética com letras maiúsculas;
* `I`: Mostra os itens com letras romanas.

#### Usando `<i>` e `<em>`

A aparência das *tags* `<i>` e `<em>` é a mesma, mas a diferença entre elas é que a *tag* `<i>` é usada para palavras de outras línguas, termos técnicos, textos em itálico, citações e etc. Já a *tag* `<em>` é usada para dar ênfase, como mostrar a sílaba tônica de uma palavra ou dar ênfase na palavra de uma sentença, por exemplo, quando ela tem uma pronúncia diferente.

A *tag* `<i>` também tem o atributo "lang", no qual você pode indicar a língua do termo que você está usando.

```html
<body>
    <h1>Diferença entre as <i>tags</i> &lt;i&gt; e &lt;em&gt;</h1>
    
    <h2>Usando a <i>tag</i> &lt;i&gt;</h2>
    <p>Isso deixa um <i lang="fr">je ne sais quoi</i> no ar.</p>
    
    <p>"<i>O que estou fazendo é usar ingredientes italianos e combiná-los para criar pratos com um gosto moderno para revigorar nossos clientes</i>", disse Steven.</p>

    <h2>Usando a <i>tag</i> &lt;em&gt;</h2>
    <p><em>Gatos</em> são animais fofos.</p>
</body>
```

Como visto, na aparência não há muita diferença. A maior diferença é a sintática.

#### Usando `<b>` e `<strong>`

Essas duas tags fazem a mesma coisa aparentemente, pois elas deixam o texto em negrito. A diferença entre as duas é somente na semântica. Quando quisermos realçar uma palavra, utilizamos `<strong>`. Geralmente utilizamos `<b>` mais do que `<strong>`.

### Como Adicionar Imagens

Vamos aprender a inserir uma imagem em nossa página web.

Para adicionar uma imagem utilizaremos a tag `<img>`. Ela se fecha sozinha. Ela tem alguns atributos. O primeiro que iremos utilizar é o `src` ("source" ou "fonte" do inglês), que indica a fonte da imagem. Você pode dar o caminho de um diretório que leva até a imagem, ou um link da Internet. Utilizaremos os dois.

Outros atributos:

* `width`: largura da imagem;
* `height`: altura da imagem;
* `title`: texto que aparece quando o mouse é colocado sobre a imagem;
* `alt`: texto que aparece se a imagem não for mostrada.

```html
<body>
    <!--Imagem de uma pasta-->
    <img src="./imagens/pexels-nyara-aquino-5643427.jpg" height="200" alt="Imagem ilustrativa de pato com laranja" title="Pato com Laranja">

    <!--Imagem da Internet-->
    <img src="https://external-content.duckduckgo.com/iu/?u=http%3A%2F%2F4.bp.blogspot.com%2F-BfKwJQgzWcc%2FUjM2ey19flI%2FAAAAAAAABQg%2FWu5L19XUO_I%2Fs1600%2FSAM_3338.JPG&f=1&nofb=1&ipt=677571b2d65e41fdfe0a04e4e459ccdffbfd1a77b469758fd7d99ee29a338e32&ipo=images" height="200" alt="Imagem ilustrativa de pato com laranja" title="Pato com Laranja">
<body>
```

#### Alterando o alinhamento da imagem

Usando o arquivo anterior como exemplo, observe que a imagem aparece em uma linha, enquanto que o texto aparece em outra linha. Isso é porque a imagem é um elemento e o texto é outro elemento. Elementos são separados automaticamente.

Vamos supor que queiramos que o texto apareça ao lado direito da imagem. Podemos fazer isso utilizando estilos (que faz parte do CSS). Para isso, utilizaremos o estilo em linha, que é o estilo feito dentro da *tag* que queremos estilizar.

Como um atributo da *tag* `<img>` digite `style="float:left";`. Isso significa que a imagem vai ficar presa à esquerda e tudo o que estiver debaixo dela vai vir para a direita dela. "float" significa "flutuar" em português.

```html
[...]
<img src="./imagens/pexels-nyara-aquino-5643427.jpg" height="200" alt="Imagem ilustrativa de pato com laranja" title="Pato com Laranja" style="float:left;">
<img src="https://external-content.duckduckgo.com/iu/?u=http%3A%2F%2F4.bp.blogspot.com%2F-BfKwJQgzWcc%2FUjM2ey19flI%2FAAAAAAAABQg%2FWu5L19XUO_I%2Fs1600%2FSAM_3338.JPG&f=1&nofb=1&ipt=677571b2d65e41fdfe0a04e4e459ccdffbfd1a77b469758fd7d99ee29a338e32&ipo=images" height="200" alt="Imagem ilustrativa de pato com laranja" title="Pato com Laranja" style="float:left;">
[...]
```

Os comandos em CSS não utilizam igual (=) como os atributos em HTML. Eles utilizam dois pontos (:) e terminam com ponto e vírgula (;).

Depois de fazer isso, você vai perceber que o texto estará muito próximo da imagem. Para resolver, vamos adicionar uma margem na parte direita da última imagem:

```html
[...]
<img 
    src="https://external-content.duckduckgo.com/iu/?u=http%3A%2F%2F4.bp.blogspot.com%2F-BfKwJQgzWcc%2FUjM2ey19flI%2FAAAAAAAABQg%2FWu5L19XUO_I%2Fs1600%2FSAM_3338.JPG&f=1&nofb=1&ipt=677571b2d65e41fdfe0a04e4e459ccdffbfd1a77b469758fd7d99ee29a338e32&ipo=images" height="200" 
    alt="Imagem ilustrativa de pato com laranja" 
    title="Pato com Laranja" 
    
    style="float:left; margin-right:20px;"
>
[...]
```

Podemos adicionar uma borda também:

```html
<img 
    src="https://external-content.duckduckgo.com/iu/?u=http%3A%2F%2F4.bp.blogspot.com%2F-BfKwJQgzWcc%2FUjM2ey19flI%2FAAAAAAAABQg%2FWu5L19XUO_I%2Fs1600%2FSAM_3338.JPG&f=1&nofb=1&ipt=677571b2d65e41fdfe0a04e4e459ccdffbfd1a77b469758fd7d99ee29a338e32&ipo=images" 
    height="200" 
    alt="Imagem ilustrativa de pato com laranja" 
    title="Pato com Laranja" 
    
    style="float:left; margin-right:20px; border: solid 3px #000;"
>
```

Significado:
* `solid`: a borda é sólida, uma linha única ao redor do elemento;
* `3px`: a borda tem 3 pixels de expessura;
* `#000`: a borda tem a cor preta em hexadecimal.

**Aplicando o estlo de forma diferente**

Desta vez iremos abrir uma *tag* `<style>` na parte *head*, e criaremos uma classe que terá um conjunto de instruções que iremos adicionar a uma determinada *tag*.

Para adicionar uma classe a um elemento HTML, utilizamos a palavra *class*. Vamos adicionar uma classe a nossa imagem:

```html 
<img 
    src="https://external-content.duckduckgo.com/iu/?u=https%3A%2F%2Fwww.teleculinaria.pt%2Fwp-content%2Fuploads%2F2017%2F11%2FPato-com-laranja-18.jpg&f=1&nofb=1&ipt=53c77f3d81e01c30b9ffd5c679df60624a73e92555c7f12dba2af1ef5dc4c962&ipo=images"
    height="200"
    alt="Imagem de pato com laranja"
    title="Pato com laranja"
    class="img-prato"
>
```

Agora vamos criar a *tag* `<style>` e vamos mudar o alinhamento da imagem:

```html
<head>
    <style>
        .img-prato {
            float: right;
            margin-left: 10px;
            border: 1px solid #000;
        }
    </style>
</head>
```

**Usando o atributo `clear`**

Este atributo é usado para modificar o fluxo de elementos com a propriedade `float`. Ela especifica o que deve acontecer com um elemento que está ao lado de um elemento flutuante.

Vamos supor que queiramos deixar um texto ao lado da imagem na parte de baixo dela; para isso, vamos criar uma classe para o h4 abaixo dela:

```html
<h4 class="abaixo">Segredo do chef</h4>
```

Agora vamos modificar a *tag* `<style>` e vamos adicionar o atributo `clear: right;` no h4:

```html
[...]
<style>
    .img-prato {
        float: right;
        margin-left: 10px;
        border: 1px solid #000;
    }
    
    .abaixo {
        clear: right;
    }
</style>
[...]
```

Agora o texto foi para baixo da imagem. Colocando a opção `clear: right;` no h4 estamos falando que este elemento h4 não permite nada flutuando em seu lado direito, sendo assim, este elemento é empurrado para baixo, enquanto o elemento que flutua fica acima.

#### Utilizando elementos *figure* e *figcaption*

A *tag* `<figure>` configura uma imagem em um documento, e a *tag* `<figcaption>` define uma legenda para a imagem.

```html
<figure>
    <img
        src="https://external-content.duckduckgo.com/iu/?u=https%3A%2F%2Ftse1.mm.bing.net%2Fth%3Fid%3DOIP.dQD4_4ZCo6DymuTzpZwNIQHaE8%26pid%3DApi&f=1&ipt=86c13989c3e00e1b738cc120b90e90802b529b6c9f8fb427902e2e8d5e593549&ipo=images"
        alt="Baleia Jubarte pulando para fora d'água"
        title="Baleia Jubarte"
    >
    <figcaption>Baleia Jubarte pulando para fora d'água. Fonte: Infoescola</figcaption>
</figure>
```

A *tag* `<figure>` é bastante usada também para mostrar ilustrações, diagramas, listas de códigos e etc.

Estilizando as *tags* `<figure>` e `<figcaption>`:

```html
<style>
    figure {
        border: 2px solid;
        float: right;
    }
    
    figcaption {
        text-align: center;
        background: aliceblue;
    }
</style>
```

### Como Adicionar Links

Um link é quando vinculamos uma página à outra.

É preciso utilizar a *tag* `<a>`, que significa "âncora". Devemos utilizar também o atributo `href`, que vai receber o nome do arquivo.

Vamos criar um link que aponta para uma página com o prato do dia. Para isso, ambos os arquivos devem estar na mesma pasta.

```html
<p><a href="./prato-dia.html">Conheça o prato do dia.</a></p>
```

Podemos também vincular uma página externa:

```html
<p><a href="https://duckduckgo.com/?hps=1&q=pato+com+laranja&atb=v377-1&iax=images&ia=images">Veja imagens de pato com laranja.</a></p>
```

Podemos usar um atributo chamado `target` para abrir o site externo em outra aba:

```html
<p><a href="https://duckduckgo.com/?hps=1&q=pato+com+laranja&atb=v377-1&iax=images&ia=images" target="_blank">Veja imagens de pato com laranja.</a></p>
```

#### Compreendendo Links Relativos

Vamos supor que queiramos encontrar um arquivo que está localizado em outra pasta; para isso devemos utilizar os links relativos.

Em links relativos o ponto "." é usado para se referir à pasta atual, e dois pontos seguidos ".." são usados para se referir à pasta anterior. As pastas são separadas por barra "/".

Vamos acessar a pasta "receitas" e linkar o arquivo "prato-dia.html":

```html
<p><a href="./receitas/prato-dia.html">Conheça o prato do dia.</a></p>
```

No código acima nós utilizamos o ponto para nos referir à pasta atual, então usamos a barra e escolhemos a pasta "receitas", e logo em seguida escolhemos o arquivo "prato-dia.html".

Agora vamos usar o caminho de uma imagem que está em uma pasta filha da pasta mãe (isto é, uma pasta irmã):

```html
<p>Esta é a página da <a href="../fundamentos/pizza-calabresa.html">pizza de calabresa</a>.</p>
```

Se quisermos ir ainda mais acima, podemos utilizar outro `../`, e podemos ficar repetindo isso o quanto for necessário.

```html
<p><a href="../../../../pagina-inicial.html">Página inicial</a>.</p>
```

#### Links para Dentro da Própria Página

Inicialmente você precisa ter um destino do link. Para isso é necessário adicionar um `id` ao elemento para o qual você quer levar o usuário, que é um código de identificação. O `id` é único e não é repetido na página.

```html
<h2 id="aperitivos">Aperitivos</h2>
```

Agora no `href` do link nós colocamos o nome do *id* com uma cerquilha (#) no começo:

```html
<a href="#aperitivos">Aperitivos</a>
```

#### Criando um Link em uma Imagem

Rodeie a *tag* `<img>` pela *tag* `<a>` e assim você terá uma imagem que serve como um link quando clicada.

```html
<a href="https://www.google.com.br/">
    <img src="https://upload.wikimedia.org/wikipedia/commons/thumb/2/2f/Google_2015_logo.svg/2560px-Google_2015_logo.svg.png" alt="Imagem da logo do Google" width="100%">
</a>
```

### Criação de listas

**Unidade 8 - Arquivo 1**

Para criar uma lista, inicialmente definimos o tipo da lista, e logo em seguida os itens da lista.

Os itens da lista são definidos com a *tag* `<li>`, que significa "list item" ou "item da lista" em português.

Vamos definir uma lista não ordenada `<ul>`:

```html
<body>
    <ul>
        <li>Brasil</li>
        <li>Argentina</li>
        <li>Mexico</li>
        <li>Angola</li>
    </ul>
</body>
```

Agora, vamos criar uma lista ordenada `<ol>`:

```html
<body>
    <ol>
        <li>Brasil</li>
        <li>Argentina</li>
        <li>Mexico</li>
        <li>Angola</li>
    </ol>
</body>
```

**Tipos de lista**

Usando CSS podemos mudar o tipo da lista:

```html
<head>
    <style>
        li {
            list-style-type: circle;
        }
    </style>
</head>
```

Estes são os tipos:

* `armenian`: Utiliza numeração armênia tradicional
* `circle`: Utiliza um círculo preenchido como marcador de item de lista
* `decimal`: Utiliza números decimais como marcador de item de lista
* `decimal-leading-zero`: Utiliza números decimais com zeros à esquerda
* `disc`: Utiliza um círculo preenchido como marcador de item de lista (similar a `circle`)
* `georgian`: Utiliza numeração georgiana tradicional
* `lower-alpha`: Utiliza letras minúsculas (a, b, c, etc.) como marcador de item de lista
* `lower-greek`: Utiliza letras gregas minúsculas como marcador de item de lista
* `lower-latin`: Utiliza letras latinas minúsculas como marcador de item de lista
* `lower-roman`: Utiliza numerais romanos minúsculos como marcador de item de lista
* `none`: Remove o marcador de item de lista, fazendo com que os itens da lista apareçam sem nenhum símbolo
* `square`: Utiliza um quadrado preenchido como marcador de item de lista
* `upper-alpha`: Utiliza letras maiúsculas (A, B, C, etc.) como marcador de item de lista
* `upper-latin`: Utiliza letras latinas maiúsculas como marcador de item de lista
* `upper-roman`: Utiliza numerais romanos maiúsculos como marcador de item de lista
* `inherit`: Herda a propriedade `list-style-type` do elemento pai
* `initial`: Define a propriedade `list-style-type` para seu valor padrão
* `unset`: Reinicia a propriedade list-style-type para seu valor herdado, se existir; caso contrário, define-o para o valor inicial.

**Definindo uma imagem como marcador de item de lista**

Utilize o atributo `list-style-image: url();` para escolher uma imagem como marcador da lista. Utilize uma imagem muito pequena.

```html
<style>
    ul {
        list-style-type: none;
        list-style-image: url('https://external-content.duckduckgo.com/iu/?u=http%3A%2F%2Fclipartmag.com%2Fimages%2Fstar-with-transparent-background-20.png&f=1&nofb=1&ipt=05d1e258e4c2e914c57e2de457e905cbcd10076f65cd432859e9a1821d50d315&ipo=images'); 
        padding-left: 300px;
        
    }

    li {
        margin-bottom: 10px;
    }
</style>
```


```html

```
```html

```
```html

```
```html

```
```html

```
```html

```
```html

```
```html

```
```html

```
```html

```
```html

```
```html

```
```html

```
```html

```
```html

```
```html

```
```html

```
```html

```
```html

```
```html

```
```html

```
```html

```
