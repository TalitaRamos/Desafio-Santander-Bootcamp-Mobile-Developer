# Arquitetura

[Componentes, Layouts e UI/UX em apps android](https://github.com/TalitaRamos/Desafio-Santander-Bootcamp-Mobile-Developer/tree/main/Arquitetura/layout.md)

### AndroidManifest

Recebe informações essenciais para as ferramentas de compilação do Android, para o SO Android e para a Google Play.

Recebe a declaração de todas as activities, permissões do app,etc

### Ciclo de vida

Responsável por informar a criação, interrupção ou retomada de uma tela ou da destruição do processo pelo sistema

* onCreate: Momento em que a tela é criada mas ainda não é possível ver e nem interagir com nada. Ponto inicial do ciclo e só é chamado uma vez

* onStart: Desenha os componentes visualmente

* onResume: Aqui é o ponto onde o usuário já pode interagir com a tela. Enquanto o usuário está interagindo com a tela o estado é o onResume. O onResume é o ponto final do ciclo visível

* onPause: Quando o foco é perdido, ou seja,algo está sobrescrevendo a minha tela porém ela ainda está parcialmente visível. Se o usuário voltar para a tela o onResume é retomado

* onStop: Quando a tela não está visível, ou seja, minimizada. Se o usuário retornar ele passa pelo onRestart(voltando para redesenhar a tela como estava antes passando pelo onStart) 

* onRestart: Processo feito quando a tela estava minimizada e o usuário volta para ela. A tela será redesenhada pois não estava mais sendo exibida porém será redesenhada com base no estado anterior da tela passando pelo onStart.

* onDestroy: Final do ciclo. Quando o usuário decide sair de vez da aplicação

> Ciclo visível: Enquanto o usuário está com a aplicação aberta

> Ciclo invisível: Enquanto a aplicação está em segundo plano ou quando o usuário fecha o app

![Ciclo de vida](../imagens/ciclo_de_vida.png)

### Arquitetura

O Android é uma pilha de software com base em Linux de código aberto criada para diversos dispositivos e fatores de forma. 

[Arquitetura da plataforma ](https://developer.android.com/guide/platform?hl=pt-br#:~:text=O%20Android%20%C3%A9%20uma%20pilha,pilha%20de%20software%20do%20Android.)

### Segurança

* Proteger a troca de informações

 - Configurar segurança de rede: como âncoras de segurança personalizadas, cancelar o usp do tráfego de texto simples, fixar certificados
 
 - SafetyNet: Conjuntos de servições que ajudam a proteger o app de ameças a segurança
 
 - Criptografia: Especificar um provedor, escolher um algoritmo de criptografia
 
 - Aparelhos com android 9 é possível usar confirmação protegida pelo android(útil para transações)
 
* Oferecer as permissões corretas (mínimo de permissões)

* Armazenar dados de forma segura

 - Armazenamento interno: Acesso só pelo app
 - Armazenamento externo: Qualquer app pode acessar
 - Provedor de conteúdo: Mecanismo e armazenamento que pode permitir ou não que outros apps acessem
 
* Manter serviços e dependências atualizadas

* Resolver problemas encontrados pelo Google Play

 - O programa App Security Improvement auxilia os desenvolvedores a achar falhas no app e indicam ajustes. Os apps são analisados quando colocados na loja


[Usar o Google Play Protect para manter a segurança dos seus apps e a privacidade dos seus dados](https://support.google.com/googleplay/answer/2812853?hl=pt-BR)


[Programa de divulgação de vulnerabilidades](https://developers.google.com/android/play-protect/starting-a-vdp)

[Security](https://source.android.com/security)

### Android App Bundle

formato que inclui todo o código e recursos compilados do seu aplicativo e adia a geração e assinatura de APK no Google Play

### MVVM

Model-View-View-Model

A recomendação da google é usar a arquitetura MVVM em projetos android

![MVVM](../imagens/mvvm.png)

* Activity/Fragment (View): Camada onde teremos as partes relacionadas a componentes visuais(activities/fragments) e lógica relacionada a esses componentes

* ViewModel: Responsável por ter a lógica de negócio (o viewmodel não deve "conhecer" os componentes de UI)

* Repository: Manipula operações de dados com o banco de dados e/ou webservice

* Datasorce: Fonte dos dados(local ou remoto). Pode ser únido em uma camada que é o model

* LiveData: Armazena dados observáveis

[Guia para a arquitetura do app](https://developer.android.com/jetpack/guide)

[Visão geral do ViewModel ](https://developer.android.com/topic/libraries/architecture/viewmodel?hl=pt-br)

### clean Architeture

* Domain: Modelos e regras de negócio

* Data: Abstração para acessar o datasource

* Usecases: Transmite as ações do usuário

* App: Irá conter as implementações das interfaces da camada de dados