# EduMaterial — Histórias de Usuário

**Versão:** 0.3  
**Status:** Em revisão documental  
**Referência:** `requisitos.md`

## 1. Objetivo

Este documento descreve as histórias de usuário do EduMaterial e seus respectivos critérios de aceitação.

As histórias representam os comportamentos esperados do Produto Mínimo Viável (MVP), considerando professores que procuram materiais educacionais para utilizar em suas aulas.

Os critérios de aceitação devem orientar a futura implementação e verificação das funcionalidades. Eles não representam evidências de que as funcionalidades já foram implementadas ou validadas com usuários reais.

## 2. Histórias de usuário

### US-001 — Visualizar catálogo de materiais

**História**

Como professor que procura materiais educacionais, quero visualizar o catálogo de materiais disponíveis para conhecer minhas opções de recursos para as aulas.

**Critérios de aceitação**

- [ ] O sistema apresenta os materiais cadastrados e disponíveis para consulta.
- [ ] Cada item do catálogo apresenta um título que permita identificar o material.
- [ ] Os itens apresentam as informações resumidas disponíveis para orientar a escolha do usuário.
- [ ] O usuário consegue selecionar um material para consultar seus detalhes.
- [ ] Quando não houver materiais cadastrados, o sistema apresenta uma mensagem informativa sobre o catálogo vazio.
- [ ] O catálogo vazio não é confundido com uma pesquisa que não encontrou correspondências.

**Requisito relacionado:** RF-001.

### US-002 — Pesquisar materiais por palavras-chave

**História**

Como professor que procura materiais educacionais, quero pesquisar por palavras-chave para encontrar recursos relacionados ao assunto que pretendo trabalhar em aula.

**Critérios de aceitação**

- [ ] O sistema permite informar uma palavra ou expressão para pesquisar materiais.
- [ ] A busca consulta os campos título, tipo de material, resumo e descrição.
- [ ] A busca não diferencia letras maiúsculas de minúsculas.
- [ ] A busca ignora diferenças de acentuação.
- [ ] A busca permite correspondências parciais. Por exemplo, pesquisar `geog` deve permitir encontrar materiais que contenham `geografia` em um dos campos pesquisáveis.
- [ ] Os resultados são apresentados em ordem de relevância.
- [ ] A prioridade dos campos para relevância segue esta ordem: título, tipo de material, resumo e descrição.
- [ ] Quando a pesquisa não encontra correspondências, o sistema apresenta uma mensagem informativa.
- [ ] Após visualizar os resultados, o usuário consegue modificar a consulta e realizar uma nova pesquisa.

**Requisitos relacionados:** RF-002, RF-003 e RF-005.

**Pendências de especificação**

A fórmula detalhada de relevância, os critérios de desempate, a prioridade entre correspondências exatas e parciais e o tratamento de expressões com várias palavras ainda precisam ser definidos antes da implementação.

### US-003 — Filtrar materiais

**História**

Como professor que procura materiais educacionais, quero filtrar os materiais por características relevantes para localizar recursos mais adequados à minha necessidade.

**Critérios de aceitação**

- [ ] O sistema disponibiliza filtros por tipo de material e etapa de ensino.
- [ ] A aplicação de um filtro atualiza os materiais apresentados de acordo com o critério selecionado.
- [ ] O usuário consegue identificar quais filtros estão aplicados.
- [ ] O usuário consegue remover os filtros aplicados.
- [ ] Quando a combinação de filtros não encontra materiais, o sistema apresenta uma mensagem informativa.
- [ ] A ausência de resultados não é apresentada como se o catálogo estivesse vazio.

**Requisito relacionado:** RF-004.

**Pendências de especificação**

Ainda precisam ser definidos os valores disponíveis em cada filtro, a possibilidade de seleção múltipla, a combinação entre filtros e o comportamento conjunto entre filtros e pesquisa por palavras-chave.

### US-004 — Consultar detalhes de um material

**História**

Como professor que encontrou um material de interesse, quero consultar seus detalhes para avaliar se o recurso é adequado ao conteúdo e à etapa de ensino que pretendo trabalhar.

**Critérios de aceitação**

- [ ] O sistema apresenta o título do material consultado.
- [ ] O sistema apresenta as informações disponíveis e pertinentes ao material.
- [ ] Quando disponíveis, os detalhes incluem tipo de material, etapa de ensino, resumo e descrição.
- [ ] As informações de autoria, fonte e condições de uso são apresentadas quando estiverem disponíveis no cadastro.
- [ ] O usuário consegue identificar claramente qual material está consultando.
- [ ] A ausência de um campo opcional não é apresentada como se o material não existisse.
- [ ] As opções de acesso são apresentadas de acordo com os recursos efetivamente cadastrados.

**Requisito relacionado:** RF-006.

**Pendência de especificação**

Os campos obrigatórios e opcionais de cada material ainda precisam ser definidos.

### US-005 — Acessar um material por link externo

**História**

Como professor que encontrou um material disponibilizado em uma fonte externa, quero acessar o link correspondente para consultar ou utilizar o recurso na sua origem.

**Critérios de aceitação**

- [ ] Quando houver um link externo cadastrado, o sistema apresenta uma opção clara para acessá-lo.
- [ ] A opção direciona ao endereço associado ao material.
- [ ] O acesso externo é distinguido da consulta aos detalhes do material na plataforma.
- [ ] Quando não houver link externo, o sistema não apresenta um controle de acesso a um endereço inexistente.
- [ ] Quando uma falha de acesso puder ser identificada, o sistema apresenta o tratamento previsto para essa situação.

**Requisitos relacionados:** RF-007, RF-009 e RF-010.

### US-006 — Acessar um arquivo hospedado na plataforma

**História**

Como professor que encontrou um material disponibilizado em um arquivo hospedado na plataforma, quero acessar esse arquivo para consultar ou utilizar o recurso.

**Critérios de aceitação**

- [ ] Quando houver um arquivo hospedado e disponível, o sistema apresenta uma opção clara para acessá-lo.
- [ ] A opção corresponde ao arquivo associado ao material consultado.
- [ ] Quando não houver arquivo hospedado, o sistema não apresenta um controle de acesso a um arquivo inexistente.
- [ ] Quando uma falha de acesso puder ser identificada, o sistema apresenta o tratamento previsto para essa situação.

**Requisitos relacionados:** RF-008, RF-009 e RF-010.

**Pendência de especificação**

Os formatos de arquivo aceitos e o comportamento esperado para cada formato ainda precisam ser definidos.

### US-007 — Identificar as opções de acesso disponíveis

**História**

Como professor que consulta os detalhes de um material, quero identificar quais formas de acesso estão disponíveis para saber como posso chegar ao recurso.

**Critérios de aceitação**

- [ ] Quando houver somente um link externo, o sistema apresenta a opção de acesso ao link.
- [ ] Quando houver somente um arquivo hospedado, o sistema apresenta a opção de acesso ao arquivo.
- [ ] Quando houver link externo e arquivo hospedado, o sistema apresenta as duas opções.
- [ ] Quando não houver link externo nem arquivo hospedado, o sistema informa que não há acesso direto disponível para o material.
- [ ] A ausência de acesso direto não impede que o material seja apresentado no catálogo ou tenha seus detalhes consultados.
- [ ] O sistema não apresenta opções de acesso que não correspondam a recursos cadastrados.

**Requisito relacionado:** RF-009.

### US-008 — Receber informações sobre falhas de acesso

**História**

Como professor que tenta acessar um material, quero receber uma informação clara quando o acesso falhar para compreender a situação e saber como proceder.

**Critérios de aceitação**

- [ ] Quando uma falha de acesso puder ser identificada, o sistema apresenta uma mensagem compreensível.
- [ ] A mensagem distingue, quando possível, uma falha de acesso da ausência de um link ou arquivo no cadastro.
- [ ] O sistema não afirma que um recurso está indisponível sem que essa condição possa ser identificada.
- [ ] Uma falha de acesso não é apresentada como se o material tivesse sido removido do catálogo.
- [ ] A mensagem não deve indicar que o acesso foi bem-sucedido quando ocorrer uma falha identificada.

**Requisito relacionado:** RF-010.

**Pendência de especificação**

Ainda precisam ser definidos os mecanismos de detecção de falhas e o comportamento posterior, incluindo a possibilidade de tentar novamente.

## 3. Rastreabilidade entre histórias e requisitos

| História | Requisitos relacionados |
|---|---|
| US-001 — Visualizar catálogo | RF-001 |
| US-002 — Pesquisar materiais | RF-002, RF-003, RF-005 |
| US-003 — Filtrar materiais | RF-004 |
| US-004 — Consultar detalhes | RF-006 |
| US-005 — Acessar por link externo | RF-007, RF-009, RF-010 |
| US-006 — Acessar arquivo hospedado | RF-008, RF-009, RF-010 |
| US-007 — Identificar opções de acesso | RF-009 |
| US-008 — Tratar falhas de acesso | RF-010 |

A rastreabilidade deve ser mantida alinhada com `requisitos.md`, `backlog.md`, `arquitetura-da-informacao.md` e `user-flow.md`.

## 4. Relação com o MVP

As oito histórias deste documento fazem parte do escopo funcional previsto para o MVP:

- Visualização do catálogo.
- Pesquisa por palavras-chave.
- Ordenação dos resultados por relevância.
- Aplicação de filtros.
- Consulta aos detalhes dos materiais.
- Acesso por link externo.
- Acesso a arquivos hospedados.
- Identificação das opções de acesso e tratamento de falhas.

A inclusão dessas histórias no escopo não significa que as funcionalidades estejam implementadas. O projeto permanece em fase de revisão documental.

Funcionalidades como envio de materiais pelos usuários, edição, adaptação e pré-visualização de arquivos permanecem fora do escopo atual.

## 5. Decisões confirmadas e pendências

### Decisões confirmadas

- O público prioritário são professores que procuram materiais para suas aulas.
- A busca consulta título, tipo de material, resumo e descrição.
- A busca ignora diferenças entre maiúsculas e minúsculas e entre palavras acentuadas e não acentuadas.
- A busca permite correspondências parciais.
- Os resultados são ordenados por relevância, com prioridade para título, tipo de material, resumo e descrição, nessa ordem.
- Os filtros previstos são tipo de material e etapa de ensino.
- Um material pode ter link externo, arquivo hospedado, ambos ou nenhum dos dois.
- A ausência de acesso direto não significa que o material esteja ausente do catálogo.
- O escopo atual não inclui pré-visualização, edição, adaptação ou envio de materiais pelos usuários.

### Pendências

- Fórmula de relevância e critérios de desempate.
- Tratamento de expressões com várias palavras.
- Valores disponíveis e regras de combinação dos filtros.
- Interação entre busca e filtros.
- Campos obrigatórios e opcionais dos materiais.
- Formatos de arquivo aceitos.
- Detecção e tratamento de falhas de acesso.

As pendências devem ser acompanhadas no `backlog.md`. Uma decisão já confirmada não deve ser reaberta sem uma justificativa explícita.

## 6. Considerações metodológicas

As histórias e os critérios de aceitação descrevem comportamentos esperados para orientar etapas futuras do projeto.

O formulário de pesquisa inicialmente considerado foi abandonado. Dados simulados não devem ser apresentados como respostas reais, evidências empíricas ou validação das necessidades dos professores.

A implementação, os testes de qualidade e a avaliação com usuários reais pertencem a etapas futuras. Nenhuma história deve ser considerada validada apenas por estar documentada.

## 7. Documentos relacionados

- `README.md`
- `product-brief.md`
- `requisitos.md`
- `backlog.md`
- `arquitetura-da-informacao.md`
- `objetivos-de-ux.md`
- `user-flow.md`
- `design-system.md`
