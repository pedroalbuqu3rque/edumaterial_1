# EduMaterial — Requisitos do Produto

**Versão:** 0.2  
**Status:** Proposta documental revisada  
**Referência principal:** [`product-brief.md`](./product-brief.md)  

## 1. Objetivo

Este documento define os requisitos funcionais e não funcionais previstos para o MVP do EduMaterial, uma proposta de plataforma digital voltada à descoberta e à seleção de materiais didáticos por professores.

Os requisitos estabelecem os comportamentos esperados para o produto e servem como referência para as etapas futuras de especificação, implementação e avaliação.

As funcionalidades descritas são planejadas, não necessariamente implementadas. A documentação ainda está em revisão, e os requisitos não foram validados por testes do sistema nem por pesquisa com usuários reais.

## 2. Público-alvo

O público prioritário é formado por professores que procuram materiais didáticos para utilizar em suas aulas.

A interface e os comportamentos previstos devem apoiar a localização dos recursos, a consulta às suas informações e o acesso aos materiais disponíveis.

## 3. Requisitos funcionais

Os requisitos funcionais descrevem as ações e os comportamentos que o sistema deverá oferecer.

### RF-001 — Exibir catálogo de materiais

**Descrição:** O sistema deve apresentar um catálogo com os materiais didáticos cadastrados previamente.

**Critérios de aceitação:**
- O catálogo deve apresentar os materiais disponíveis.
- Cada item deve possuir um título que permita identificar o recurso.
- Os itens devem apresentar as informações resumidas definidas para o catálogo.
- O usuário deve conseguir acessar os detalhes de um material.
- Quando não houver materiais cadastrados, o sistema deve apresentar uma mensagem informativa.

**Prioridade:** Essencial para o MVP.

### RF-002 — Pesquisar materiais por palavras-chave

**Descrição:** O sistema deve permitir que o professor pesquise materiais por meio de palavras ou expressões relacionadas ao recurso procurado.

**Critérios de aceitação:**
- O sistema deve disponibilizar um campo para informar os termos da pesquisa.
- A pesquisa deve considerar os campos definidos para busca no catálogo.
- O sistema deve apresentar os materiais que correspondam aos termos informados, conforme as regras de pesquisa estabelecidas.
- O professor deve conseguir realizar uma nova pesquisa após consultar os resultados.
- Quando não houver correspondências, o sistema deve apresentar uma mensagem informativa.

**Prioridade:** Essencial para o MVP.

**Pendência:** Definir os campos pesquisáveis e as regras de correspondência, incluindo o tratamento de acentos, letras maiúsculas e minúsculas e correspondências parciais.

### RF-003 — Filtrar materiais

**Descrição:** O sistema deve permitir que o professor refine os materiais apresentados no catálogo utilizando filtros por tipo de material e etapa de ensino.

**Critérios de aceitação:**
- O sistema deve disponibilizar um filtro por tipo de material.
- O sistema deve disponibilizar um filtro por etapa de ensino.
- Os resultados devem corresponder aos filtros selecionados.
- O usuário deve conseguir remover os filtros aplicados.
- A interface deve indicar quais filtros estão ativos.
- Quando não houver resultados para os filtros selecionados, o sistema deve apresentar uma mensagem informativa.

**Prioridade:** Incluída no MVP.

**Pendência:** Definir as opções de cada filtro e o comportamento da combinação entre filtros e pesquisa por palavras-chave.

### RF-004 — Exibir detalhes do material

**Descrição:** O sistema deve apresentar informações que permitam ao professor identificar e avaliar inicialmente um material didático.

**Critérios de aceitação:**
- A página de detalhes deve identificar o material consultado.
- Deve apresentar as informações descritivas previstas para o recurso.
- Quando disponíveis, devem ser apresentadas informações como tipo de material e etapa de ensino indicada.
- Deve ser possível identificar a forma de acesso cadastrada para o recurso.
- A consulta aos detalhes não deve depender de uma visualização prévia do conteúdo.

**Prioridade:** Essencial para o MVP.

**Observação:** A visualização prévia do conteúdo dentro da plataforma está fora do escopo do MVP.

### RF-005 — Disponibilizar acesso por link externo

**Descrição:** Quando um material possuir um link externo cadastrado, o sistema deve disponibilizar uma ação para acessar o recurso no endereço correspondente.

**Critérios de aceitação:**
- A página de detalhes deve indicar que o material pode ser acessado por um link externo.
- A ação de acesso deve estar identificada de maneira clara.
- O endereço utilizado deve corresponder ao link cadastrado para o material.
- Quando não houver link externo cadastrado, o sistema não deve apresentar uma ação de acesso por link.

**Prioridade:** Essencial para o MVP.

**Pendência:** Definir o comportamento esperado para links inválidos, indisponíveis ou que deixem de funcionar.

### RF-006 — Disponibilizar acesso a arquivos hospedados na plataforma

**Descrição:** Quando um material possuir um arquivo disponibilizado diretamente na plataforma, o sistema deve oferecer uma ação para acessar ou baixar esse arquivo, conforme o comportamento definido para o recurso.

**Critérios de aceitação:**
- A página de detalhes deve indicar quando o material possui um arquivo disponível na plataforma.
- A ação de acesso ao arquivo deve estar identificada de maneira clara.
- O arquivo disponibilizado deve corresponder ao material cadastrado.
- Quando não houver arquivo disponível, o sistema não deve apresentar uma ação de acesso a arquivo.
- A interface deve informar quando não houver nenhuma forma de acesso cadastrada para o material.

**Prioridade:** Essencial para o MVP.

**Pendências:** Definir os formatos de arquivo aceitos, os limites aplicáveis e as regras de armazenamento e disponibilização dos arquivos.

### RF-007 — Informar ausência de resultados

**Descrição:** O sistema deve informar quando uma pesquisa ou combinação de filtros não retornar materiais correspondentes.

**Critérios de aceitação:**
- A mensagem deve indicar claramente que nenhum material corresponde aos critérios utilizados.
- A interface deve permitir que o professor compreenda que a ausência de resultados está relacionada à pesquisa ou aos filtros aplicados.
- O professor deve conseguir alterar a pesquisa ou remover filtros para tentar localizar outros materiais.
- A ausência de resultados não deve ser apresentada como erro do sistema sem que haja evidência de uma falha técnica.

**Prioridade:** Essencial para o MVP.

### RF-008 — Informar ausência de forma de acesso

**Descrição:** Quando um material não possuir link externo nem arquivo disponível na plataforma, o sistema deve informar que não há uma forma de acesso cadastrada.

**Critérios de aceitação:**
- A página de detalhes deve distinguir a ausência de acesso da ausência de informações sobre o material.
- O sistema não deve apresentar um link ou arquivo inexistente como disponível.
- As informações descritivas do material devem continuar acessíveis, mesmo quando não houver uma forma de acesso cadastrada.

**Prioridade:** Essencial para o MVP.

## 4. Requisitos não funcionais

Os requisitos não funcionais descrevem características esperadas de qualidade e uso do produto.

### RNF-001 — Clareza e usabilidade

**Descrição:** A interface deve utilizar textos, rótulos e controles compreensíveis para o público prioritário.

**Diretriz:** As ações de pesquisa, filtragem, consulta aos detalhes e acesso aos materiais devem ser identificáveis sem depender de instruções externas para compreender sua finalidade.

**Status:** Critério de qualidade proposto; ainda não avaliado.

### RNF-002 — Responsividade

**Descrição:** A interface deve adaptar sua apresentação a diferentes tamanhos de tela, incluindo computadores e dispositivos móveis.

**Diretriz:** As informações dos materiais e os principais controles devem continuar acessíveis em diferentes larguras de tela.

**Status:** Critério de qualidade proposto; ainda não avaliado.

### RNF-003 — Consistência das informações

**Descrição:** As informações apresentadas no catálogo, nos resultados de pesquisa e na página de detalhes devem ser coerentes com os dados cadastrados para cada material.

**Diretriz:** O mesmo material não deve apresentar informações contraditórias entre as diferentes áreas da plataforma.

**Status:** Critério de qualidade proposto; ainda não avaliado.

### RNF-004 — Clareza das formas de acesso

**Descrição:** A interface deve distinguir links externos, arquivos disponibilizados na plataforma e materiais sem forma de acesso cadastrada.

**Diretriz:** O usuário deve conseguir identificar o tipo de ação disponível antes de tentar acessar o recurso.

**Status:** Critério de qualidade proposto; ainda não avaliado.

### RNF-005 — Identificação das condições de uso

**Descrição:** A estrutura de informações deve permitir registrar e apresentar dados sobre autoria, origem e condições de uso dos materiais, conforme as regras que vierem a ser definidas para o catálogo.

**Diretriz:** O sistema não deve atribuir autoria, licenças ou permissões de uso sem informações que sustentem essas declarações.

**Status:** Diretriz proposta; os campos obrigatórios e as regras correspondentes ainda precisam ser definidos.

## 5. Fora do escopo do MVP

As seguintes funcionalidades não fazem parte da primeira versão planejada:

- Cadastro de usuários e autenticação.
- Publicação ou envio de materiais pelos próprios usuários.
- Favoritos e coleções pessoais.
- Recomendações automáticas de materiais.
- Edição ou adaptação de materiais dentro da plataforma.
- Visualização prévia do conteúdo dos materiais dentro da plataforma.

A visualização prévia poderá ser considerada em uma versão futura. As demais funcionalidades também poderão ser reavaliadas posteriormente, caso sejam identificadas necessidades que justifiquem sua inclusão.

## 6. Resumo do escopo do MVP

| Área | Decisão para o MVP |
|---|---|
| Catálogo | Incluído |
| Busca por palavras-chave | Incluída |
| Filtro por tipo de material | Incluído |
| Filtro por etapa de ensino | Incluído |
| Detalhes do material | Incluídos |
| Acesso por link externo | Incluído |
| Acesso a arquivo hospedado na plataforma | Incluído |
| Mensagem de ausência de resultados | Incluída |
| Mensagem de ausência de forma de acesso | Incluída |
| Visualização prévia | Fora do escopo |
| Publicação de materiais por usuários | Fora do escopo |
| Edição ou adaptação de materiais | Fora do escopo |
| Favoritos e recomendações | Fora do escopo |

## 7. Decisões confirmadas, hipóteses e pendências

### 7.1. Decisões confirmadas

- O público prioritário é formado por professores que procuram materiais para suas aulas.
- O MVP contempla catálogo, busca, filtros e detalhes dos materiais.
- Os filtros iniciais serão por tipo de material e etapa de ensino.
- O acesso aos recursos poderá ocorrer por links externos ou arquivos disponibilizados diretamente na plataforma.
- A visualização prévia não faz parte do MVP.
- A implementação e o QA não fazem parte da etapa atual de revisão documental.

### 7.2. Hipóteses de produto

- Um catálogo organizado poderá facilitar a descoberta de materiais didáticos.
- A busca por palavras-chave poderá ajudar os professores a localizar recursos.
- Os filtros poderão facilitar a seleção de materiais adequados.
- Informações descritivas poderão auxiliar a avaliação inicial dos recursos.

Essas hipóteses não constituem evidências de pesquisa com professores e ainda não foram validadas empiricamente.

### 7.3. Pendências de especificação

- Definir os campos obrigatórios e opcionais de cada material.
- Definir quais campos serão considerados na busca.
- Especificar o comportamento de busca e filtragem combinadas.
- Definir as opções disponíveis nos filtros.
- Definir formatos de arquivo aceitos e limites aplicáveis.
- Definir as regras de armazenamento e acesso aos arquivos.
- Definir como serão tratados links e arquivos indisponíveis.
- Definir os campos e as regras referentes a autoria, origem e condições de uso.
- Definir os requisitos técnicos de desempenho, segurança e acessibilidade aplicáveis ao produto.

Essas pendências não devem ser interpretadas como decisões já tomadas. Elas precisam ser resolvidas e registradas nos documentos correspondentes antes da implementação.

## 8. Relação com as histórias de usuário

Os requisitos funcionais estão relacionados às histórias de usuário de [`historias-de-usuario.md`](./historias-de-usuario.md):

| Requisito | História relacionada |
|---|---|
| RF-001 — Exibir catálogo | US-001 — Visualizar catálogo de materiais |
| RF-002 — Pesquisar materiais | US-002 — Pesquisar materiais por palavras-chave |
| RF-003 — Filtrar materiais | US-004 — Filtrar materiais do catálogo |
| RF-004 — Exibir detalhes | US-003 — Consultar detalhes de um material |
| RF-005 — Acesso por link externo | US-005 — Acessar um material didático |
| RF-006 — Acesso a arquivos | US-005 — Acessar um material didático |
| RF-007 — Ausência de resultados | US-002 e US-004 |
| RF-008 — Ausência de forma de acesso | US-005 |

Esta relação permite verificar se as funcionalidades descritas nos requisitos estão representadas nas histórias de usuário.

## 9. Observações metodológicas e status

Os requisitos foram estruturados como parte de um estudo de caso de planejamento de produto digital.

A coleta de respostas por meio do Google Forms foi abandonada. Não há resultados desse questionário que possam ser utilizados como evidência empírica para validar os requisitos ou comprovar necessidades dos professores.

Eventuais cenários e dados simulados devem ser identificados explicitamente como fictícios. Eles podem ser utilizados para ilustrar situações de uso ou organizar a documentação, mas não devem ser apresentados como resultados de pesquisa com participantes reais.

**Status atual:** requisitos em revisão documental. A implementação, os testes de software, as atividades de QA e a validação empírica das hipóteses não são considerados concluídos nem fazem parte desta etapa.
