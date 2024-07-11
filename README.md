# Dados do Mercado Financeiro (Brasil)

Este documento contém uma coleção de dados e endpoints de diversas fontes de dados relacionados ao mercado financeiro no Brasil. Cada seção inclui o endpoint, uma descrição e o formato dos dados retornados. Estes endpoints são úteis para acessar informações históricas e atuais sobre diversos indicadores econômicos, como taxas de juros, índices de preços, e outros dados relevantes para análises financeiras e econômicas.

#### Disclaimer

Este documento é fornecido apenas para fins informativos e não constitui aconselhamento financeiro ou recomendação de investimento. As informações contidas aqui são obtidas de fontes consideradas confiáveis, mas não garantimos sua precisão, completude ou atualidade. O uso dos endpoints e dos dados fornecidos é de inteira responsabilidade do usuário. Recomendamos que todas as decisões financeiras ou de investimento sejam feitas em consulta com profissionais qualificados.

## Índice

- [Dados Gerais CVM](#dados-gerais-cvm-csv)
- [Dados de Fundos de Investimento Imobiliário (FII)](#dados-de-fundos-de-investimento-imobiliário-fii-csv)
- [Dados de Fundos de Investimentos](#dados-de-fundos-de-investimentos-csv)
- [Abate - aves - peso das carcaças](#abate---aves---peso-das-carcaças)
- [SGS - Sistema Gerenciador de Séries Temporais](#sgs---sistema-gerenciador-de-séries-temporais)
- [IPCA Anualizado [IPEA]](#ipca-anualizado-ipea)
- [Índice de Preços ao Consumidor Ampliado (IPCA) [IPEA]](#índice-de-preços-ao-consumidor-ampliado-ipca-ipea)
- [IPCA [mês] Anualizado [IPEA]](#ipca-mês-anualizado-ipea)
- [Selic Acumulada no Mês [IPEA]](#selic-acumulada-no-mês-ipea)
- [CDI Mês [IPEA]](#cdi-mês-ipea)
- [IGP-M Mês [IPEA]](#igp-m-mês-ipea)
- [Selic Diário [Bacen]](#selic-diário-bacen)
- [IPCA Mês [Bacen]](#ipca-mês-bacen)
- [IMAB Diário [Bacen]](#imab-diário-bacen)
- [IMAB5 Diário [Bacen]](#imab5-diário-bacen)
- [IMAB5+ Diário [Bacen]](#imab5-diário-bacen)
- [CDI Diário [Bacen]](#cdi-diário-bacen)
- [CDI Mês [Bacen]](#cdi-mês-bacen)
- [Selic Mês [Bacen]](#selic-mês-bacen)
- [IGP-M Mês [Bacen]](#igp-m-mês-bacen)
- [TR Mês [Bacen]](#tr-mês-bacen)

---

## Dados Gerais CVM (CSV)

### URL

`https://dados.cvm.gov.br/dados/`

### Descrição

Este conjunto de diretórios contém diversos tipos de documentos financeiros e informações relacionadas a diferentes entidades e operações no mercado financeiro, incluindo administradores de carteira, fundos de investimento imobiliário, agentes autônomos, agentes fiduciários, auditores, companhias abertas, companhias estrangeiras, companhias incentivadas, consultores de valores mobiliários, crowdfunding, emissores de CEPAC, fundos de investimento, fundos de investimento em direitos creditórios, fundos de investimento em empresas emergentes, fundos de investimento imobiliário, fundos de investimento em participações, intermediários, investidores não residentes, ofertas públicas e securitizadoras.

### Estrutura

```
ADM_CART/
ADM_FII/
AGENTE_AUTON/
AGENTE_FIDUC/
AUDITOR/
CIA_ABERTA/
CIA_ESTRANG/
CIA_INCENT/
CONSULTOR_VLMOB/
CROWDFUNDING/
EMISSOR_CEPAC/
FI/
FIDC/
FIE/
FII/
FIP/
INTERMED/
INVNR/
OFERTA/
SECURIT/
```

---

## Dados de Companhias Abertas (CSV)

### URL

`https://dados.cvm.gov.br/dados/CIA_ABERTA/DOC/`

### Descrição

Este conjunto de diretórios contém diversos tipos de documentos financeiros relacionados a companhias abertas, incluindo governança corporativa, demonstrações financeiras padronizadas, fichas cadastrais, formulários de referência, informações periódicas, informes trimestrais e valores mobiliários.

### Estrutura

```
CGVN/
DFP/
FCA/
FRE/
IPE/
ITR/
VLMO/
```

---

## Dados de Fundos de Investimento Imobiliário (FII) (CSV)

### URL

`https://dados.cvm.gov.br/dados/FII/DOC/`

### Descrição

Este conjunto de diretórios contém diversos tipos de documentos financeiros relacionados a fundos de investimento imobiliário, incluindo informações anuais, mensais e trimestrais.

### Estrutura

```
INF_ANUAL/
INF_MENSAL/
INF_TRIMESTRAL/
```

---

## Dados de Fundos de Investimentos (FI) (CSV)

### URL

`https://dados.cvm.gov.br/dados/FI/DOC/`

### Descrição

Este conjunto de diretórios contém diversos tipos de documentos financeiros relacionados a fundos de investimento, incluindo resumos contábeis, carteiras diárias de ativos, informações complementares, registros de eventos não recorrentes, resumos periódicos de movimentações, informações diárias, documentos de desempenho e perfis mensais detalhados.

### Estrutura

```
BALANCETE/
CDA/
COMPL/
EVENTUAL/
EXTRATO/
INF_DIARIO/
LAMINA/
PERFIL_MENSAL/
```

---

## Abate - aves - peso das carcaças

### Endpoint

`http://www.ipeadata.gov.br/api/odata4/Metadados`

### Descrição

O abate de aves é mensurado pelo peso total das carcaças, incluindo estabelecimentos sob inspeção federal, estadual ou municipal. Não inclui abate clandestino. As carcaças podem ou não incluir pescoços, rins, pés e cabeças. Dados disponíveis a partir de 1958, com atualização anual.

### Tipo

```typescript
{
  SERCODIGO: string;
  SERNOME: string;
  SERCOMENTARIO: string;
  SERATUALIZACAO: string;
  BASNOME: string;
  FNTSIGLA: string;
  FNTNOME: string;
  FNTURL: string;
  PERNOME: string;
  UNINOME: string;
  MULNOME: string;
  SERSTATUS: string;
  TEMCODIGO: number;
  PAICODIGO: string;
  SERNUMERICA: boolean;
}
```

---

## SGS - Sistema Gerenciador de Séries Temporais

### Endpoint

`https://api.bcb.gov.br/dados/serie/bcdata.sgs.25436/dados?formato=json`

### Descrição

Interface JSON do serviço BCData/SGS - Sistema Gerenciador de Séries Temporais. Este serviço permite o acesso a dados temporais através do fornecimento de parâmetros específicos na URL.

### Tipo

```typescript
{
  data: string;
  valor: number;
}
```

---

## IPCA Anualizado [IPEA]

### Endpoint

`http://ipeadata.gov.br/api/odata4/ValoresSerie(SERCODIGO='PAN12_IPCAG12')`

### Descrição

A série histórica do IPCA Anualizado fornecida pelo IPEA. Este endpoint retorna os valores do Índice de Preços ao Consumidor Amplo (IPCA) anualizado, uma medida de inflação no Brasil, com dados disponíveis em formato JSON.

### Tipo

```typescript
{
  SERCODIGO: string;
  VALDATA: string;
  VALVALOR: number;
  NIVNOME: string;
  TERCODIGO: string;
}
```

---

## Índice de Preços ao Consumidor Ampliado (IPCA) [IPEA]

### Endpoint

`http://www.ipeadata.gov.br/ExibeSerie.aspx?serid=38391`

### Descrição

A série histórica do Índice de Preços ao Consumidor Amplo (IPCA), fornecida pelo IPEA e produzida pelo Instituto Brasileiro de Geografia e Estatística (IBGE) através do Sistema Nacional de Índices de Preços ao Consumidor (SNIPC). Este índice mede a inflação no Brasil com dados disponíveis mensalmente de janeiro de 1980 até junho de 2024. A taxa de inflação é anualizada e os dados estão atualizados em tempo real.

### Tipo

```typescript
{
  Data: string;
  IPCA: number;
}
```

---

## IPCA [mês] Anualizado [IPEA]

### Endpoint

`http://ipeadata.gov.br/api/odata4/ValoresSerie(SERCODIGO='PAN12_IPCAG12')`

### Descrição

A série histórica do IPCA Anualizado fornecida pelo IPEA. Este endpoint retorna os valores do Índice de Preços ao Consumidor Amplo (IPCA) anualizado, uma medida de inflação no Brasil, com dados disponíveis em formato JSON.

### Tipo

```typescript
{
  SERCODIGO: string;
  VALDATA: string;
  VALVALOR: number;
  NIVNOME: string;
  TERCODIGO: string;
}
```

---

## IPCA Anualizado [IPEA]

### Endpoint

`http://ipeadata.gov.br/api/odata4/ValoresSerie(SERCODIGO='PAN12_IPCAG12')`

### Descrição

A série histórica do IPCA Anualizado fornecida pelo IPEA. Este endpoint retorna os valores do Índice de Preços ao Consumidor Amplo (IPCA) anualizado, uma medida de inflação no Brasil, com dados disponíveis em formato JSON.

### Tipo

```typescript
{
  SERCODIGO: string;
  VALDATA: string;
  VALVALOR: number;
  NIVNOME: string;
  TERCODIGO: string;
}
```

---

## Selic Acumulada no Mês [IPEA]

### Endpoint

`http://ipeadata.gov.br/api/odata4/ValoresSerie(SERCODIGO='BM12_TJOVER12')`

### Descrição

A série histórica da Selic acumulada no mês fornecida pelo IPEA. Este endpoint retorna os valores mensais acumulados da taxa Selic, uma taxa de juros essencial no Brasil, com dados disponíveis em formato JSON.

### Tipo

```typescript
{
  SERCODIGO: string;
  VALDATA: string;
  VALVALOR: number;
  NIVNOME: string;
  TERCODIGO: string;
}
```

---

## CDI Mês [IPEA]

### Endpoint

`http://ipeadata.gov.br/api/odata4/ValoresSerie(SERCODIGO='BM12_TJCDI12')`

### Descrição

A série histórica do CDI mensal fornecida pelo IPEA. Este endpoint retorna os valores mensais da taxa do Certificado de Depósito Interbancário (CDI), uma taxa de referência importante para o mercado financeiro brasileiro, com dados disponíveis em formato JSON.

### Tipo

```typescript
{
  SERCODIGO: string;
  VALDATA: string;
  VALVALOR: number;
  NIVNOME: string;
  TERCODIGO: string;
}
```

---

## IGP-M Mês [IPEA]

### Endpoint

`http://ipeadata.gov.br/api/odata4/ValoresSerie(SERCODIGO='IGP12_IGPMG12')`

### Descrição

A série histórica do IGP-M mensal fornecida pelo IPEA. Este endpoint retorna os valores mensais do Índice Geral de Preços - Mercado (IGP-M), um indicador amplamente utilizado para reajustes de contratos, tarifas públicas e aluguéis no Brasil, com dados disponíveis em formato JSON.

### Tipo

```typescript
{
  SERCODIGO: string;
  VALDATA: string;
  VALVALOR: number;
  NIVNOME: string;
  TERCODIGO: string;
}
```

---

## Selic Diário [Bacen]

### Endpoint

`https://api.bcb.gov.br/dados/serie/bcdata.sgs.11/dados?formato=json&dataInicial=01/01/2020&dataFinal=31/12/2020`

### Descrição

A série histórica da taxa Selic diária fornecida pelo Banco Central do Brasil (Bacen). Este endpoint retorna os valores diários da taxa Selic, a taxa básica de juros da economia brasileira, com dados disponíveis em formato JSON para o período de 01/01/2020 a 31/12/2020.

### Tipo

```typescript
{
  data: string;
  valor: number;
}
```

---

## IPCA Mês [Bacen]

### Endpoint

`http://api.bcb.gov.br/dados/serie/bcdata.sgs.433/dados?formato=json`

### Descrição

A série histórica do IPCA mensal fornecida pelo Banco Central do Brasil (Bacen). Este endpoint retorna os valores mensais do Índice de Preços ao Consumidor Amplo (IPCA), um dos principais indicadores de inflação no Brasil, com dados disponíveis em formato JSON.

### Tipo

```typescript
{
  data: string;
  valor: number;
}
```

---

## IMAB Diário [Bacen]

### Endpoint

`https://api.bcb.gov.br/dados/serie/bcdata.sgs.12466/dados?formato=json`

### Descrição

A série histórica do IMAB diário fornecida pelo Banco Central do Brasil (Bacen). Este endpoint retorna os valores diários do Índice de Mercado Anbima - Brasil (IMAB), que reflete a evolução dos preços dos títulos públicos brasileiros, com dados disponíveis em formato JSON.

### Tipo

```typescript
{
  data: string;
  valor: number;
}
```

---

## IMAB5 Diário [Bacen]

### Endpoint

`https://api.bcb.gov.br/dados/serie/bcdata.sgs.12467/dados?formato=json`

### Descrição

A série histórica do IMAB5 diário fornecida pelo Banco Central do Brasil (Bacen). Este endpoint retorna os valores diários do Índice de Mercado Anbima - Brasil 5 anos (IMAB5), que reflete a evolução dos preços dos títulos públicos brasileiros com prazo de até 5 anos, com dados disponíveis em formato JSON.

### Tipo

```typescript
{
  data: string;
  valor: number;
}
```

---

## IMAB5+ Diário [Bacen]

### Endpoint

`https://api.bcb.gov.br/dados/serie/bcdata.sgs.12468/dados?formato=json`

### Descrição

A série histórica do IMAB5+ diário fornecida pelo Banco Central do Brasil (Bacen). Este endpoint retorna os valores diários do Índice de Mercado Anbima - Brasil 5 anos ou mais (IMAB5+), que reflete a evolução dos preços dos títulos públicos brasileiros com prazo igual ou superior a 5 anos, com dados disponíveis em formato JSON.

### Tipo

```typescript
{
  data: string;
  valor: number;
}
```

---

## CDI Diário [Bacen]

### Endpoint

`https://api.bcb.gov.br/dados/serie/bcdata.sgs.12/dados?formato=json`

### Descrição

A série histórica do CDI diário fornecida pelo Banco Central do Brasil (Bacen). Este endpoint retorna os valores diários da taxa do Certificado de Depósito Interbancário (CDI), uma taxa de referência crucial para o mercado financeiro brasileiro, com dados disponíveis em formato JSON.

### Tipo

```typescript
{
  data: string;
  valor: number;
}
```

---

## CDI Mês [Bacen]

### Endpoint

`https://api.bcb.gov.br/dados/serie/bcdata.sgs.4391/dados?formato=json`

### Descrição

A série histórica do CDI mensal fornecida pelo Banco Central do Brasil (Bacen). Este endpoint retorna os valores mensais da taxa do Certificado de Depósito Interbancário (CDI), uma taxa de referência importante para o mercado financeiro brasileiro, com dados disponíveis em formato JSON.

### Tipo

```typescript
{
  data: string;
  valor: number;
}
```

---

## Selic Diário [Bacen]

### Endpoint

`https://api.bcb.gov.br/dados/serie/bcdata.sgs.11/dados?formato=json`

### Descrição

A série histórica da taxa Selic diária fornecida pelo Banco Central do Brasil (Bacen). Este endpoint retorna os valores diários da taxa Selic, a taxa básica de juros da economia brasileira, com dados disponíveis em formato JSON.

### Tipo

```typescript
{
  data: string;
  valor: number;
}
```

---

## Selic Mês [Bacen]

### Endpoint

`https://api.bcb.gov.br/dados/serie/bcdata.sgs.4390/dados?formato=json`

### Descrição

A série histórica da taxa Selic mensal fornecida pelo Banco Central do Brasil (Bacen). Este endpoint retorna os valores mensais da taxa Selic, a taxa básica de juros da economia brasileira, com dados disponíveis em formato JSON.

### Tipo

```typescript
{
  data: string;
  valor: number;
}
```

---

## IGP-M Mês [Bacen]

### Endpoint

`https://api.bcb.gov.br/dados/serie/bcdata.sgs.189/dados?formato=json`

### Descrição

A série histórica do IGP-M mensal fornecida pelo Banco Central do Brasil (Bacen). Este endpoint retorna os valores mensais do Índice Geral de Preços - Mercado (IGP-M), um indicador amplamente utilizado para reajustes de contratos, tarifas públicas e aluguéis no Brasil, com dados disponíveis em formato JSON.

### Tipo

```typescript
{
  data: string;
  valor: number;
}
```

---

## TR Mês [Bacen]

### Endpoint

`https://api.bcb.gov.br/dados/serie/bcdata.sgs.226/dados?formato=json`

### Descrição

A série histórica da Taxa Referencial (TR) mensal fornecida pelo Banco Central do Brasil (Bacen). Este endpoint retorna os valores mensais da TR, uma taxa de referência utilizada no Brasil, com dados disponíveis em formato JSON.

### Tipo

```typescript
{
  data: string;
  dataFim: string;
  valor: number;
}
```
