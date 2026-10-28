# EduMaterial — Product Brief

**Versão:** 0.2  
**Status:** Proposta documental revisada  
**Tipo de projeto:** Estudo de caso de planejamento de produto digital educacional

## 1. Visão do produto

O EduMaterial é uma proposta de plataforma digital destinada a facilitar a descoberta e a seleção de materiais didáticos por professores.

A plataforma pretende reunir recursos educacionais em um catálogo organizado, permitindo que os professores pesquisem materiais, refinem os resultados de acordo com características relevantes e consultem informações que auxiliem na escolha dos recursos para suas aulas.

O acesso aos materiais deverá ocorrer por meio de links externos ou de arquivos disponibilizados diretamente na plataforma.

O foco do MVP é facilitar a localização, a avaliação inicial e o acesso aos recursos, sem incluir funcionalidades de visualização prévia, edição ou adaptação de materiais dentro da plataforma.

## 2. Problema

Professores que procuram materiais didáticos podem precisar consultar diferentes fontes para localizar recursos adequados aos conteúdos e objetivos de suas aulas.

A centralização dos materiais em um catálogo com busca, filtros e informações descritivas é proposta como uma possível forma de facilitar esse processo.

Entretanto, essa descrição constitui uma **hipótese de produto**, e não um problema comprovado por pesquisa empírica. A coleta de respostas por meio do Google Forms foi abandonada, e não há resultados de uma pesquisa com professores que permitam afirmar a frequência, a intensidade ou os efeitos dessa dificuldade.

Assim, o problema orienta o planejamento inicial do EduMaterial, mas permanece pendente de validação com o público prioritário.

## 3. Público-alvo

### Público prioritário

Professores que procuram materiais didáticos para utilizar em suas aulas.

A proposta considera que esses usuários precisam localizar recursos, compreender suas características e identificar como acessá-los.

### Público secundário

Outros profissionais da educação que também procuram materiais para atividades educacionais poderão se beneficiar da plataforma. Entretanto, esse público não constitui a prioridade para a definição do MVP.

A produção, o envio e a publicação de materiais por usuários não fazem parte do escopo inicial.

## 4. Objetivo do produto

Facilitar a descoberta e a seleção de materiais didáticos por professores, oferecendo um catálogo organizado, mecanismos de pesquisa e filtragem e informações sobre os recursos disponíveis.

O objetivo funcional do MVP é permitir que o professor:

1. Explore o catálogo de materiais.
2. Pesquise recursos por palavras-chave.
3. Refine os resultados por tipo de material e etapa de ensino.
4. Consulte as informações de um material específico.
5. Acesse o recurso por meio de um link externo ou de um arquivo disponibilizado na plataforma, quando houver uma forma de acesso cadastrada.

## 5. Proposta de valor

O EduMaterial propõe reunir, em um único ambiente, informações sobre materiais didáticos e formas de acesso aos recursos.

A proposta de valor está na possibilidade de facilitar a descoberta e a seleção de materiais por meio de um catálogo estruturado, reduzindo a necessidade de procurar e comparar recursos sem uma organização comum.

Esse benefício é esperado, mas ainda não foi demonstrado por testes ou por pesquisa com usuários reais.

## 6. Escopo do MVP

O MVP deverá contemplar as seguintes funcionalidades.

### 6.1. Catálogo de materiais

Apresentar os materiais disponíveis de forma organizada, com informações suficientes para identificá-los e iniciar a avaliação de sua adequação.

### 6.2. Busca por palavras-chave

Permitir que o professor pesquise materiais utilizando palavras ou expressões relacionadas ao recurso procurado.

Os campos considerados na pesquisa e as regras de correspondência dos termos ainda precisam ser definidos.

### 6.3. Filtros

Permitir o refinamento dos resultados por:

- Tipo de material.
- Etapa de ensino.

Os valores disponíveis para cada filtro e o comportamento combinado entre busca e filtros permanecem pendentes de especificação.

### 6.4. Detalhes do material

Apresentar informações descritivas que ajudem o professor a compreender as características do recurso e avaliar sua possível adequação à aula.

Os campos obrigatórios e opcionais deverão ser definidos de maneira consistente com a arquitetura da informação e os requisitos funcionais.

### 6.5. Acesso aos materiais

Disponibilizar uma forma de acesso ao recurso por meio de:

- Link externo para o material.
- Arquivo disponibilizado diretamente na plataforma.

A existência de uma dessas formas de acesso dependerá do cadastro de cada material. O sistema deverá distinguir os recursos acessíveis daqueles que não possuem um endereço ou arquivo disponível.

As regras para formatos de arquivo, limites de armazenamento, condições de uso e tratamento de recursos indisponíveis ainda precisam ser especificadas.

### 6.6. Funcionalidades fora do MVP

Não fazem parte do escopo inicial:

- Visualização prévia do material dentro da plataforma.
- Edição ou adaptação de materiais na própria plataforma.
- Publicação de materiais por usuários.
- Autenticação e contas de usuário.
- Favoritos e coleções pessoais.
- Recomendações automatizadas de materiais.

A visualização prévia poderá ser considerada em uma versão futura, após a avaliação das necessidades do produto e das prioridades de evolução.

## 7. Princípios do produto

### 7.1. Autonomia docente

A plataforma deve apoiar a escolha dos professores, fornecendo informações para que possam avaliar quais recursos são adequados aos seus objetivos pedagógicos.

### 7.2. Facilidade de descoberta

A organização do catálogo, a busca e os filtros devem favorecer a localização de materiais de maneira clara e compreensível.

### 7.3. Transparência das informações

As informações disponíveis sobre o material, sua origem, autoria e condições de uso devem ser apresentadas com clareza, conforme os dados efetivamente cadastrados e disponíveis.

### 7.4. Clareza no acesso

O professor deve conseguir identificar se o material está disponível por link externo, por arquivo hospedado na plataforma ou se não possui uma forma de acesso cadastrada.

### 7.5. Coerência de escopo

As funcionalidades e os critérios documentados devem corresponder ao escopo definido para o MVP. Possibilidades de evolução futura não devem ser descritas como funcionalidades da primeira versão.

## 8. Premissas, hipóteses e limitações

### 8.1. Decisões confirmadas

- O público prioritário é formado por professores que procuram materiais para suas aulas.
- O produto terá um catálogo de materiais didáticos.
- A busca por palavras-chave fará parte do MVP.
- Os filtros por tipo de material e etapa de ensino farão parte do MVP.
- Os materiais terão uma página ou seção de detalhes.
- O acesso poderá ocorrer por links externos ou arquivos disponibilizados diretamente na plataforma.
- A visualização prévia não fará parte do MVP.
- A implementação e as atividades de QA não fazem parte da etapa atual de revisão documental.

### 8.2. Hipóteses de produto

- Professores podem encontrar dificuldades ao procurar materiais em diferentes fontes.
- Um catálogo organizado pode facilitar a descoberta de recursos.
- A busca por palavras-chave pode ajudar a localizar materiais relacionados a determinados conteúdos.
- Os filtros por tipo de material e etapa de ensino podem facilitar a seleção.
- Informações descritivas podem ajudar os professores a avaliar a adequação de um recurso antes de acessá-lo.

Essas hipóteses orientam a proposta, mas não devem ser tratadas como conclusões comprovadas.

### 8.3. Pendências de definição

- Campos obrigatórios e opcionais do cadastro de materiais.
- Campos considerados na pesquisa por palavras-chave.
- Regras de combinação entre busca e filtros.
- Valores disponíveis nos filtros.
- Formatos de arquivos aceitos e limites aplicáveis.
- Regras de armazenamento e disponibilização dos arquivos.
- Informações necessárias sobre autoria, origem, licença e condições de uso.
- Comportamento esperado quando um link ou arquivo estiver indisponível.
- Critérios para inclusão, revisão e retirada de materiais do catálogo.

Essas pendências deverão ser resolvidas na documentação correspondente antes de serem tratadas como requisitos definidos.

### 8.4. Limitações metodológicas

O projeto é desenvolvido como um estudo de caso de planejamento de produto digital.

A coleta de respostas por meio do Google Forms foi abandonada. Portanto, não há resultados desse questionário que possam ser utilizados como evidência empírica sobre as necessidades ou os comportamentos do público.

Eventuais dados simulados e cenários fictícios devem ser identificados como tais. Eles podem apoiar exercícios de estruturação e análise do produto, mas não podem ser apresentados como respostas de participantes reais nem como validação das hipóteses.

## 9. Etapas do projeto

O projeto está organizado em etapas, que não devem ser interpretadas como atividades já concluídas.

1. **Definição do problema e do público:** estruturação da proposta inicial e registro das hipóteses.
2. **Documentação do produto:** consolidação da visão, dos requisitos, das histórias de usuário e das prioridades do MVP.
3. **Planejamento de UX/UI:** organização da arquitetura da informação, dos fluxos de uso, dos objetivos de UX e das diretrizes visuais.
4. **Implementação futura:** desenvolvimento da aplicação conforme o escopo e os requisitos consolidados.
5. **QA e avaliação futura:** verificação dos comportamentos implementados e avaliação dos critérios de aceitação.
6. **Documentação dos resultados:** registro das atividades efetivamente realizadas e dos resultados obtidos.

### Etapa atual

O trabalho está concentrado na revisão e consolidação da documentação de produto e UX/UI. A implementação, a execução de testes e a validação empírica das hipóteses não são consideradas concluídas nem fazem parte da atividade documental atual.

## 10. Relação com os demais documentos

Este Product Brief deve permanecer alinhado aos seguintes documentos:

- [`historias-de-usuario.md`](./historias-de-usuario.md): descreve as necessidades dos usuários e os critérios de aceitação das funcionalidades.
- [`requisitos.md`](./requisitos.md): especifica os requisitos funcionais, não funcionais e as limitações do MVP.
- [`arquitetura-da-informacao.md`](../ux-ui/arquitetura-da-informacao.md): organiza as informações e as áreas da plataforma.
- [`objetivos-de-ux.md`](../ux-ui/objetivos-de-ux.md): descreve os objetivos de experiência propostos.
- [`user-flow.md`](../ux-ui/user-flow.md): representa os caminhos previstos para a interação com o produto.
- [`design-system.md`](../ux-ui/design-system.md): registra as diretrizes visuais e os componentes previstos.

Caso uma decisão de escopo seja alterada, os documentos relacionados deverão ser revisados para evitar contradições.
