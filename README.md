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

Uma API deve definir uma interface e expor suas funcionalidades sem expor os aspectos de sua implementação. Em uma aplicação monolítica, principalmente em uma linguagme fortemente tipada - como o Java, caso uma interface mude de forma a ficar incompatível com um cliente, a aplicação apresentará erro em tempo de compilação. Embora possa ser trabalhoso, os erros podem ser facilmente encontrados e corrigidos, permitindo a alteração da interface.

Porém, em uma arquitetura de microsserviços, se um serviço muda sua API de forma a ficar incompatível com o que os seus clientes usam atualmente, teremos um problema sério. Como os serviços são independentes e no são compilados juntos - normalmente sendo responsabilidades de times diferentes - a incompatibilidade se manisfetará como erros em tempo de execução, os quais não serão simples de encontrar a causa raiz.

Por isso, a definição da API e suas interfaces é extremamente importante em uma arquitetura de microsserviços, independente dos estilo de comunicação ou immplementaçes escolhidas. Precisa-se ter uma mentalidade de "API-first design" e alinhar muito bem as interfaces da API antes de realizar qualquer tipo de implementação e alteração.

#### 3.1.3: 

...em progresso...

### 3.2: Comunicações Síncronas

...em progresso...

### 3.3: Comunicações Assíncronas

...em progresso...
