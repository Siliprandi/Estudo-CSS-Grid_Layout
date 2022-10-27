# Criação da seção destaque do site 



Na parte de destaque do site, terá as principais informações sobre jogos e aplicativos, além de algumas categorias que servem de filtros para esses elementos.



Abaixo uma imagem que retrata a separação da Grid do destaque: 

![](C:\Users\User\Desktop\1_1_2_linhas+e+colounas.png)



Precisamos definir um grid para a área de destaque. Basicamente, teremos três linhas: a do PUBG, Slack e outra do WhatSapp e quatro colunas. As grids não estão precisas, mas trata-se apenas de uma base para desenvolvermos a organização do nosso site. 

Para isso, no arquivo index.html, na seção destaque, terá o seguinte código:



```html
<section class="destaques">
            <div class="destaques__principal caixa">
                <h3 class="destaques__titulo">Fornite</h3>
            </div>
            <div class="destaques__secundario caixa">
                <h3 class="destaques__titulo">PUBG</h3>
            </div>
            <div class="destaques__secundario caixa">
                <h3 class="destaques__titulo">Slack</h3>
            </div>
            <div class="destaques__secundario caixa">
                <h3 class="destaques__titulo">Whatsapp</h3>
            </div>
            <div class="destaques__secundario caixa">
                <h3 class="destaques__titulo">CS: GO</h3>
            </div>
            <div class="destaques__categorias">
                <ul class="destaques__categorias___lista">
                    <li class="destaques__categorias___item">
                        <a class="destaques__categorias___link" href="#">
<i class="destaques__categorias___icone fab fa-buromobelexperte"></i>
```



No arquivo **destaque.css**, colocaremos a classe .destaque, e faremos com que ela se comporte como grid. Para isso, colocaremos o **display:grid;**

Feito isso, será necessário definir as quatro colunas. Logo, cada coluna terá o valor de 25% (divisão de 100%):



```css
.destaques { 
    display: grid;
    grid-template-columns: 25% 25% 25% 25%;
}
```



Logo em seguida, será definido as três linhas da grid e seus tamanhos, seguindo a mesma lógica da definição de colunas:



```css
.destaques { 
    display: grid;
    grid-template-columns: 25% 25% 25% 25%;
    grid-template-rows: 33.33% 33.33% 33.33%; 
}
```



Adiante, será necessário, nesse caso, definir o **height** que será calculada a partir de **100vh**, ou seja, a base no tamanho total da área do browser, e retiraremos a área que deve ser ocupada pelo cabeçalho, que sabemos possuir `50px`:



```css
.destaques { 
    background: red;
    display: grid;
    grid-template-columns: 25% 25% 25% 25%;
    grid-template-rows: 33.33% 33.33% 33.33%;
    height: calc(100vh - 50px);
}
```



