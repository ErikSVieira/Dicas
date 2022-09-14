# Códigos HTML

## Estrutura Básica de uma página HTML

    <!DOCTYPE html>
    <html lang="pt-BR">
    <head>
        <meta charset="UTF-8">
        <meta http-equiv="X-UA-Compatible" content="IE=edge">
        <meta name="viewport" content="width=device-width, initial-scale=1.0">
        <title>Document</title>
    </head>
    <body>
        
    </body>
    </html>

### A tag html é a raiz do seu documento, todos os elementos HTML devem estar dentro dela. E nela nós informamos ao navegador qual é o idioma desse nosso documento, através do atributo lang, para o português brasileiro usamos pt-BR.

    <html></html>

### A tag head contém elementos que serão lidos pelo navegador, como os metadados - um exemplo é o charset, que é a codificação de caracteres e a mais comum é a UTF-8, o JavaScript com a tag script, o CSS através das tags style e link - veremos a diferença quando falarmos sobre CSS - e o título da página com a tag title.

    <head></head>

### E dentro da tag body colocamos todo o conteúdo visível ao usuário: textos, imagens, vídeos.

    <body></body>

### Representa uma seção genérica de conteúdo quando não houver um elemento mais específico para isso.

    <section></section>

### É o cabeçalho da página ou de uma seção da página e normalmente contém logotipos, menus, campos de busca.

    <header></header>

### Representa um conteúdo independente e de maior relevância dentro de uma página, como um post de blog, uma notícia em uma barra lateral ou um bloco de comentários. Um article pode conter outros elementos, como header, cabeçalhos, parágrafos e imagens.

    <article></article>

### É uma seção que engloba conteúdos relacionados ao conteúdo principal, como artigos relacionados, biografia do autor e publicidade. Normalmente são representadas como barras laterais.

    <aside></aside>



### Esse elemento representa o rodapé do conteúdo ou de parte dele, pois ele é aceito dentro de vários elementos, como article e section e até do body. Exemplos de conteúdo de um footer são informações de autor e links relacionados.

    <footer></footer>



### Eles não foram criados na versão 5 do HTML e nem são específicos para semântica, mas servem para esse propósito. São utilizados para marcar a importância dos títulos, sendo h1 o mais importante e h6 o menos. Uma dica: use apenas um h1 por página, pois ele representa o objetivo da sua página.

    <h1></h1>
    <h2></h2>
    <h3></h3>
    <h4></h4>
    <h5></h5>
    <h6></h6>

### A web também é feita de imagens e para representá-las temos o elemento img, ele é um daqueles elementos sem tag de fechamento.

O elemento img é bem simples, contendo apenas 2 atributos próprios, o src e o alt.

O src é obrigatório e guarda o caminho para a imagem que você quer mostrar na página.

O alt não é obrigatório mas é altamente recomendado por melhorar a acessibilidade, ele mostra a descrição da imagem caso ela não carregue e leitores de tela usam esse atributo para descrever a imagem para o usuário saber o que ela significa.

    <img></img>

###
    <details></details>

    <summary></summary>

#### Exemplo 1

    <details>
        <summary>
            <section>
                <div></div>
                <div></div>
                <div></div>
            </section> 
        </summary>
    </details>

#### Exemplo 2

    <label for="weekday">Selecione o dia</label>
    <input type="week" name="weekday" id="weekday">
    <input type="text">
    <details id="weekday">
        <option value="Domingo"></option>
        <option value="Segunda"></option>
        <option value="Terça"></option>
        <option value="Quarta"></option>
        <option value="Quinta"></option>
        <option value="Sexta"></option>
        <option value="Sábado"></option>
    </details>


### contenteditable

#### Exemplo 

    <h1 contenteditable></h1>


###

    <mark></mark>


###

    <cite></cite>


###

    <optgroup></optgroup>


#### Exemplo

    <label for=""></label>
    <section>
        <optgroup label="19h00">
            <option value="1"></option>
            <option value="2"></option>
            <option value="3"></option>
            <option value="4"></option>
        </optgroup>
        <optgroup label="20h00">
            <option value="5"></option>
            <option value="6"></option>
            <option value="7"></option>
            <option value="8"></option>
        </optgroup>
    </section>


###

     <progress></progress>



#### Exemplo

    <progress id="bar" value="0" max="100" class="w-full">Progresso a: 50%</progress>


### 

    <input type="text">
<input type="text">


#### Exemplos

    <input type="range" name="" id="">
<input type="range" name="" id="">

    <input type="date" name="" id="">
<input type="date" name="" id="">

    <input type="color" name="" id="">
<input type="color" name="" id="">

    <input type="time" name="" id="">
<input type="time" name="" id="">