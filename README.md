# Marketing Bancário usando IA Generativa
![ROBO LEGAL](https://dm0fehhuxv6f6.cloudfront.net/wp-content/uploads/2023/02/17090245/imagem_2023-01-18_110006323.webp)
Este projeto tem como objetivo envolver os clientes de maneira mais personalizada, utilizando o poder da Inteligência Artificial Generativa (IA) para criar mensagens de marketing personalizadas que serão entregues a cada cliente. Para alcançar esse objetivo, vamos seguir as seguintes condições do problema:

## Entendimento do Negócio
Foi solicitado que envolvêssemos nossos clientes de maneira mais personalizada, destacando a importância dos investimentos. Para isso, utilizaremos a IA Generativa para criar mensagens de marketing altamente personalizadas.

## Condições do Problema
### 1. Fonte de Dados
Recebemos uma planilha simples em formato CSV chamada 'SDW2023.csv', contendo uma lista de IDs de usuário do banco. Um exemplo da estrutura da planilha:

|UserID|

|1747|

|1748|

|1749|

|...|

### 2. Consumo da API de Dados
Nosso trabalho consiste em consumir o endpoint GET https://sdw-2023-prd.up.railway.app "/users/{id}" da API da Santander Dev Week para obter os dados de cada cliente. Os dados fornecidos pela API incluem informações relevantes sobre cada cliente, como nome, idade, saldo na conta, entre outros.

### 3. Geração de Mensagens Personalizadas
Após obter os dados dos clientes, utilizaremos a API do ChatGPT da OpenAI para gerar mensagens de marketing altamente personalizadas para cada cliente. O foco dessas mensagens será a importância dos investimentos e como eles podem ajudar a alcançar metas financeiras.

### 4. Atualização da Lista de "News"
Uma vez que a mensagem personalizada para cada cliente esteja pronta, enviaremos essas informações de volta para a API, atualizando a lista de "news" de cada usuário. Isso será feito por meio do endpoint PUT https://sdw-2023-prd.up.railway.app "/users/{id}" da API.

## Fluxo de Trabalho
* Ler a planilha CSV 'SDW2023.csv' para obter a lista de IDs de usuário.
### Para cada ID de usuário:
* Fazer uma solicitação GET para a API da Santander Dev Week para obter os dados do cliente.
* Utilizar a API do ChatGPT para gerar uma mensagem de marketing personalizada com base nos dados do cliente.
* Enviar a mensagem de marketing de volta para a API para atualizar a lista de "news" do cliente.
* Repetir o processo para todos os IDs de usuário na lista.
  
O resultado final será uma lista de clientes com mensagens de marketing altamente personalizadas que destacam a importância dos investimentos.

## Requisitos do Projeto

Linguagens de programação: Python
Bibliotecas principais: pandas, requests
Acesso à API da Santander Dev Week e à API do ChatGPT
Acesso à planilha 'SDW2023.csv'
Conexão à internet para fazer solicitações às APIs
