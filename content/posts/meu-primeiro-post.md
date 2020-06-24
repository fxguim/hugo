---
title: "Meu Primeiro Post"
date: 2020-06-04T12:07:43-03:00
tag:
---
![Ideia](https://github.com/fxguim/hugo/blob/master/static/images/meu-primeiro-post/wordpress-265132_1920.jpg?raw=true)

Ao pensar sobre Blogs normalmente você começa com Wordpress, bancos de dados, hospedagem e dores de cabeça similares quando na verdade você só quer escrever sobre algo sem se preocupar com detalhes técnicos. 

Para esse cenário existe os geradores de site estático e abaixo destaco cada uma das ferramentas que escolhi para os relatos deste blog aqui.

<!--more-->

# Programa do Hugo?

O Hugo é um gerador de sites estáticos, existem vários mas quem precisa saber de outros :smile:

A instalação do Hugo varia por sistema operacional, o ideal é que você faça a instalação seguindo a documentação oficial da ferramenta neste link:

<a href="https://gohugo.io/getting-started/installing/" target="_blank">Hugo - Installing</a>

## Programa instalado. E agora ?
Com o Hugo instalado é só criar o blog com o comando 

```bash
hugo new site nome_do_blog
cd nome_do_blog
```

Será necessário possuir um repositório Git para instalarmos temas em nosso blog, então execute o comando

```bash
git init
```

Como o objetivo é não se preocupar então vamos procurar um tema no site https://themes.gohugo.io/ e instalar via submodules do Git.

O comando para instalação é o seguinte:

```bash
git submodule add tema.git themes/tema
```

Cada tema tem uma configuração especifica que é explicado no próprio site do tema em https://themes.gohugo.io/ 

# Estamos versionando corretamente?

Além dos comandos git init e git submodule devemos criar um repositório no <a href="https://github.com/" target="_blank">GitHub</a> para armazenar remotamente nosso site.  

Alguns comandos Git na sequencia que nunca devem ser esquecidos:
```bash
git add -A
git commit -m "Site atualizado"
git push origin master -f
```

# E como criar um artigo?

A sintaxe de comando é por padrão:

```bash
hugo new pasta/nome_do_artigo.md
```

Precisamos sempre especificar o diretório, nome do arquivo e extensão. No caso deste meu primeiro post criei com o comando:

```bash
hugo new posts/meu-primeiro-post.md
```

Com isso será gerado o novo post que inicialmente tera como conteúdo do arquivo o seguinte <a href="https://gohugo.io/content-management/front-matter/" target="_blank">front matter</a>:

```markdown
---
title: "Meu Primeiro Post"
date: data de criação
draft: true
---
```

Agora é só escrever o texto desejado.
 
# Devo usar algum editor de textos? 

Os textos que o Hugo processa são escritos utilizando a linguagem <a href="https://www.markdownguide.org/" target="_blank">Markdown</a> e podemos utilizar varias ferramentas:
* Bloco de notas?
* <a href="https://notepad-plus-plus.org/" target="_blank">Notepad++?</a>
* <a href="https://www.netlifycms.org/" target="_blank">Interface administativa do Netlify?</a>

Mas e se nossa vontade seja apenas escrever um texto sem se preocupar nem com esse detalhe técnico? Nesse caso nada melhor que a ferramenta <a href="https://markdownmonster.west-wind.com/" target="_blank">Markdown Monster</a>. 

Mais detalhes sobre essa nobre ferramenta encontramos no próprio blog deles em https://medium.com/markdown-monster-blog ou lendo a bem detalhada documentação disponível em https://markdownmonster.west-wind.com/docs/.
 
# Onde hospedar?

Diretamente da Wikipedia: 
> A Netlify é uma empresa de computação em nuvem sediada em São Francisco que oferece serviços de hospedagem e back-end sem servidor para aplicativos da Web e sites estáticos.

Sendo assim, acesse https://www.netlify.com/ e crie sua conta.

Clique em “New site from Git” siga os detalhes e seja feliz :wink:.

Lembrar que o nosso artigo ainda não está em produção. Isso porque nós não configuramos para que fosse publicado. Para fazer isso precisamos alterar o <a href="https://gohugo.io/content-management/front-matter/" target="_blank">front matter</a>, retirando a linha

```markdown
draft: true
```

# E as imagens?

Organize qualquer imagem ou video de acordo com os posts 

```plaintext
/static/images/nome-do-post/nome-da-imagem-ou-video.extensão
```

Exemplificando os arquivos deste post seriam assim:

```plaintext
/content/posts/meu-primeiro-post.md
/static/images/meu-primeiro-post/arquivo_imagem.jpg
```

## Onde consigo imagens legais?

Existem diversos sites com bancos de imagens gratuitos como por exemplo o 
https://pixabay.com/pt/

Seja consciente com o direito autoral, respeite a imagem alheia, evite o <a href="https://images.google.com/" target="_blank">Google Images</a>

## E como fazer os gifs legais?

Portátil, fácil de usar e gratis, só poderia ser o 
<a href="https://www.screentogif.com/" target="_blank">ScreenToGif</a>

# Mensagem final genérica

> Nenhuma quantidade de evidência jamais convencerá um idiota
> <cite>Mark Twain[^1]</cite>

[^1]: No amount of evidence will ever persuade an idiot" ~ Mark Twain.
