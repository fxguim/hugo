---
title: "Escrevendo mais mas digitando menos no Android Studio"
date: 2020-06-26T06:22:00-03:00
description: "Reusabilidade de códido é otimizar seu tempo"
images:
- https://github.com/fxguim/hugo/blob/master/static/images/live-template/code-1839406_640.jpg?raw=true
tag:
- Live Template
draft: true
---
![Live Template]("https://github.com/fxguim/hugo/blob/master/static/images/live-template/code-1839406_640.jpg?raw=true")

Reusabilidade de códido é otimizar seu tempo, e existe uma funcionalidade comum em todos os IDEs da IntelliJ IDEA chamada Live Template que certamente aumentará a sua produção.

O trabalho com live templates vai fazer com que você economize em tempo a digitação de linhas de código mas ganhos expressivos dependem da metodologia trabalhada, nível de repetição inconsciente e tamanho do projeto, além é claro do envolvimento ou não de equipes.

<!--more-->

veja https://www.thecodecampus.de/blog/introduction-to-live-templates-in-intellij-idea/

# O que são Live Templates?

Os live templates são templates de código que agilizam o processo de codificação, templates já disponibilizados pelo próprio IDE em uso ou disponibilizados, pois criados ou importados, de alguma outra fonte..

# Criando um template

A criação de live templates é simples, veja a seguir um trecho de código que pode seguramente beneficiar o tempo de desenvolvimento em projeto caso se torne um código template:


Neste artigo vamos ao estudo de uma funcionalidade do Android Studio IDE que permite aos desenvolvedores Android o aumento de produtividade.

Mais precisamente, estaremos estudando: como utilizar os Live Templates. Funcionalidade comum em todos os IDEs da IntelliJ IDEA.

Animação de uso do Live Template Android Studio

Antes de prosseguir se inscreva 📩 na lista de e-mails do Blog para ter acesso aos conteúdos exclusivos sobre o dev Android.

O que são Live Templates?

Os live templates são templates de código que agilizam o processo de codificação, templates já disponibilizados pelo próprio IDE em uso ou disponibilizados, pois criados ou importados, de alguma outra fonte.

Exemplo: quando programando em Kotlin no Android Studio nós temos alguns templates padrões, um deles é o fun0 que gera um código generalizado de uma função sem argumentos, fazendo com que nós desenvolvedores somente tenhamos de colocar o nome da função e o corpo dela.

Veja a seguir:

Animação Live Template Android Studio fun0

Os live templates são uma excelente ferramenta para o reaproveitamento de códigos em diferentes projetos Android.
Criando um template

A criação de live templates é simples, veja a seguir um trecho de código que pode seguramente beneficiar o tempo de desenvolvimento em projeto caso se torne um código template:

...
val starter = Intent( this, MessagesActivity::class.java )
starter.putExtra( "message", "Nova mensagem de testes" )
startActivity( starter )
...

 

Selecionando o código anterior e copiando ele, podemos partir para o acesso a área de configuração de live templates, seguindo o roteiro:

    Entre no menu Android Studio;
    Acione "Preferences";
    Acione "Editor";
    Acione "Live Templates".

Animação abrindo a área de Live Template

Como estamos trabalhando aqui com códigos em Kotlin, vamos seguir as recomendações da documentação da IntelliJ IDEA e não vamos atualizar um grupo de live templates e sim criar um novo grupo.

No topo direito da área de live templates:

    Acione o "+";
    Escolha "Template Group";
    Na caixa de diálogo informe "KotlinCustom";
    Acione "Ok".

Animação criando um novo Live Template group

Agora o trecho final para termos o nosso primeiro template:

    Selecione "KotlinCustom";
    Novamente, no topo direito, acione o "+";
    Escolha a opção "Live Template";
    Cole o código anterior, de abertura de atividade, na área "Template text".

Animação criando um novo Live Template

Antes de prosseguir, vamos melhor entender a seguinte área de configuração de live template:

Configuração de um novo live template

    Abbreviation: permite a definição do termo que será utilizado para que o template de código seja colocado no lugar dele;
    Description: quando o programador digitar a abreviação, uma pequena janela de contexto apresentará a opção juntamente à descrição dela. Com a descrição o desenvolvedor saberá se deve ou não colocar aquele template de código;
    Template text: local onde ficará o código template. Temos três possíveis tipos de template:
        Simples;
        Parametrizado (quando há uso de variáveis);
        Cercado (blocos de códigos, como if(...) else).
    Options:
        Expand with: a tecla que o usuário terá de acionar para trocar a abreviação pelo código template. Por padrão é a tecla Tab;
        Reformat according to style: Se o código template adicionado deverá seguir as regras de formatação (espaços, tabulações, quebras de linhas, ...) já empregadas pelo desenvolvedor do código do projeto. Por padrão essa opção vem desmarcada e segundo alguns testes ela não segue fielmente o estilo em código;
        Shorten FQ names: quando adicionamos códigos em "Template text" o recomendado é que os nomes completos, incluindo os nomes de pacotes, sejam utilizados, assim os imports corretos serão adicionados em código quando o live template for colocado. A opção "Shorten FQ names" permite que os nomes completos dos tipos em uso não sejam colocados junto ao live template.
    Not applicable contexts yet. Define: aqui escolheremos os contextos onde nosso live template poderá ser utilizado.

A opção "Edit variables" nós abordaremos na próxima seção deste artigo.

Assim podemos ir aos preenchimentos:

    Em "Abbreviation" coloque o termo "startact";
    Em "Description" coloque "Código de chamada de atividade.";
    Em "Not applicable contexts yet. Define" clique em "Define" e marque "Kotlin". É possível filtrar ainda mais os contextos, mas aqui vamos permitir que todos os contextos de Kotlin aceitem o nosso novo live template;

Escolhendo o contexto do novo live template

    Em "Template text" vamos colocar os nomes completos, qualificados, dos tipos que aparecem em código, como a seguir:

val starter = android.content.Intent(
    this, 
    thiengo.com.br.livetemplate.MessagesActivity::class.java 
)
starter.putExtra( "message", "Nova mensagem de testes" )
startActivity( starter )

    Todas as outras opções deixe como estão. Clique em "Apply" e depois em "Ok".

Assim podemos, em código, digitar startact, visualizar a descrição:

Abreviação live template startact

E então acionar a tecla Tab:

Live template startact

Dessa forma criamos um simples live template. Agora vamos aprimorá-lo.
Trabalhando com variáveis

As variáveis em códigos de template devem estar entre $, exemplo: $contexto$. E há duas variáveis pré-definidas que não podem ser alteradas:

    $SELECTION$: utilizada para criar live templates cercados, ou seja, live templates de blocos de código;
    $END$: que indica onde estará o cursor assim que o live template for adicionado em código.

A principal vantagem na utilização de variáveis nos códigos templates é a possibilidade de criar códigos ainda mais genéricos e que assim poderão ser utilizados nos mais diversos contextos Android.

Veja o código a seguir:

...
Toast
    .makeText(
        this,
        "Mensagem toast",
        Toast.LENGTH_SHORT
    )
    .show()
...

 

Este certamente é um trecho de código que poderá ser utilizado em diversos projetos Android e em diferentes contextos, atividades e fragmentos, por exemplo. Com isso podemos criar um novo live template:

    Acesse o menu Android Studio;
    Acione "Preferences";
    Acione "Editor";
    Acione "Live Templates";
    Expanda "KotlinCustom";
    Crie um novo live template com as seguintes configurações:
        Abbreviation: toastm;
        Description: Cria um código Toast genérico;
        Not applicable contexts yet. Define: marque Kotlin;
        Em "Template text" coloque o código a seguir:

android.widget.Toast
    .makeText
        $context$, 
        "$END$", 
        android.widget.Toast.LENGTH_SHORT 
    )
    .show()

    Acione "Apply";

Note o uso de $END$ para que o programador já tenha o cursor no ponto que aguardará a mudança no template, a área de mensagem.

Temos também $context$ que ainda não faz nada. Vamos colocar uma característica em $context$ que fará com que ele utilize o contexto correto de acordo com a classe atual, vamos criar uma configuração para atividades e fragmentos.

Clique em "Edit variables", botão presente na área de configuração de um live template. A seguinte caixa de diálogo será aberta:

Edição de variável de live template

Em "Edit Template Variables" é possível modificar o nome de qualquer variável, escolher uma expressão pré-definida, definir um valor padrão e marcar se o cursor deve ou não pular a área desta variável caso haja algum valor válido para ser colocado no lugar dela.

A parte mais crítica é em "Expression", pois até mesmo condicional, operador ternário, é possível colocar. Em nosso caso coloque:

    Expression: groovyScript("_1.endsWith('Activity') ? 'this@'+_1 : 'activity'", kotlinClassName());
    Default value: "this" (sim, o valor padrão tem de vir entre aspas, mesmo sendo um nome reservado);
    Skip if defined: marcar.

Você notará que será necessário acionar a tecla Enter para que o valor definido em coluna permaneça. Ao final acione "Ok" e então acione "Apply". Por fim acione "Ok" novamente para fechar a caixa de diálogo de live template.

A função groovyScript() é uma das funções pré-definidas que podemos utilizar como expressão em valor de variável. Essa aceita como primeiro argumento um script em sintaxe Groovy (que é uma linguagem na plataforma Java) e os próximos argumentos definidos podem ser referenciados dentro do script Groovy por meio da posição dele.

Nosso primeiro argumento depois do script Groovy é o kotlinClassName(), que também é uma função pré-definida para ser utilizada somente em códigos Kotlin, onde será retornado o nome da classe que receberá o código template.

Se houvesse mais argumentos, por exemplo, um segundo argumento além do script Groovy, este poderia ser acessado pelo rótulo _2. Em nosso caso o retorno de kotlinClassName() é acessado pelo rótulo _1.

Na próxima seção estudaremos outras funções pré-definidas para variáveis de live templates.

Agora, em código, digitando toastm e acionando Tab, temos:

Animação live template toastm

Assim em qualquer projeto em nosso IDE Android Studio poderemos utilizar o novo live template toastm.
Funções pré-definidas para variáveis de template

Como informado na seção anterior, há várias funções pré-definidas que permitem que variáveis tenham expressões como valores. Na tabela a seguir há todas as funções disponíveis no Android Studio:
Função	Descrição
anonymousSuper()	Sugere um supertipo para uma expressão de objeto Kotlin.
camelCase(String)	Retorna a String passada como parâmetro no estilo CamelCase. Por exemplo, meu-arquivo-de-texto / meu arquivo de texto / meu_arquivo_de_texto será convertido para MeuArquivoDeTexto.
capitalize(String)	Capitaliza a primeira letra da String passada como um parâmetro.
capitalizeAndUnderscore(String)	Capitaliza todas as letras de uma String em CamelCase passada como parâmetro, e insere um sublinhado entre as partes. Por exemplo, a String DevProfissional seria retornada como DEV_PROFISSIONAL.
classNameComplete()	Retorna o nome completo da classe, incluindo o pacote dela.
clipboard()	Retorna o conteúdo da área de transferência do sistema (conteúdo em memória devido a operações de cortar e copiar).
complete()	Coloca o cursor exatamente onde está a variável com a definição complete() e já com um menu de contexto aberto e contendo sugestões para completar a expressão em curso, um nome de classe, por exemplo.
completeSmart()	Tem a mesma funcionalidade de complete(), porém com opções inteligentes, de acordo com o já foi utilizado pelo desenvolvedor em projeto.
concat(expression_1, ..., expression_n)	Concatena os resultados das expressões passadas como argumento.
date(String)	Retorna a data atual do sistema no formato especificado. Por padrão a data atual é retornada no formato de sistema. No entanto, se você especificar o formato de data entre aspas duplas, a data será apresentada neste formato. Exemplo: "mm-dd-YYYY" retornaria 10-01-2018 ao invés do padrão 01/10/2018.
decapitalize(String)	Substitui a primeira letra da String passada como argumento pela letra minúscula correspondente.
enum(string_1, ..., string_n)	Lista de Strings separadas por vírgula sugeridas para conclusão na chamada de template.
escapeString(String)	Escapa a String especificada.
expressionType(expression)	Retornar o tipo de dado do retorno da expressão passada como argumento. Exemplo: a expressão "true ? '1' :  '2'" tem como retorno um char, logo expressionType() retornará char.
fileName()	Retorna o nome do arquivo atual, contendo também a extensão dele.
fileNameWithoutExtension()	Retorna o nome do arquivo atual sem conter a extensão dele.
firstWord(String)	Retorna a primeira palavra da String passada como parâmetro.
functionParameters()	Retorna os parâmetros da função onde o live template está sendo adicionado. Todos eles separados por vírgulas e entre colchetes, [].
groovyScript("groovy code")	Retorna o script Groovy com o código especificado. Você pode usar a função groovyScript() com vários argumentos. O primeiro argumento é um texto de script que é executado ou um caminho para o arquivo que contém um script. Os próximos argumentos estão limitados às variáveis _1, _2, _3, ..._ n que estão disponíveis dentro do script. Além disso, a variável _editor (EditorImpl) está disponível dentro do script. Esta variável está vinculada ao editor atual.
kotlinAnyVariable()	Abre o menu de contexto com todas as variáveis possíveis para o local.
kotlinClassName()	Retorna o nome da classe atual onde o código template está sendo adicionado.
kotlinFunctionName()	Retorna o nome da função atual onde o código template está sendo adicionado.
kotlinPackageName()	Retorna o nome do pacote do projeto onde o código template está sendo adicionado.
kotlinSuggestVariableName()	Nomes possíveis são sugeridos para a variável.
kotlinVariable()	Abre o menu de contexto com todas as variáveis Kotlin possíveis para o local.
lineNumber()	Retorna o número da linha atual.
lowercaseAndDash(String)	Retorna letras minúsculas separadas por traços da String passada como argumento. Exemplo: a String MinhaClasse é convertida em minha-classe.
snakeCase(String)	Retorna a String no modelo snakeCase. Exemplo: se a String passada como parâmetro for minha_classe, a função retornará minhaClasse.
spaceSeparated(String)	Retorna a String separada por espaços, String CamelCase passada como argumento. Exemplo: se a String informada for MinhaClasse, a função retornará Minha Classe.
time(String)	Retorna o horário atual do sistema no formato especificado. Por padrão, o horário atual é retornado no formato de sistema. No entanto, se você especificar o formato de horário entre aspas duplas, o horário será apresentado neste formato. Exemplo: "hh:mm:ss" retornaria 10:54:38 ao invés do padrão 10:54.
underscoresToCamelCase(String)	Retorna a String passada como argumento no modelo CamelCase, substituindo os sublinhados. Exemplo: se a String informada for minha_variavel, a função retornará MinhaVariavel.
underscoresToSpaces(String)	Retorna a String passada como argumento com espaços em branco substituindo os sublinhados. Exemplo: a String minha_variavel será substituída por minha variavel.
user()	Retorna o nome do usuário atual, usuário de sistema.

Algumas dessas funções não funcionam no Kotlin e algumas outras não funcionam no Java. As funções que é garantido o funcionamento no Kotlin têm no rótulo também o nome desta linguagem.
Live template de bloco

Caso você precise criar um código template de bloco, basta fazer todo o caminho de criação de um live template comum e então utilizar a variável pré-definida $SELECTION$.

Siga o roteiro:

    Acesse o menu Android Studio;
    Acione "Preferences";
    Expanda "Editor";
    Selecione "Live Templates";
    Selecione "KotlinCustom";
    Agora crie um novo live template com as seguintes configurações:

Configuração live template de bloco

Acionando "Apply" e "Ok", podemos partir para os testes.

Para adicionar o bloco de código no entorno de algum código, selecione este script e pressione Alt + Ctrl (ou Command se estiver com o Mac) + T. Veja a seguir:

Animação live template de bloco
Templates pré-definidos

No Android Studio há inúmeros templates pré-definidos e que você certamente já utilizou alguns e provavelmente não sabia que o nome deles era live templates.

A seguir a listagem dos grupos de templates pré-definidos até a época da construção deste artigo (exceto o grupo KotlinCustom):

Live templates pré-definidos

Fique sempre ciente do contexto atendido pelo código live template, pois segundo alguns testes, todos os live templates disponíveis no grupo "Android" funcionam somente para contextos Java:

Live templates Android Java

A recomendação da documentação ItelliJ IDEA é que em caso de atualização de templates ou de adição, que estes ocorram em um novo grupo criado ou no grupo vazio e pré-definido "user", sempre em novos templates criados e não em templates pré-definidos.
Classes utilitárias vs Live templates

Classes utilitárias são excelentes em qualquer projeto de software, não somente em projetos Android. São elas que suportam métodos que fogem da responsabilidade das classes de domínio.

Porém classes utilitárias são de contexto menor do que códigos template, classes utilitárias atendem a projetos específicos, códigos template atendem a todos os projetos, de uma determinada linguagem / plataforma, em desenvolvimento.

Resumo: live templates e classes utilitárias se complementam.
Pontos negativos

    Há pouco material, oficial ou não, sobre os live templates;
    A documentação do JetBrains IntelliJ IDEA não está atualizada, nem mesmo abordando as funções pré-definidas para códigos em Kotlin;
    Para algumas "autoridades" no Android o assunto "live templates" é considerado avançado, quando na verdade não tem nada de complexo.

Pontos positivos

    Para aqueles desenvolvedores que programam vários projetos Android, pode ser uma maneira simples de diminuir o tempo de desenvolvimento;
    Também é possível importar e exportar live templates;
    O trabalho com variáveis, live templates parametrizados, facilita em muito na criação de códigos genéricos e que atendam a distintos projetos.

Slides

Abaixo os slides com a apresentação dos live templates no Android Studio:

Vídeos

A seguir os vídeos com o passo a passo para uso dos live templates no Android Studio:

Conclusão

Conhecer por completo o ambiente de desenvolvimento para a criação de seus aplicativos Android é algo que certamente aumentará em muito a sua produção.

O trabalho com live templates vai fazer com que você economize em tempo a digitação de linhas de código para, por exemplo: mensagens Toast; inicialização de atividades; e adapters de frameworks de listas.

Mas confesso que não vejo ganhos expressivos se você trabalha em cima da metodologia de códigos limpos, sem repetição, e em um único projeto longo, sem equipes envolvidas.