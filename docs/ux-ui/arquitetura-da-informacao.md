# Arquitetura da Informação — EduMaterial

**Versão:** 0.3  
**Status:** Em revisão documental

## 1. Objetivo

Definir como os materiais educacionais são organizados, apresentados e acessados no EduMaterial.

A arquitetura da informação busca tornar a navegação compreensível, facilitar a localização de recursos educacionais e ajudar o usuário a identificar como cada material pode ser acessado.

Esta proposta está alinhada ao escopo atual do MVP, centrado na descoberta, consulta e acesso aos materiais, sem incluir funcionalidades de visualização prévia, edição, adaptação ou envio de recursos pelos usuários.

## 2. Público e necessidades de informação

O público prioritário do EduMaterial é formado por professores que procuram materiais para preparar, complementar ou desenvolver suas aulas.

Durante a navegação, o usuário deve conseguir:

- Descobrir quais materiais estão disponíveis.
- Pesquisar recursos por palavras-chave.
- Refinar os resultados por tipo de material e etapa de ensino.
- Compreender o conteúdo e a finalidade de um recurso.
- Identificar as formas de acesso disponíveis.
- Retornar aos resultados e continuar a busca quando necessário.

A organização das informações deve apoiar essas necessidades sem pressupor que todos os materiais possuem os mesmos metadados ou formas de acesso.

## 3. Estrutura geral

O MVP está organizado em três áreas principais:

1. **Catálogo:** apresenta os materiais disponíveis e permite explorar, pesquisar e filtrar os recursos.
2. **Resultados da busca:** apresenta os materiais correspondentes à consulta e aos filtros aplicados.
3. **Detalhes do material:** reúne as informações de um recurso específico e apresenta as formas de acesso disponíveis.

Os estados de carregamento, catálogo vazio, ausência de resultados e falha de acesso complementam essas áreas e devem ser tratados como parte da experiência de navegação.

## 4. Hierarquia de navegação

```text
EduMaterial
│
└── Catálogo
    ├── Campo de pesquisa
    ├── Filtros
    │   ├── Tipo de material
    │   └── Etapa de ensino
    ├── Lista de materiais
    │   └── Selecionar material
    │       └── Detalhes do material
    │           ├── Título
    │           ├── Tipo de material
    │           ├── Etapa de ensino
    │           ├── Resumo
    │           ├── Descrição
    │           ├── Orientações de uso, quando disponíveis
    │           └── Formas de acesso
    │               ├── Link externo, quando disponível
    │               ├── Arquivo hospedado, quando disponível
    │               ├── Link e arquivo, quando ambos existirem
    │               └── Informações sem ação de acesso,
    │                   quando não houver acesso disponível
    │
    └── Estados da interface
        ├── Catálogo vazio
        ├── Carregamento
        ├── Resultados encontrados
        ├── Pesquisa sem resultados
        └── Erro de carregamento ou acesso
```

A hierarquia representa a organização conceitual proposta para o MVP. Ela não determina, por si só, se cada área será implementada como uma página independente ou como um estado de uma mesma página.

## 5. Organização e metadados dos materiais

Cada material deve possuir informações suficientes para que o usuário possa identificá-lo e avaliar sua pertinência.

| Informação | Finalidade |
|---|---|
| Título | Identificar o recurso e facilitar sua localização. |
| Tipo de material | Informar a categoria do recurso e permitir filtragem. |
| Etapa de ensino | Indicar a etapa educacional à qual o material se destina, quando essa informação estiver disponível. |
| Resumo | Apresentar rapidamente a proposta do material. |
| Descrição | Explicar o conteúdo e a finalidade do recurso. |
| Orientações de uso | Apoiar a compreensão de como utilizar o material, quando disponíveis. |
| Link externo | Direcionar o usuário à fonte externa, quando disponível. |
| Arquivo hospedado | Permitir o acesso ao arquivo disponibilizado diretamente na plataforma, quando disponível. |
| Informações de autoria e origem | Ajudar a identificar a procedência do material, conforme os metadados definidos para o cadastro. |
| Condições de uso | Informar licenças ou restrições conhecidas, quando aplicáveis e disponíveis. |

A definição dos campos obrigatórios, dos campos opcionais e das regras para informações ausentes deverá ser consolidada na especificação dos requisitos e do modelo de dados.

A interface não deve inventar informações nem apresentar campos opcionais como se estivessem preenchidos quando os dados não estiverem disponíveis.

## 6. Catálogo e apresentação dos resultados

O catálogo deve apresentar os materiais disponíveis de forma organizada e permitir que o usuário identifique os recursos antes de abrir seus detalhes.

A apresentação de cada item deve priorizar informações que facilitem a identificação e a seleção do material, especialmente título, tipo e etapa de ensino, conforme a disponibilidade desses dados.

A ordenação dos resultados da busca deve seguir a relevância da correspondência com os termos pesquisados.

A fórmula exata de pontuação e os critérios de desempate ainda precisam ser definidos. A arquitetura da informação não estabelece uma fórmula própria, devendo respeitar as regras funcionais consolidadas nos requisitos.

A interface deverá distinguir os seguintes estados:

- **Catálogo inicial:** apresenta os materiais disponíveis sem uma pesquisa ativa.
- **Resultados encontrados:** apresenta os materiais correspondentes à pesquisa e aos filtros.
- **Pesquisa sem resultados:** informa que nenhum material corresponde aos critérios utilizados e permite ajustar a pesquisa ou os filtros.
- **Catálogo vazio:** informa que não há materiais cadastrados ou disponíveis para exibição, quando essa for a situação real.

O estado de catálogo vazio não deve ser confundido com uma pesquisa sem resultados: são situações diferentes e podem exigir orientações distintas.

## 7. Pesquisa e filtros

### 7.1 Campos pesquisáveis

A pesquisa por palavras-chave deverá considerar os seguintes campos:

1. Título.
2. Tipo de material.
3. Resumo.
4. Descrição.

A prioridade de relevância definida para a busca é:

1. Título.
2. Tipo de material.
3. Resumo.
4. Descrição.

### 7.2 Comportamento esperado da busca

A interface deverá refletir as seguintes regras funcionais:

- Ignorar diferenças entre letras maiúsculas e minúsculas.
- Ignorar diferenças de acentuação.
- Aceitar correspondências parciais.
- Apresentar os resultados em ordem de relevância.

Por exemplo, uma pesquisa por `historia` deve poder localizar materiais que contenham `história`, e uma pesquisa por `geog` deve poder localizar materiais que contenham `geografia`.

Esses exemplos descrevem o comportamento esperado e não comprovam que ele já esteja implementado.

### 7.3 Filtros

Os filtros previstos para o MVP são:

- Tipo de material.
- Etapa de ensino.

A interface deverá indicar quais filtros estão disponíveis e permitir que o usuário compreenda quais critérios estão restringindo os resultados.

A combinação de múltiplos filtros, a remoção individual ou conjunta de critérios e a interação entre filtros e pesquisa devem seguir as regras funcionais que forem definidas nos requisitos.

Quando a combinação dos critérios não produzir resultados, a interface deverá apresentar um estado sem resultados que permita ao usuário revisar a consulta e os filtros aplicados.

## 8. Detalhes do material

A área de detalhes deve reunir as informações necessárias para que o usuário compreenda o recurso selecionado e identifique como acessá-lo.

A apresentação deverá priorizar:

- Título.
- Tipo de material.
- Etapa de ensino, quando disponível.
- Resumo.
- Descrição.
- Orientações de uso, quando disponíveis.
- Informações de autoria, origem e condições de uso, quando disponíveis e previstas nos metadados.
- Formas de acesso efetivamente disponíveis.

A página de detalhes não implica a existência de uma visualização prévia do conteúdo do arquivo. No escopo atual, sua função é apresentar as informações do material e as opções de acesso existentes.

O usuário deve conseguir retornar ao catálogo ou aos resultados depois de consultar um material.

## 9. Formas de acesso aos materiais

O EduMaterial deverá representar corretamente as diferentes situações de disponibilidade de acesso.

| Situação | Organização e comportamento esperado |
|---|---|
| Link externo disponível, sem arquivo hospedado | Apresentar uma ação para abrir a fonte externa. |
| Arquivo hospedado, sem link externo | Apresentar uma ação para acessar ou baixar o arquivo, conforme o comportamento definido para a plataforma. |
| Link externo e arquivo hospedado disponíveis | Apresentar as duas opções, identificando claramente cada uma. |
| Nenhuma forma de acesso disponível | Exibir as informações do material sem apresentar uma ação de acesso inexistente. |

As opções devem ser identificadas de maneira clara, para que o usuário saiba se será direcionado a um site externo ou se acessará um arquivo hospedado na plataforma.

A presença de um link ou arquivo cadastrado não garante que o recurso esteja sempre acessível. Se ocorrer uma falha, a interface deverá informar o problema sem sugerir que o acesso foi bem-sucedido.

## 10. Navegação entre áreas

O usuário deverá conseguir:

- Acessar o catálogo.
- Pesquisar materiais.
- Aplicar e revisar filtros.
- Abrir um material a partir do catálogo ou dos resultados.
- Consultar os detalhes do material selecionado.
- Identificar as opções de acesso disponíveis.
- Retornar à lista de materiais.
- Ajustar a pesquisa ou os filtros quando não encontrar resultados.
- Compreender quando uma tentativa de acesso falhar.

A navegação deve manter uma relação clara entre a lista de materiais e os detalhes do item selecionado.

A preservação da consulta e dos filtros ao retornar à lista é um comportamento desejável, mas precisa ser confirmado como requisito antes de ser tratado como uma regra obrigatória de implementação.

## 11. Estados da interface

A arquitetura deve contemplar os principais estados necessários para uma experiência compreensível.

| Estado | Comportamento esperado |
|---|---|
| Carregamento | Indicar que o conteúdo está sendo carregado, quando houver uma operação que justifique essa indicação. |
| Catálogo vazio | Informar que não existem materiais disponíveis para exibição. |
| Resultados encontrados | Apresentar os materiais correspondentes aos critérios utilizados. |
| Pesquisa sem resultados | Informar a ausência de correspondências e permitir revisar a consulta ou os filtros. |
| Detalhes do material | Apresentar as informações disponíveis e as opções de acesso. |
| Acesso indisponível | Informar que não existe uma forma de acesso cadastrada para o material. |
| Falha ao abrir um recurso | Informar que houve um problema e, quando possível, permitir uma nova tentativa. |
| Dados incompletos | Apresentar as informações disponíveis sem inventar ou presumir dados ausentes. |

As mensagens e as ações específicas de cada estado deverão ser detalhadas durante a especificação da interface.

## 12. Responsividade e acessibilidade

A organização da informação deverá permanecer compreensível em diferentes tamanhos de tela.

A interface deve considerar:

- Hierarquia visual clara entre título, informações complementares e ações.
- Identificação compreensível dos campos de pesquisa e dos filtros.
- Textos e controles legíveis em dispositivos móveis.
- Distinção entre links externos, arquivos e informações descritivas.
- Mensagens de erro e estados vazios compreensíveis.
- Navegação e controles acessíveis, conforme os critérios de acessibilidade a serem especificados.

Essas diretrizes representam objetivos de projeto. Sua conformidade deverá ser verificada em etapas futuras de design, implementação e avaliação.

## 13. Limites da arquitetura

A arquitetura proposta contempla a descoberta, a consulta e o acesso aos materiais educacionais.

Não fazem parte do MVP atual:

- Visualização prévia do conteúdo dos materiais dentro da plataforma.
- Edição de materiais.
- Adaptação de materiais pelos usuários.
- Envio de arquivos pelos usuários.
- Criação de materiais dentro da plataforma.

Essas funcionalidades não devem ser incluídas nos fluxos principais sem uma decisão explícita de ampliação do escopo.

## 14. Questões pendentes

As seguintes questões ainda precisam ser resolvidas ou detalhadas:

- Quais campos serão obrigatórios no cadastro de cada material?
- Quais metadados complementares serão adotados?
- Como serão definidas e apresentadas as opções dos filtros?
- Como a busca interagirá com filtros combinados?
- Como serão calculadas as pontuações de relevância e tratados os empates?
- A consulta e os filtros serão preservados ao retornar dos detalhes?
- Quais formatos de arquivo e limites de tamanho serão aceitos?
- Como serão tratadas falhas de carregamento, arquivos inválidos e links externos indisponíveis?
- Quais critérios específicos de acessibilidade serão utilizados para avaliar a interface?

Essas pendências devem ser resolvidas em conjunto com os documentos de requisitos, histórias de usuário, fluxo de navegação e backlog.

## 15. Relação com os demais documentos

Esta arquitetura deve permanecer alinhada aos seguintes arquivos:

- `README.md`: apresentação geral e escopo do projeto.
- `docs/product/product-brief.md`: visão, objetivos e limites do produto.
- `docs/product/requisitos.md`: requisitos funcionais e não funcionais.
- `docs/product/historias-de-usuario.md`: necessidades dos usuários e critérios de aceitação.
- `docs/product/backlog.md`: tarefas, prioridades e andamento.
- `docs/ux-ui/objetivos-de-ux.md`: objetivos da experiência de uso.
- `docs/ux-ui/design-system.md`: diretrizes visuais e componentes.
- `docs/ux-ui/user-flow.md`: fluxos de navegação e acesso.

Quando houver mudanças nos requisitos, as informações, os estados e os fluxos relacionados deverão ser revisados para manter a consistência documental.

## 16. Considerações metodológicas

Este documento descreve a arquitetura proposta para o MVP, não uma arquitetura cuja implementação já tenha sido verificada.

A revisão documental atual não comprova que as funcionalidades estejam implementadas, que a navegação tenha sido testada ou que as hipóteses de produto tenham sido validadas com professores.

Dados simulados podem ser utilizados para ilustrar cenários de funcionamento, mas não devem ser apresentados como evidência de pesquisa com usuários reais.

A arquitetura deverá ser revisitada quando houver decisões funcionais adicionais, protótipos, implementação ou resultados de avaliações futuras.
