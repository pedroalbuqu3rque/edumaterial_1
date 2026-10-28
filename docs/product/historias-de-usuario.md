# EduMaterial — Histórias de Usuário

**Versão:** 0.3  
**Status:** Em revisão documental  
**Referência:** [`requisitos.md`](./requisitos.md)  
**Escopo:** MVP do EduMaterial

## 1. Objetivo

Este documento descreve as histórias de usuário que representam os principais comportamentos esperados para o MVP do EduMaterial.

As histórias foram organizadas para manter alinhados os requisitos funcionais, a arquitetura da informação, os objetivos de UX e os fluxos de navegação.

O público prioritário considerado é o de professores que procuram materiais didáticos para utilizar em suas aulas.

As histórias representam funcionalidades planejadas. Não indicam que o sistema já tenha sido implementado, testado ou validado com usuários reais.

## 2. US-001 — Visualizar catálogo de materiais

### História de usuário

Como professor que procura materiais didáticos para minhas aulas, quero visualizar um catálogo organizado para conhecer os recursos disponíveis.

### Critérios de aceitação

- O catálogo apresenta os materiais cadastrados e disponíveis.
- Cada material apresenta um título que permita identificá-lo.
- Os itens apresentam as informações resumidas definidas para o catálogo.
- O professor consegue identificar como consultar os detalhes de um material.
- Quando não houver materiais cadastrados, o sistema apresenta uma mensagem informativa de catálogo vazio.
- O catálogo vazio não deve ser confundido com uma pesquisa sem resultados.

**Prioridade:** Essencial para o MVP.

## 3. US-002 — Pesquisar materiais por palavras-chave

### História de usuário

Como professor que procura materiais didáticos para minhas aulas, quero pesquisar por palavras-chave para localizar recursos relacionados ao conteúdo que pretendo trabalhar.

### Critérios de aceitação

- O sistema permite informar uma palavra ou expressão de pesquisa.
- Os resultados correspondem aos termos informados, de acordo com as regras de pesquisa definidas.
- Quando nenhum material corresponder à pesquisa, o sistema apresenta uma mensagem informativa.
- O professor consegue alterar os termos e realizar uma nova pesquisa.
- A ausência de resultados não é apresentada como se o catálogo estivesse vazio.

**Prioridade:** Essencial para o MVP.

**Pendência relacionada:** Definir os campos considerados na pesquisa e as regras de correspondência, incluindo acentuação, letras maiúsculas e minúsculas e correspondências parciais.

## 4. US-003 — Filtrar materiais

### História de usuário

Como professor que procura materiais didáticos para minhas aulas, quero filtrar os materiais por tipo e etapa de ensino para restringir as opções às que parecem mais relevantes para minha necessidade.

### Critérios de aceitação

- O sistema disponibiliza filtros por tipo de material e etapa de ensino.
- A aplicação de um filtro restringe os resultados conforme o critério selecionado.
- A interface permite identificar os filtros ativos.
- O professor consegue remover filtros aplicados.
- Quando não houver materiais correspondentes aos filtros, o sistema apresenta uma mensagem informativa.
- O professor consegue alterar os filtros e consultar os resultados novamente.

**Prioridade:** Incluída no MVP.

**Pendência relacionada:** Definir as opções de cada filtro e como eles funcionarão em conjunto com a pesquisa por palavras-chave.

## 5. US-004 — Consultar detalhes de um material

### História de usuário

Como professor que procura materiais didáticos para minhas aulas, quero consultar os detalhes de um recurso para avaliar inicialmente sua adequação ao conteúdo e aos objetivos da minha aula.

### Critérios de aceitação

- A página de detalhes identifica claramente o material consultado.
- O sistema apresenta os campos descritivos disponíveis e definidos para o produto.
- As informações ajudam a compreender as características e a finalidade do recurso.
- O tipo de material e a etapa de ensino são apresentados quando estiverem disponíveis.
- A autoria, a fonte e as condições de utilização são apresentadas quando essas informações estiverem disponíveis e forem aplicáveis.
- O professor consegue identificar as formas de acesso cadastradas.
- A consulta aos detalhes não depende de uma pré-visualização do conteúdo.

**Prioridade:** Essencial para o MVP.

**Pendência relacionada:** Definir os campos obrigatórios e opcionais da página de detalhes.

## 6. US-005 — Acessar um material

### História de usuário

Como professor que encontrou um material de interesse, quero identificar e utilizar as formas de acesso disponíveis para consultar o recurso.

### Critérios de aceitação

- Quando houver um link externo cadastrado, o sistema apresenta uma ação que permite acessar o endereço correspondente.
- Quando houver um arquivo hospedado na plataforma, o sistema apresenta uma ação para abrir ou baixar o arquivo, conforme os formatos e recursos definidos.
- Quando o material possuir link e arquivo, as duas opções são identificadas separadamente.
- Quando não houver link nem arquivo disponível, o sistema informa que não existe uma forma de acesso cadastrada.
- O sistema não apresenta ações indisponíveis como se fossem funcionais.
- O professor consegue retornar ao catálogo ou selecionar outro material.

**Prioridade:** Essencial para o MVP.

**Pendências relacionadas:** Definir os formatos de arquivo aceitos e o tratamento de links ou arquivos que não possam ser acessados.

## 7. Relação entre histórias e requisitos

| História | Requisitos relacionados |
|---|---|
| US-001 — Catálogo | RF-001 e RF-007 |
| US-002 — Pesquisa | RF-002 e RF-007 |
| US-003 — Filtros | RF-003 e RF-007 |
| US-004 — Detalhes | RF-004 e RF-008 |
| US-005 — Acesso | RF-005, RF-006 e RF-008 |

## 8. Decisões, hipóteses e pendências

### Decisões confirmadas

- O público prioritário são professores.
- O catálogo, a pesquisa, os filtros, os detalhes e o acesso fazem parte do MVP.
- Os filtros previstos são tipo de material e etapa de ensino.
- O acesso poderá ocorrer por link externo, arquivo hospedado na plataforma ou ambas as opções.
- A pré-visualização e a edição de materiais estão fora do escopo inicial.

### Hipóteses

As histórias refletem necessidades e comportamentos esperados para o público prioritário. Essas expectativas ainda não foram validadas por pesquisa com usuários reais.

### Pendências

- Regras de pesquisa;
- Opções e combinação dos filtros;
- Campos obrigatórios e opcionais;
- Formatos de arquivo;
- Tratamento de indisponibilidade de acesso.

## 9. Status da documentação

As histórias descrevem comportamentos previstos, não funcionalidades implementadas ou testadas. Elas deverão permanecer alinhadas aos requisitos e aos documentos de UX/UI.

A atual fase do projeto está restrita à revisão e consolidação documental. Implementação, QA e testes com usuários pertencem a etapas futuras.
