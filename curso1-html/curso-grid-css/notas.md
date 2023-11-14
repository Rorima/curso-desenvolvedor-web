# Notas

A Udemy não está funcionando bem no momento, então decidi procurar por um curso de CSS *grid* para aprender melhor como posicionar os elementos em uma página.

[Este](https://www.youtube.com/playlist?list=PLYgzkrmJnLwpeeGgdADYq3cE2yUwLLTOv) foi o curso que usei para aprender *grid*.

## Terminologia do *grid*

* Uma *grid* pode ter qualquer número de linhas e qualquer número de colunas
* O *grid* é definido dentro do *grid container*
* Dentro de um *grid*, cada uma das células é chamada de *grid item* ou "célula de *grid*"
* Uma linha ou uma coluna em um *grid container* se chama *grid track*. O termo *row track* é usado para linhas, e o termo *column track* é usado para colunas, mas ambas podem ser chamadas de *grid track*
* As *grid lines* podem ser verticais ou horizontais, que são as linhas numeram as células. Elas têm sua própria numeração
* Quando se pega mais de uma célula de *grid*, se tem uma *grid area*. Não importa o tamanho, contanto que mais de uma célula esteja selecionada
* Os espaços entre as células são chamados de *grid gaps* ou *grid gutters*
* Há também o "aninhamento de *grid*", que é uma *grid* dentro da outra

## CSS *Grid* vs *Flexbox*

O *grid* não substitui o *flexbox*. São tecnologias diferentes que servem para propósitos diferentes, e que podem ser usadas em conjunto.

Alguns fatos sobre os dois:

1. Com o CSS *Grid*, é possível fazer coisas que o *flexbox* não consegue.
2. Com o *Flexbox*, é possível fazer coisas que o *grid* não consegue.

| Flexbox | CSS Grid |
|---|---|
| Unidimensional (trabalha com coluna **OU** linha) | Bidimensional (trabalha com coluna **E** linha) |
| Tarabalha-se a partir do conteúdo | Trabalha-se a partir da definição da *grid* |
| Trabalha-se com a distribuição de espaços | Trabalha-se com a ocuapção de espaços pré-definidos |
| Bom para porções de leiaute | Bom para leiautes mais completos |
| Bom para elementos de UI | Bom para leiautes mais abrangentes |
| Requer mais *media queries* | Requer menos *media queries* |

## Sua Primeira *Grid*

`./arquivo1.html`

Crie um arquivo HTML e no *body* coloque uma série de divs com um conteúdo qualquer, e deixe todas essas divs envolvidas por uma div com a classe *wrapper*, pois ela é o conteiner, e ela receberá a propriedade `display: grid`.

```html
<body>
    <div class="wrapper">
        <div>1</div>
        <div>2</div>
        <div>3</div>
        <div>4</div>
        <div>5</div>
        <div>6</div>
        <div>7</div>
        <div>8</div>
    </div>
</body>
```

Vamos estilizar um pouco essas divs para ficar mais fácil de ver. Esta estilização não dem nada a ver com o *grid*, é somente para ficar mais fácil de ver.

```css
.wrapper div {
    background-color: royalblue;
    padding: 1rem;
}

.wrapper div:nth-child(even) {
    background-color: skyblue;
}
```

Agora colocamos que o *wrapper* tem um `display: grid;`. Vamos adicionar outro atributo que é muito importante, o `grid-template-columns:`, que recebe o valor do tamanho de cada coluna que teremos. Vamos fazer três colounas:

```css
.wrapper {
    display: grid;
    grid-template-columns: 200px 200px 200px;
}
```

Você pode perceber que os elementos já são separados em fileiras automaticamente.

**Outras Medidas**

Também é possível utilizar outros tipos de de medida:

```css
.wrapper {
    display: grid;
    grid-template-columns: 20% 20%;
}
```

**Espaço entre as Células**

Podemos dar um espaço para que as células não fiquem tão juntas:

```css
.wrapper {
    display: grid;
    grid-template-columns: 200px 200px 200px;
    gap: 1rem;
}
```

Se o espaço for o mesmo para as linhas e as colunas, podemos usar um só atributo, chamado de `gap`:

```css
.wrapper {
    display: grid;
    grid-template-columns: 200px 200px 200px;
    gap: 1rem;
}
```

**Especificando Linhas**

```css
.wrapper {
    display: grid;
    grid-template-columns: 200px 200px 200px;

    /*Especificando as linhas*/
    grid-template-rows: 200px 200px 200px; 
    
    column-gap: 1rem;
    row-gap: 1rem;
}
```

***Grid* explícita e *grid* implícita**

Na *grid* explícita, nós codificamos exatamente como vai ser a *grid*, e se novos elementos forem adicionados, eles não irão seguir o padrão. Já na *grid* implícita, todos os elementos novos que forem adicionados ficarão no mesmo padrão da *grid*. Até agora fizemos somente uma *grid* explícita. Se novos elementos forem adicionados e novas linhas forem criadas, elas não seguirão o padrão de 200px.

Usando o atributo `grid-auto-rows` vai garantir que qualquer linha criada automaticamente vai seguir um padrão:

```css
.wrapper {
    display: grid;
    grid-template-columns: 200px 200px 200px;

    /*
        Este comando não precisa estar aqui, já que temos o
        `grid-auto-rows`. Apagando este comando, todas as
        linhas já seriam automáticas
    */
    grid-template-rows: 200px 200px 200px;
    
    column-gap: 1rem;
    row-gap: 1rem;

    /*Adicionando um valor padrão para novas linhas*/
    grid-auto-rows: 200px;
}
```


```css
```
```css
```
```css
```
```css
```
```css
```
```css
```
```css
```
```css
```
```css
```
```css
```

Onde parei:
https://www.youtube.com/watch?v=gpV7b-vVVD0&list=PLYgzkrmJnLwpeeGgdADYq3cE2yUwLLTOv&index=4&ab_channel=dpw

Curso flexbox:
https://www.youtube.com/watch?v=SAl0i5rzX3U&list=PLYgzkrmJnLwo8IDD2v7RP_oyE3yzc1fY4&ab_channel=dpw