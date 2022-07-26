# Android Studio

## Manutenção

Existem ferramentas no Android studio que ajudam em correções do código em tempo real, sem que seja necessário rodá-lo novamente, e no monitoramento da performance do nosso aplicativo


### Apply changes and restart activity

O Apply changes and restart activity aplica as modificações no código e reinicia a Activity sem reiniciar o app

### Android Profiler

O Android Profile oferece em tempo real dados para ajudar a entender como o app usa recursos de CPU, memória, rede e bateria

## Debugger

Ferramentas que auxiliam na investigação de bugs no código

### Breakpoint

Pontos de parada no código

### Debug App

O Debug App executa o aplicativo em modo de depuração e pausa a execução conforme os pontos de interrupção definidos

### Attach debugger

Adiciona um debugger com o app em execução, sem que ele tenha que reinicar o build

### ADB e ADB plugin

Android Debug Bridge

Operações que facilitam a manipulação no mode debug

Pode ser chamado pelo temrinal mas possui plugin com principais funcionalidades (ADB Idea)

Pode revogar permissões, limpar dados do app

### LogCat

Aba em que são exibidos logs da aplicação e do aparelho (do SO, de outros apps, etc)

> Tipos de logs da aplicação

> Criação de tags

> Emisssão dinâmica de logs

> Omissão de logs irrelevantes

> Contextualização para crashs e exceptions

#### Tipos de log

> Debug(log.d)

> error(log.e)

> Info(log.i)

> Verbose(log.v)

> Warning(log.w)

#### Exceptions

A Throwable é uma superclasse de todos os Erros e Exception

> Erros podem ocorrer tanto durante a execução quanto na aplicação

> Exception  - geralmente quebram (causam crash) na aplicação

> Ex: ActivityNotFoundException, NullPointerException, IndexOutOfBoundsException, classCastException

Para pegar todas as exceptions que não tiveram tratamento : 
````
val currentThread = Thread.currentThread()
currentThread.setIncaughtExceptionHandler{_, throwable ->

    val t = throwable.message

}
````

### Evaluate Expressions

Funciona quando a aplicação já está pausada em um ponto de interrupção, abrindo um console,onde você consegue simular novas ocasiões no app

> Atalho: Alt + F8

## Pesquisas

O Android Studio possui ferramentos que auxiliam na pesquisa de código, classes, palavras-chave.

### Pesquisa de classes 

A pesquisa de classes possibilita que você encontre determinada classe sem navegar no projeto

Clicando duas vezes em `Shift` ou na lupa você abre uma aba de pesquisa de classes e arquivos

### Find in path

Permite encontrar qualquer tipo de texto, código, classe, método e etc, no projeto apenas digitando aquilo que você precisa encontrar

> Atalho: `Ctrl + shift + f`

### Layout Inspector

Tira um screenchot da tela que está em exibição no dispositivo e te detalha toda a estrutura de layout, como ids, textos e o tipo dos layouts e componentes da tela

## Atalhos

* Evaluate: `Alt + F8`

* Parcelabre: Selecionar o nome da classe e clicar em `alt + enter`

* Extrair para resource: `Alt + Enter`

* Replace: `Ctrl + r`

* Pesquisa de classe : `Shift shift`

* Find in path : `Ctrl + shift + f`

## Links

* [Apply changes and restart activity](https://developer.android.com/studio/run#apply-changes)

* [Android Profiler](https://developer.android.com/studio/profile/android-profiler)

* [Debugger](https://developer.android.com/studio/debug)

* [Atalhos do teclado](https://developer.android.com/studio/intro/keyboard-shortcuts)

* [Layout Inspector](https://developer.android.com/studio/debug/layout-inspector)

* [Android Roadmap](https://roadmap.sh/android)

* [ADB](https://developer.android.com/studio/command-line/adb?hl=pt&gclid=Cj0KCQjw_viWBhD8ARIsAH1mCd4g_t-kojtXURGhJcelDKrAUwLpzUjBnSDAIad75zTcr6EIQrlnxBUaAntFEALw_wcB&gclsrc=aw.ds)
