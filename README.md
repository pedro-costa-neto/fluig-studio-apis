## API's que são utilizadas pelo plugin Fluig Studio (Eclipse)
### Dataset
#### Listar todos os datasets
**GET {host}/ecm/api/rest/ecm/dataset/getFullDatasets**

Parâmetros da solicitação

| Nome     | Tipo        | Descrição |
| -------- | ----------- | --------- |
| username | QueryString | Usuário   |
| password | QueryString | Senha     |

------
#### Listar datasets
**GET {host}/ecm/api/rest/ecm/dataset/getDatasets**

Parâmetros da solicitação

| Nome     | Tipo        | Descrição |
| -------- | ----------- | --------- |
| username | QueryString | Usuário   |
| password | QueryString | Senha     |

------
#### Listar registros do dataset
**GET {host}/ecm/api/rest/ecm/dataset/loadDataset**

Parâmetros da solicitação

| Nome      | Tipo        | Descrição         |
| --------- | ----------- | ----------------- |
| username  | QueryString | Usuário           |
| password  | QueryString | Senha             |
| datasetId | QueryString | Código do dataset |

------
#### Criar dataset
**POST {host}/ecm/api/rest/ecm/dataset/createDataset**

Parâmetros da solicitação

| Nome     | Tipo        | Descrição |
| -------- | ----------- | --------- |
| username | QueryString | Usuário   |
| password | QueryString | Senha     |

Corpo da Solicitação

| Tipo de midia | Tipo de dados | Descrição |
| -------- | ----------- | ------------------------------------------------------------ |
| application/json | JSON        | {<br/>	"datasetPK": {<br/>		"companyId": number,<br/>		"datasetId": string<br/>	},<br/>	"datasetDescription": string,<br/>	"datasetImpl": string,<br/>	"datasetBuilder": string,<br/>	"serverOffline": boolean,<br/>	"mobileCache": boolean,<br/>	"lastReset": number,<br/>	"lastRemoteSync": number,<br/>	"type": string,<br/>	"mobileOffline": boolean,<br/>	"updateIntervalTimestamp": number<br/>} |

------
#### Atualizar dataset
**POST {host}/ecm/api/rest/ecm/dataset/editDataset**

Parâmetros da solicitação

| Nome                | Tipo        | Descrição                                                 |
| ------------------- | ----------- | --------------------------------------------------------- |
| username            | QueryString | Usuário                                                   |
| password            | QueryString | Senha                                                     |
| confirmnewstructure | QueryString | Confirmar se é estrutura nova, informar "true" ou "false" |

Corpo da Solicitação

| Tipo de midia | Tipo de dados | Descrição |
| -------- | ----------- | ------------------------------------------------------------ |
| application/json | JSON        | {<br/>	"datasetPK": {<br/>		"companyId": number,<br/>		"datasetId": string<br/>	},<br/>	"datasetDescription": string,<br/>	"datasetImpl": string,<br/>	"datasetBuilder": string,<br/>	"serverOffline": boolean,<br/>	"mobileCache": boolean,<br/>	"lastReset": number,<br/>	"lastRemoteSync": number,<br/>	"type": string,<br/>	"mobileOffline": boolean,<br/>	"updateIntervalTimestamp": number<br/>} |

------
#### Excluir  dataset
**POST {host}/ecm/api/rest/ecm/dataset/deleteDataset**

Parâmetros da solicitação

| Nome      | Tipo        | Descrição         |
| --------- | ----------- | ----------------- |
| username  | QueryString | Usuário           |
| password  | QueryString | Senha             |
| datasetId | QueryString | Código do dataset |

------
### Colleague
#### Consultar colleague
**GET {host}/ecm/api/rest/ecm/zoom/valuesByPlugin/foundation.business.ColleagueBI**

Parâmetros da solicitação

| Nome          | Tipo        | Descrição                                                    |
| ------------- | ----------- | ------------------------------------------------------------ |
| username      | QueryString | Usuário                                                      |
| password      | QueryString | Senha                                                        |
| filterColumns | QueryString |                                                              |
| filter        | QueryString | Informar o nome da coluna e o valor do filtro separado por ponto e virgula, exemplo "filter=active;false" |
| search        | QueryString |                                                              |
| rows          | QueryString | Quantidade de registro                                       |
| page          | QueryString | Pagina                                                       |
| sidx          | QueryString | Informar o campo que deve ser ordenado, exemplo "colleagueName" |
| sord          | QueryString | Informar se a ordenação será crescente (ASC) ou decrescente (DESC) |

------
#### Verificar documentos privados
**GET {host}/ecm/api/rest/ecm/colleague/checkPrivateDocuments**

Parâmetros da solicitação

| Nome     | Tipo        | Descrição |
| -------- | ----------- | --------- |
| username | QueryString | Usuário   |
| password | QueryString | Senha     |
| login    | QueryString | Login     |

------
#### Encontrar usuário por login
**GET {host}/portal/api/rest/wcmservice/rest/user/findUserByLogin**

Parâmetros da solicitação

| Nome     | Tipo        | Descrição |
| -------- | ----------- | --------- |
| username | QueryString | Usuário   |
| password | QueryString | Senha     |
| login    | QueryString | Login     |

------
### Eventos globais
#### Listar eventos
**GET {host}/ecm/api/rest/ecm/globalevent/getEventList**

Parâmetros da solicitação

| Nome          | Tipo        | Descrição |
| ------------- | ----------- | --------- |
| username      | QueryString | Usuário   |
| password      | QueryString | Senha     |

------
#### Listar eventos
**GET {host}/ecm/api/rest/ecm/globalevent/getEventList**

Parâmetros da solicitação

| Nome          | Tipo        | Descrição |
| ------------- | ----------- | --------- |
| username      | QueryString | Usuário   |
| password      | QueryString | Senha     |

------
#### Salvar evento
**POST {host}/ecm/api/rest/ecm/globalevent/saveEventList**

Parâmetros da solicitação

| Nome          | Tipo        | Descrição |
| ------------- | ----------- | --------- |
| username      | QueryString | Usuário   |
| password      | QueryString | Senha     |

Corpo da Solicitação

| Tipo de midia | Tipo de dados | Descrição |
| -------- | ----------- | ------------------------------------------------------------ |
| application/json | JSON    | [<br/>	{<br/>		"globalEventPK": {<br/>			"companyId": number,<br/>			"eventId": string<br/>		},<br/>		"eventDescription": string<br/>	}<br/>] |

------
### Formulário
#### Obter os campos principais
**GET /ecm/api/rest/ecm/cardIndexPublisher/getFormPrincipalFields/{documentId}**

Parâmetros da solicitação

| Nome       | Tipo        | Descrição                   |
| ---------- | ----------- | --------------------------- |
| documentId | Path        | Código do formulário no ECM |
| username   | QueryString | Usuário                     |
| password   | QueryString | Senha                       |

------
### Serviços
#### Listar
**GET /ecm/api/rest/ecm/ecmservices/getServices**

Parâmetros da solicitação

| Nome       | Tipo        | Descrição                   |
| ---------- | ----------- | --------------------------- |
| username   | QueryString | Usuário                     |
| password   | QueryString | Senha                       |

------
### Mecanismo de atribuição
#### Listar mecanismos customizados
**GET /ecm/api/rest/ecm/mechanism/getCustomAttributionMechanismList**

Parâmetros da solicitação

| Nome       | Tipo        | Descrição                   |
| ---------- | ----------- | --------------------------- |
| username   | QueryString | Usuário                     |
| password   | QueryString | Senha                       |

------
### Validar versão
#### Obter a versão do Fluig
**GET /ecm/api/rest/ecm/studioWorkflowRest/version**

Parâmetros da solicitação

| Nome       | Tipo        | Descrição                   |
| ---------- | ----------- | --------------------------- |
| username   | QueryString | Usuário                     |
| password   | QueryString | Senha                       |

------
#### Obter compatibilidade de cliente
**GET /ecm/api/rest/ecm/studioWorkflowRest/getClientCompatibility**

Parâmetros da solicitação

| Nome       | Tipo        | Descrição                   |
| ---------- | ----------- | --------------------------- |
| username   | QueryString | Usuário                     |
| password   | QueryString | Senha                       |
