# tech-for-recruiters

Vamos abrir um documento novo no Sublime Text
E inicar com a estrutura básica de uma página ```HTML```.

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

Essa página está precisando de um pouco mais de estilo, vamos adicionar um arquivo ```CSS``` no repositório.
Adicione o dentro do ```head``` de seu ```HTML``` um link para o arquivo ```CSS```

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
<link href="https://fonts.googleapis.com/css2?family=Poppins:wght@100;400;800&display=swap" rel="stylesheet">
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
