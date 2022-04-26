# tech-for-recruiters

Vamos abrir um documento novo no Sublime Text
E inicar com a estrutura básica de uma página ```HTML```.

```
<!DOCTYPE html>
<html>
  <head>
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

E no ```CSS``, vamos colocar algum estilo no nosso ```body```:

```
body {
  color: grey;
  font-size: 16px;
  font-family: Poppins;
}
```



