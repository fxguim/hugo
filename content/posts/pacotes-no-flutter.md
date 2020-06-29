---
title: Pacotes no flutter, qual usar?
date: '2020-06-15T17:19:44-03:00'
description: "Configurações do pubspec: O que é? Porque usar? Onde encontro?"
images:
- https://github.com/fxguim/hugo/blob/master/static/images/pacotes-no-flutter/idea-1876659_640.jpg?raw=true
tag:
---
![Ideia](https://github.com/fxguim/hugo/blob/master/static/images/pacotes-no-flutter/idea-1876659_640.jpg?raw=true)

No aprendizado recursivo em Flutter um dos pontos que mais me chamou atenção no começo ao cair de paraquedas é a dúvida existencial de qual pacote usar. Entretanto :
- Porque aprender [Flutter](https://medium.com/toshiossada/por-que-flutter-8f17cc2bb02e) ?
- Porque salvar no [Github](http://blog.virtuacreative.com.br/introducao-ao-github.html) ?
- Porque <a href="https://guimacoders.netlify.app/posts/meu-primeiro-post/" target="_blank">estou escrevendo? E como? E onde</a> ?

Desconsiderando esses detalhes, um projeto básico de software permite ao desenvolvedor utilizar um arcabouço já pensado, refletivo e, preferencialmente, testado. Não que venha ser o nosso caso de início pois ainda estamos aprendendo. 

<!--more-->

# Configurações do pubspec.yaml

O pubspec é o arquivo de meta-dados que especifica as dependências de um projeto flutter. Dentre as centenas de pacotes existentes que podem ser apreciados em [Pub.dev](https://pub.dev/) alguns destacam se para o nosso Template App:

## effective_dart 
**O que é?** ferramentas que analisam código-fonte para acusar erros de programação, bugs, erros estilísticos, e construções suspeitas.  
**Por que usar?** encontrar artefatos indesejáveis  
**Onde encontro?** [https://pub.dev/packages/effective_dart](https://pub.dev/packages/effective_dart)

## Mock library(mockito)
**O que é?** Objetos que simulam o comportamento de objetos reais de forma controlada. Útil para testar comportamento de uma classe.  
**Por que usar?** viver em TDD (Desenvolvimento Orientado por Testes) que tem por lema : se algo não é possível de ser testado então foi desenvolvido de forma errada!  
**Onde encontro?** [https://pub.dev/packages/mockito](https://pub.dev/packages/mockito)

## Functional programming in Dart
**O que é?** programação funcional é um paradigma de programação que trata a computação como uma avaliação de funções matemáticas e que evita estados ou dados mutáveis.  
**Por que usar?** aprender um novo paradigma ?!?  
**Onde encontro?** [https://pub.dev/packages/dartz](https://pub.dev/packages/dartz)
  
## Service locator
**O que é?** encapsulamento dos processos envolvidos na obtenção de um serviço com uma forte camada de abstração  
**Por que usar?** [https://pub.dev/packages/get_it#why-getit](https://pub.dev/packages/get_it#why-getit)  
**Onde encontro?** [https://pub.dev/packages/get_it](https://pub.dev/packages/get_it)
  
## Bloc for state management
**O que é?** implementação do padrão Bloc(Business Logic Component)  
**Por que usar?** separar apresentação da logica de negócios.  
**Onde encontro?** [https://pub.dev/packages/flutter_bloc](https://pub.dev/packages/flutter_bloc)

## Bloc for state management (Test)
**O que é?** ferramenta pra testar Blocs integrado ao Mockito  
**Por que usar?**  facilitar o TDD em Blocs  
**Onde encontro?** [https://pub.dev/packages/bloc_test](https://pub.dev/packages/bloc_test)  
  
## Code generator for unions/pattern-matching/copy
**O que é?** gerador de código  
**Por que usar?** diminuir o boilerplate code  
**Onde encontro?** [https://pub.dev/packages/freezed](https://pub.dev/packages/freezed)

# Mensagem final genérica

> Quem não está superando algum medo todos os dias, não aprendeu o segredo da vida.
> <cite>Ralph Waldo Emerson[^1]</cite>

[^1]: <a href="https://www.azquotes.com/quote/89297" title="Ralph Waldo Emerson quote"><img src="https://www.azquotes.com/picture-quotes/quote-he-who-is-not-everyday-conquering-some-fear-has-not-learned-the-secret-of-life-ralph-waldo-emerson-8-92-97.jpg" alt="He who is not everyday conquering some fear has not learned the secret of life. - Ralph Waldo Emerson"></a>

