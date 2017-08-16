# Challenge para desenvolvedor Full Stack

Objetivo deste desafio é avaliarmos o seu domínio em desenvolvimento fullstack, ou seja, sua organização, estilo e boas práticas com o código, criação de APIs Restfull, conhecimento dos frameworks e tecnologias utilizadas.

## Regras

1. Todo o seu código deve ser disponibilizado num repositório público ou privado em seu github ou bitbucket pessoal. Envie o link para william.kennedy@routeasy.com.br;
2. Desenvolver o projeto utilizando: 
    - MEAN Stack (pode ser um fork do [MEAN.js](https://github.com/meanjs/mean))
    - Mongoose para modelagem dos dados a serem gravados no banco
    - HTML e CSS (ou algum pré-processador)
    - Google Geocode API
    - [Leaflet](http://leafletjs.com/) para manipulação do mapa. O mapa a ser utilizado pode ser qualquer um (Google, Mapbox, OSM, etc).


## O Desafio

Este é o layout que deverá ser produzido:
![layout](layout-challenge.png)

## Especificação das funcionalidades

Ao finalizar o desafio, o usuário deverá estar habilitado a cadastrar os clientes no formulário, e ao salvar, atualizar o mapa com o ponto daquele cadastro e a tabela com os dados do cliente. Na tabela há um botão para excluir o cliente, que deverá removê-lo do banco, mapa e tabela.

#### POST /deliveries

Você deve fazer um cadastro de entregas, que ter os seguintes campos:
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
Note que no formulário há apenas um campo para colocar o endereço. Isso se deve ao fato de que o usuário deverá preencher apenas uma linha de endereço. Ao clicar em **Salvar**, os dados devem ser enviados à API do Google para buscar as informações de localização, incorporados ao objeto da delivery e salvos no banco.

#### GET /deliveries

A requisição GET para /deliveries deve trazer um json com as informações das deliveries que existem no banco e exibí-las no mapa e na tabela.

#### DELETE /deliveries

Há um botão na tabela para excluir a delivery. Ele deverá remover o cliente tanto do banco quanto do mapa/tabela.


### Algumas dicas e observações
> Obs 1.: Fique a vontade para utilizar qualquer 3rd party;

> Obs 2.: Considere que todos os campos são de preenchimento obrigatório no formulário.

> Obs 3.: Considere validar os campos também na API e em caso de inconsistência retornar erro num JSON estruturado com código HTTP 400



## Dúvidas
Envie suas dúvidas diretamente para william.kennedy@routeasy.com.br ou abrindo uma issue.
