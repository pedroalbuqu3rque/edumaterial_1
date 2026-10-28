# Arquitetura da Informação — EduMaterial

**Status:** Em revisão documental  
**Versão:** 0.4  
**Escopo:** MVP do EduMaterial

## 1. Objetivo

Definir como os materiais educacionais são organizados, apresentados, encontrados e acessados no EduMaterial.

A arquitetura da informação deve ajudar professores a localizar materiais relevantes para suas aulas, compreender as características de cada recurso e identificar claramente as possibilidades de acesso disponíveis.

Este documento descreve a estrutura proposta para o MVP. Não representa funcionalidades já implementadas ou validadas com usuários.

## 2. Princípios de organização

A arquitetura da informação segue os seguintes princípios:

- **Encontrabilidade:** facilitar a localização de materiais por pesquisa e filtros.
- **Clareza:** apresentar informações que ajudem o professor a entender o conteúdo e a finalidade do recurso.
- **Consistência:** utilizar uma estrutura coerente entre catálogo, resultados e detalhes.
- **Transparência de acesso:** informar se o material possui link externo, arquivo hospedado na plataforma, ambos ou nenhum dos dois.
- **Representação fiel dos dados:** não apresentar informações, formatos ou ações que não correspondam ao material cadastrado.
- **Simplicidade:** manter a navegação compatível com o escopo do MVP.

## 3. Estrutura geral

O MVP é organizado em três áreas principais:

1. **Catálogo:** apresenta os materiais disponíveis e permite explorar, pesquisar e filtrar os recursos.
2. **Resultados da pesquisa:** apresenta os materiais que correspondem aos termos pesquisados e aos filtros ativos.
3. **Detalhes do material:** reúne as informações de um recurso específico e apresenta as opções de acesso disponíveis.

Os resultados da pesquisa podem ser apresentados no próprio catálogo. A separação entre catálogo e resultados representa uma diferença de estado da interface, não necessariamente páginas distintas.

## 4. Hierarquia de navegação

```text
EduMaterial
│
└── Catálogo
    ├── Pesquisa
    ├── Filtros
    ├── Lista de materiais
    │   └── Selecionar material
    │       └── Detalhes do material
    │           ├── Título
    │           ├── Tipo de material
    │           ├── Etapa de ensino
    │           ├── Resumo
    │           ├── Descrição
    │           ├── Orientações de uso, quando disponíveis
    │           └── Opções de acesso
    │               ├── Link externo
    │               ├── Arquivo hospedado
    │               ├── Link externo e arquivo hospedado
    │               └── Nenhuma opção de acesso disponível
    │
    └── Estados da interface
        ├── Catálogo inicial
        ├── Resultados encontrados
        ├── Nenhum resultado
        ├── Carregamento
        ├── Falha ao carregar dados
        └── Falha ao acessar um material
```

Os estados de carregamento e falha são estados da interface, não áreas permanentes da navegação.

## 5. Organização e apresentação dos materiais

Cada material deve possuir um conjunto de metadados que permita identificá-lo, compreendê-lo e avaliar sua pertinência para uma aula.

| Informação | Finalidade | Situação |
|---|---|---|
| Título | Identificar o material | Campo central para identificação e pesquisa |
| Tipo de material | Indicar a categoria do recurso | Previsto |
| Resumo | Apresentar brevemente a proposta do material | Previsto |
| Descrição | Explicar o conteúdo e a finalidade do recurso | Previsto |
| Etapa de ensino | Indicar a etapa educacional à qual o recurso se destina | Previsto; obrigatoriedade a definir |
| Orientações de uso | Apoiar a compreensão de como utilizar o recurso | Quando disponíveis; obrigatoriedade a definir |
| Link externo | Permitir acessar um recurso em outro endereço | Opcional |
| Arquivo hospedado | Permitir acessar um arquivo disponibilizado pela plataforma | Opcional |

A tabela define a função dos campos, mas não estabelece que todos sejam obrigatórios. As regras definitivas de preenchimento, validação e exibição dos metadados permanecem pendentes.

### 5.1. Catálogo e resultados

Cada item apresentado no catálogo deve oferecer informações suficientes para que o professor reconheça o material e decida se deseja consultar seus detalhes.

A composição definitiva do cartão ou item de listagem ainda deve ser especificada. A seleção de informações precisa equilibrar identificação, legibilidade e espaço disponível, especialmente em dispositivos móveis.

A lista não deve depender exclusivamente da presença de um link externo: a disponibilidade de acesso deve ser representada de acordo com os dados cadastrados para cada material.

### 5.2. Detalhes do material

A área de detalhes deve reunir as informações disponíveis sobre o recurso em uma estrutura clara e consistente.

A interface deve distinguir:

- informações descritivas do material;
- metadados usados para organização e pesquisa;
- orientações de uso, quando cadastradas;
- opções de acesso efetivamente disponíveis.

Informações ausentes não devem ser substituídas por conteúdo inventado. A regra de exibição para cada campo opcional deverá ser definida durante o refinamento do modelo de dados e da interface.

## 6. Pesquisa e filtros

### 6.1. Pesquisa textual

A pesquisa deve considerar os seguintes campos:

1. Título;
2. Tipo de material;
3. Resumo;
4. Descrição.

As regras funcionais já estabelecidas são:

- ignorar diferenças entre letras maiúsculas e minúsculas;
- ignorar diferenças de acentuação;
- permitir correspondência parcial de termos;
- ordenar os resultados por relevância, priorizando os campos na ordem: título, tipo de material, resumo e descrição.

A fórmula exata de pontuação, os critérios de desempate, o tratamento de consultas com várias palavras e a tolerância a erros de digitação ainda precisam ser definidos.

### 6.2. Filtros

Os filtros devem restringir os materiais apresentados conforme os critérios disponibilizados pelo MVP.

Tipo de material e etapa de ensino são critérios previstos para avaliação. A lista definitiva de opções, o comportamento de seleção, a possibilidade de combinar filtros e a interação entre filtros e pesquisa ainda precisam ser formalizados.

A interface deverá indicar os filtros ativos de forma compreensível e permitir ajustar a seleção. O mecanismo exato para limpar filtros e combinar critérios permanece pendente.

### 6.3. Estados dos resultados

A interface deve distinguir claramente:

- **Catálogo inicial:** não há pesquisa ativa nem filtros aplicados.
- **Resultados encontrados:** há materiais correspondentes à pesquisa e aos filtros.
- **Nenhum resultado:** a combinação atual de termos e filtros não retorna materiais.

No estado sem resultados, a interface deve orientar o professor a revisar os termos pesquisados ou ajustar os filtros.

A ausência de resultados não deve ser confundida com falha de carregamento ou indisponibilidade de acesso a um material.

## 7. Organização das opções de acesso

O acesso deve ser representado conforme a disponibilidade real de cada material. Existem quatro cenários previstos:

| Cenário | Comportamento esperado |
|---|---|
| Somente link externo | Apresentar a ação para abrir o endereço externo. |
| Somente arquivo hospedado | Apresentar a ação para acessar o arquivo disponibilizado na plataforma. |
| Link externo e arquivo hospedado | Apresentar as duas opções de acesso, identificando-as claramente. |
| Nenhuma opção de acesso | Informar que não há uma opção de acesso disponível no momento, sem exibir uma ação que prometa abrir um recurso inexistente. |

As ações de acesso devem ser identificadas de acordo com seu destino. Quando houver duas opções, a interface não deve induzir o usuário a acreditar que elas levam necessariamente ao mesmo conteúdo ou formato.

Os detalhes técnicos de abertura, download, permissões, formatos aceitos e tratamento de erros precisam ser especificados nos requisitos e na documentação técnica antes da implementação.

## 8. Navegação e retorno

O usuário deve conseguir:

- explorar o catálogo;
- realizar uma pesquisa;
- aplicar e ajustar filtros;
- abrir os detalhes de um material a partir da listagem;
- identificar as opções de acesso disponíveis;
- retornar à listagem;
- corrigir a pesquisa ou os filtros quando não encontrar resultados.

A navegação entre a listagem e os detalhes deve manter uma relação clara entre o material selecionado e suas informações.

A preservação automática da consulta e dos filtros ao retornar à listagem é um comportamento desejável, mas ainda precisa ser confirmado como requisito.

## 9. Estados de carregamento e falha

A arquitetura deve prever estados distintos para problemas diferentes:

- **Carregamento:** os dados ainda estão sendo obtidos ou processados.
- **Falha ao carregar dados:** não foi possível apresentar o catálogo ou as informações solicitadas.
- **Falha de acesso:** o usuário selecionou uma opção de acesso, mas não conseguiu abrir ou obter o recurso.
- **Nenhum resultado:** a consulta foi processada, mas não encontrou correspondências.

Quando ocorrer uma falha, a mensagem deve explicar o problema em linguagem compreensível e, quando aplicável, indicar uma ação possível, como tentar novamente ou retornar à listagem.

Os mecanismos de detecção de falhas, as mensagens definitivas e as estratégias de recuperação ainda precisam ser detalhados. Não se deve presumir que a plataforma consiga detectar automaticamente todos os problemas ocorridos em sites externos.

## 10. Responsividade e acessibilidade

A organização das informações deve permanecer compreensível em diferentes tamanhos de tela.

Como critérios a detalhar durante o projeto da interface, devem ser considerados:

- hierarquia visual clara entre título, metadados, descrição e ações;
- identificação textual das opções de acesso;
- navegação por teclado;
- foco visível nos elementos interativos;
- rótulos claros para pesquisa e filtros;
- mensagens de estado compreensíveis;
- contraste adequado e uso de informações que não dependam exclusivamente de cores.

Os critérios verificáveis de acessibilidade e os requisitos de conformidade deverão ser definidos em documentação própria e conferidos durante a implementação e a validação.

## 11. Limites do MVP

A arquitetura descrita contempla catálogo, pesquisa, filtros, detalhes dos materiais, opções de acesso e estados necessários para orientar a navegação.

Não fazem parte do escopo atual:

- pré-visualização integrada dos materiais;
- edição ou adaptação de materiais na plataforma;
- criação ou envio de materiais pelos usuários.

Essas funcionalidades não devem aparecer como recursos disponíveis no MVP. Uma eventual inclusão futura exige revisão de escopo, requisitos e arquitetura.

## 12. Decisões pendentes

Antes de considerar a arquitetura pronta para implementação, devem ser resolvidos ou documentados:

- os campos obrigatórios e opcionais do cadastro;
- as regras de exibição de metadados ausentes;
- a composição definitiva dos itens do catálogo;
- as opções de filtros e as regras de combinação;
- os detalhes do cálculo de relevância da pesquisa;
- a preservação da pesquisa e dos filtros durante a navegação;
- os formatos de arquivo aceitos e o comportamento de acesso;
- as mensagens e estratégias de recuperação para falhas;
- os critérios verificáveis de acessibilidade.

Esses pontos devem ser tratados como pendências, e não como decisões já aprovadas.

## 13. Relação com os demais documentos

Este documento deve permanecer alinhado com:

- `docs/product/product-brief.md` — visão, escopo e limites do MVP;
- `docs/product/requisitos.md` — requisitos funcionais e não funcionais;
- `docs/product/historias-de-usuario.md` — necessidades e objetivos dos usuários;
- `docs/product/backlog.md` — tarefas, prioridades e decisões pendentes;
- `docs/ux-ui/objetivos-de-ux.md` — objetivos de experiência;
- `docs/ux-ui/user-flow.md` — percursos e transições entre estados;
- `docs/ux-ui/design-system.md` — padrões visuais e componentes.

Se houver divergência entre documentos, ela deve ser registrada e resolvida durante a revisão documental, evitando que uma hipótese seja tratada como requisito confirmado.

## 14. Validação e evolução

A versão atual descreve uma proposta documental para a arquitetura da informação. Ela ainda precisa ser comparada com o conjunto de requisitos, o modelo de dados e os fluxos de navegação.

A revisão documental não equivale à implementação, à avaliação de usabilidade ou à validação com professores. Essas atividades pertencem a etapas posteriores do projeto.

**Próximo passo:** resolver as pendências registradas, manter os documentos consistentes e, quando o projeto avançar, validar a arquitetura com protótipos e testes apropriados.
