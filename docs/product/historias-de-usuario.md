# EduMaterial — Histórias de Usuário

**Versão:** 0.2  
**Status:** Proposta documental revisada  
**Referência:** [`requisitos.md`](./requisitos.md)  
**Escopo:** MVP do EduMaterial

## 1. Objetivo

Este documento descreve as histórias de usuário que representam os principais comportamentos esperados para o MVP do EduMaterial.

As histórias foram elaboradas a partir do escopo definido para o produto e servem como referência para manter alinhados os requisitos funcionais, a arquitetura da informação e os fluxos de uso.

O público prioritário considerado é o de professores que procuram materiais didáticos para utilizar em suas aulas.

As histórias representam funcionalidades planejadas. Elas não indicam que o sistema já foi implementado, testado ou validado com usuários reais.

## 2. US-001 — Visualizar catálogo de materiais

### História de usuário

Como professor que procura materiais didáticos para minhas aulas, quero visualizar um catálogo de recursos educacionais para conhecer as opções disponíveis.

### Critérios de aceitação

- O catálogo apresenta os materiais disponíveis no sistema.
- Cada material apresenta, no mínimo, um título que permita identificá-lo.
- Os itens do catálogo apresentam as informações resumidas definidas para sua identificação.
- O professor consegue identificar como consultar os detalhes de um material.
- Quando não houver materiais disponíveis, o sistema apresenta uma mensagem informativa sobre o catálogo vazio.

### Prioridade

Essencial para o MVP.

## 3. US-002 — Pesquisar materiais por palavras-chave

### História de usuário

Como professor que procura materiais didáticos para minhas aulas, quero pesquisar por palavras-chave para localizar recursos relacionados ao conteúdo que pretendo trabalhar.

### Critérios de aceitação

- O sistema permite informar uma palavra ou expressão de pesquisa.
- A pesquisa retorna os materiais que correspondem aos termos informados, conforme as regras de busca definidas para o produto.
- Os resultados apresentados correspondem à pesquisa realizada.
- Quando nenhum material corresponder à pesquisa, o sistema apresenta uma mensagem informativa.
- Após consultar os resultados, o professor consegue realizar uma nova pesquisa.
- A ausência de resultados para uma pesquisa não deve ser confundida com a ausência de materiais cadastrados no catálogo.

### Prioridade

Essencial para o MVP.

### Pendência relacionada

Definir quais campos dos materiais serão considerados na pesquisa e como serão tratados aspectos como acentuação, diferenças entre letras maiúsculas e minúsculas e correspondências parciais.

## 4. US-003 — Consultar detalhes de um material

### História de usuário

Como professor que procura materiais didáticos para minhas aulas, quero consultar os detalhes de um recurso para avaliar sua adequação ao conteúdo e aos objetivos da minha aula.

### Critérios de aceitação

- A página de detalhes identifica claramente o material consultado.
- O sistema apresenta as informações disponíveis e previstas para a descrição do recurso.
- As informações permitem compreender a finalidade e as características do material, conforme os campos definidos para o catálogo.
- Quando houver informações sobre o tipo de material e a etapa de ensino indicada, elas serão apresentadas ao professor.
- O professor consegue identificar se há uma forma de acessar o recurso.
- A consulta aos detalhes não depende da existência de uma visualização prévia do conteúdo.

### Prioridade

Essencial para o MVP.

### Observação de escopo

A visualização prévia do material dentro da plataforma não faz parte do MVP. Nesta versão, a avaliação inicial do recurso será baseada nas informações descritivas disponibilizadas.

## 5. US-004 — Filtrar materiais do catálogo

### História de usuário

Como professor que procura materiais didáticos para minhas aulas, quero filtrar os materiais por características relevantes para localizar recursos mais adequados às minhas necessidades.

### Critérios de aceitação

- O catálogo disponibiliza filtros por tipo de material e etapa de ensino.
- O professor consegue selecionar um ou mais filtros disponíveis.
- Os resultados são atualizados de acordo com os filtros selecionados.
- O professor consegue remover os filtros aplicados.
- Quando os filtros selecionados não produzirem resultados, o sistema apresenta uma mensagem informativa.
- A interface permite identificar quais filtros estão ativos.

### Prioridade

Incluída no MVP.

### Pendência relacionada

Definir os valores disponíveis em cada filtro e estabelecer como a filtragem será combinada com a pesquisa por palavras-chave.

## 6. US-005 — Acessar um material didático

### História de usuário

Como professor que encontrou um material de interesse, quero acessar o recurso por meio de um link externo ou de um arquivo disponibilizado na plataforma para utilizá-lo no planejamento das minhas aulas.

### Critérios de aceitação

- A página de detalhes informa a forma de acesso disponível para o material.
- Quando houver um link externo, o sistema disponibiliza uma ação identificável para acessar o endereço correspondente.
- Quando houver um arquivo hospedado diretamente na plataforma, o sistema disponibiliza uma ação para acessar ou baixar o arquivo, conforme o comportamento definido para esse tipo de recurso.
- O sistema não apresenta uma ação de acesso quando não houver um link ou arquivo disponível.
- Quando não houver uma forma de acesso disponível, o sistema informa essa condição ao professor.
- A forma de acesso apresentada corresponde ao recurso cadastrado.
- A interface distingue o acesso ao material da consulta às informações descritivas do catálogo.

### Prioridade

Essencial para o MVP.

### Pendências relacionadas

- Definir os formatos de arquivo aceitos pela plataforma.
- Estabelecer os limites de tamanho dos arquivos, caso aplicáveis.
- Definir as regras de armazenamento e disponibilização dos arquivos.
- Determinar como serão identificados links inválidos ou arquivos indisponíveis.
- Definir quais informações sobre autoria, licença e condições de uso deverão acompanhar cada material.

## 7. Observações sobre as histórias

As histórias descritas neste documento representam os comportamentos esperados para o MVP, e não uma descrição de funcionalidades já disponíveis.

Os critérios de aceitação estabelecem as condições que deverão ser consideradas quando as funcionalidades forem especificadas em maior detalhe. Eles não constituem evidência de implementação, testes ou validação com usuários.

As prioridades indicadas representam a importância das funcionalidades dentro do escopo documental atual. Não foram derivadas de resultados de uma pesquisa empírica com professores.

## 8. Observação metodológica

O EduMaterial é tratado, nesta etapa, como um estudo de caso de planejamento de produto digital.

A coleta de respostas por meio do Google Forms foi abandonada. Portanto, não existem resultados desse questionário que possam ser apresentados como evidência de necessidades, preferências ou comportamentos de professores.

As hipóteses de produto, os cenários ilustrativos e os eventuais dados simulados devem ser identificados como tais. Eles não devem ser apresentados como respostas de participantes reais nem utilizados para afirmar que as funcionalidades foram validadas empiricamente.

As histórias de usuário foram formuladas com base no escopo definido e poderão ser revisadas caso surjam novas informações ou decisões documentadas.

A implementação e as atividades de Quality Assurance (QA) pertencem a etapas posteriores e não fazem parte do trabalho documental atual.
