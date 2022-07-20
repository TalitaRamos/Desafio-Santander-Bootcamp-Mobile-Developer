# Componentes, Layouts e UI/UX em apps android

## Android Jetpack

#### Introdução

Conjuntos de bibliotecas que encapsula uma série de boas práticas e componentes para reduzir códigos repetitivos

![Android Jetpack](../imagens/jetpack.png)

> Androidx : Substitui as antigas bibliotecas de suporte e faz a padronização dessas bibliotecas

> Core-ktx: Traz o core das dependências de extensão do kotlin 

> AppCompat : Biblioteca de compatibilidade para versões mais antigas da API do android

> ConstraintLayout : Uma das formas mais flexíveis para construir layouts

#### View Binding

Facilita/centraliza o acesso aos componentes definidos no XML

```
android {
    buildFeatures {
        viewBinding true
    }
}
```

#### SwipeRefreshLayout

Componente para fazer refresh de uma listagem de elementos

```
implementation 'androidx.swiperefreshlayout:swiperefreshlayout:1.1.0'
```

## Material Design

Sistema de design genérico que pode ser aplicado em diversas plataformas

Referências importantes:

* [Sistemas de cores](https://material.io/design/color/the-color-system.html#tools-for-picking-colors)
    * [Color Tool](https://material.io/resources/color/#!/?view.left=0&view.right=0)
    
* [Temas claro e escuro](https://material.io/design/color/dark-theme.html#ui-application)
    
* [Variações de "Top App Bars"](https://material.io/components/app-bars-top/android#regular-top-app-bar) 

> Alt + Enter: Extrair para resource
> Ctrl + r: Replace
## Layouts do App

## Glide

Gerenciador de mídia rápido e eficiente que abstrai o processo de carregamento de imagens em Android, gerenciando desde a decodificação e transformação até o controle do cache das mesmas

> implementation 'com.github.bumptech.glide:glide:4.11.0'

> annotationProcessor 'com.github.bumptech.glide:compiler:4.11.0'

## Retrofit

Cliente HTTP para Android e Java. Tem a função de abstrair a complexidade no consumo de APIs. Possui uma série de facilidades que facilita o consumo de recursos.

> implementation 'com.squareup.retrofit2:retrofit:2.9.0'

> implementation 'com.squareup.retrofit2:converter-gson:2.9.0'

## Parcelable

É uma estratégia de (de)serialização de dados padrão em apps android, ou seja, é a implementação utilizada para troca de mensagem entre telas.

```
plugins {

    id 'kotlin-parcelize'
}    
```

```
@Parcelize
data class Match (
    @SerializedName("descricao")
    val description: String,
    @SerializedName("local")
    val place: Place,
    @SerializedName("mandante")
    val homeTeam: Team,
    @SerializedName("visitante")
    val awayTeam: Team
) : Parcelable
```
```
public class Place implements Parcelable {
    @SerializedName("nome")
    private String name;
    @SerializedName("imagem")
    private String image;
}
//Ao selecionar o nome da classe e clicar em alt + enter o parcelabre é implementado
```

## Criar efeito de clique

```
android:clickable="true"
android:focusable="true"

//ripple effect
android:background="?attr/selectableItemBackgroundBorderless"

//selectablet effect
android:background="?attr/selectableItemBackground"

//Button effect
android:adjustViewBounds="true"
style="?android:attr/borderlessButtonStyle"
```

## Links

* [Documentação Android Jetpack](https://developer.android.com/jetpack?gclid=CjwKCAjwk_WVBhBZEiwAUHQCmejNWru4iWG4PrezVv7iarzW4OlPUx3W2hHDaEodcRbwVJ-8iGwv6xoC1VsQAvD_BwE&gclsrc=aw.ds)

* [Material.io](https://material.io/)


* [Android Open Source Project](https://source.android.com/)

* [Retrofit (HTTP Client)](https://square.github.io/retrofit)

* [Glide (Image Loading)](https://github.com/bumptech/glide)

* [Parcelable](https://developer.android.com/kotlin/parcelize?hl=pt-br)

* [Listar dinâmicas com Recycler View](https://developer.android.com/guide/topics/ui/layout/recyclerview?hl=pt-br)

* [LiveData](https://developer.android.com/topic/libraries/architecture/livedata?hl=pt-br)

* [ViewModel](https://developer.android.com/topic/libraries/architecture/viewmodel?gclid=Cj0KCQjwlK-WBhDjARIsAO2sErRFMssdP13ObaIhR9Z7k8Z67v8_r05_6mCPBncziAmEj9dEj-sp854aAlu7EALw_wcB&gclsrc=aw.ds)

* [Room](https://developer.android.com/training/data-storage/room)
