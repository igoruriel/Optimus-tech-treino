# Treino front-end

## Proposta 

Criar um layout completo de um site, em 7 dias, utilizando HTML e CSS. 

### Dia 1 

Fazer o cabecalho.
    
Iniciando o planejamento, no projeto do Figma procurei por padrões, imagens, icones, tipografia e cores utilizadas afim de iniciar a organização e produção do projeto.

Dando início a organização, criei a pasta do projeto e criei o arquivo chamado "briefing.md", adicionei a pasta de assets e dentro da pasta de assets eu adicionei a pasta css e a pasta img. Do projeto no figma, salvei as imagens encontradas para a pasta "./assets/img/", retirei todas as informações de cores e tipografia e adicionei no arquivo "./briefing.md/".
    
Na etapa de execução, dentro do arquivo "./index.html/", escrevi o código padrão do html(doctype, metas, head, body) e adicionei o link de fontes do google fonts. Dentro da pasta css, na pasta "base" criei os arquivos de "_variaveis,_reset e base", na pasta "componentes" criei os arquivos "botoes, cartao e input". Peguei as informações de cores e tipografia e transformei em variáveis no arquivo "_variaveis".

Analisando os componentes no projeto no Figma, criei o código css dos componentes de botão, cartão e input. Depois que fiz os componentes comecei a criação do trabalho proposto para o dia, o cabeçalho. 

Para o cabeçalho comecei fazendo o código simples: 

```html
<header class="cabecalho">
    <section class="cabecalho__container">
        <a href="/" class="cabecalho__logo__link">
            <img class="cabecalho__logo__img" src="/assets/img/logo.svg" alt="Logo Optimus Tech">
        </a>
        <nav class="cabecalho__nav">
            <ul class="cabecalho__lista">
                <li class="cabecalho__lista__item">
                    <a href="#" class="lista__item__link">Home</a>
                </li>
                <li class="cabecalho__lista__item">
                    <a href="#" class="lista__item__link">Produtos</a>
                </li>
                <li class="cabecalho__lista__item">
                    <a href="#" class="lista__item__link">Recursos</a>
                </li>
                <li class="cabecalho__lista__item">
                    <a href="#" class="lista__item__link">Sobre nós</a>
                </li>
            </ul>
        </nav>
        <div class="cabecalho__login">
            <button class="botao botao--entrar">Entrar</button>
            <button class="botao">Cadastrar</button>
        </div>
    </section>
</header>    
```

E agora quero enfatizar o CSS abaixo, porque vai ser preciso para um problema futuro:

```css
.cabecalho {
    box-sizing: border-box;
    width: 100%;
}

.cabecalho__container {
    padding: 1rem 2rem;

    display: flex;
    flex-direction: row;
    align-items: center;
    justify-content: space-between;
}

.cabecalho__nav {
    box-sizing: border-box;
}

.cabecalho__lista {
    display: flex;
    flex-direction: row;
    align-items: center;
    gap: 2rem;
}

.cabecalho__lista__item {
    padding: .25rem 0;
}

.cabecalho__login {
    display: flex;
    flex-direction: row;
    gap: .75rem;
}
```

Nos parâmetros do código apresentado acima, há um problema, um pequenininininho desafio. 

O projeto aqui no HTML/CSS está centralizado e aparentemente perfeito, mas no projeto do Figma existe uma grande diferença na área do "nav" e "logo". Na barra de navegação do projeto no Figma tem uma imagem escondida entre o menu e os botões de login que aplica um espaçamento diferente do que eu consegui inicialmente, no código acima.

Então, enfim para resolver o problema eu fiz alguns teste, coloquei algumas divs separando o "logo" e "menu" da área de botões, botei um grid, milhares de teorias passando pela cabeça... que enfim... provei a mim mesmo que eu conseguia deixar o meu código html/css idêntico ao projeto do Figma, e o código ficou feio. ponto! Ficou feio. 

Vou reverter o projeto para o código inicial, simples, onde eu aplico apenas um "space-around" e tudo fica centralizado. 
E uma segunda opção é colocar apenas um "span" entre o menu e os botões de login/cadastro, que vai ficar estranho.. mas enfim...

E partiremos para o dia 2. 

### Dia 2

Criar "Sobre nós".

Esse foi interessante. A proposta é continuar o desenvolvimento partindo pra área do "Sobre nós", na solicitação do desafio é chamado de "Cabeçalho", mas eu entendo por cabeçalho apenas a área que está o menu ou "header". 

**Planejamento**

Procurei os padrões no projeto e encontrei o seguinte: título, subtítulo e parágrafo.

**Organização** 

Separei as informações básicas do que é essa área de texto e criei o componente "tipogra.css". Eu não sei muito bem se deve ser tratato como componente.
Dessas informações de tipografia, comparei quais informações se encaixavam com o que já estava previamente em código no "base.css". 

**Execução**

Fiz o código da área "Sobre nós" no html, fiz o código dos componentes de titulo, subtitulo e parágrafo e por último ajustei a estilização do texto no arquivo "sobre.css". 

Adicionei flexbox para centralizar o texto. 

**Controle**

Verifiquei se o projeto do código está idêntico ao proposto no projeto do figma. 

Está idêntico.

**Conclusão**

Finalizei mais um dia do desafio. 


### Dia 3

Seção de métricas.

Hoje foi mais tranquilo, mais fácil. A maior parte já estava pronta na forma de componentes, então o que eu tive que fazer foi consertar apenas os pontos específicos na classe específica das métricas.

A construção do html foi ok.. eu pensei primeiro em deixar todo o conteúdo dentro de apenas uma "div". Então ficaria assim: 

```html
<div class="metrica__caixa">
    <h2 class="titulo metrica__titulo">500+</h2>
    <h3 class="subtitulo metrica__subtitulo">Reviews 5 estrelas</h3>
    <p class="paragrafo metrica__paragrafo">
        Estamos orgulhosos de contar com mais de 500 reviews 5 estrelas em nossos produtos.
    </p>
</div>
```

Só que no processo, eu vi que o que me deixaria feliz seria colocar o subtitulo e o texto do parágrafo dentro de uma segunda div dentro da primeira div. 

O que me facilitou alinhar e colocar espaçamento vertical usando o display "grid", e o resultado foi este que vemos hoje. 

E hoje foi um dia estranho... só digo isso.

### Dia 4

Seção de vagas abertas até a imagem. 

Outra dia fácil, todo o planejamento do início tá recompensando hoje. Faz até parecer que é um trabalho fácil... O layout também parece que facilita tudo. Será que todos os designers de figma são assim? Deus ajude... 

Para a seção de vagas eu resolvi copiar a estrutura de div das métricas, mas adicionando uma div extra pra imagem, então ficou: "div>img+div>h2+div>h3+p". as classes foram iguais as anteriores, mas claro, adicionei as classes específicas para fazer as alterações pontuais. O resultado até agora, me parece perfeito. 

### Dia 5

Segunda seção de vagas. 

Finalizei.. pensei muito sobre, e sim... eu coloquei min-width de 768px no cartão... paciência... 

Tô cansado... to trabalhando em 4 empregos