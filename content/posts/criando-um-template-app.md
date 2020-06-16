---
title: Criando um Template App
date: '2020-06-15T17:19:44-03:00'
autoThumbnailImage: true
thumbnailImagePosition: top
coverImage: /images/uploads/idea-1876659_640.jpg
---
Para um aprendizado recursivo em Flutter resolvi criar um projeto básico de software, um projeto chamado "Template App" no Android Studio e salva-lo no Github mas :

* Porque aprender [Flutter](https://medium.com/toshiossada/por-que-flutter-8f17cc2bb02e) ?
* Porque salvar no [Github](http://blog.virtuacreative.com.br/introducao-ao-github.html) ?

Desconsiderando esses detalhes, um projeto básico de software permite ao desenvolvedor utilizar um arcabouço já pensado, refletivo e, preferencialmente, testado. Não que venha ser o nosso caso de início pois ainda estamos aprendendo. 

<!--more-->

## Configurações do pubspec.yaml

O pubspec é o arquivo de meta-dados que especifica as dependências de um projeto flutter. Dentre as centenas de pacotes existentes que podem ser apreciados em [Pub.dev](https://pub.dev/) alguns destacam se para o nosso Template App:

### effective_dart

 Linter rules corresponding to the guidelines in Effective Dart.

### Mock library

  mockito: ^4.1.1

### Functional programming thingies

  dartz: ^0.9.1

### Service locator

  get_it: ^4.0.2

### Bloc for state management

  flutter_bloc: ^4.0.0

### Code generator for unions/pattern-matching/copy

  freezed_annotation: ^0.7.1

***

> Nenhuma quantidade de evidência jamais convencerá um idiota
> — <cite>Mark Twain\[^1]</cite>

\[^1]: No amount of evidence will ever persuade an idiot" ~ Mark Twain.
