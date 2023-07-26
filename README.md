# AWS Lambda

Função lambda para calcular o dobro de um número criada a partir de um código de exemplo gerado automaticamente na criação de um novo projeto no Intellij, utilizando o plugin AWS Toolkit.

Comandos utilizados no terminal do Intellij para criar função lambda:

mvn clean package

aws lambda create-function \ \
  --function-name **<nome_da_função>** \ \
  --runtime java11 \ \
  --handler **<localização_da_classe>**::handleRequest \ \
  --role **<IAM_ROLE_ARN>** \ \
  --zip-file fileb://target/**<arquivo_.jar_criado_no_passo_anterior>**

  Após esses dois passos, a função foi testada com sucesso no console da AWS Lambda, com o seguinte JSON do evento:

{ \
  "httpMethod": "GET", \
  "queryStringParameters": { \
    "numero": "10" \
  } \
}

Então, ainda no console, foi criado um trigger API Gateway.

Os prints dos resultados exibidos no console estão salvos na pasta **Printscreens**.
