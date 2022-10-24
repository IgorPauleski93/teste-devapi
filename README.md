# integração-javascript-devapi

## Características
- Integração com Google Sheet
- Integração com Hubspot
- Criar ou atualizar contatos
- ESLint

## Dependências
Para executar este projeto, você precisa instalar localmente em sua máquina conforme as seguintes dependências:
- Node v16.17.0 ou superior;
- NPM v8.15.0 ou superior;

# Credenciais
Em primeiro lugar, precisamos gerar algumas credenciais.<br>
Copie o arquivo .env.example e renomeie para .env, complementamos o ambiente variável.

## Google Sheets
API do Planilhas Google primeiro. Acesse este <a href="https://console.developers.google.com/" target="_blank">website</a> e faça login com sua conta do Google que tenha uma planilha.

Após o login, chore um projeto:

1

Selecione o projeto criado e vamos ativar o Serviço da Folha do Google.

3

são por Folhas do Google e ativo-o.

4

Crie as credenciais.

5

Após a credencial criada, precisamos gerar a chave privada.

7

Gere com a opção JSON.

8

No arquivo gerado, copie "client_email" para **GOOGLE_SHEETS_CLIENT_EMAIL**<br>
e copie todo o conteúdo em "private_key" para **GOOGLE_SHEETS_PRIVATE_KEY** para arquivo .env

Agora, vá para a planilha que você usará e copie o ID da planilha para a variável **GOOGLE_SHEET_ID** em .env

Print

#### !AVISO IMPORTANTE!
Os campos de colunas da planilha precisam ser escritos exatamente assim:

* Nome da empresa
* Nome completo
* Email
* Telefone
* Website

Print

## Hubspot
Vá para <a href="https://br.hubspot.com/" target="_blank">Hubspot</a> e faça o login

Nas configurações, clique em Integrações, aplicativos privados e Criar aplicativo privado

Print

No escopo e CRM permitem escrever e ler crm.objects.contacts e clicar em criar aplicação.

Print

Copie o token gerado para HUBSPOT_TOKEN no arquivo .env.

## Rodando Projeto
- 1. Abra a pasta do projeto e execute 'npm install';
- 2. Agora corra para verificar o código 'npm run eslint';
- 3. Depois de adicionar ou atualizar algum contato na planilha, execute 'npm run integration'.
