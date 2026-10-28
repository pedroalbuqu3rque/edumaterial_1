# EduMaterial — Requisitos do Produto

**Versão:** 0.3  
**Status:** Em revisão documental  
**Referência:** `product-brief.md`

## 1. Objetivo

Este documento define os requisitos funcionais e não funcionais do EduMaterial, com foco na descoberta, consulta e acesso a materiais educacionais.

O público prioritário são professores que procuram recursos para utilizar em suas aulas.

Os requisitos representam o comportamento previsto para o Produto Mínimo Viável (MVP). A implementação e a avaliação com usuários reais estão previstas para etapas futuras.

## 2. Requisitos funcionais

### RF-001 — Exibir catálogo de materiais

O sistema deve apresentar um catálogo de materiais educacionais previamente cadastrados.

**Critérios:**
- Cada material deve apresentar informações que permitam identificá-lo.
- O catálogo deve permitir que o usuário selecione um material para consultar seus detalhes.
- Quando não houver materiais cadastrados, o sistema deve apresentar um estado vazio informativo.

### RF-002 — Pesquisar materiais por palavras-chave

O sistema deve permitir que o usuário pesquise materiais educacionais por meio de palavras-chave.

A busca deve consultar os seguintes campos:
- Título.
- Tipo de material.
- Resumo.
- Descrição.

**Regras funcionais confirmadas:**

1. A busca não deve diferenciar letras maiúsculas de minúsculas. Por exemplo, `Geografia` e `geografia` devem produzir correspondências equivalentes.
2. A busca deve ignorar diferenças de acentuação. Por exemplo, pesquisar `historia` deve permitir encontrar materiais que contenham `história`, e vice-versa.
3. A busca deve permitir correspondências parciais. Por exemplo, pesquisar `geog` deve permitir encontrar materiais que contenham `geografia` em um dos campos pesquisáveis.
4. Os resultados devem ser ordenados por relevância, seguindo a prioridade dos campos definida no RF-003.
5. A busca deve considerar os dados disponíveis nos campos pesquisáveis de cada material.

Essas regras representam a especificação prevista para o MVP e não significam que a busca já esteja implementada.

### RF-003 — Ordenar resultados por relevância

O sistema deve ordenar os materiais encontrados conforme a relevância das correspondências com os termos pesquisados.

A prioridade dos campos deve seguir esta ordem:

1. **Título:** maior prioridade.
2. **Tipo de material:** segunda prioridade.
3. **Resumo:** terceira prioridade.
4. **Descrição:** quarta prioridade.

Quando houver correspondências em diferentes campos, os resultados devem priorizar os materiais que apresentem correspondências nos campos de maior prioridade.

**Pendências de especificação:**
- Definir como a relevância será calculada quando houver diferentes tipos de correspondência.
- Definir o comportamento quando vários materiais apresentarem relevância equivalente.
- Definir se a correspondência exata de uma palavra terá prioridade sobre a correspondência parcial.
- Definir como serão tratadas expressões com várias palavras.

A prioridade entre os campos está definida, mas a fórmula detalhada de pontuação e os critérios de desempate permanecem pendentes. Esses critérios deverão ser detalhados antes da implementação.

### RF-004 — Filtrar materiais

O sistema deve permitir a aplicação de filtros para refinar os materiais apresentados no catálogo.

Os filtros previstos para o MVP são:
- Tipo de material.
- Etapa de ensino.

Os filtros devem apresentar resultados coerentes com os critérios selecionados pelo usuário.

**Pendências de especificação:**
- Definir as opções disponíveis em cada filtro.
- Definir se será possível selecionar várias opções simultaneamente no mesmo filtro.
- Definir como diferentes filtros serão combinados.
- Definir como os filtros poderão ser removidos.
- Especificar a interação entre os filtros e a busca por palavras-chave.

### RF-005 — Informar ausência de resultados

Quando uma busca ou combinação de filtros não encontrar materiais correspondentes, o sistema deve apresentar uma mensagem informativa.

A interface deve permitir que o usuário revise os termos pesquisados ou altere os filtros aplicados.

A ausência de resultados não deve ser confundida com um catálogo vazio: o catálogo vazio ocorre quando não existem materiais cadastrados, enquanto a ausência de resultados ocorre quando existem materiais, mas nenhum corresponde aos critérios da consulta.

### RF-006 — Exibir detalhes do material

O sistema deve apresentar informações que permitam ao usuário identificar e avaliar um material educacional.

Conforme os dados disponíveis, os detalhes poderão incluir:
- Título.
- Tipo de material.
- Etapa de ensino.
- Resumo.
- Descrição.
- Instruções de utilização.
- Autor ou fonte.
- Informações de autoria e licença, quando aplicáveis.
- Link externo para acesso.
- Arquivo hospedado na própria plataforma.

Os campos obrigatórios e opcionais ainda deverão ser definidos na especificação dos dados dos materiais.

A ausência de informações opcionais não deve ser apresentada como se o material não existisse.

### RF-007 — Permitir acesso por link externo

Quando um material possuir um link externo disponível, o sistema deve apresentar uma opção clara para que o usuário acesse o recurso na fonte correspondente.

O acesso deverá direcionar o usuário ao endereço associado ao material.

A plataforma deve distinguir o acesso ao recurso externo das informações apresentadas na página de detalhes.

Quando não houver link externo disponível, o sistema não deve apresentar uma opção de acesso a um endereço inexistente.

### RF-008 — Permitir acesso a arquivos hospedados na plataforma

Quando um material possuir um arquivo hospedado na própria plataforma, o sistema deve disponibilizar uma opção clara de acesso ao arquivo correspondente.

Quando não houver arquivo disponível, o sistema não deve apresentar uma opção de acesso a um arquivo inexistente.

Os formatos aceitos e o comportamento específico para cada tipo de arquivo ainda precisam ser definidos.

### RF-009 — Tratar as diferentes formas de acesso

O sistema deve representar corretamente os seguintes cenários:

- **Somente link externo:** apresentar a opção de acesso ao link.
- **Somente arquivo hospedado:** apresentar a opção de acesso ao arquivo.
- **Link e arquivo:** disponibilizar as duas opções de acesso.
- **Sem link e sem arquivo:** informar que não há acesso direto disponível para o material.

A ausência de um link ou arquivo não deve ser interpretada automaticamente como ausência do material no catálogo.

### RF-010 — Informar falhas de acesso

Quando um link externo ou arquivo não puder ser acessado e essa condição puder ser identificada, o sistema deve apresentar uma mensagem compreensível sobre a indisponibilidade.

A mensagem deve distinguir, quando possível, uma falha de acesso da ausência de um recurso no cadastro.

O sistema não deve afirmar que um recurso está indisponível sem que essa condição possa ser identificada.

O comportamento específico para detectar e tratar falhas de acesso, incluindo a possibilidade de tentar novamente, deverá ser definido antes da implementação.

## 3. Requisitos não funcionais

### RNF-001 — Usabilidade

A interface deve apresentar informações, mensagens e controles compreensíveis para professores que procuram materiais educacionais.

### RNF-002 — Responsividade

A interface deve se adaptar a diferentes tamanhos de tela, incluindo computadores, tablets e celulares.

### RNF-003 — Consistência

As informações e os estados apresentados devem ser coerentes com os dados disponíveis e com as ações realizadas pelo usuário.

### RNF-004 — Clareza de acesso

A interface deve distinguir claramente entre:
- Consultar os detalhes de um material.
- Acessar um link externo.
- Acessar um arquivo hospedado.
- Consultar um material sem acesso direto disponível.

### RNF-005 — Transparência das informações

Quando disponíveis, as informações de autoria, fonte e condições de uso devem ser apresentadas de forma clara, respeitando os dados cadastrados para cada material.

### RNF-006 — Acessibilidade

A interface deverá considerar práticas de acessibilidade, incluindo legibilidade dos textos, identificação clara dos controles, contraste adequado e navegação compreensível.

Os critérios técnicos de acessibilidade serão detalhados em etapa posterior.

## 4. Escopo do MVP

### Incluído no MVP

- Visualização do catálogo de materiais previamente cadastrados.
- Busca por palavras-chave nos campos definidos no RF-002.
- Busca sem distinção entre maiúsculas e minúsculas.
- Busca sem distinção de acentuação.
- Correspondência parcial de termos.
- Ordenação dos resultados conforme a prioridade dos campos definida no RF-003.
- Filtros por tipo de material e etapa de ensino.
- Visualização dos detalhes dos materiais.
- Acesso por link externo, quando disponível.
- Acesso a arquivos hospedados na plataforma, quando disponíveis.
- Representação dos quatro cenários de acesso definidos no RF-009.
- Tratamento dos estados de catálogo vazio, ausência de resultados e falha de acesso.

### Fora do escopo do MVP

- Cadastro e autenticação de usuários.
- Envio ou publicação de materiais pelos usuários.
- Criação ou edição de materiais dentro da plataforma.
- Adaptação de materiais pelos usuários.
- Pré-visualização de arquivos diretamente na plataforma.
- Favoritos e coleções pessoais.
- Recomendação automática de materiais.

Essas funcionalidades poderão ser avaliadas em versões futuras.

## 5. Prioridades e dependências

A busca, os filtros, o catálogo, os detalhes e as opções de acesso constituem o escopo funcional previsto para o MVP.

Algumas regras ainda precisam ser especificadas antes da implementação, especialmente:
- O cálculo de relevância dos resultados.
- Os critérios de desempate.
- O tratamento de expressões com várias palavras.
- As opções e combinações dos filtros.
- Os campos obrigatórios e opcionais dos materiais.
- Os formatos de arquivo aceitos.
- O tratamento de falhas de acesso.
- Os critérios técnicos de acessibilidade.

Essas pendências devem ser acompanhadas no documento `backlog.md`. Uma regra já confirmada não deve voltar a ser registrada como uma decisão em aberto, embora seus detalhes de implementação ainda possam precisar de especificação.

## 6. Rastreabilidade

Os requisitos devem ser mantidos em alinhamento com os documentos relacionados:

| Requisito | Documentos relacionados |
|---|---|
| RF-001 — Catálogo | `historias-de-usuario.md`, `arquitetura-da-informacao.md`, `user-flow.md` |
| RF-002 — Busca | `historias-de-usuario.md`, `objetivos-de-ux.md`, `arquitetura-da-informacao.md`, `user-flow.md` |
| RF-003 — Relevância | `historias-de-usuario.md`, `backlog.md`, `user-flow.md` |
| RF-004 — Filtros | `historias-de-usuario.md`, `backlog.md`, `arquitetura-da-informacao.md`, `user-flow.md` |
| RF-005 — Ausência de resultados | `historias-de-usuario.md`, `arquitetura-da-informacao.md`, `user-flow.md` |
| RF-006 — Detalhes | `historias-de-usuario.md`, `arquitetura-da-informacao.md`, `user-flow.md` |
| RF-007 — Link externo | `historias-de-usuario.md`, `user-flow.md` |
| RF-008 — Arquivo hospedado | `historias-de-usuario.md`, `user-flow.md` |
| RF-009 — Formas de acesso | `historias-de-usuario.md`, `arquitetura-da-informacao.md`, `user-flow.md` |
| RF-010 — Falhas de acesso | `historias-de-usuario.md`, `arquitetura-da-informacao.md`, `user-flow.md`, `backlog.md` |

## 7. Decisões confirmadas, hipóteses e pendências

### Decisões confirmadas

- O público prioritário são professores.
- O MVP inclui catálogo, busca, filtros, detalhes e acesso aos materiais disponíveis.
- A busca consulta título, tipo de material, resumo e descrição.
- A busca ignora diferenças entre maiúsculas e minúsculas.
- A busca ignora diferenças de acentuação.
- A busca permite correspondências parciais.
- Os resultados são ordenados por relevância, priorizando título, tipo de material, resumo e descrição, nessa ordem.
- Os filtros previstos são tipo de material e etapa de ensino.
- Os materiais podem ter link externo, arquivo hospedado, ambos ou nenhum dos dois.
- A ausência de acesso direto não significa que o material esteja ausente do catálogo.
- A pré-visualização, a edição e a adaptação de materiais não fazem parte do MVP.
- O projeto está em fase de revisão documental; a implementação e a avaliação com usuários reais pertencem a etapas futuras.

### Hipóteses a avaliar futuramente

- A busca e os filtros facilitarão a localização de materiais adequados às necessidades dos professores.
- A apresentação clara das opções de acesso reduzirá a incerteza sobre como utilizar os materiais.

Essas hipóteses ainda não devem ser tratadas como resultados validados por pesquisa com usuários.

### Questões pendentes

- Cálculo detalhado da relevância.
- Critérios de desempate entre resultados.
- Tratamento de expressões com várias palavras.
- Opções, seleção múltipla e combinação dos filtros.
- Interação entre busca e filtros.
- Campos obrigatórios e opcionais dos materiais.
- Formatos de arquivo aceitos.
- Detecção e tratamento de falhas de acesso.
- Critérios técnicos de acessibilidade.

## 8. Considerações metodológicas

O projeto está em fase de revisão documental. A implementação e a avaliação das funcionalidades ocorrerão em etapas futuras.

Um formulário de pesquisa foi considerado anteriormente, mas sua aplicação foi abandonada. Portanto, dados simulados não devem ser apresentados como respostas reais, evidências empíricas ou validação das necessidades dos professores.

As decisões registradas neste documento representam a especificação atual do produto, não resultados de testes, pesquisa empírica ou implementação concluída.

## 9. Documentos relacionados

- `README.md`
- `product-brief.md`
- `historias-de-usuario.md`
- `backlog.md`
- `arquitetura-da-informacao.md`
- `objetivos-de-ux.md`
- `user-flow.md`
- `design-system.md`
