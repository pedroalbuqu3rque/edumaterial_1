# EduMaterial — Requisitos do Produto

**Versão:** 0.3  
**Status:** Em revisão documental  
**Referência:** `product-brief.md`

## 1. Objetivo

Este documento define os requisitos funcionais e não funcionais do EduMaterial, com foco na descoberta, consulta e acesso a materiais educacionais.

O público prioritário são professores que procuram recursos para utilizar em suas aulas.

Os requisitos representam o comportamento previsto para o Produto Mínimo Viável (MVP). A implementação ainda está prevista para uma etapa futura.

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

**Regras funcionais:**

1. A busca não deve diferenciar letras maiúsculas de minúsculas.
2. A busca deve ignorar diferenças de acentuação. Por exemplo, pesquisar `historia` deve permitir encontrar materiais com o termo `história`.
3. A busca deve permitir correspondências parciais. Por exemplo, pesquisar `geog` deve permitir encontrar materiais que contenham `geografia` em um dos campos pesquisáveis.
4. Os resultados devem ser ordenados por relevância, seguindo a prioridade dos campos definida no RF-003.
5. A busca deve considerar os dados disponíveis nos campos pesquisáveis de cada material.

A definição dessas regras não implica que a funcionalidade já esteja implementada.

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

Esses critérios deverão ser detalhados antes da implementação.

### RF-004 — Filtrar materiais

O sistema deve permitir a aplicação de filtros para refinar os materiais apresentados no catálogo.

Os filtros previstos para o MVP são:
- Tipo de material.
- Etapa de ensino.

**Pontos pendentes:**
- Definir as opções disponíveis em cada filtro.
- Definir se será possível selecionar várias opções simultaneamente.
- Definir como diferentes filtros serão combinados.
- Definir como os filtros poderão ser removidos.
- Especificar a interação entre os filtros e a busca por palavras-chave.

Os filtros devem apresentar resultados coerentes com os critérios selecionados pelo usuário.

### RF-005 — Informar ausência de resultados

Quando uma busca ou combinação de filtros não encontrar materiais correspondentes, o sistema deve apresentar uma mensagem informativa.

A interface deve permitir que o usuário revise os termos pesquisados ou altere os filtros aplicados.

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

### RF-007 — Permitir acesso por link externo

Quando um material possuir um link externo disponível, o sistema deve apresentar uma opção clara para que o usuário acesse o recurso na fonte correspondente.

O acesso deverá direcionar o usuário ao endereço associado ao material.

A plataforma deve distinguir o acesso ao recurso externo das informações apresentadas na página de detalhes.

### RF-008 — Permitir acesso a arquivos hospedados na plataforma

Quando um material possuir um arquivo hospedado na própria plataforma, o sistema deve disponibilizar uma opção clara de acesso ao arquivo.

Os formatos aceitos e o comportamento específico para cada tipo de arquivo ainda precisam ser definidos.

### RF-009 — Tratar as diferentes formas de acesso

O sistema deve representar corretamente os seguintes cenários:

- **Somente link externo:** apresentar a opção de acesso ao link.
- **Somente arquivo hospedado:** apresentar a opção de acesso ao arquivo.
- **Link e arquivo:** disponibilizar as duas opções de acesso.
- **Sem link e sem arquivo:** informar que não há acesso direto disponível para o material.

A ausência de um link ou arquivo não deve ser interpretada automaticamente como ausência do material no catálogo.

### RF-010 — Informar falhas de acesso

Quando um link externo ou arquivo não puder ser acessado, o sistema deve apresentar uma mensagem compreensível sobre a indisponibilidade, quando essa condição puder ser identificada.

O comportamento específico para detectar e tratar falhas de acesso deverá ser definido antes da implementação.

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
- Tratamento dos estados sem materiais, sem resultados e sem acesso direto.

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
- Os critérios de desempate entre materiais.
- As opções e combinações dos filtros.
- Os campos obrigatórios dos materiais.
- Os formatos de arquivo aceitos.
- O tratamento de falhas de acesso.

Essas pendências devem ser acompanhadas no documento `backlog.md`.

## 6. Rastreabilidade

Os requisitos devem ser mantidos em alinhamento com os documentos relacionados:

| Requisito | Documentos relacionados |
|---|---|
| RF-001 — Catálogo | `historias-de-usuario.md`, `arquitetura-da-informacao.md` |
| RF-002 — Busca | `historias-de-usuario.md`, `objetivos-de-ux.md`, `arquitetura-da-informacao.md` |
| RF-003 — Relevância | `historias-de-usuario.md`, `user-flow.md` |
| RF-004 — Filtros | `historias-de-usuario.md`, `user-flow.md`, `arquitetura-da-informacao.md` |
| RF-005 — Ausência de resultados | `historias-de-usuario.md`, `user-flow.md`, `arquitetura-da-informacao.md` |
| RF-006 — Detalhes | `historias-de-usuario.md`, `arquitetura-da-informacao.md` |
| RF-007 — Link externo | `historias-de-usuario.md`, `user-flow.md` |
| RF-008 — Arquivo hospedado | `historias-de-usuario.md`, `user-flow.md` |
| RF-009 — Formas de acesso | `historias-de-usuario.md`, `user-flow.md` |
| RF-010 — Falhas de acesso | `user-flow.md`, `arquitetura-da-informacao.md` |

## 7. Decisões confirmadas, hipóteses e pendências

### Decisões confirmadas

- O público prioritário são professores.
- O MVP inclui catálogo, busca, filtros, detalhes e acesso aos materiais disponíveis.
- A busca consulta título, tipo de material, resumo e descrição.
- A busca ignora diferenças entre maiúsculas e minúsculas.
- A busca ignora diferenças de acentuação.
- A busca permite correspondências parciais.
- Os resultados são ordenados por relevância, priorizando título, tipo de material, resumo e descrição, nessa ordem.
- Os materiais podem ser acessados por link externo, arquivo hospedado, ambos ou nenhum dos dois.
- A pré-visualização e a edição de materiais não fazem parte do MVP.

### Hipóteses a avaliar futuramente

- A busca e os filtros facilitarão a localização de materiais adequados às necessidades dos professores.
- A apresentação clara das opções de acesso reduzirá a incerteza sobre como utilizar os materiais.

Essas hipóteses ainda não devem ser tratadas como resultados validados por pesquisa com usuários.

### Questões pendentes

- Cálculo detalhado da relevância.
- Critérios de desempate.
- Opções e combinações dos filtros.
- Campos obrigatórios e opcionais dos materiais.
- Formatos de arquivo aceitos.
- Comportamento diante de falhas de acesso.
- Critérios técnicos de acessibilidade.

## 8. Considerações metodológicas

O projeto está em fase de revisão documental. A implementação e a avaliação das funcionalidades ocorrerão em etapas futuras.

Um formulário de pesquisa foi considerado anteriormente, mas sua aplicação foi abandonada. Portanto, dados simulados não devem ser apresentados como respostas reais, evidências empíricas ou validação das necessidades dos professores.

As decisões registradas neste documento representam a especificação atual do produto, não resultados de testes ou de uma implementação concluída.

## 9. Documentos relacionados

- `README.md`
- `product-brief.md`
- `historias-de-usuario.md`
- `backlog.md`
- `arquitetura-da-informacao.md`
- `objetivos-de-ux.md`
- `user-flow.md`
- `design-system.md`
