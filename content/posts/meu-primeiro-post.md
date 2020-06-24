---
title: "Meu Primeiro Post"
date: 2020-06-04T12:07:43-03:00
tag:
---

Ao pensar sobre Blogs normalmente você começa com Wordpress, bancos de dados, hospedagem e dores de cabeça similares quando na verdade você só quer escrever sobre algo sem se preocupar com detalhes técnicos. 

Para esse cenário existe os geradores de site estático e abaixo destaco cada uma das ferramentas que escolhi para os relatos deste blog aqui.

Programa do Hugo?

Local ok mas e remotamente?


### Como criar um artigo?

A sintaxe de comando é por padrão:

```powershell
hugo new pasta/nome_do_artigo.md
```

Precisamos utilizar a nossa versão de acordo com as configurações e tema escolhidos, no meu caso o meu primeiro post criei com o comando:

```powershell
hugo new posts/meu-primeiro-post.md
```

Com isso sera gerado o novo post que inicialmente tera como conteúdo do arquivo:

```markdown
---
title: "Meu Primeiro Post"
date: data de criação
draft: true
---
```

Agora é só escrever o texto desejado.

### Devo usar algum editor de textos? 

Os textos que o Hugo processa são escritos utilizando a linguagem <a href="https://www.markdownguide.org/" target="_blank">Markdown</a> e podemos utilizar varias ferramentas:
* Bloco de notas?
* <a href="https://notepad-plus-plus.org/" target="_blank">Notepad++?</a>
* <a href="https://www.netlifycms.org/" target="_blank">Interface administativa do Netlify?</a>

Mas e se nossa vontade seja apenas escrever um texto sem se preocupar nem com esse detalhe técnico? Nesse caso nada melhor que a ferramenta <a href="https://markdownmonster.west-wind.com/" target="_blank">Markdown Monster</a>. 

Mais detalhes sobre essa nobre ferramenta encontramos no próprio blog deles em https://medium.com/markdown-monster-blog ou lendo a bem detalhada documentação disponível em https://markdownmonster.west-wind.com/docs/.

Onde hospedar?
> GitHub+Netfily.

E as imagens?
Put them in /static/, typically /static/img/. I often use subdirectories with names identical to post slugs, ie:

/content/future-of-bali.md
/static/img/future-of-bali/green-school-power-plant.jpg

to store images for that particular post.
https://pixabay.com/pt/
E como fazer os gifs?


> Nenhuma quantidade de evidência jamais convencerá um idiota
> <cite>Mark Twain[^1]</cite>

[^1]: No amount of evidence will ever persuade an idiot" ~ Mark Twain.
