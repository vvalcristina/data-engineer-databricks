# Lakehouse with Delta Lake Deep Dive

## Prática com Delta Lake - Ingestão e Transformação

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