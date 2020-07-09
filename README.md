# Padroes-de-Microservicos-Java
Um estudo do livro Microservices Patterns With examples in Java

## Capítulo 3: Comunicação entre Processos na Arquitetura de Microsserviços 

### 3.1: Visão Geral

#### 3.1.1: Estilos de Interação

Quando analisamos os estilos de interação entre serviços, temos duas dimensões a considerar. Uma delas diz respeito a quantidade de serviços que irão processar uma requisição (um-para-um vs um-para-muitos) e a  outra diz respeito ao sincronismo (síncrona vs assíncrona). Ao combinarmos essas duas dimenssões, temos os seguintes estilos de comunicação:

* request/response (requisição/resposta) - é uma comunicação síncrona onde um cliente faz uma requisição para um serviço e fica aguardando a resposta antes de prosseguir. Esse tipo de comunicação geralmente leva a serviços altamente acoplados;
* asynchronous request/response (requisição/resposta assíncrona) - um serviço cliente faz uma requisição a um outro serviço e aguarda a resposta, mas de maneira assíncrona, pois a resposta não será necessariamente imediata. A diferença, nesse caso, é que o serviço cliente não depende da resposta do serviço chamado para continuar suas atividades, ou seja, não fica bloqueado.
* one-way notifications (notificações de mão-única) - um serviço faz uma requisição para outro serviço, mas ambos serviços não esperam que uma resposta seja enviada.
* publish/subscribe (publicar/assinar) - um serviço cliente publica uma mensagem, a qual pode ser consumida por quantos serviços estiverem interessados nessa mensagem, podendo ser de 0 a "n" serviços.
* publish/async reponses (publicar/ respostas asíncronas) - um serviço cliente publica uma mensagem de requisição e espera, por um certo tempo, por respostas de serviços interessados.

#### 3.1.2: Definindo APIs em uma arquitetura de microsserviços

...em progresso...

### 3.2: Comunicações Síncronas

...em progresso...

### 3.3: Comunicações Assíncronas

...em progresso...
