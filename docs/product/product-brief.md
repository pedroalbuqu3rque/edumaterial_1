# EduMaterial — Product Brief

**Versão:** 0.3  
**Status:** Em revisão documental  
**Tipo de projeto:** Estudo de caso de planejamento de produto digital educacional

## 1. Visão do produto

O EduMaterial é uma proposta de plataforma digital destinada a facilitar a descoberta, a seleção e o acesso a materiais didáticos por professores.

A plataforma pretende reunir recursos educacionais em um catálogo organizado, permitindo que os usuários explorem materiais, pesquisem por palavras-chave, apliquem filtros e consultem informações que auxiliem na avaliação inicial dos recursos.

O acesso poderá ocorrer por meio de links externos, arquivos hospedados diretamente na plataforma ou ambas as opções, conforme a disponibilidade de cada material.

O MVP concentra-se em localizar, compreender e acessar recursos. Não contempla pré-visualização de conteúdo dentro da plataforma nem funcionalidades de criação, edição ou adaptação dos materiais.

## 2. Problema

Professores que procuram materiais didáticos podem precisar consultar diferentes fontes para localizar recursos relacionados aos conteúdos e objetivos de suas aulas.

A organização de materiais em um catálogo com pesquisa, filtros e informações descritivas é proposta como uma possível forma de facilitar essa procura.

Essa descrição constitui uma **hipótese de produto**, não um problema comprovado por pesquisa empírica. A coleta de respostas pelo Google Forms foi abandonada, e não há resultados desse questionário que permitam afirmar a frequência, a intensidade ou os efeitos dessa dificuldade.

O problema orienta o planejamento inicial, mas permanece pendente de validação com o público prioritário.

## 3. Público-alvo

### 3.1. Público prioritário

Professores que procuram materiais didáticos para utilizar em suas aulas.

A proposta considera que esses usuários precisam localizar recursos, compreender suas características e identificar as formas disponíveis de acesso.

### 3.2. Público secundário

Outros profissionais da educação que procuram recursos para atividades educacionais poderão se beneficiar da plataforma. Entretanto, esse público não constitui a prioridade para a definição do MVP.

A criação, o envio e a publicação de materiais por usuários não fazem parte do escopo inicial.

## 4. Objetivo do produto

Planejar uma plataforma que facilite a descoberta e a seleção de materiais didáticos por meio de um catálogo organizado, mecanismos de pesquisa e filtragem e informações sobre os recursos disponíveis.

No MVP, o professor deverá conseguir:

1. Explorar o catálogo;
2. Pesquisar materiais por palavras-chave;
3. Refinar os resultados por tipo de material e etapa de ensino;
4. Consultar os detalhes de um material;
5. Identificar as formas de acesso disponíveis;
6. Acessar o recurso por link externo, arquivo hospedado na plataforma ou ambas as opções, quando disponíveis.

## 5. Proposta de valor

O EduMaterial propõe reunir, em um único ambiente, informações organizadas sobre materiais didáticos e as formas de acesso a esses recursos.

A proposta de valor consiste em facilitar a descoberta e a avaliação inicial de materiais, oferecendo uma estrutura comum para explorar, comparar e acessar os recursos cadastrados.

Esse benefício é esperado, mas ainda não foi demonstrado por testes de usabilidade ou pesquisa com usuários reais.

## 6. Escopo do MVP

### 6.1. Catálogo de materiais

Apresentar os materiais cadastrados de forma organizada, com informações resumidas que permitam identificá-los e iniciar a avaliação de sua adequação.

O comportamento do catálogo deverá considerar tanto a existência de materiais quanto a possibilidade de o catálogo estar vazio.

### 6.2. Pesquisa por palavras-chave

Permitir que o professor informe palavras ou expressões relacionadas ao material procurado.

Os campos considerados na pesquisa e as regras de correspondência ainda precisam ser definidos.

### 6.3. Filtros

Permitir o refinamento dos materiais por tipo de material e etapa de ensino.

As opções disponíveis em cada filtro e o comportamento da combinação entre filtros e pesquisa permanecem pendentes de especificação.

### 6.4. Detalhes do material

Apresentar informações que ajudem o professor a compreender o recurso antes de acessá-lo. Os campos propostos incluem título, tipo, etapa de ensino, resumo, descrição, orientações de uso, autoria ou fonte e condições de utilização, quando conhecidas.

A obrigatoriedade de cada campo ainda precisa ser definida.

### 6.5. Acesso aos materiais

Apresentar as formas de acesso cadastradas para cada recurso:

- Link externo;
- Arquivo hospedado diretamente na plataforma;
- Link e arquivo, quando ambas as opções estiverem disponíveis.

Quando não houver uma forma de acesso cadastrada, a interface deverá informar essa condição sem apresentar uma ação indisponível como se fosse funcional.

O tratamento específico de links ou arquivos que falhem ao abrir permanece pendente.

### 6.6. Estados informativos

A experiência deverá contemplar, no mínimo, os seguintes estados:

- Catálogo vazio;
- Pesquisa ou filtragem sem resultados;
- Material sem forma de acesso cadastrada.

O tratamento de falhas de acesso será detalhado posteriormente.

## 7. Fora do escopo do MVP

Não fazem parte da versão inicial planejada:

- Pré-visualização de materiais dentro da plataforma;
- Edição ou adaptação de materiais;
- Criação de materiais pelos usuários;
- Envio e publicação de materiais por usuários;
- Validação de hipóteses por meio de resultados de pesquisa ainda inexistentes;
- Funcionalidades não documentadas ou não aprovadas no escopo atual.

## 8. Princípios do produto

- **Clareza:** as informações e as ações devem ser compreensíveis.
- **Organização:** os materiais devem seguir uma estrutura consistente.
- **Descoberta:** o usuário deve poder explorar o catálogo, pesquisar e filtrar.
- **Transparência:** as formas de acesso e suas limitações devem ser explícitas.
- **Consistência:** requisitos, histórias de usuário, arquitetura e fluxos devem representar o mesmo comportamento.
- **Integridade metodológica:** hipóteses e exemplos simulados não devem ser apresentados como evidências empíricas.

## 9. Decisões, hipóteses e pendências

### 9.1. Decisões confirmadas

- O público prioritário são professores que procuram materiais para suas aulas.
- O MVP contempla catálogo, pesquisa, filtros, detalhes e acesso aos recursos.
- Os filtros previstos são tipo de material e etapa de ensino.
- O acesso poderá ocorrer por links externos, arquivos hospedados na plataforma ou ambas as opções.
- A pré-visualização e a edição de materiais não fazem parte do MVP.
- O projeto está em fase de revisão documental.

### 9.2. Hipóteses

- Professores podem enfrentar dificuldades para localizar materiais adequados ao planejamento de suas aulas.
- Um catálogo organizado pode facilitar a descoberta e a comparação inicial de recursos.
- Informações claras sobre os materiais e suas formas de acesso podem ajudar na seleção.

Essas hipóteses ainda não foram validadas por pesquisa com usuários reais.

### 9.3. Pendências

- Definir os campos pesquisáveis e as regras de correspondência.
- Definir as opções de cada filtro.
- Definir como pesquisa e filtros serão combinados.
- Definir os campos obrigatórios e opcionais dos materiais.
- Definir os formatos de arquivo aceitos.
- Definir como serão apresentadas autoria, fonte e condições de utilização.
- Definir o comportamento esperado quando links ou arquivos estiverem indisponíveis.

## 10. Etapas futuras

Após a consolidação documental, o projeto poderá avançar para atividades de prototipação, implementação e avaliação, conforme as decisões futuras.

Essas etapas não fazem parte do trabalho atual. Nenhuma funcionalidade deve ser descrita como implementada ou validada sem evidências correspondentes.

## 11. Documentos relacionados

- [`requisitos.md`](./requisitos.md)
- [`historias-de-usuario.md`](./historias-de-usuario.md)
- [`arquitetura-da-informacao.md`](../ux-ui/arquitetura-da-informacao.md)
- [`user-flow.md`](../ux-ui/user-flow.md)
- [`objetivos-de-ux.md`](../ux-ui/objetivos-de-ux.md)
- [`design-system.md`](../ux-ui/design-system.md)
