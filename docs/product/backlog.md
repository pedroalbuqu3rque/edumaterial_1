# Backlog do EduMaterial

**Versão:** 0.3  
**Status:** Em revisão documental  
**Última atualização:** Outubro de 2026

## 1. Objetivo

Este documento organiza as tarefas necessárias para o desenvolvimento do EduMaterial, estabelecendo prioridades, entregáveis, dependências e critérios de conclusão.

O backlog acompanha a evolução do projeto desde a consolidação da documentação até as futuras etapas de prototipação, avaliação, implementação e verificação de qualidade.

As prioridades representam uma proposta de organização do trabalho e poderão ser ajustadas conforme as decisões do projeto.

## 2. Escopo atual

A etapa atual está concentrada na revisão e consolidação da documentação do produto.

As atividades atuais envolvem:

- Revisar e padronizar os documentos existentes.
- Identificar inconsistências entre requisitos, histórias de usuário, arquitetura da informação e fluxos.
- Registrar decisões confirmadas, hipóteses e questões pendentes.
- Alinhar o backlog ao escopo atualizado do MVP.
- Organizar as próximas etapas do projeto.

Não fazem parte da etapa atual:

- Implementação do sistema.
- Execução de testes de qualidade sobre uma aplicação implementada.
- Realização de pesquisas com usuários.
- Validação empírica das hipóteses com professores.
- Desenvolvimento de funcionalidades em produção.

Essas atividades poderão ser planejadas para etapas futuras. Sua inclusão no backlog não significa que tenham sido iniciadas ou concluídas.

## 3. Critérios de prioridade

| Prioridade | Significado |
|---|---|
| P0 | Necessário para consolidar a documentação e permitir o avanço organizado do projeto. |
| P1 | Necessário para esclarecer decisões e especificar o comportamento do produto. |
| P2 | Relacionado à organização da informação e à preparação da experiência de uso. |
| P3 | Atividades futuras de prototipação e avaliação. |
| P4 | Atividades futuras de implementação e verificação de qualidade. |

## 4. Backlog de tarefas

### P0 — Consolidação documental

#### BK-001 — Organizar e padronizar os documentos do projeto

**Status:** Em andamento

**Descrição:** Revisar os documentos de produto e UX/UI, padronizando estrutura, terminologia, escopo e identificação de decisões.

**Entregáveis:**

- `README.md`
- `docs/product/product-brief.md`
- `docs/product/requisitos.md`
- `docs/product/historias-de-usuario.md`
- `docs/product/backlog.md`
- `docs/ux-ui/arquitetura-da-informacao.md`
- `docs/ux-ui/design-system.md`
- `docs/ux-ui/objetivos-de-ux.md`
- `docs/ux-ui/user-flow.md`

**Critérios de conclusão:**

- Todos os documentos previstos estão presentes no repositório.
- Os nomes e caminhos dos arquivos estão corretos.
- A versão e o status dos documentos estão atualizados.
- As informações são consistentes entre os documentos.
- O escopo do MVP está descrito de maneira uniforme.
- As mudanças revisadas foram efetivamente aplicadas ao repositório.

#### BK-002 — Verificar referências e links internos

**Status:** Pendente

**Descrição:** Conferir se os caminhos e as referências entre os documentos correspondem à estrutura real do repositório.

**Critérios de conclusão:**

- Os links internos apontam para arquivos existentes.
- Os caminhos documentados correspondem à estrutura do projeto.
- Não há referências a documentos inexistentes como se já estivessem disponíveis.
- O README e os documentos relacionados refletem a organização atual do repositório.

#### BK-003 — Consolidar decisões, hipóteses e pendências

**Status:** Em andamento

**Descrição:** Garantir que decisões confirmadas, hipóteses de trabalho e questões pendentes estejam claramente diferenciadas.

**Critérios de conclusão:**

- As funcionalidades previstas no MVP estão identificadas.
- As decisões confirmadas estão refletidas nos documentos pertinentes.
- As hipóteses não são apresentadas como fatos comprovados.
- As questões ainda não resolvidas estão registradas.
- Dados simulados não são apresentados como resultados de pesquisas reais.
- As tarefas do backlog não são consideradas concluídas apenas por terem sido documentadas.

### P1 — Especificação funcional do MVP

#### BK-004 — Definir e consolidar o comportamento da busca

**Status:** Em andamento

**Descrição:** Documentar as regras da busca de materiais educacionais e identificar as decisões restantes para sua especificação completa.

**Decisões já estabelecidas:**

- Campos pesquisáveis: título, tipo de material, resumo e descrição.
- A busca ignora diferenças entre letras maiúsculas e minúsculas.
- A busca ignora diferenças de acentuação.
- A busca aceita correspondências parciais.
- Os resultados são ordenados por relevância.
- A prioridade dos campos é: título, tipo de material, resumo e descrição, nessa ordem.

**Questões pendentes:**

- Como será calculada a pontuação de relevância?
- Como serão tratados resultados com pontuação equivalente?
- Como serão processadas consultas com múltiplas palavras?
- Como serão tratados erros de digitação?
- Como a busca se combinará com os filtros selecionados?
- Qual será o comportamento da busca quando não houver correspondências?

**Critérios de conclusão:**

- As regras já definidas estão registradas nos requisitos e nas histórias de usuário.
- As questões restantes estão resolvidas ou explicitamente delimitadas para uma etapa posterior.
- Os critérios de ordenação dos resultados estão suficientemente especificados.
- Os exemplos de comportamento da busca estão documentados.
- Os documentos relacionados não apresentam regras contraditórias.

#### BK-005 — Especificar os filtros

**Status:** Em andamento

**Descrição:** Consolidar o comportamento dos filtros utilizados para localizar materiais educacionais.

**Decisões já estabelecidas:**

- Os filtros previstos para o MVP são tipo de material e etapa de ensino.

**Questões pendentes:**

- Quais opções estarão disponíveis em cada filtro?
- Será possível combinar vários filtros simultaneamente?
- Como a busca e os filtros funcionarão em conjunto?
- Como o usuário poderá remover filtros aplicados?
- Como a interface apresentará o estado sem resultados após a filtragem?

**Critérios de conclusão:**

- Os filtros previstos estão documentados.
- As opções de cada filtro estão definidas.
- As regras de combinação e remoção estão especificadas.
- O comportamento conjunto da busca e dos filtros está descrito.
- Os requisitos, as histórias de usuário e os fluxos estão alinhados.

#### BK-006 — Definir os metadados dos materiais

**Status:** Em andamento

**Descrição:** Determinar quais informações serão necessárias para descrever, organizar, localizar e disponibilizar cada material educacional.

**Campos já previstos:**

- Título.
- Tipo de material.
- Etapa de ensino.
- Resumo.
- Descrição.
- Link externo, quando disponível.
- Arquivo hospedado na plataforma, quando disponível.

**Campos e informações a avaliar:**

- Autor ou fonte.
- Instruções de utilização.
- Informações de autoria e licença, quando aplicáveis.
- Formato do arquivo, quando aplicável.
- Outras informações que ajudem o professor a avaliar a pertinência do material.

**Critérios de conclusão:**

- Os campos obrigatórios e opcionais estão identificados.
- As regras para materiais com informações incompletas estão documentadas.
- As informações de autoria, origem e condições de uso foram consideradas.
- Os metadados estão alinhados à arquitetura da informação.
- Os campos utilizados pela busca correspondem às definições funcionais.

#### BK-007 — Consolidar as regras de acesso aos materiais

**Status:** Em andamento

**Descrição:** Especificar como a plataforma apresentará as formas de acesso aos materiais e como tratará situações em que o acesso não esteja disponível.

**Cenários estabelecidos:**

1. Material disponível por link externo, sem arquivo hospedado.
2. Material disponível por arquivo hospedado, sem link externo.
3. Material disponível por link externo e arquivo hospedado.
4. Material sem link externo ou arquivo hospedado disponível.

**Questões pendentes:**

- Quais formatos de arquivo serão aceitos?
- Quais serão os limites de tamanho dos arquivos?
- Como serão apresentados arquivos indisponíveis ou inválidos?
- Como serão tratadas falhas ao abrir um link externo?
- Quais informações de autoria, origem e uso deverão acompanhar cada material?
- Como serão apresentadas as opções de acesso quando ambas estiverem disponíveis?

**Critérios de conclusão:**

- Os quatro cenários estão especificados.
- As ações disponíveis em cada cenário estão descritas.
- As mensagens de ausência de acesso e de falha estão documentadas.
- Os requisitos, as histórias de usuário e os fluxos representam os cenários corretamente.
- A interface não apresenta ações de acesso que não estejam disponíveis.

### P2 — Preparação da experiência de uso

#### BK-008 — Revisar a arquitetura da informação

**Status:** Em andamento

**Descrição:** Conferir a organização das páginas, os elementos de navegação e as informações apresentadas em cada etapa da experiência.

**Critérios de conclusão:**

- A estrutura contempla catálogo, resultados e detalhes do material.
- A busca e os filtros estão representados.
- Os estados sem resultados e sem materiais cadastrados estão previstos.
- Os quatro cenários de acesso estão representados.
- As informações dos materiais estão alinhadas aos metadados definidos.
- A arquitetura está consistente com os requisitos e as histórias de usuário.

#### BK-009 — Revisar o fluxo principal do usuário

**Status:** Em andamento

**Descrição:** Consolidar o fluxo desde a entrada na plataforma até a localização, consulta e tentativa de acesso a um material.

**Critérios de conclusão:**

- O fluxo contempla catálogo, busca e filtros.
- Os caminhos com resultados e sem resultados estão representados.
- A consulta aos detalhes do material está prevista.
- Os cenários de link externo, arquivo hospedado, ambos e ausência de acesso estão contemplados.
- As situações de falha de acesso estão documentadas.
- As decisões pendentes estão identificadas.
- O fluxo está alinhado aos requisitos e às histórias de usuário.

#### BK-010 — Consolidar as diretrizes visuais

**Status:** Pendente

**Descrição:** Organizar as diretrizes iniciais do design system e identificar os elementos visuais que ainda precisam ser definidos ou validados.

**Critérios de conclusão:**

- A proposta visual está documentada.
- Cores, tipografia, espaçamentos e componentes estão organizados.
- Os valores ainda não confirmados estão identificados como provisórios.
- Os estados de interface relevantes estão previstos.
- As diretrizes de acessibilidade e responsividade estão registradas.
- A documentação visual é consistente com os objetivos de UX.

### P3 — Prototipação e avaliação futura

As tarefas desta seção estão previstas para etapas posteriores à consolidação documental.

#### BK-011 — Criar wireframes do MVP

**Status:** Planejado para etapa futura

**Descrição:** Elaborar representações estruturais das principais telas, sem exigir a implementação do sistema.

**Telas previstas:**

- Catálogo inicial.
- Resultados da busca.
- Resultados com filtros aplicados.
- Detalhes do material.
- Estado sem resultados.
- Estado sem materiais cadastrados.
- Estado sem acesso disponível.
- Situação de falha de acesso.

**Critérios de conclusão:**

- As telas principais estão representadas.
- Os wireframes correspondem aos requisitos e fluxos documentados.
- Os estados alternativos relevantes estão contemplados.
- A navegação entre as telas está representada.
- As decisões ainda pendentes não são tratadas como definitivas.

#### BK-012 — Desenvolver o protótipo visual

**Status:** Planejado para etapa futura

**Descrição:** Aplicar as diretrizes visuais aos wireframes e elaborar um protótipo navegável para representar a experiência planejada.

**Critérios de conclusão:**

- O protótipo representa o fluxo principal do MVP.
- Os componentes seguem as diretrizes visuais definidas.
- Os estados alternativos relevantes estão representados.
- A navegação entre as telas pode ser demonstrada.
- As decisões visuais ainda provisórias estão identificadas.

#### BK-013 — Planejar uma avaliação com professores

**Status:** Planejado para etapa futura

**Descrição:** Planejar uma avaliação da experiência de uso com professores, público prioritário do EduMaterial.

**Critérios de conclusão:**

- Os objetivos da avaliação estão definidos.
- As tarefas a serem realizadas pelos participantes estão descritas.
- Os critérios de observação e análise estão documentados.
- O método de recrutamento e os cuidados com os dados estão considerados.
- As limitações da avaliação estão previstas.
- Os resultados serão registrados somente após a coleta e análise de dados reais.

O planejamento desta tarefa não significa que uma avaliação já tenha sido realizada.

### P4 — Implementação e qualidade futuras

#### BK-014 — Planejar a implementação do MVP

**Status:** Planejado para etapa futura

**Descrição:** Transformar os requisitos aprovados em tarefas técnicas de implementação.

**Critérios de conclusão:**

- As funcionalidades do MVP estão suficientemente especificadas.
- As decisões técnicas necessárias estão registradas.
- As tarefas de implementação possuem escopo e critérios de aceitação.
- As dependências técnicas estão identificadas.
- As limitações conhecidas estão documentadas.

#### BK-015 — Planejar a verificação de qualidade

**Status:** Planejado para etapa futura

**Descrição:** Definir como será verificado o funcionamento das funcionalidades após sua implementação.

**Aspectos a considerar:**

- Busca e ordenação por relevância.
- Tratamento de maiúsculas, minúsculas, acentuação e correspondências parciais.
- Combinação entre busca e filtros.
- Navegação entre catálogo, resultados e detalhes.
- Acesso por links externos.
- Acesso a arquivos hospedados.
- Estados vazios e mensagens de erro.
- Responsividade e acessibilidade.

**Critérios de conclusão:**

- Os cenários de verificação estão documentados.
- Cada cenário possui um resultado esperado.
- Os critérios de aceitação são verificáveis.
- As verificações de software serão executadas somente quando houver uma implementação disponível.

## 5. Ordem recomendada de execução

A sequência proposta para orientar o andamento do projeto é:

1. Concluir a revisão e a padronização dos documentos.
2. Conferir as referências e a consistência entre os arquivos.
3. Consolidar as decisões funcionais pendentes da busca, dos filtros e dos metadados.
4. Consolidar as regras de acesso aos materiais.
5. Atualizar requisitos, histórias de usuário, arquitetura e fluxos conforme as decisões tomadas.
6. Finalizar a revisão das diretrizes visuais.
7. Criar wireframes e protótipo visual em uma etapa futura.
8. Planejar e, quando viável, realizar avaliações com professores.
9. Planejar a implementação e a verificação de qualidade em etapas posteriores.

A ordem poderá ser ajustada quando uma atividade depender de decisões ou recursos ainda indisponíveis.

## 6. Controle de andamento

O backlog deverá ser atualizado conforme as tarefas forem iniciadas, concluídas, bloqueadas ou replanejadas.

Os status utilizados são:

- **Pendente:** tarefa identificada, mas ainda não iniciada.
- **Em andamento:** tarefa em execução.
- **Concluído:** tarefa finalizada, com os critérios de conclusão atendidos.
- **Bloqueado:** tarefa que depende de uma decisão, recurso ou atividade anterior.
- **Planejado para etapa futura:** atividade reconhecida, mas que não pertence à fase atual.

Uma tarefa não deverá ser marcada como concluída apenas por ter sido descrita ou revisada documentalmente. A conclusão exige que os critérios correspondentes tenham sido efetivamente atendidos.

Os status deste documento são referências de organização e devem ser conferidos com o andamento real do trabalho antes de cada atualização.

## 7. Considerações metodológicas

O EduMaterial encontra-se em uma etapa de organização e revisão documental. A documentação define o comportamento pretendido do produto, mas não comprova que as funcionalidades foram implementadas ou que as hipóteses de produto foram validadas.

Um formulário de pesquisa foi considerado anteriormente, mas sua aplicação foi abandonada. Portanto, dados simulados não devem ser tratados como respostas reais, evidências empíricas ou validação das necessidades dos professores.

As futuras atividades de avaliação deverão distinguir claramente o planejamento metodológico, a coleta de dados e os resultados efetivamente obtidos.

## 8. Documentos relacionados

- `README.md`
- `docs/product/product-brief.md`
- `docs/product/requisitos.md`
- `docs/product/historias-de-usuario.md`
- `docs/product/backlog.md`
- `docs/ux-ui/arquitetura-da-informacao.md`
- `docs/ux-ui/design-system.md`
- `docs/ux-ui/objetivos-de-ux.md`
- `docs/ux-ui/user-flow.md`

As mudanças de escopo ou de comportamento do produto devem ser refletidas nos documentos relacionados, evitando contradições e mantendo a rastreabilidade das decisões.
