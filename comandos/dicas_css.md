# Introdução ao CSS
 
### Utilize a # para declarar um ID de uma Tag HTML no CSS

    #NomeID{
        margin: 0;
    }


### Utilize o . para declarar uma CLASS de uma Tag HTML no CSS

    .NomeClass{
        margin: 10px;
    }


### Usar o sinal de > para configurar somente os parametros das TAGs filhas ou que estejam diretamente ligadas aquela TAG, ID ou CLASS 

    .NomeClass > div{
        margin: 10px;
    }

    .NomeClass > h1{
        color: red;
    }

### Observação: caso não use > para configurar os parametros das TAGs filhas, os parametros serão aplicados em **TODAS** as TAGs que estejam dentro da NomeClass

    .NomeClass h1{
        color: red;
    }


### Algumas variaveis para formatar textos

    text-transform: uppercase;
    text-transform: lowercase;
    text-transform: capitalize;

    text-decoration: underline;
    text-decoration: overline;
    text-decoration: line-trough;



<br>

## Boas pratias

### Ao iniciar a criação de um código CSS costuma se usar * para resetar configruções defaut dos navegadores

    *{
        margin: 0;
        padding: 0;
    }
 
### Logo em seguida costuma se usar esté código para deixar a página responsiva

    html,body{
        height: 100%;
    }

### O seu códio CSS tem que ser organizado seguindo uma logica, por quê disso, pois outros programadores irião visitar seu codigo. Alguns custemes que alguns programadores utilizado é declarar as TAGs, depois as CLASS, os IDs e por ultimo os JavaScript

<br>

## Exemplo Código CSS com JavaScript

    @media screen and (max-width: 600px){
        .box{
            height: auto;
        }
    }