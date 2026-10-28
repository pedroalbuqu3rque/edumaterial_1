# EduMaterial — Product Brief

**Versão:** 0.3  
**Status:** Em revisão documental  
**Tipo de projeto:** Projeto de estudo de caso para Product Ownership e documentação de produto

## 1. Visão do produto

O EduMaterial é uma proposta de plataforma digital para facilitar a descoberta e a consulta de materiais educacionais, especialmente por professores que buscam recursos para preparar e desenvolver suas aulas.

A plataforma pretende reunir materiais em um catálogo organizado, permitindo que os usuários pesquisem por palavras-chave, refinem os resultados por filtros, consultem informações sobre cada recurso e acessem o conteúdo quando houver uma forma de acesso disponível.

O EduMaterial busca simplificar a localização de recursos educacionais sem pressupor que todos os materiais possam ser visualizados, baixados ou modificados diretamente na plataforma.

## 2. Problema

Professores que procuram materiais para suas aulas podem precisar consultar diferentes fontes até encontrar recursos adequados aos seus objetivos pedagógicos e contextos de ensino.

A dificuldade de localizar, comparar e acessar materiais relevantes é a hipótese de problema que orienta este projeto.

Essa hipótese ainda não foi validada por uma pesquisa com usuários reais. Portanto, não deve ser tratada como uma conclusão comprovada sobre o comportamento ou as necessidades dos professores.

## 3. Público-alvo

### Público prioritário

- Professores que procuram materiais educacionais para preparar, complementar ou desenvolver suas aulas.

### Público secundário

- Pessoas envolvidas na produção de materiais para atividades, oficinas e outras ações educacionais.

O desenvolvimento inicial será orientado principalmente pelas necessidades de descoberta e acesso a materiais do público prioritário.

## 4. Objetivo do produto

Facilitar a descoberta, a seleção e o acesso a materiais educacionais relevantes, reduzindo o esforço necessário para localizar recursos que possam contribuir para o planejamento e a realização de aulas.

## 5. Proposta de valor

Oferecer um catálogo centralizado e organizado de materiais educacionais, com recursos de busca, filtragem e consulta de informações, permitindo que o usuário identifique opções relevantes e acesse os conteúdos disponíveis.

A plataforma deve informar com clareza como cada material pode ser acessado, distinguindo arquivos disponibilizados diretamente no EduMaterial de links para fontes externas.

## 6. Escopo do MVP

A primeira versão do produto será orientada à descoberta e ao acesso aos materiais educacionais.

### 6.1 Funcionalidades previstas

- **Catálogo de materiais:** apresentar os recursos educacionais disponíveis.
- **Busca por palavras-chave:** permitir pesquisas nos campos definidos para o MVP.
- **Ordenação por relevância:** priorizar os resultados de acordo com a correspondência entre a consulta e as informações de cada material.
- **Filtros:** permitir o refinamento dos resultados por tipo de material e etapa de ensino.
- **Detalhes do material:** apresentar informações que ajudem o usuário a compreender e selecionar o recurso.
- **Acesso por link externo:** direcionar o usuário à fonte externa quando houver um link disponível.
- **Acesso a arquivo hospedado:** disponibilizar o arquivo diretamente quando houver um arquivo hospedado na plataforma.
- **Estados de interface:** apresentar mensagens adequadas quando não houver resultados ou quando ocorrer uma falha de acesso.

### 6.2 Regras definidas para a busca

A busca do MVP deverá considerar os seguintes campos:

1. Título.
2. Tipo de material.
3. Resumo.
4. Descrição.

O comportamento esperado é:

- Ignorar diferenças entre letras maiúsculas e minúsculas.
- Ignorar diferenças de acentuação.
- Aceitar correspondências parciais entre os termos pesquisados e o conteúdo dos campos.
- Ordenar os resultados por relevância.
- Priorizar correspondências no título, seguidas pelo tipo de material, pelo resumo e, por último, pela descrição.

A fórmula exata de pontuação da relevância, os critérios de desempate e o tratamento de consultas com múltiplas palavras permanecem pendentes de definição.

### 6.3 Formas de acesso aos materiais

Cada material poderá apresentar uma das seguintes situações:

| Situação | Comportamento esperado |
|---|---|
| Link externo disponível, sem arquivo hospedado | Permitir acesso à fonte externa. |
| Arquivo hospedado, sem link externo | Permitir acesso ao arquivo disponibilizado na plataforma. |
| Link externo e arquivo hospedado disponíveis | Apresentar as duas possibilidades de acesso. |
| Nenhuma forma de acesso disponível | Apresentar as informações do material sem oferecer uma ação de acesso indisponível. |

A disponibilidade de uma forma de acesso não garante que a fonte externa continuará ativa ou que o conteúdo estará sempre acessível. Falhas de acesso devem ser tratadas de maneira clara para o usuário.

## 7. Informações dos materiais

O catálogo e a página de detalhes deverão apresentar informações suficientes para ajudar o usuário a identificar e avaliar a pertinência de cada recurso.

Os campos previstos incluem:

- Título.
- Descrição.
- Resumo.
- Tipo de material.
- Etapa de ensino.
- Informações de acesso, conforme a disponibilidade de link externo ou arquivo hospedado.

A definição dos campos obrigatórios, dos metadados complementares e das informações sobre autoria, origem e condições de uso ainda poderá ser refinada durante a especificação do produto.

Não se deve presumir que todos os materiais terão todos os campos preenchidos ou que todos permitirão download ou reutilização.

## 8. Funcionalidades fora do escopo atual

Não fazem parte do MVP definido nesta etapa:

- Visualização prévia do conteúdo de um material diretamente na plataforma.
- Edição ou adaptação de materiais dentro do EduMaterial.
- Envio de arquivos pelos usuários.
- Criação de materiais pelos usuários dentro da plataforma.
- Validação de hipóteses por meio de pesquisa com usuários reais.

Essas possibilidades poderão ser avaliadas futuramente, caso haja justificativa e priorização explícitas. Não devem ser consideradas funcionalidades já comprometidas para a primeira versão.

## 9. Princípios do produto

### 9.1 Facilidade de descoberta

A organização do catálogo, a busca e os filtros devem ajudar o usuário a localizar recursos relevantes de maneira compreensível.

### 9.2 Autonomia docente

O EduMaterial deve apoiar o trabalho dos professores, oferecendo recursos para consulta e seleção sem substituir suas decisões pedagógicas.

### 9.3 Transparência

A interface deve deixar claro quais informações estão disponíveis, como cada material pode ser acessado e quais limitações existem.

### 9.4 Consistência

Os mesmos termos, critérios de busca, padrões de apresentação e comportamentos de interface devem ser utilizados de forma coerente em todo o produto.

### 9.5 Acessibilidade e responsividade

A experiência deve considerar diferentes dispositivos, tamanhos de tela e necessidades de acesso, conforme os requisitos de UX e os critérios técnicos que forem definidos.

### 9.6 Integridade metodológica

Decisões de produto devem distinguir requisitos confirmados, hipóteses de trabalho e questões ainda pendentes. Cenários e dados simulados não devem ser apresentados como resultados de pesquisas reais.

## 10. Premissas, decisões e pendências

### 10.1 Decisões confirmadas

- O público prioritário é formado por professores que procuram materiais para suas aulas.
- O MVP será centrado na descoberta, na consulta e no acesso aos materiais.
- A busca considerará título, tipo de material, resumo e descrição.
- A busca ignorará diferenças de caixa e acentuação e aceitará correspondências parciais.
- Os resultados serão ordenados por relevância, com prioridade para título, tipo de material, resumo e descrição, nessa ordem.
- Os filtros previstos incluem tipo de material e etapa de ensino.
- Os materiais poderão ser acessados por link externo, por arquivo hospedado, por ambos ou não apresentar uma forma de acesso disponível.
- A visualização prévia, a edição, a adaptação e o envio de materiais não fazem parte do MVP atual.
- A revisão em andamento é documental e não corresponde à implementação ou à validação do produto.

### 10.2 Hipóteses de trabalho

- Um catálogo centralizado poderá facilitar a localização de materiais educacionais.
- A busca e os filtros poderão reduzir o esforço necessário para encontrar recursos pertinentes.
- Informações claras sobre os materiais e suas formas de acesso poderão ajudar os professores a selecionar recursos mais adequados às suas necessidades.

Essas hipóteses ainda precisam de evidências apropriadas para serem validadas.

### 10.3 Questões pendentes

- Qual será a fórmula de pontuação utilizada para ordenar os resultados por relevância?
- Como serão tratados empates entre resultados com relevância equivalente?
- Como a busca tratará consultas compostas por várias palavras?
- Como a busca interagirá com os filtros selecionados?
- Quais campos serão obrigatórios no cadastro de um material?
- Quais informações sobre autoria, origem e condições de uso serão exibidas?
- Quais formatos de arquivo serão aceitos e quais serão os limites de tamanho?
- Como serão tratados links externos indisponíveis e arquivos que não puderem ser acessados?
- Quais requisitos técnicos de acessibilidade, segurança e desempenho serão adotados?

As questões pendentes deverão ser resolvidas antes das etapas de implementação que dependam dessas definições.

## 11. Etapas do projeto

O projeto será conduzido de forma incremental, respeitando o estágio atual de definição.

1. **Revisão documental:** alinhar a visão do produto, os requisitos, as histórias de usuário, a arquitetura da informação, o fluxo de navegação e os objetivos de UX.
2. **Consolidação dos requisitos:** resolver pendências relevantes e definir critérios de aceitação verificáveis.
3. **Design da experiência:** detalhar a interface e os estados previstos para os fluxos do MVP.
4. **Implementação futura:** desenvolver as funcionalidades priorizadas após a consolidação das definições.
5. **Testes futuros:** verificar o comportamento da aplicação em relação aos requisitos e critérios de aceitação.
6. **Avaliação futura:** caso seja realizada, conduzir uma avaliação com usuários reais e documentar método, participantes, resultados e limitações.
7. **Documentação e portfólio:** registrar decisões, mudanças, resultados e aprendizados do projeto.

As etapas de implementação, testes e avaliação são previstas para fases futuras. Não devem ser descritas como concluídas enquanto não forem efetivamente realizadas.

## 12. Contexto metodológico

O EduMaterial é desenvolvido como um projeto de estudo de caso para praticar documentação de produto, Product Ownership e fundamentos de desenvolvimento de software e Quality Assurance.

A pesquisa por meio de Google Forms foi abandonada, e os dados simulados utilizados no projeto servem apenas para exercitar análise, especificação e tomada de decisão.

Esses dados não representam respostas reais de participantes e não podem ser utilizados como evidência empírica sobre as necessidades, preferências ou comportamentos de professores.

Qualquer futura validação com usuários reais deverá ser conduzida e documentada separadamente.

## 13. Relação com os demais documentos

Este Product Brief deve permanecer alinhado aos seguintes documentos:

- `README.md`: apresentação geral do projeto e de seu escopo.
- `docs/product/requisitos.md`: requisitos funcionais e não funcionais.
- `docs/product/historias-de-usuario.md`: necessidades dos usuários e critérios de aceitação.
- `docs/product/backlog.md`: organização e priorização das atividades.
- `docs/ux-ui/arquitetura-da-informacao.md`: organização das informações e das páginas.
- `docs/ux-ui/user-flow.md`: fluxos de navegação e acesso.
- `docs/ux-ui/objetivos-de-ux.md`: objetivos da experiência do usuário.
- `docs/ux-ui/design-system.md`: diretrizes visuais e componentes de interface.

Quando uma decisão de escopo for alterada, os documentos relacionados deverão ser revisados para evitar contradições.
