# producer-service

Este projeto é um exemplo simples de como utilizar o RabbitMQ para enviar mensagens em um cenário de microsserviços.

## Requisitos

Para executar o projeto, é necessário ter o Docker e o Docker Compose instalados.

## Como executar

1. Clone este repositório: `git clone https://github.com/samuelalmeida95/producer-service.git`
2. Acesse o diretório do projeto: `cd producer-service`
3. Inicie os containers do RabbitMQ e do aplicativo com Docker Compose: `docker-compose up -d`
4. Envie uma mensagem para a fila: `http://localhost:8080/send-message?message=Hello%20World`

## Funcionamento

Este projeto consiste em um aplicativo Spring Boot que envia mensagens para uma fila do RabbitMQ.

O aplicativo expõe um endpoint HTTP `/send-message` que recebe uma mensagem como parâmetro de consulta e envia a mensagem para a fila `product.log` do RabbitMQ. Quando uma mensagem é enviada com sucesso, o aplicativo exibe um log.

O RabbitMQ é executado em um contêiner Docker separado, com suas configurações definidas no arquivo `docker-compose.yml`.

## Licença

Este projeto está licenciado sob a Licença MIT. Consulte o arquivo `LICENSE` para obter detalhes.

