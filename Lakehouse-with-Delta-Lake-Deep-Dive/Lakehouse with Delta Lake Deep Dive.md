# Lakehouse with Delta Lake Deep Dive

## [Prática com Delta Lake](https://github.com/vvalcristina/data-engineer-databricks/tree/main/Lakehouse-with-Delta-Lake-Deep-Dive/)

### Estudo de caso

* Neste estudo de caso, você é um engenheiro de dados de uma empresa fictícia de rastreadores de saúde chamada Moovio. 
* Atualmente, a Moovio possui dois rastreadores de fitness no mercado - Moovio Classic e Moovio +. O modelo clássico é o modelo básico do Moovio. Ele coleta dados do cliente sobre as etapas executadas. Moovio + é o modelo mais recente da Moovio, que coleta dados de frequência cardíaca continuamente. 

### Dados

* Você estará fazendo a ingestão de dados do sensor IoT que contêm informações sobre a freqüência cardíaca do usuário durante um período de um mês. Os arquivos são arquivos JSON de várias linhas e se assemelham a strings passadas por Kafka. Você analisará as strings para criar um DataFrame e, em seguida, escreverá esses dados em uma tabela. Começaremos com um esquema semelhante a este: 

```
    name: string
    heartrate: double
    device_id: long
    time: float
```

### Objetivo

Moovio precisa de grandes melhorias em seu pipeline de dados atual. Neste laboratório, você irá: 
  * Criar um pipeline de dados OLAP de ponta a ponta
  * Use os padrões de design recomendados do Delta Lake para disponibilizar os dados às partes interessadas a jusante.
  * Documentar os dados no nível da tabela para promover a descoberta de dados e a comunicação entre equipes

### Estrutura de Diretórios

#### [Ingest and Transform](https://github.com/vvalcristina/data-engineer-databricks/tree/main/Lakehouse-with-Delta-Lake-Deep-Dive/01_Ingest_and_Transform)

* [Ingestão de dados](https://github.com/vvalcristina/data-engineer-databricks/blob/main/Lakehouse-with-Delta-Lake-Deep-Dive/01_Ingest_and_Transform/00_ingest_raw.ipynb): Ingestão dos dados.
* [Review](https://github.com/vvalcristina/data-engineer-databricks/blob/main/Lakehouse-with-Delta-Lake-Deep-Dive/01_Ingest_and_Transform/01_review_and_visualize.ipynb):  As transações com as quais estamos trabalhando mostram dados de eventos dos usuários. 
* [Criando uma tabela parquet](02_Delta%20Tables/03_creating_the_delta_table.ipynb)):Criamos uma tabela parquet para praticar.

#### [Delta Tables](https://github.com/vvalcristina/data-engineer-databricks/tree/main/Lakehouse-with-Delta-Lake-Deep-Dive/02_Delta_Tables)

* [Criando uma tabela Delta](https://github.com/vvalcristina/data-engineer-databricks/blob/main/Lakehouse-with-Delta-Lake-Deep-Dive/02_Delta_Tables/03_creating_the_delta_table.ipynb): Criando uma tabela Delta.
* [Gravação em batch para tabelas Delta]:  Lembre-se de que, como Moovio, estamos usando Kafka para transmitir dados. Agora, praticaremos anexar um lote de dados às tabelas com as quais estamos trabalhando. 
* 
