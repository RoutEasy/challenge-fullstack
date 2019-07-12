# Challenge para desenvolvedor Full Stack

O objetivo deste desafio é avaliarmos o seu domínio em desenvolvimento fullstack, ou seja, sua organização, boas práticas com o código, criação e consumo de APIs Restfull, conhecimento dos frameworks e tecnologias utilizadas.

Um layout final bem elaborado e desenhado aponta para um diferencial seu, mas não é necessário se preocupar muito com o design. Afinal, não estamos buscando um designer para essa vaga! 

## Regras

1. Todo o seu código deve ser disponibilizado num repositório público ou privado em seu github ou bitbucket pessoal. Envie o link para william.kennedy@routeasy.com.br no prazo de 3 dias após o recebimento deste desafio;
2. Desenvolver o projeto utilizando: 
    - MEAN Stack (com AngularJS 1.x)
    - [Mongoose](http://mongoosejs.com) para modelagem dos dados a serem gravados no banco
    - HTML e CSS (ou algum pré-processador)
    - [Google Geocode API](https://developers.google.com/maps/documentation/geocoding/intro?hl=pt-br) (se precisar de uma API Key do Google, basta solicitar por e-mail)
    - [Leaflet](http://leafletjs.com/) para manipulação do mapa. O mapa a ser utilizado pode ser qualquer um (Google, Mapbox, OSM, etc).


## O Desafio

Este é o layout que deverá ser produzido:
![layout](challenge.png)

## Especificação das funcionalidades

Ao finalizar o desafio, o usuário deverá estar habilitado a cadastrar os clientes no formulário, e ao salvar, atualizar o mapa com o ponto (pin) daquele cadastro e a tabela com os dados do cliente. Na tabela deverá conter um botão para excluir o cliente, que deverá removê-lo do banco, mapa e tabela.

#### POST /deliveries

Você deve fazer um cadastro de entregas, que terá os seguintes campos:
1. Nome do cliente
2. Peso em kg
3. Endereço
    - Logradouro
    - Número
    - Bairro
    - Complemento
    - Cidade
    - Estado
    - País
    - Geolocalização
        - Latitude
        - Longitude

Estes dados devem ser salvos numa collection _deliveries_ do Mongo.
Note que no formulário há apenas um campo para colocar o endereço. Isso se deve ao fato de que o usuário deverá preencher apenas uma linha de endereço. Ao clicar em **Buscar**, os dados deste campo devem ser enviados à API do Google para buscar as informações de localização e incorporados ao objeto da delivery. Neste ponto, os campos de latitude e longitude devem ser preenchidos, mas devem ficar como _disabled_. Ao clicar em **Salvar**, salva os dados no banco, limpa o formulário e atualiza o mapa e a tabela. O botão **Resetar Cadastro** deve limpar a base de deliveries, tabela e pontos do mapa.

#### GET /deliveries

A requisição GET para /deliveries deve trazer um json com as informações das deliveries que existem no banco e exibí-las no mapa e na tabela.

#### DELETE /deliveries

Há um botão na tabela para excluir a delivery. Ele deverá remover todos os clientes tanto do banco quanto do mapa/tabela.


### Algumas dicas e observações
> Obs 1.: Fique a vontade para utilizar qualquer 3rd party;

> Obs 2.: Considere que todos os campos são de preenchimento obrigatório no formulário.

> Obs 3.: Considere validar os campos também na API e em caso de inconsistência retornar erro num JSON estruturado com código HTTP 400



## Dúvidas
Envie suas dúvidas diretamente para william.kennedy@routeasy.com.br ou abrindo uma issue.
