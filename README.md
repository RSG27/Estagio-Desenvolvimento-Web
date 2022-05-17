# Teste para vaga de Estagiário Dev Web

O objetivo deste teste é entender o candidato, sua experiência e sua capacidade de resolução de problemas com dúvidas e detalhes que serão exigidos no dia-a-dia como Estagiário em Desenvolvimento Web.
O teste é baseado em questionamentos e problemas a serem resolvidos.

## Questões Teóricas

1. Qual a função do "head" no HTML?

    R: Dispor informações gerais (metadados) sobre o documento, incluindo itens como título e links para scripts e folhas de estilos, por exemplo.

2. Quando uma página é criada, ela automaticamente se adapta a todos os tipos de tela? Por que?

    R: Sim, para isso temos de usar um layout responsivo, ou seja, o site deve ser estruturado para se enquadrar ao tamanho de um determinado dispositivo. Por isso, é importante observar os breakpoints, que são aqueles pontos de "quebra de página" e usar media queries, para determinar a posição dos elementos da nossa página nesses dispositivos.

    Correção: Sim, o HTML é naturalmente responsivo, só que a maioria dos layouts que nós criamos vão contra essa responsividade natural do HTML (ele só cria layouts de uma coluna e texto corrido), e por isso que geralmente temos que readaptar o site para ele voltar a ser responsivo;

3. O código HTML e CSS é renderizado no servidor e repassado para o navegador em forma de imagem?

    R: Sim, esse processo ocorre basicamente em cinco etapas: 

    I. Envio de requisições para o web server – se o usuário digitar http://www. nomedosite.com.br, o browser procura o endereço DNS (Domain Name System) www.webdevacademy.com.br e usa o HTTP para conectar ao server desse site, e requisita a página inicial.

    II. Autentica o server – se o server tiver um certificado SSL e a requisição for feita com HTTPS, o browser usa o certificado para autenticar o server e então pode desfazer a criptografia das futuras comunicações.

    III. Processa a resposta – se o server tiver enviado um HTML, o browser vai buscar os objetos embutidos, como as imagens, vídeos ou arquivos referenciados no HTML. Se o server enviou um erro, redirecionamento, ou alguma outra resposta, o browser responde de forma apropriada.

    IV. Exibe o HTML e os objetos – os browsers usam os padrões HTML para definir como exibe uma página para o usuário. Como o HTML pode conter objetos embutidos, como um MP3, o browser pode ter que carregar dezenas de objetos e arquivos para renderizar uma única página.

    V. Executa os scripts de cliente – os scripts client, como os que são escritos em Javascript, possibilitam criar páginas interativas e dinâmicas sem a necessidade de recarregar a página, e é o browser que interpreta esses códigos.

    fonte: https://webdevacademy.com.br/artigos/como-funcionam-comunicacoes-web/

    Correção: Ele não é enviado na forma de imagem, ele é enviado na forma de um documento HTML, se fosse uma imagem você não ia conseguir selecionar os textos por exemplo;

4. Qual a função das tags H (h1, h2, h3, etc) no HTML?

    R: Destacar títulos e subtítulos de uma página. As chamadas Heading Tags são usadas na hierarquização e estruturação de uma página.

5. O que é SEO e como funciona?

    R: "É a sigla de Sarch Engine Optimization (Ótimização dos mecanismos de busca) e é o conjunto de técnicas usadas, geralmente divididas entre tecnologia, conteúdo e autoridade, para alcançar bom posicionamento de páginas de um site no Google e em outros buscadores, gerando tráfego orgânico."

    Fonte: https://resultadosdigitais.com.br/o-que-e-seo/#:~:text=SEO%20%C3%A9%20a%20sigla%20de,outros%20buscadores%2C%20gerando%20tr%C3%A1fego%20org%C3%A2nico.

6. O uso de media query é obrigatório em todas as páginas?

    R: Sim, pois é através dele que vamos delimitar o layout responsivo do site aos diferentes dispositivos.

    Correção: Não, não é obrigatório, um layout de um blog simples por exemplo, onde você só tem o título do blog e um grid com os cards pode ser feito de forma totalmente responsiva sem o uso de nenhuma media query, ainda no exemplo do blog, o layout do artigo pode ser feito sem nenhuma media query uma vez que ele seria só o título e o texto por exemplo;

7. Qual a diferença entre CSS Inline e CSS em um arquivo?

    R: O CSS inline é aplicado em uma tag específica do HTML que queremos estilizar, para isso é preciso que usemos o atributo (style=" ") no elemento em questão. Já o CSS externo, é aquele em que linkamos as páginas com um "style.css" no head do site e após o title: "<link rel="stylesheet" type="text/css" href="style.css" />".

    Correção: A tag link pode ser incluída tanto antes quanto após o title.

8. Como criar animações no CSS? Dê um exemplo.

    R: Por meio de propriedades como o Transition e o Animation com Keyframes, por exemplo. Como podemos ver a seguir com quadrados que após determinado tempo, assumem uma dada posição na página:

    HTML:
    
    div class="squares"

    CSS:

    @keyframes duracao_animacao {
      0% {background-color:#BA55D3;top:0;left:0;}
      25% {background-color:#9932CC;top:0;left:200px;}
      50% {background-color: #4169E1;top:200px;left:200px;}
      75% {background-color: #0000FF;top:200px;left:0;}
      100% {background-color: #BA55D3;top:0;left:0;}  
    }

    body {
      margin: 0;
    }

    .squares {
      width: 150px;
      height: 150px;
      background-color: #A020F0;
      position: absolute;
      animation-name: duracao_animacao;
      animation-duration: 7s;
      animation-delay: 1s;
      animation-iteration-count: 2;
    }

9. Qual a diferença entre class e ID no CSS?

    R: A class é um seletor em que podemos trabalhar com vários elementos relacionados a uma mesma classe, sendo denotado pelo ".", enquanto o id é um seletor que trabalha de forma rígida permitindo apenas o uso de um único elemento, sendo denotado pelo "#".

10. Quais os diferentes tipos de seletores CSS?

    R: Além dos tradicionais id('#') e class('.'), temos também o '*' que estiliza todos os elementos de uma página,a seguir temos uma lista de seletores, sendo alguns mais e outros menos usados:

    Seletor por elemento (p {});
    Seletor de primeira letra e primeira linha (p::first-letter and p::first-line {});
    Seletor de Primeiro e Último Elemento (p:first-child and p:last-child {});
    Seletor Negativo (:not(p) {});
    Seletor NTH (nth:first-child() {});
    Seletor before/after(span::before/after {content: "";});
    Agrupamento por elementos (p, h1 {});
    Agrupamento por descêndencia de elementos (div img {});
    Agrupamento por classes(.elemento1.elemento2 {});
    Agrupamento por descêndencia de classes (.elemento1 .elemento2 {}); 

## Projeto prático

O candidato deve criar a página da imagem a seguir:
![Layout](https://i.ibb.co/Bydq2FZ/screencapture-spotify-br-2022-05-10-15-13-17.png)

Link da Solução:
[clique aqui](https://animated-baklava-68d0f4.netlify.app/)

Algumas observações importantes:
- Fazer a página responsiva não é obrigatório, mas a apresentação dos elementos deve ser o mais próximo possível da imagem.
- Todas as imagens necessárias estão neste repositório, na pasta "assets".
- Efeitos de hover não são obrigatórios, mas são um plus.

O candidato deve estar atento para obedecer principalmente as cores corretas e tamanhos aproximados.
