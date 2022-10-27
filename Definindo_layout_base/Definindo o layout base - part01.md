# Definindo o layout base - aula 01. 



Primeiramente, é preciso aplicar o Grid Layout CSS. Para isso, abriremos o arquivo '**style.css'**, em que utilizaremos a classe '**app'**- que refere-se ao '**body**'.



Para começar a estilização, precisaremos de um "**pai**" para nossos elementos. Nesse caso, estamos utilizando o `<body>`, que se comportará como grid. Para tanto, incluiremos **display: grid**, como pode ser visto no exemplo abaixo:



```css
.app {
    background: #f1f1f1; 
    display: grid;
    font-family: Arial, Helvetica, sans-serif;
}
```



Precisamos especificar no código, que nosso template será dividido em áreas, como já sabemos. Para realizarmos essa especificação, usaremos a propriedade  **grid-tamplete-areas**, quer receberá as strings **cabecalho, conteudo, rodape**.



Uma delas é especificar qual será o tamanho das colunas e linhas do site, e isso será feito por meio de **grid-tamplete-columns**.



Como utilizaremos apenas uma coluna, definiremos como `auto`. Em seguida, definiremos o tamanho das linhas via  **grid-template-rows**:



```css
.app {
    background: #f1f1f1;
    display: grid;  
    grid-template-areas: 
        "cabecalho"
        "conteudo"
        "rodape";
    grid-template-columns: auto;
    grid-template-rows: 50px auto auto; 
}
```



Em seguida, foi inserido um background em todas as classes de área para ficar visível essa separação:



```css
cabecalho {
    background #00cc99
}

.conteudo {
    background #ff8080
}

.rodape {
    background #0099ff;
}
```





No entanto, apensar de termos essa organização de cores, ainda precisamos explicitar para o Grid que um cabeçalho é de fato um cabeçalho e deve se relacionar com a classe `cabecalho`, por exemplo. Retornando ao código de **style.css**, usaremos a propriedade  **grid-area**, que receberá o nome de cada área correspondente.



```css
.app {
    background: #f1f1f1;
    display: grid;  
    grid-template-areas: 
        "cabecalho"
        "conteudo"
        "rodape";
    grid-template-columns: auto;
    grid-template-rows: 50px auto auto; 
}

.cabecalho {
    background #00cc99
    grid-area: cabecalho;
}

.conteudo {
    background #ff8080
    grid-area: conteudo;
}

.rodape {
    background #0099ff;
    grid-area: rodape;
}
```



