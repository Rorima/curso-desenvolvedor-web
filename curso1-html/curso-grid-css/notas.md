# Notas

A Udemy não está funcionando bem no momento, então decidi procurar por um curso de CSS *grid* no Youtube para aprender melhor como posicionar os elementos em uma página.

[Este](https://www.youtube.com/playlist?list=PLYgzkrmJnLwpeeGgdADYq3cE2yUwLLTOv) foi o curso que usei para aprender *grid*.

## Terminologia do *grid*

* Uma *grid* pode ter qualquer número de linhas e qualquer número de colunas
* O *grid* é definido dentro do *grid container*
* Dentro de um *grid*, cada uma das células é chamada de *grid item* ou "célula de *grid*"
* Uma linha ou uma coluna em um *grid container* se chama *grid track*. O termo *row track* é usado para linhas, e o termo *column track* é usado para colunas, mas ambas podem ser chamadas de *grid track*
* As *grid lines* podem ser verticais ou horizontais, que são as linhas que numeram as células. Elas têm sua própria numeração
* Quando se pega mais de uma célula de *grid*, se tem uma *grid area*. Não importa o tamanho, contanto que mais de uma célula esteja selecionada
* Os espaços entre as células são chamados de *grid gaps* ou *grid gutters*
* Há também o "aninhamento de *grid*", que é uma *grid* dentro da outra

## CSS *Grid* vs *Flexbox*

O *grid* não substitui o *flexbox*. São tecnologias diferentes que servem para propósitos diferentes, e que podem ser usadas em conjunto.

Alguns fatos sobre os dois:

1. Com o CSS *grid*, é possível fazer coisas que o *flexbox* não consegue.
2. Com o *flexbox*, é possível fazer coisas que o *grid* não consegue.

| Flexbox | CSS Grid |
|---|---|
| Unidimensional (trabalha com coluna **OU** linha) | Bidimensional (trabalha com coluna **E** linha) |
| Tarabalha-se a partir do conteúdo | Trabalha-se a partir da definição da *grid* |
| Trabalha-se com a distribuição de espaços | Trabalha-se com a ocupação de espaços pré-definidos |
| Bom para porções de leiaute | Bom para leiautes mais completos |
| Bom para elementos de UI | Bom para leiautes mais abrangentes |
| Requer mais *media queries* | Requer menos *media queries* |

## Sua Primeira *Grid*

`./arquivo1.html`

Crie um arquivo HTML e no *body* coloque uma série de divs com um conteúdo qualquer, e deixe todas essas divs envolvidas por uma div com a classe *wrapper*, pois ela é o contêiner, e ela receberá a propriedade `display: grid`.

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

Vamos estilizar um pouco essas divs para ficar mais fácil de ver. Esta estilização não tem nada a ver com o *grid*, é somente para ficar mais fácil de ver.

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

Também é possível utilizar outros tipos de medida:

```css
.wrapper {
    display: grid;
    grid-template-columns: 20% 20%;
}
```

**Espaço entre as Células**

Podemos dar um espaço para que as células não fiquem tão juntas utilizando o `column-gap` e o `row-gap`:

```css
.wrapper {
    display: grid;
    grid-template-columns: 200px 200px 200px;
    column-gap: 1rem;
    row-gap: 1rem;
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

Usando o atributo `grid-auto-rows` vai garantir que qualquer linha criada automaticamente siga o padrão:

```css
.wrapper {
    display: grid;
    grid-template-columns: 200px 200px 200px;

    /*
        Este comando não precisa estar aqui, já que temos o
        `grid-auto-rows`. Por causa do último comando, todas as linhas já são automáticas
    */
    grid-template-rows: 200px 200px 200px;
    
    column-gap: 1rem;
    row-gap: 1rem;

    /*Adicionando um valor padrão para novas linhas*/
    grid-auto-rows: 200px;
}
```

## `repeat()` e `minmanx()`

O `repeat()` é uma espécie de função que possibilita repetir valores.

No atributo `grid-template-rows: 200px 200px 200px;`, nós especificamos as três colunas. Podemos fazer isso de maneira mais simplificada utilizando o `repeat()`. Primeiro colocamos quantas vezes queremos repetir, e depois colocamos o tamanho das colunas.

```css
.wrapper {
    display: grid;
    grid-template-columns: repeat(3, 200px);
    gap: 1rem;
    grid-auto-rows: 200px;
}
```

Podemos colocar colunas customizadas também junto com essas do `repeat()`:

```css
.wrapper {
    display: grid;
    grid-template-columns: 100px repeat(3, 200px) 10%;
    gap: 1rem;
    grid-auto-rows: 200px;
}
```

Assim temos uma coluna de 100px, três de 200px, e uma que pega 10% da página.

**`minmax()`**

Esta função especifica um tamanho mínimo e um tamanho máximo pra cada linha e cada coluna. Isso significa que o tamanho do elemento vai mudar de acordo com o tamanho da tela. Quanto maior a tela, maior vai ser o elemento, até ele atingir o tamanho máximo. Quanto menor for a tela, menor vai ser o elemento, até ele atingir o tamanho mínimo.

```css
.wrapper {
    display: grid;
    grid-template-columns: 100px repeat(3, 200px) 10% minmax(10%, 50%);
    gap: 1rem;
    grid-auto-rows: 200px;
}
```

Podemos também utilizá-lo junto com a palavra reservada `auto` para fazer com que o conteúdo caiba dentro da célula:

```css
.wrapper {
    display: grid;
    grid-template-columns: 100px repeat(3, 200px) 10% minmax(10%, 50%);
    gap: 1rem;
    grid-auto-rows: minmax(200px, auto);
}
```

## Unidade `fr`

`./arquivo3.html`

O nome "fr" é a abreviação de "fração". Vamos dar uma fração para cada coluna de uma *grid*:

```css
.wrapper {
    display: grid;
    grid-template-columns: 1fr 1fr 1fr;
    gap: 1rem;
    grid-auto-rows: 100px;
}
```

Podemos utilizar o `repeat()` para deixar o código mais bonito:

```css
.wrapper {
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    gap: 1rem;
    grid-auto-rows: 100px;
}
```

## Alinhamento de Conteúdo

`./arquivo4.html`

O *grid* ocupa por padrão o tamanho total de onde ele se encontra. Aqui vão alguns atributos que podem ser usado no elemento *grid*:

**`align-items`**

Este atributo tem alguns valores:

`start`: o conteúdo fica no topo da célula;
`center`: o conteúdo fica centralizado na célula de maneira horizontal;
`end`: o conteúdo fica na parte de baixo da célula;
`stretch`: ocupa toda a célula (é o comportamento padrão).

**`justify-items`**

Este atributo tem alguns valores:

`start`: o conteúdo fica na parte esquerda da célula;
`center`: o conteúdo fica centralizado na célula de maneira vertical;
`end`: o conteúdo fica na parte direita da célula;
`stretch`: ocupa toda a célula (é o comportamento padrão).

**`align-self`**

Este atributo deve ser usado em um único elemento da *grid*. Ele funciona exatamente como o `align-items`, mas ele é feito para ser usado por uma célula em específico, e não no contêiner.

`start`: o conteúdo fica no topo da célula;
`center`: o conteúdo fica centralizado na célula de maneira horizontal;
`end`: o conteúdo fica na parte de baixo da célula;
`stretch`: ocupa toda a célula (é o comportamento padrão).

**`justify-self`**

Este atributo funciona como o `justify-items`, mas deve ser usado em uma célula em específico, e não no contêiner.

`start`: o conteúdo fica na parte esquerda da célula;
`center`: o conteúdo fica centralizado na célula de maneira vertical;
`end`: o conteúdo fica na parte direita da célula;
`stretch`: ocupa toda a célula (é o comportamento padrão).

## Ocupando Espaços Parte 1

`./arquivo5.html`

A *grid* é especificada no elemento *wrapper*, ao invés de o fluxo ser controlado em cada elemento. Uma vez definida a *grid*, cabe agora em cada elemento especificar em qual espaço da *grid* o elemento vai ficar.

Vamos especificar uma *grid*:

```css
.wrapper {
    display: grid;
    grid-template-columns: repeat(4, 1fr);
    grid-auto-rows: 100px;
    padding: 10px;
    gap: 10px;
}
```

Com o atributo `grid-column-start` é possível indicar em qual coluna o elemento começará na *grid*. Já pelo atributo `grid-column-end`, podemos especificar até qual coluna ele vai. Com esses dois é possível colocar elementos em espaços específicos da *grid*, e também é possível utilizar mais de uma célula.

```css
.wrapper div:nth-child(1) {
    grid-column-start: 1;
    grid-column-end: 3;
}
```

No código acima estamos configurando a primeira `div` para começar na coluna 1 e terminar onde a coluna 3 começa. Os outros elementos são jogados para as próximas células de acordo com que as células de cima vão sendo utilizadas.

Podemos também utilizar o atributo abreviado, chamado somente de `grid-column`. Colocamos o primeiro e o segundo valor e separamos eles por uma barra, desta maneira:

```css
.wrapper div:nth-child(4) {
    grid-column: 1 / 3;
}
```

Podemos também utilizar o valor reservado `-1` para o `grid-column-end`, que indica que o elemento cobrirá todas as colunas, isto é, uma fileira inteira.

```css
.wrapper div:nth-child(2) {
    grid-column: 1 / -1;
}
```

Podemos também utilizar a palavra `span`, que indica a quantidade de espaços que o elemento vai tomar.

```css
.wrapper div:nth-child(3) {
    grid-column: 1 / span 3;
}
```

## Ocupando Espaços Parte 2

`arquivo6.html`

Podemos usar somente um valor no `grid-column`, indicando somente a célula inicial em que o elemento estará localizado:

```css
.wrapper div:nth-child(2) {
    grid-column: 1;
}
```

Se houver um elemento antes do elemento selecionado e nós colocarmos que ele irá inicial na coluna 1, ele passa para a próxima linha.

Veja um pequeno exemplo de uma maquete de um site:

```css
/* header */
.wrapper div:nth-child(1) {
    grid-column: 1 / -1;
}
/* menu lateral */
.wrapper div:nth-child(2) {
    grid-column: 1;
}
/* conteúdo */
.wrapper div:nth-child(3) {
    grid-column: 2 / span 2;
}
/* footer */
.wrapper div:nth-child(5) {
    grid-column: 1 / -1;
}
```

## Ocupando Espaços Parte 3

Vamos fazer um site responsivo utilizando *grid*. De acordo com que redimensionamos a página, a *grid* vai seguir, ficando cada vez menor ou maior. Seria interessante mudar isso, se a página for redimensionada para ficar bem pequena. Assim poderíamos dividir o conteúdo da página, jogando certas partes para baixo e deixando outras na parte de cima.

Para fazer isso utilizaremos *media queries*, e modificaremos a configuração de linhas e colunas.

Este é o atual leiaute da página:

**HTML**

```html
<body>
    <div class="wrapper">
        <div>1</div>
        <div>2</div>
        <div>3</div>
        <div>4</div>
        <div>5</div>
    </div>
</body>
```

**CSS**

```css
body {
    background-color: gray;
}

.wrapper {
    display: grid;
    grid-template-columns: repeat(4, 1fr);
    grid-auto-rows: minmax(100px, auto);
    padding: 10px;
    gap: 10px;
}

.wrapper div {
    background-color: skyblue;
}

.wrapper div:nth-child(even) {
    background-color: aliceblue;
}

.wrapper div:nth-child(1) {
    grid-column: 1 / -1;
}

.wrapper div:nth-child(2) {
    grid-column: 1;
}

.wrapper div:nth-child(3) {
    grid-column: 2 / span 2;
}

.wrapper div:nth-child(5) {
    grid-column: 1 / -1;
}
```

Mudaremos a página de maneira que ela tenha somente uma coluna com várias linhas quando a página for redimensionada para um tamanho de 600px ou menos.

```css
@media (max-width: 600px) {
    .wrapper {
        grid-template-columns: 1fr;
    }

    .wrapper div:nth-child(3) {
        grid-column: 1;
    }
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

Onde parei:
https://www.youtube.com/watch?v=Y-s0zP24lfU&list=PLYgzkrmJnLwpeeGgdADYq3cE2yUwLLTOv&index=10&ab_channel=dpw

NO EXERCÍCIO 10 TENTANDO REPRODUZIR O QUE APRENDEU NO ARQUIVO 7. não tá aparecendo conteúdo. tente resolver

Curso flexbox:
https://www.youtube.com/watch?v=SAl0i5rzX3U&list=PLYgzkrmJnLwo8IDD2v7RP_oyE3yzc1fY4&ab_channel=dpw