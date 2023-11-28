# Projeto Spring de Serviço de Email

Este projeto é um exemplo de como enviar emails utilizando o AWS SES (Simple Email Service) em uma aplicação Spring.

## Requisitos

- JDK (Java Development Kit) 8 ou superior
- Maven
- Conta na AWS com acesso ao serviço SES

## Configuração

1. Clone este repositório.
2. Abra o arquivo `application.properties` localizado no diretório `src/main/resources`.
3. Configure as seguintes propriedades:

   ```properties
    aws:
    accessKeyId: ${AWS_ACCESS_KEY_ID}
    secretAccessKey: ${AWS_SECRET_ACCESS_KEY}
    region: ${AWS_REGION}
   
    springdoc.swagger-ui.path=/doc.html

4. Execute o método main da classe EmailServiceApplication

## Uso

Após iniciar o aplicativo, você pode enviar emails chamando a API fornecida. Por exemplo, você pode usar uma ferramenta como o Insomnia para enviar uma solicitação POST para o endpoint `/api/email com o seguinte corpo:

```json
  {
    "to": "destinatario@example.com",
    "subject": "Assunto do Email",
    "body": "Conteúdo do Email"
  }
```

Certifique-se de substituir os valores de "to", "subject" e "body" pelos valores desejados.

Também é possível enviar requisições acessando a página `localhost:8080/doc.html`, gerada pelo SpringDocs.

## Atenção

Lembre-se de colocar sua accessKeyId, secretAccessKey e região(citadas no application.properties) nas suas variáveis de ambiente(environment variables)!