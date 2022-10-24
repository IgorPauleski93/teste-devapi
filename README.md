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

1- Após o login, crie um projeto:
    -CRIAR PROJETO

2- Selecione o projeto criado e vamos ativar o Google Sheet Service.
    -SELECIONE O PROJOETO CRIADO
    -SELECIONE "ATIVAR APIS E SERVIÇOS"

3- Pesquise o Planilhas Google e ative-o.
    -NORMALMENTE ESTÁ "GOOGLE SHEETS API"

4- Crie as credenciais.
    -SELECIONE "CREDENCIAIS"
    -SLECIONE "CREATE CREDENTIALS"
    -E SELECIONE A SEGUNDA OPÇÃO "CONTA DE SERVIÇO"

5- Após a credencial criada, precisamos gerar a chave privada.
    -PROCURE O CAMPO "CONTAS DE SERVIÇO"
    -VOCÊ VAI VER QUE VAI EXISTIR UMA CONTA CRIADA, NA MESMA LINHA VOCÊ VAI ENCONTRAR UM LOCAL CHAMADO "AÇÕES" E SELECIONE EDITAR

6- Gere com a opção JSON.
    -SELECINE A ABA "CHAVES""
    -EM SEGUIDA "ADICIONAR CHAVE"
    -SELECIONE "CRIAR NOVA CHAVE"

No arquivo gerado, copie "client_email" para **GOOGLE_SHEETS_CLIENT_EMAIL**<br>
e copie todo o conteúdo em "private_key" para **GOOGLE_SHEETS_PRIVATE_KEY** para arquivo .env

Agora, vá para a planilha que você usará e copie o ID da planilha para a variável **GOOGLE_SHEET_ID** em .env

![Captura de Tela - URL](https://user-images.githubusercontent.com/61367245/197607251-3b3d5ac4-d6d4-4896-b498-b281b405baa1.png)

#### !AVISO IMPORTANTE!
Os campos de colunas da planilha precisam ser escritos exatamente assim:

* Nome da empresa
* Nome completo
* Email
* Telefone
* Website

![Captura de Tela - Planilha Google](https://user-images.githubusercontent.com/61367245/197607412-4422e164-e625-4d85-a7d7-ff6ccfc16b88.png)
## Hubspot
Vá para <a href="https://br.hubspot.com/" target="_blank">Hubspot</a> e faça o login

Selecione configurações (Uma engrenagem que fica no canto superior direito), clique em "INTEGRAÇÕES", "APLICATIVOS PRIVADOS" e "CRIAR UM APLICATIVO PRIVADO"

Na nova tela selecione "ESCOPO" e "CRM", em seguida selecione permitem "ESCREVER" e "LER" 'crm.objects.contacts' e SELECIONE em "CRIAR APLICATIVO".

Copie o token gerado e coloque o mesmo em HUBSPOT_TOKEN no arquivo .env.

## Rodando Projeto
- Abra a pasta do projeto e execute 'npm install';
- Agora corra para verificar o código 'npm run eslint';
- Depois de adicionar ou atualizar algum contato na planilha, execute 'npm run integrate'.
