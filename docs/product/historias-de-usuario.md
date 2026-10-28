# EduMaterial — Histórias de Usuário

**Versão:** 0.3  
**Status:** Em revisão documental  
**Referência:** `requisitos.md`

## 1. Objetivo

Este documento descreve as histórias de usuário do EduMaterial e seus critérios de aceitação.

O público prioritário do produto são professores que procuram materiais educacionais para utilizar em suas aulas.

As histórias representam comportamentos esperados para o MVP. Elas não significam que as funcionalidades já estejam implementadas ou validadas com usuários reais.

## US-001 — Visualizar catálogo de materiais

**História de usuário**

Como professor, quero visualizar os materiais educacionais disponíveis para conhecer as opções que posso utilizar em minhas aulas.

**Critérios de aceitação**

- O sistema apresenta os materiais cadastrados no catálogo.
- Cada material apresenta, no mínimo, um título identificável.
- As informações apresentadas permitem distinguir um material dos demais.
- O usuário consegue selecionar um material para consultar seus detalhes.
- Quando não houver materiais cadastrados, o sistema apresenta uma mensagem informativa sobre o catálogo vazio.

**Prioridade:** Essencial para o MVP.

**Requisito relacionado:** RF-001.

## US-002 — Pesquisar materiais por palavras-chave

**História de usuário**

Como professor, quero pesquisar materiais educacionais por palavras-chave para encontrar recursos relacionados ao assunto que desejo ensinar.

**Critérios de aceitação**

- O sistema permite informar uma palavra ou expressão para pesquisar materiais.
- A pesquisa considera os campos título, tipo de material, resumo e descrição.
- A pesquisa não diferencia letras maiúsculas de minúsculas. Por exemplo, `Geografia` e `geografia` devem produzir correspondências equivalentes.
- A pesquisa ignora diferenças de acentuação. Por exemplo, pesquisar `historia` deve permitir encontrar materiais que contenham `história`.
- A pesquisa permite correspondências parciais. Por exemplo, pesquisar `geog` deve permitir encontrar materiais que contenham `geografia` em um dos campos pesquisáveis.
- Os resultados são ordenados por relevância, priorizando os campos nesta ordem: título, tipo de material, resumo e descrição.
- Quando não houver correspondências, o sistema apresenta uma mensagem informativa.
- O usuário consegue modificar os termos e realizar uma nova pesquisa.

**Prioridade:** Essencial para o MVP.

**Requisitos relacionados:** RF-002, RF-003 e RF-005.

**Pendências de especificação:**

- Definir os critérios detalhados de cálculo da relevância.
- Definir como serão tratados materiais com relevância equivalente.
- Definir o comportamento para expressões com várias palavras e diferentes tipos de correspondência.

## US-003 — Refinar resultados com filtros

**História de usuário**

Como professor, quero filtrar os materiais disponíveis para localizar recursos mais adequados às minhas necessidades de ensino.

**Critérios de aceitação**

- O sistema apresenta os filtros definidos para o MVP.
- Os filtros previstos são tipo de material e etapa de ensino.
- A aplicação dos filtros atualiza os materiais apresentados de acordo com os critérios selecionados.
- O usuário consegue remover os filtros aplicados.
- Quando a combinação de filtros não produzir resultados, o sistema apresenta uma mensagem informativa.
- A interação entre busca e filtros respeita as regras de combinação definidas para o produto.

**Prioridade:** Prevista para o MVP.

**Requisito relacionado:** RF-004.

**Pendências de especificação:**

- Definir as opções disponíveis em cada filtro.
- Definir se vários valores poderão ser selecionados no mesmo filtro.
- Definir como diferentes filtros serão combinados.
- Definir o comportamento conjunto entre busca por palavras-chave e filtros.

## US-004 — Consultar detalhes de um material

**História de usuário**

Como professor, quero consultar os detalhes de um material educacional para avaliar se ele atende às necessidades da minha aula.

**Critérios de aceitação**

- O usuário consegue abrir os detalhes de um material a partir do catálogo ou dos resultados da busca.
- A página apresenta um título identificável.
- O sistema apresenta as informações disponíveis sobre o material.
- Quando disponíveis, os detalhes incluem tipo de material, etapa de ensino, resumo, descrição, instruções de utilização, autor ou fonte.
- Quando aplicável e disponível, o sistema apresenta informações de autoria e licença.
- As opções de acesso disponíveis são apresentadas de forma clara.
- A ausência de informações opcionais não deve ser apresentada como se o material não existisse.

**Prioridade:** Essencial para o MVP.

**Requisito relacionado:** RF-006.

## US-005 — Acessar um material por link externo

**História de usuário**

Como professor, quero acessar o link externo associado a um material para consultar ou utilizar o recurso na fonte original.

**Critérios de aceitação**

- Quando houver um link externo disponível, o sistema apresenta uma opção clara de acesso.
- A opção direciona o usuário ao endereço associado ao material.
- O usuário consegue distinguir o link de acesso das informações descritivas do material.
- Quando não houver link externo, o sistema não apresenta um botão de acesso a um endereço inexistente.

**Prioridade:** Essencial para o MVP, quando houver link disponível.

**Requisito relacionado:** RF-007.

## US-006 — Acessar um arquivo hospedado na plataforma

**História de usuário**

Como professor, quero acessar um arquivo disponibilizado diretamente na plataforma para consultar ou utilizar o material educacional.

**Critérios de aceitação**

- Quando houver um arquivo hospedado disponível, o sistema apresenta uma opção clara para acessá-lo.
- A opção corresponde ao arquivo associado ao material.
- Quando não houver arquivo disponível, o sistema não apresenta um botão de acesso a um arquivo inexistente.
- Os formatos de arquivo aceitos seguem as regras definidas para o produto.

**Prioridade:** Essencial para o MVP, quando houver arquivo disponível.

**Requisito relacionado:** RF-008.

## US-007 — Identificar as opções de acesso disponíveis

**História de usuário**

Como professor, quero identificar se um material possui link externo, arquivo hospedado ou ambas as opções para saber como posso acessá-lo.

**Critérios de aceitação**

- Quando houver somente link externo, o sistema apresenta essa opção.
- Quando houver somente arquivo hospedado, o sistema apresenta essa opção.
- Quando houver link e arquivo, o sistema disponibiliza ambas as opções.
- Quando não houver link nem arquivo, o sistema informa que não há acesso direto disponível.
- A ausência de acesso direto não deve ser confundida com a ausência do material no catálogo.

**Prioridade:** Essencial para o MVP.

**Requisitos relacionados:** RF-006, RF-007, RF-008 e RF-009.

## US-008 — Compreender uma falha de acesso

**História de usuário**

Como professor, quero receber uma informação clara quando um link ou arquivo estiver indisponível para compreender a situação e decidir o que fazer em seguida.

**Critérios de aceitação**

- Quando uma falha de acesso puder ser identificada, o sistema apresenta uma mensagem compreensível.
- A mensagem distingue, quando possível, a indisponibilidade do recurso de sua ausência no cadastro.
- O sistema não deve afirmar que um recurso está indisponível sem que essa condição possa ser identificada.
- O comportamento para tentar novamente ou informar um problema deverá seguir as regras definidas para o produto.

**Prioridade:** Prevista para o MVP, conforme as possibilidades de detecção de falhas.

**Requisito relacionado:** RF-010.

## 2. Relação entre histórias e requisitos

| História | Requisitos relacionados |
|---|---|
| US-001 — Visualizar catálogo | RF-001 |
| US-002 — Pesquisar materiais | RF-002, RF-003, RF-005 |
| US-003 — Refinar resultados | RF-004 |
| US-004 — Consultar detalhes | RF-006 |
| US-005 — Acessar link externo | RF-007 |
| US-006 — Acessar arquivo hospedado | RF-008 |
| US-007 — Identificar opções de acesso | RF-006, RF-007, RF-008, RF-009 |
| US-008 — Compreender falha de acesso | RF-010 |

## 3. Decisões confirmadas

- O público prioritário do EduMaterial são professores.
- O MVP prevê catálogo, busca, filtros, detalhes e acesso aos materiais disponíveis.
- A busca considera título, tipo de material, resumo e descrição.
- A busca ignora diferenças entre maiúsculas e minúsculas.
- A busca ignora diferenças de acentuação.
- A busca permite correspondências parciais.
- A relevância prioriza título, tipo de material, resumo e descrição, nessa ordem.
- Um material pode ter link externo, arquivo hospedado, ambos ou nenhum.
- A pré-visualização e a edição de materiais não fazem parte do MVP.

## 4. Questões pendentes

- Critérios detalhados para calcular relevância e desempatar resultados.
- Regras de combinação entre busca e filtros.
- Opções e valores disponíveis nos filtros.
- Campos obrigatórios e opcionais dos materiais.
- Formatos de arquivo aceitos.
- Comportamento diante de falhas de acesso.

As questões pendentes devem ser acompanhadas no documento `backlog.md`.

## 5. Considerações metodológicas

As histórias de usuário e seus critérios de aceitação representam requisitos planejados, não funcionalidades já implementadas.

Um formulário de pesquisa foi considerado anteriormente, mas sua aplicação foi abandonada. Dados simulados não devem ser tratados como respostas reais nem como evidência de validação das necessidades dos professores.

A avaliação das histórias com usuários reais poderá ocorrer em uma etapa futura, quando houver condições para realizá-la.

## 6. Documentos relacionados

- `README.md`
- `product-brief.md`
- `requisitos.md`
- `backlog.md`
- `arquitetura-da-informacao.md`
- `objetivos-de-ux.md`
- `user-flow.md`
- `design-system.md`
