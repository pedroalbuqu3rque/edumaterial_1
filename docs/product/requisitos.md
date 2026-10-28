# EduMaterial — Requisitos do Produto

**Versão:** 0.3  
**Status:** Em revisão documental  
**Referência principal:** [`product-brief.md`](./product-brief.md)

## 1. Objetivo

Este documento define os requisitos funcionais e não funcionais previstos para o MVP do EduMaterial, uma proposta de plataforma digital voltada à descoberta, à seleção e ao acesso a materiais didáticos por professores.

Os requisitos descrevem os comportamentos esperados para o produto e servem de referência para as etapas futuras de especificação, implementação e avaliação.

As funcionalidades descritas são planejadas. Não representam funcionalidades necessariamente implementadas, testadas ou validadas com usuários reais.

## 2. Público-alvo

O público prioritário é formado por professores que procuram materiais didáticos para utilizar em suas aulas.

A interface e os comportamentos previstos devem apoiar a localização dos recursos, a consulta às suas informações e a identificação das formas disponíveis de acesso.

## 3. Requisitos funcionais

### RF-001 — Exibir catálogo de materiais

**Descrição:** O sistema deve apresentar um catálogo com os materiais cadastrados.

**Critérios de aceitação:**

- O catálogo deve apresentar os materiais disponíveis.
- Cada material deve possuir um título que permita identificá-lo.
- Os itens devem apresentar as informações resumidas definidas para o catálogo.
- O usuário deve conseguir acessar os detalhes de um material.
- Quando não houver materiais cadastrados, o sistema deve apresentar um estado informativo de catálogo vazio.

**Prioridade:** Essencial para o MVP.

### RF-002 — Pesquisar materiais por palavras-chave

**Descrição:** O sistema deve permitir que o professor pesquise materiais por palavras ou expressões relacionadas ao recurso procurado.

**Critérios de aceitação:**

- O sistema deve disponibilizar um campo de pesquisa identificável.
- O usuário deve conseguir informar palavras ou expressões.
- O sistema deve apresentar os materiais correspondentes aos termos informados, de acordo com as regras de pesquisa definidas.
- O usuário deve conseguir realizar uma nova pesquisa.
- Quando não houver correspondências, o sistema deve apresentar um estado informativo sem resultados.
- A ausência de resultados em uma pesquisa não deve ser confundida com a ausência de materiais cadastrados no catálogo.

**Prioridade:** Essencial para o MVP.

**Pendências:** Definir os campos pesquisáveis e as regras de correspondência, incluindo o tratamento de acentos, letras maiúsculas e minúsculas e correspondências parciais.

### RF-003 — Filtrar materiais

**Descrição:** O sistema deve permitir que o professor refine os materiais apresentados no catálogo por tipo de material e etapa de ensino.

**Critérios de aceitação:**

- O sistema deve disponibilizar um filtro por tipo de material.
- O sistema deve disponibilizar um filtro por etapa de ensino.
- Os resultados devem corresponder aos filtros selecionados.
- O usuário deve conseguir remover os filtros aplicados.
- A interface deve permitir identificar os filtros ativos.
- Quando os filtros não retornarem materiais, o sistema deve apresentar um estado informativo sem resultados.

**Prioridade:** Incluída no MVP.

**Pendências:** Definir as opções de cada filtro e o comportamento da combinação entre filtros e pesquisa por palavras-chave.

### RF-004 — Exibir detalhes do material

**Descrição:** O sistema deve apresentar informações que permitam ao professor identificar e avaliar inicialmente um material didático.

**Critérios de aceitação:**

- A página de detalhes deve identificar claramente o material selecionado.
- O sistema deve apresentar os campos disponíveis para a descrição do recurso, conforme a estrutura de dados definida.
- As informações devem ajudar o usuário a compreender as características do material.
- O tipo de material e a etapa de ensino devem ser apresentados quando estiverem disponíveis.
- A autoria, a fonte e as condições de utilização devem ser apresentadas quando essas informações estiverem disponíveis e forem aplicáveis.
- A página deve indicar as formas de acesso cadastradas.
- A consulta aos detalhes não deve depender de uma pré-visualização do conteúdo.

**Prioridade:** Essencial para o MVP.

**Pendência:** Definir quais campos serão obrigatórios e quais poderão ser opcionais.

### RF-005 — Acessar material por link externo

**Descrição:** O sistema deve permitir que o professor acesse um material por meio de um link externo, quando essa forma de acesso estiver cadastrada.

**Critérios de aceitação:**

- O link deve estar associado ao material correspondente.
- A interface deve identificar claramente a ação de acesso.
- A ação deve direcionar o usuário ao endereço cadastrado.
- O link não deve ser apresentado como disponível quando não houver um endereço cadastrado.
- Quando o material também possuir um arquivo hospedado na plataforma, as duas formas de acesso devem poder ser identificadas separadamente.

**Prioridade:** Essencial para o MVP.

**Pendência:** Definir o comportamento da interface quando o endereço externo estiver indisponível ou inválido.

### RF-006 — Acessar arquivo hospedado na plataforma

**Descrição:** O sistema deve permitir que o professor acesse um arquivo disponibilizado diretamente na plataforma, quando essa forma de acesso estiver cadastrada.

**Critérios de aceitação:**

- O arquivo deve estar associado ao material correspondente.
- A interface deve identificar a ação de acesso ao arquivo.
- O usuário deve conseguir abrir ou baixar o arquivo conforme o formato e os recursos definidos para o produto.
- A ação não deve ser apresentada como disponível quando não houver um arquivo cadastrado.
- Quando houver também um link externo, as opções de acesso devem ser apresentadas de forma clara e distinta.

**Prioridade:** Essencial para o MVP.

**Pendências:** Definir os formatos de arquivo aceitos e o comportamento esperado quando um arquivo não puder ser acessado.

### RF-007 — Informar ausência de resultados

**Descrição:** O sistema deve comunicar quando a pesquisa ou os filtros não retornarem materiais.

**Critérios de aceitação:**

- A interface deve informar que nenhum material corresponde aos critérios utilizados.
- O estado sem resultados deve ser visualmente distinto do catálogo vazio.
- O usuário deve conseguir alterar os termos da pesquisa ou remover filtros.
- A interface não deve apresentar resultados fictícios para preencher a listagem.

**Prioridade:** Essencial para o MVP.

### RF-008 — Informar ausência de forma de acesso

**Descrição:** O sistema deve comunicar quando um material não possuir link externo nem arquivo disponível para acesso.

**Critérios de aceitação:**

- A página de detalhes deve informar que não há uma forma de acesso cadastrada.
- A interface não deve apresentar uma ação de acesso indisponível como se fosse funcional.
- As informações descritivas do material devem continuar acessíveis.
- O usuário deve conseguir retornar ao catálogo ou escolher outro material.

**Prioridade:** Essencial para o MVP.

## 4. Requisitos não funcionais

### RNF-001 — Usabilidade

A interface deve organizar informações e ações de modo compreensível, facilitando a exploração do catálogo, a pesquisa, a filtragem, a consulta aos detalhes e o acesso aos recursos.

**Critério de avaliação futura:** observar se usuários conseguem concluir tarefas representativas em uma avaliação de usabilidade.

### RNF-002 — Responsividade

A interface deve ser planejada para preservar a legibilidade e a utilização em diferentes tamanhos de tela.

**Critério de avaliação futura:** verificar a apresentação e a utilização dos principais elementos em diferentes resoluções.

### RNF-003 — Consistência visual e funcional

Componentes que desempenham funções equivalentes devem manter padrões coerentes de apresentação, nomenclatura e comportamento.

**Critério de avaliação futura:** revisar os componentes e os fluxos em conjunto com o Design System e a arquitetura da informação.

### RNF-004 — Clareza das formas de acesso

O sistema deve distinguir links externos, arquivos hospedados na plataforma e materiais sem forma de acesso cadastrada.

**Critério de avaliação futura:** verificar se usuários conseguem identificar corretamente as opções disponíveis em cada material.

### RNF-005 — Transparência sobre origem e utilização

Quando essas informações estiverem disponíveis e forem aplicáveis, o sistema deve permitir identificar a autoria ou a fonte do material e suas condições de utilização.

**Critério de avaliação futura:** verificar se os campos definidos para autoria, fonte e condições de uso são apresentados de forma compreensível.

## 5. Itens fora do escopo

Os seguintes itens não fazem parte do MVP:

- Pré-visualização de materiais dentro da plataforma;
- Edição ou adaptação de materiais;
- Criação, envio ou publicação de materiais pelos usuários;
- Funcionalidades não previstas no escopo documental atual.

## 6. Decisões, hipóteses e pendências

### Decisões confirmadas

- O público prioritário são professores.
- O produto contempla catálogo, pesquisa, filtros, detalhes e acesso aos materiais.
- Os filtros previstos são tipo de material e etapa de ensino.
- O acesso poderá ocorrer por link externo, arquivo hospedado na plataforma ou ambas as opções.
- O MVP não inclui pré-visualização nem edição de materiais.
- O projeto está em fase de revisão documental.

### Hipóteses

- Um catálogo organizado pode facilitar a descoberta de materiais.
- A pesquisa e os filtros podem ajudar o professor a localizar recursos relevantes.
- A clareza das informações pode facilitar a avaliação inicial e o acesso.

Essas hipóteses não foram validadas por pesquisa com usuários reais.

### Pendências

- Campos pesquisáveis e regras de correspondência;
- Opções e combinação dos filtros;
- Campos obrigatórios e opcionais dos materiais;
- Formatos de arquivo aceitos;
- Tratamento de links e arquivos indisponíveis;
- Regras de apresentação de autoria, fonte e condições de utilização.

## 7. Rastreabilidade com as histórias de usuário

| Requisito | História relacionada |
|---|---|
| RF-001 — Catálogo | US-001 |
| RF-002 — Pesquisa | US-002 |
| RF-003 — Filtros | US-003 |
| RF-004 — Detalhes | US-004 |
| RF-005 — Link externo | US-005 |
| RF-006 — Arquivo hospedado | US-005 |
| RF-007 — Ausência de resultados | US-001, US-002 e US-003 |
| RF-008 — Ausência de forma de acesso | US-004 e US-005 |

## 8. Status da documentação

Os requisitos representam comportamentos previstos para o MVP. Não constituem evidência de implementação, testes de software ou validação com usuários.

A especificação deverá ser mantida alinhada ao Product Brief, às histórias de usuário e aos documentos de UX/UI.
