---
title: Criando um Template App
date: '2020-06-15T17:19:44-03:00'
autoThumbnailImage: true
thumbnailImagePosition: top
coverImage: /images/uploads/idea-1876659_640.jpg
---
Criando um Template App

Para um aprendizado recursivo em Flutter resolvi criar um projeto básico de software, um projeto chamado "Template App" no Android Studio e salva-lo no Github mas :
- Porque aprender [Flutter](https://medium.com/toshiossada/por-que-flutter-8f17cc2bb02e) ?
- Porque salvar no [Github](http://blog.virtuacreative.com.br/introducao-ao-github.html) ?

Desconsiderando esses detalhes, um projeto básico de software permite ao desenvolvedor utilizar um arcabouço já pensado, refletivo e, preferencialmente, testado. Não que venha ser o nosso caso de início pois ainda estamos aprendendo. 

<!--more-->

## Configurações do pubspec.yaml

O pubspec é o arquivo de meta-dados que especifica as dependências de um projeto flutter. Dentre as centenas de pacotes existentes que podem ser apreciados em [Pub.dev](https://pub.dev/) alguns destacam se para o nosso Template App:

### effective_dart 
**O que é?** ferramentas que analisam código-fonte para acusar erros de programação, bugs, erros estilísticos, e construções suspeitas.  
**Por que usar?** encontrar artefatos indesejáveis  
**Onde encontro?** [https://pub.dev/packages/effective_dart](https://pub.dev/packages/effective_dart)

### Mock library(mockito)
**O que é?** Objetos que simulam o comportamento de objetos reais de forma controlada. Útil para testar comportamento de uma classe.  
**Por que usar?** viver em TDD (Desenvolvimento Orientado por Testes) que tem por lema : se algo não é possível de ser testado então foi desenvolvido de forma errada!  
**Onde encontro?** [https://pub.dev/packages/mockito](https://pub.dev/packages/mockito)

### Functional programming in Dart
**O que é?** programação funcional é um paradigma de programação que trata a computação como uma avaliação de funções matemáticas e que evita estados ou dados mutáveis.  
**Por que usar?** aprender um novo paradigma ?!?  
**Onde encontro?** [https://pub.dev/packages/dartz](https://pub.dev/packages/dartz)
  
### Service locator
**O que é?** encapsulamento dos processos envolvidos na obtenção de um serviço com uma forte camada de abstração  
**Por que usar?** [https://pub.dev/packages/get_it#why-getit](https://pub.dev/packages/get_it#why-getit)  
**Onde encontro?** [https://pub.dev/packages/get_it](https://pub.dev/packages/get_it)
  
### Bloc for state management
**O que é?** implementação do padrão Bloc(Business Logic Component)  
**Por que usar?** separar apresentação da logica de negócios.  
**Onde encontro?** [https://pub.dev/packages/flutter_bloc](https://pub.dev/packages/flutter_bloc)

### Bloc for state management (Test)
**O que é?** ferramenta pra testar Blocs integrado ao Mockito  
**Por que usar?**  facilitar o TDD em Blocs  
**Onde encontro?** [https://pub.dev/packages/bloc_test](https://pub.dev/packages/bloc_test)  
  
### Code generator for unions/pattern-matching/copy
**O que é?** gerador de código  
**Por que usar?** diminuir o boilerplate code  
**Onde encontro?** [https://pub.dev/packages/freezed](https://pub.dev/packages/freezed)
  
> Nenhuma quantidade de evidência jamais convencerá um idiota
> <cite>Mark Twain[^1]</cite>

[^1]: No amount of evidence will ever persuade an idiot" ~ Mark Twain.
