# tech-for-recruiters

### Parte I - Desenvolvimento da versão 1 da nossa página tech-for-recruiters ###

Vamos abrir um documento novo no Sublime Text e iniciar com a estrutura básica de uma página ```HTML```.

```
<!DOCTYPE html>
<html>
  <head>
    <meta charset="utf-8">
    <meta name="viewport" content="width=device-width, initial-scale=1">
    <title>Tech For Recruiters</title>    
  </head>

  <body>
  </body>
</html>
```

Agora vamos salvar esse documento com o nome ```index.html``` dentro de um repositório (uma pasta) que terá todo o código do nosso projeto. Que tal nomeá-la tech-for-recruiters?

Vamos colocar uma primeira mensagem na tela do navegador!? "Hello world!" é uma escolha tradicional no universo tech.

Adicione o texto dentro da tag de parágrafo, dentro do body:

```
<p>Hello world!</p>
````
Shooow! Já temos algo no ar... viram, não foi tão difícil!

Mas voltando ao nosso objetivo, estamos construindo um site do curso Tech for Recruiter, então vamos colocar nossos headers no lugar desse parágrafo:

```
<h1>99Hunters + Le Wagon</h1>
<h2>Tech for Recruiters</h2>
```
(atenção com a identação do seu código)

Essa página está precisando de um pouco mais de estilo, vamos adicionar um arquivo ```CSS``` no repositório. Para isso, crie um novo arquivo no Sublime Text e salve-o como ```style.css```.

Adicione dentro do ```head``` de seu ```HTML``` um link para o arquivo ```CSS```

```<link href='style.css' rel='stylesheet'>```

E no ```CSS```, vamos colocar algum estilo no nosso ```body```:

```
body {
  color: grey;
  font-size: 16px;
  font-family: Poppins;
}
```

Precisamos também adicionar no ```head``` do ```HTML``` o link do Google Fonts para a fonte escolhida, Poppins: 

```
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Poppins:wght@200;400;800&display=swap" rel="stylesheet">
```

Vamos trazer uma imagem de fundo e um layout mais bacana para o nosso banner.

Primeiro, precisamos colocar o conteúdo que vai nessa área em uma ```div``` com ```id="banner"```

```
<div id="banner">
  <h1>99Hunters + Le Wagon</h1>
  <h2>Tech for Recruiters</h2>
</div>
```

Essa imagem tem tudo a ver com nosso curso:
https://images.unsplash.com/photo-1528901166007-3784c7dd3653?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=2970&q=80

```
#banner {
  text-align: center;
  background-image: url("https://images.unsplash.com/photo-1528901166007-3784c7dd3653?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=2970&q=80");
  background-size: cover;
  background-position: center;
  padding: 190px;
}
```
Nossos ```headers``` devem ficar melhores em branco e com uma fonte um pouco maior:

```
h1 {
  color: white;
  font-size: 50px;
}
h2 {
  color: white;
  font-size: 38px;
}
```

Com o nosso banner pronto, passamos para os próximos elementos da nossa página. 
Vamos adicionar o título da próxima sessão:

``` <h3>Conteúdo:</h3>```

Mas para que ajustar o design desse título, vamos colocá-lo dentro de uma ```div```:

```
<div id="sub-banner">
  <h3>Conteúdo:</h3>
</div>
```

E adicionar seu estílo no arquivo ```style.css```:

```
#sub-banner {
  text-align: center;
  margin: 50px 0;
}
```

Iremos então adicionar os ícones sobre os módulos do curso.

Vamos baixar uma pasta com todas as imagens que utilizaremos nesse projeto:

https://res.cloudinary.com/nineninehunters/raw/upload/v1651003563/images_ozrrn9.zip

E então, depois de descomprimir o arquivo, vamos adicionar essa pasta ```images``` dentro do nosso repositório.

Agora podemos usar todas as imagens dessa pasta em nosso código 💪

```
<img src="images/modulo1.png" alt="icone-modulo1" width="100">
<h4>Módulo 1:</h4>
<p><strong>Conhecendo</strong> o curso</p>
```

```
<img src="images/modulo2.png" alt="icone-modulo1" width="100">
<h4>Módulo 2:</h4>
<p>A profissão <strong>tech recruiter</strong></p>
```

Para organizar melhor o layout, dividir o conteúdo em colunas e ainda torná-lo responsível, vamos adicionar bootstrap.
https://getbootstrap.com/

Precisamos apenas incluir o link para o arquivo de estílos ```CSS``` do framework também na ```head``` do nosso ```HTML```:

```
<link href="https://cdn.jsdelivr.net/npm/bootstrap@5.1.3/dist/css/bootstrap.min.css" rel="stylesheet" integrity="sha384-1BmE4kWBq78iYhFldvKuhfTAU6auU8tT94WrHftjDbrCEXSU1oBoqyl2QvZ6jIW3" crossorigin="anonymous">
```

Com isso passamos a ter acesso, entre várias outras coisas, as classes ```row``` (cria uma faixa ou linha no layout, a qual poderemos quebrar em diferentes colunas), ```col``` (permite que o layout seja quebrado em colunas responsivas) e ```card``` (um container de conteúdo, flexível e extensível com múltiplos variantes e opções)

Vamos então adicionar essas classes, para melhorar o layout dos ícones sobre os módulos do curso

```
<div id="modules" class="row">
  <div class="col">
    <div class='card'>
      <img src="images/modulo1.png" alt="icone-modulo1" width="100">
      <h4>Módulo 1:</h4>
      <p><strong>Conhecendo</strong> o curso</p>
    </div>
  </div>
  <div class="col">
    <div class='card'>
      <img src="images/modulo2.png" alt="icone-modulo2" width="100">
      <h4>Módulo 2:</h4>
      <p>A profissão <strong>tech recruiter</strong></p>
    </div>
  </div>
</div>
```
    
E claro, adicionar no ```CSS``` o estílo que queremos para esses componentes:

```
#modules {
  margin-bottom: 50px;
}
.card {
  align-items: center;
  text-align: center;
  padding: 30px;
  font-weight: lighter;
  border: none;
}
.card img {
  margin-bottom: 20px;
}
```

Agora que o layout está como queremos, vamos copiar os ```cards``` e adicionar as informações de todos os módulos:

```
<div class="col">
  <div class='card'>
    <img src="images/modulo3.png" alt="icone-modulo3" width="100">
    <h4>Módulo 3:</h4>
    <p>Explicando o <strong>universo de desenvolvimento</strong></p>
  </div>
</div>
<div class="col">
  <div class='card'>
    <img src="images/modulo4.png" alt="icone-modulo4" width="100">
    <h4>Módulo 4:</h4>
    <p>Tech <strong>além do desenvolvimento</strong></p>
  </div>
</div>
<div class="col">
  <div class='card'>
    <img src="images/modulo5.png" alt="icone-modulo5" width="100">
    <h4>Módulo 5:</h4>
    <p><strong>Finalizando</strong> o curso</p>
  </div>
</div>
```

Maravilha, mais uma seção do nosso site já está pronta 🙌

Na próximas seção, vamos colocar um vídeo do youtube de uma aula do Le Wagon, você poderá depois colocar o vídeo do nosso curso de Tech for Recruiters.
https://www.youtube.com/watch?v=G0RIx2SCzAg

```
<div id='video-container'>
  <iframe width="560" height="315" src="https://www.youtube.com/embed/G0RIx2SCzAg" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
</div>
```
sem esquecer de também colocá-lo dentro de uma ```div```, para que possamos ajustar o layout dessa área do site no ```CSS```:

```
#video-container {
  text-align: center;
  margin-bottom: 80px;
}
```

Por fim, vamos adicionar um ```footer``` e encerrar essa primeira versão do nosso site.

Como incluiremos alguns ícones, vamos chamar uma biblioteca de ícones chamada Font Awesome:
https://fontawesome.com/

E assim como os outros arquivos de estílo, vamos incluir o link do Font Awesome no ```head```:

```
<link rel="stylesheet" href="https://use.fontawesome.com/releases/v5.5.0/css/all.css">
```

Bora criar nosso footer com o logo da 99Hunters então:

```
<div id="footer">
  <a href="https://www.99hunters.com/" target="_blank"><img src="images/logo-99hunters.png" alt="picture description" width="120"></a>
</div>
```

Com o logo branco, em um fundo branco, realmente não vamos conseguir enxergar nada. Vamos para o ```CSS``` adicionar estilo nesse ```footer```:

```
#footer {
  padding: 30px 80px;
  background: linear-gradient(to right, #ff6700, #fd1015);
}
```

Vamos usar nosso amigo bootstrap novamente e dividir esse ```footer``` em colunar.

Adicione a ```class="row"``` na ```div``` ```#footer``` e coloque cada ícone dentro de uma ```div``` com a ```class="col"

E para finalizar nosso footer, e o exercício de hoje, vamos colocar uma lista de ícones abaixo de cada logo:

```
<ul>
  <li><a href="#"><i class="fab fa-youtube"></i></a></li>
  <li><a href="#"><i class="fab fa-facebook"></i></a></li>
  <li><a href="#"><i class="fab fa-facebook"></i></a></li>
  <li><a href="#"><i class="fab fa-github"></i></a></li>
</ul>
```

E adicionar o estílo no ```CSS``` para trocar a cor dos ícones e remover os bullets da lista:

```
#footer a {
  color: white;
  font-size: 18px;
}
#footer ul {
  list-style-type: none;
}
```

Parabéns, seu primeiro site deve estar pronto 👏👏👏

Essa foi nossa primeira versão do site, uma página totalmente estática. Mas calma, vamos trazer um pouco mais de dinamismo para esse nosso exercício na próxima parte!

### Parte II - Desenvolvimento da API ###

Iremos agora criar um backend online em Javascript (linguagem de programação), usando Node (ambiente de desenvolvimento) e Express.js (framework), através da plataforma https://glitch.com/.

Já temos pronto um boilerplate (um esqueleto padrão pronto de onde partiremos para construir nossa aplicação) que usaremos para construir nosso backend. Este vai conversar via API com o site que desenvolvemos na parte anterior.

Vamos então acessar esse boilerplate https://glitch.com/edit/#!/99academy-boilerplate

E clicar em remix, para que possamo criar uma cópia desse servidor, na qual trabalharemos.

![image](https://user-images.githubusercontent.com/26194801/165558323-3a12afcb-df6a-4835-905b-4f0ac8995962.png)

Pronto, agora você tem uma versão sua dessa aplicação. Recomendo inclusive que clique em 'Settings' e depois em 'Edit project details', para mudar o nome do seu projeto. 

Vou renomear o meu para ```99academy-backend```!

O objetivo dessa aplicação backend é retornar uma liguagem de programação ou uma lista de frameworks, ao receber uma requisição com o nome de uma linguagem de programação ou framework.

Vamos então começar adicionando o nosso "banco de dados". No caso será um documento no formato ```JSON```, com várias linguagens de programação e alguns dos seus respectivos frameworks.

Vamos atribuir esse ```JSON``` a uma constante chamada falsoBancoDeDados:

```
const falsoBancoDeDados = {
  'Javascript':['React', 'React Native', 'JQuery', 'Vue.js', 'AngularJS', 'Ember.js', 'Express.js', 'Next.js'],
  'Python':['Django', 'AIOHTTP', 'Bottle', 'CherryPy', 'CubicWeb', 'Dash', 'Falcon', 'Flask'],
  'Java':['Spring', 'Hibernate', 'JSF (JavaServer Faces)', 'GWT (Google Web Toolkit)', 'Struts', 'Blade', 'Play', 'Vaadin', 'Grails', 'DropWizard'],
  'C#':['.NET', 'ASP.NET', 'NHibernate'],
  'C++':['Qt', 'ffead-cpp', 'Kigs framework', 'ROOT', 'Ultimate++'],
  'C':['Kore', 'facil.io', 'Duda'],
  'Go':['Gin', 'Beego', 'Iris', 'Echo', 'Fiber'],
  'Dart':['Flutter'],
  'Kotlin':['Ktor', 'Kweb', 'Javalin', 'Spark', 'Spring Boot', 'Vaadin-On-Kotlin', 'Jooby'],
  'PHP':['CakePHP', 'CodeIgniter', 'Horde', 'Laravel', 'Symfony', 'Yii', 'Zend', 'Zikula', 'Fuel', 'Slim', 'Phalcon', 'Aura'],
  'Ruby':['Ruby on Rails', 'Sinatra', 'Hanami or Lotus', 'Ramaze', 'Cuba', 'Padrino'],
  'Rust':['actix-web', 'Warp', 'Axum']
}
```

Temos já, a partir do nosso boilerplate, um ```endpoint``` para uma chamada ```GET``` na rota raiz da aplicação.

Vamos então preparar esse método para que receba um requisição com um valor para tecnologia, como parâmetro em uma query.

Podemos atribuir então o valor desse parâmetro tecnolgia a constante ```termoBuscado```:

```
const termoBuscado = request.query.tecnologia
```

Agora que já temos o termo que será buscado em nossa ```API```, vamos começar a criar uma função responsável por buscar essa tecnologia em nosso banco de dados:

```
function buscarTecnologia(termoBuscado){
    
  for (const linguagem in falsoBancoDeDados){
    const frameworks = falsoBancoDeDados[linguagem]
    
    if (linguagem == termoBuscado) {
      // o termo buscado é uma linguagem de programação
      // precisamos retornar os frameworks dessa linguagem
    } else if (frameworks.includes(termoBuscado)) {
      // o termos buscado é um framework
      // precisamos retornar a linguagem de programação correspondente
    }
  }
}
```

Já sabemos então se o usuário buscou uma linguagem de programação ou um framework. Agora precisamos em cada um dos casos retornar as informações correspondentes.

Vamos então criar, para cada um dos casos, uma função que retorna a informação esperada ao usuário.

Quando o termo buscado foi uma linguagem de programação:
```
function retornarFrameworksParaLinguagem(linguagem){
  const texto = `
      <p><b>${linguagem}</b> é uma linguagem de programação</p>
      <p>${falsoBancoDeDados[linguagem].join(', ')} são alguns de seus frameworks</p>
    `
  return texto
}
```

Quando o termo buscado foi um framework:
```
function retornarLinguagemParaFramework(linguagem, termoBuscado){
  const texto = `
    <p><b>${termoBuscado}</b> é um framework da linguagem <b>${linguagem}</b></p>
  `
  return texto
}
```

Agora, vamos chama essas funções dentro da função ```buscarTecnologia```, assim já teremos para cada um dos casos o texto formatado com a resposta correta para o usuário.

Podemos determinar, no início da função, uma varíavel resultado, com o valor "termo não encontrado" que será retornada caso a gente não caia em nenhuma das condições da função. No entento, caso entre nos condicionais do ```IF``` ou ```ELSE IF ```, o valor dessa variável será atualizado com o resultado das funções retornadas em cada um dos casos.

Depois disso, podemos então atualizar nosso método da API para que chame a função ```buscarTecnologia``` e envie uma reposta com as informações retornadas pela função.

```
app.get("/languages", (request, response) => {
  const termoBuscado = request.query.tecnologia
  const resposta = buscarTecnologia(termoBuscado)
  response.json({'resposta': resposta});
});
```
Com isso, nosso backend e sua API estão prontos!!! 🎉

Vamos voltar ao nosso frontend e criar uma chamada para essa API.

### Parte III - Chamando a API a partir da nossa página tech-for-recruiters ###

Vamos precisar inicialmente adicionar um formulário para que o usuário possa inserir um termo que será buscado:

```
    <div id='search-container'>
      <p>Buscar tecnologia</p>
      <form id='techs-form'>
        <input id='techs-input' type="text" size="60" maxlength="256" placeholder="Linguagem de programação ou framework">
        <input type="submit" name="search_button" value="Buscar">
      </form>

      <div id="techs">
        <!-- div vazia que irá receber, via AJAX, a resposta de nossa requisição na API -->
      </div>      
    </div>
```

E depois adicionar um ```script``` com um bloco de código Javascript que será responsável por pegar o i. pegar o termo buscado; ii. fazer a requisição na API com esse termo como parâmetro, iii. inserir via AJAX o conteúdo retornado pela API da ```div``` com ```id``` techs:

```
<script>
  $('#techs-form').submit(function(event){
    const searchTerm = event.target.firstElementChild.value;

    $.ajax({
      url: `https://nome-do-seu-app.glitch.me?tecnologia=${searchTerm}`
    }).done(function(data) {
      $('#techs').html(data['resposta']);
    });

    event.preventDefault();
  });
</script>
```

Agora nossa API tem tudo para rodar, vamos testar?


### Parte IV - Melhoria da API ###

Parece que tudo está funcionando bem, enquanto o usuário faz as buscas utilizando as maiúscula ou minúscula sempre igual ao nosso "banco de dados".

Mas isso é algo que podemos corrigir facilmente, convertendo os textos que estamos comparando dentro da função ```buscarTecnologia``` para minúsculo.

Com essa melhoria, nossa versão final dessa função fica assim:

```
function buscarTecnologia(termoBuscado){
  
  const termoBuscadoMinusculo = termoBuscado.toLowerCase()
  var resultado = 'não encontrado'
  
  for (const linguagem in falsoBancoDeDados){
    const linguagemMinuscula = linguagem.toLowerCase() 
    const frameworksMinusculos = falsoBancoDeDados[linguagem].map(framework => {return framework.toLowerCase()})
    
    if (linguagemMinuscula == termoBuscadoMinusculo) {
        resultado = retornarFrameworksParaLinguagem(linguagem)
     
    } else if (frameworksMinusculos.includes(termoBuscadoMinusculo)) {
      resultado = retornarLinguagemParaFramework(linguagem, termoBuscado)      
    }
  }
  return resultado
}
```

Pronto, agora nossa aplicação funciona também para buscas com formato diferente de fontes.

Fique a vontade para continuar explorando o universo do desenvolvimento, as linguagens HTML, CSS e Javascript para trazer ainda mais melhorias para esse exemplo de aplicação!
