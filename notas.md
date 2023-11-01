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

[VEJA SE ISSO É NECESSÁRIO]
### Fundamentos de HTML

Crie uma pasta chamada "fundamentos" e cole dentro desta pasta fotos de pizza. Crie um arquivo chamado "pizza-calabresa.html" e vamos começar a programar.

A linguagem HTML tem tags e atributos. Utilizaremos o atributo `lang` para definir o idioma da página.

```html
<html lang="pt-BR">
</html>
```

Precisamos de mais duas tags dentro da nossa tag HTML. O nome delas é `<head>` e `<body>`. Ambas precisam ser fechadas. Precisamos fazer isso em todas as páginas que fizermos.

```html
<html lang="pt-BR">
    <head>

    </head>
    <body>
        
    </body>
</html>
```

Vamos adicionar a tag `<title>` dentro da tag `<head>`. Dentro da tag `<title>` podemos colocar o nome do título da nossa página, que é o nome dado à aba da página. Como estamos fazendo uma página sobre pizza de calabresa, colocaremos isso como o título.

```html
<html lang="pt-BR">
    <head>
        <title>Pizza Calabresa</title>
    </head>
    <body>

    </body>
</html>
```

Com a tag `<h1>` podemos escolher um título à página, mas desta vez o título será mostrado no corpo da página.

```html
<html lang="pt-BR">
    <head>
        <title>Pizza Calabresa</title>
    </head>
    <body>
        <h1>Pizza Calabresa</h1>
    </body>
</html>
```
```html

```
```html

```