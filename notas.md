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

### Breve história do HTML5

Em 2004, a W3C iniciou o desenvolvimento do XHTML 2.0. Frustrados com os rumos do HTML 2.0, um grupo de profissionais e corporações iniciaram o desenvolvimento do HTML5. Este grupo é chamado de Web Hipertext Application Technology Working Group, ou a WHATWG. O grupo iniciou as especificações do que eles chamaram de Web Applications 1.0. Em 2007, a W3C adotou as especificações do WHATWG e o renomeou para HTML5. Desde então, o XHTML 2.0 foi revogado, deixando apenas o HTML5 como substituto do HTML 4.0

**O que tem de especial no HTML 5**

* Ele mantém a compatibilidade com as versões anteriores do HTML;
* Contém muitas características que facilitam o desenvolvimento de apilcações;
* Foco no desenvolvimento de Web Application;
* Inclui melhores campos de formulário e suporte a vários tipos de API's.

Essas características ajudam a profissionais a criarem web e mobile applications, disponibilizar vídeos e aúdios, além de um conteúdo mais interativo.

### Primeira página HTML

Toda linguagem baseada em tags tem tags que abrem e tags que fecham. Uma tag é um nome entre os símbolos `<` e `>`. Para criar uma página HTML precisamos criar um arquivo e salvá-lo com a extensão `.html`. Dentro do arquivo precisamos das tags `<html></html>`. A barra indica que a tag está sendo fechada.

```html
<html>
</html>
```

Dentro da tag HTML colocaremos uma tag chamada `<head>` e outra chamada `<body>`. Essas são as tags mais importantes do HTML. Na *head* fica todo o cabeçalho do documento, enquanto que na *body* fica o corpo da página. 

```html
<html>
    <head>
        
    </head>
    <body>
        
    </body>
</html>
```

Algumas coisas nas páginas estão expostas para as pessoas lerem, mas outras coisas estão expostas somente para as máquinas. No início do nosso arquivo nós temos que mostrar que tipo de arquivo ele é para que a máquina entenda. Para isso, é necessário digitar uma tag no início do arquivo. Esta é a tag: `<!DOCTYPE html>`. Essa tag não precisa ser fechada.

```html
<!DOCTYPE html>

<html>
    <head>

    </head>
    <body>
        
    </body>
</html>
```

As tags HTML podem ter atributos. A tag principal HTML, por exemplo, tem o atributo `lang=""`, que indica o idioma usado na página. Utilizaremos o português do Brasil.

```html
[...]
<html lang="pt-BR">
[...]
```

Os `[...]` indicam que há código antes e depois. Eles foram colocados ali para que todo o código não precisasse ser repetido.

#### Mais tags

**`<title></title>`**

Esta tag define o título da página. O título é o que aparece lá em cima, na aba do navegador.

Esta tag deve ser colocada entre as tags `<head>`.

```html
<head>
    <title>Primeira Página</title>
</head>
```

**`<meta>`**

Esta tag tem vários atributos. Entre eles, há um chamado "charset", que é a configuração de caracteres. Geralmente utilizamos o "utf-8", que abrange uma grandíssima parte dos caracteres das línguas do mundo.

Esta tag deve ser colocada entre as tags `<head>`.

```html
<head>
    <meta charset="utf-8">
</head>
```

**`<p></p>`**

Esta tag cria parágrafos. Entre elas podemos escrever o que quisermos, e o texto que escrevermos será mostrado para o leitor da página.

Esta tag deve ser colocada entre as tags `<body>`.

```html
<body>
    <p>Até manhã!</p>
</body>
```

#### Como ver seus sites

Para ver os sites que você criou, basta abrir os arquivos HTML no seu navegador. Você pode fazer isso arrastando o arquivo para o seu navegador. Todas as mudanças que você fizer podem ser vistas na página se você recarregá-la.

#### Espaços vazios e comentários

Se você adicionar múltiplos espaços em branco nos seus parágrafos, eles não serão vistos e ficará como se você tivesse colocado somente um espaço:

```html
<p>Até                                       amanhã!</p>
```

Todos esses espaços não serão vistos.

Para adicionar espaços em branco, você vai precisar usar um código. Este é o código do espaço em branco: `&nbsp;`. Usando ele você pode adicionar quantos espaços em branco você quiser.

```html
<p>Até &nbsp;&nbsp;&nbsp;&nbsp; amanhã!</p>
```

Usando o esse mesmo e comercial juntamente com o ponto e vírgula no final é possível adicionar vários símbolos. Pesquise por HTML entities e você vai ver uma lista com todas eles. Aqui vão alguns:

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

### Explorando o head

```html

```
```html

```
```html

```