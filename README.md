# tech-for-recruiters

Vamos abrir um documento novo no Sublime Text e inicar com a estrutura básica de uma página ```HTML```.

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

Vamos então adicionar essas classes, para que melhorar o layout dos ícones sobre os módulos do curso

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

Maravilha, mas uma seção do nosso site já está pronta 🙌

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
