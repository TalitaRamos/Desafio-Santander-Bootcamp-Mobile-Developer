# Kotlin

## Introdução

#### O que é Kotlin

O kotlin é gratuito e de código aberto

Kotlin é o nome de uma ilha russa**

>**Foi lançado em 2016**

>**Em 2017 o Google anuncia suporte a Kotlin**

>**2018 foi a segunda linguagem preferida dos desenvolvedores**

>**2019 Google anuncia que o Kolin é a nova linguagem oficial para desenvolvimento Android, ou seja, Kotlin First**

#### Estrutura do Kotlin

* Não utiliza ponto e vírgula
* Não possui operador térnario tradicional - possui operador próprio
* Possui Type Safe e null safe
* Inferência de tipo

#### Vantagens

* É segura, estruturada, menos verbosa, mais otimizada, tem relevância no mercado

* O Kotlin roda juntamento com o java, ou seja, é possível migrar partes de um aplicação para o kotlin enquanto outra parte ainda roda com o java.

* Smart cast (antes da execução é possível garantir que o stipos estão atribuídos corretamente)

* Null safety

#### Desvantagens

* Perde um pouco de desempenho

## Sintáxe básica

#### Tipos de dado

* int
* Long
* Float
* Double
* Array
* List 
* ArrayList
* Boolean
* Char
* Byte
* Short
* Null

> Para saber o valor máximo que uma variável pode receber basta executar o código dessa forma: `println(Int.MAX_VALUE)`

Para converter dados para outro tipo basta chamar a função de conversão na variável. Ex: `toByte(), toInt(), toLong()`. Se a conversão não for possível é retornado um erro de compilação ou um alerta é exibido em tempo de escrita.

#### Declaração de variáveis

##### Prefixos:

> CamelCase: Inicia a variável com letra minuscúla e as outras palavras possuem a primeira letra  maiúscula

> SNAKE_CASE: Sempre em letras maiúsculas e palavras separadas pelo underline(_)

* **Var** (valor mutável, CamelCase) : Variávvel que pode ter seu valor alterado durante o código

```
var currentAge = 22 // variável assume o valor recebido na primeira atribuição

var currentAge:Int? // Variável declarada apenas como int

currentAge = null || 22
```

* **Val** (valor imutável, CamelCase): Variável terá o valor atribuído somente uma vez - similar ao final

```
var currentAge = 22 // O valor não pode ser alterado

var currentAge:Int?
currentAge = null || 22
```

* **Const Val** (valor imutável, SNAKE_CASE): constante cujo o valor é atribuído durante a compilação

```
const val MIN_AGE = 16
const val MAX_AGE = 68
```

#### Erros na declaração de variáveis

* Não é permitido atribuir um valor após a declaração da variável sem que antes o tipo seja especificado ou a variável seja inicializada na declaração

```
var current
    currentAge = 90
```

* Não é permitido atribuir um valor de um tipo difente do tipo inferido na declaração da variável

```
var currentYear = 'Ano'
    currentYear = 2022
```

## Links

* [Documentação Android](https://developer.android.com/docs)

* [Documentação Kotlin](https://developer.android.com/kotlin)

* [Outra Documentação Kotlin](https://kotlinlang.org/)

* [Kotlin Playground](https://play.kotlinlang.org/)

* [KMM - Kotlin Mobile Multiplatform](https://kotlinlang.org/lp/mobile/)

* [Kotlin for javascript](https://kotlinlang.org/docs/js-overview.html)