# Backlog do EduMaterial

**Versão:** 0.1  
**Status:** Em revisão documental  
**Última atualização:** Outubro de 2026

## 1. Objetivo

Este documento organiza as tarefas necessárias para o desenvolvimento do EduMaterial, estabelecendo prioridades, entregáveis, dependências e critérios de conclusão.

O backlog acompanha a evolução do projeto desde a consolidação da documentação até as futuras etapas de prototipação, avaliação e implementação.

As prioridades apresentadas são uma proposta inicial e poderão ser ajustadas conforme as decisões do projeto.

## 2. Escopo atual

A etapa atual está concentrada na revisão e organização da documentação do produto.

**As atividades atuais envolvem:**
- Revisar e padronizar os documentos existentes.
- Identificar inconsistências entre requisitos, histórias de usuário, arquitetura da informação e fluxos.
- Registrar decisões confirmadas, hipóteses e questões pendentes.
- Organizar as próximas etapas do projeto.

**Não fazem parte da etapa atual:**
- Implementação do sistema.
- Execução de testes de qualidade do software.
- Realização de pesquisas com usuários.
- Validação das hipóteses com professores.
- Desenvolvimento de funcionalidades em produção.

Essas atividades poderão ser planejadas para etapas futuras.

## 3. Critérios de prioridade

| Prioridade | Significado |
|---|---|
| P0 | Necessário para consolidar a documentação e permitir o avanço organizado do projeto. |
| P1 | Necessário para esclarecer decisões e especificar o comportamento do produto. |
| P2 | Preparação da estrutura e da experiência de uso. |
| P3 | Atividades futuras de prototipação e avaliação. |
| P4 | Atividades futuras de implementação e verificação de qualidade. |

## 4. Backlog de tarefas

### P0 — Consolidação documental

#### BK-001 — Organizar os documentos do projeto

**Status:** Pendente

**Descrição:** Reunir e padronizar os documentos de produto e UX/UI existentes no repositório.

**Entregáveis:**
- `README.md`
- `docs/product/product-brief.md`
- `docs/product/requisitos.md`
- `docs/product/historias-de-usuario.md`
- `docs/ux-ui/arquitetura-da-informacao.md`
- `docs/ux-ui/design-system.md`
- `docs/ux-ui/objetivos-de-ux.md`
- `docs/ux-ui/user-flow.md`

**Critérios de conclusão:**
- Todos os documentos revisados estão presentes no repositório.
- Os nomes e caminhos dos arquivos estão corretos.
- As informações são consistentes entre os documentos.
- O escopo do MVP está descrito de maneira uniforme.

#### BK-002 — Verificar referências e links internos

**Status:** Pendente

**Descrição:** Conferir se os caminhos e as referências entre os documentos correspondem à estrutura real do repositório.

**Critérios de conclusão:**
- Os links internos apontam para arquivos existentes.
- Os caminhos documentados correspondem à estrutura do projeto.
- Não há referências a documentos inexistentes como se já estivessem disponíveis.

#### BK-003 — Registrar decisões e pendências

**Status:** Pendente

**Descrição:** Garantir que decisões confirmadas, hipóteses e questões pendentes estejam claramente diferenciadas.

**Critérios de conclusão:**
- As funcionalidades previstas no MVP estão identificadas.
- As hipóteses não são apresentadas como fatos comprovados.
- As decisões ainda não tomadas estão registradas.
- Informações simuladas não são apresentadas como resultados de pesquisas reais.

### P1 — Especificação funcional do MVP

#### BK-004 — Definir o comportamento da busca

**Status:** Pendente

**Descrição:** Especificar como a busca por materiais deverá funcionar.

**Questões a esclarecer:**
- Quais campos serão pesquisáveis?
- A busca considerará palavras parciais ou apenas correspondências completas?
- Como os resultados serão ordenados?
- Como serão tratados acentos, erros de digitação e termos sem correspondência?

**Critérios de conclusão:**
- As regras da busca estão documentadas.
- Os critérios de apresentação dos resultados estão definidos.
- As decisões estão refletidas nos requisitos e nas histórias de usuário.

#### BK-005 — Especificar os filtros

**Status:** Pendente

**Descrição:** Definir os filtros disponíveis para localizar materiais educacionais.

**Questões a esclarecer:**
- Quais categorias de filtros serão disponibilizadas?
- Quais opções estarão disponíveis em cada filtro?
- Será possível combinar vários filtros?
- Como a busca e os filtros funcionarão em conjunto?
- Como o usuário poderá remover filtros aplicados?

**Critérios de conclusão:**
- Os filtros previstos estão listados.
- As regras de combinação estão documentadas.
- O comportamento dos filtros está consistente nos requisitos, nas histórias e nos fluxos.

#### BK-006 — Definir os metadados dos materiais

**Status:** Pendente

**Descrição:** Determinar quais informações serão necessárias para descrever e organizar cada material.

**Campos a avaliar:**
- Título.
- Tipo de material.
- Etapa ou nível de ensino.
- Resumo.
- Descrição.
- Instruções de utilização.
- Autor ou fonte.
- Informações de autoria e licença, quando aplicáveis.
- Link externo.
- Arquivo hospedado na plataforma.

**Critérios de conclusão:**
- Os campos obrigatórios e opcionais estão identificados.
- As regras para materiais com informações incompletas estão documentadas.
- Os metadados estão alinhados à arquitetura da informação.

#### BK-007 — Definir as regras de acesso aos materiais

**Status:** Pendente

**Descrição:** Especificar como a plataforma apresentará as diferentes formas de acesso aos materiais.

**Cenários previstos:**
- Material disponível por link externo.
- Material disponível por arquivo hospedado na plataforma.
- Material disponível por link e arquivo.
- Material sem link ou arquivo disponível.

**Questões a esclarecer:**
- Quais formatos de arquivo serão aceitos?
- Como serão apresentados arquivos indisponíveis?
- Como será informado que um material não possui acesso direto?
- Quais informações de autoria, origem e uso deverão acompanhar o material?

**Critérios de conclusão:**
- Os quatro cenários de acesso estão especificados.
- As mensagens e ações correspondentes estão descritas.
- Os requisitos e os fluxos representam esses cenários corretamente.

### P2 — Preparação da experiência de uso

#### BK-008 — Revisar a arquitetura da informação

**Status:** Pendente

**Descrição:** Conferir a organização das páginas, os elementos de navegação e as informações apresentadas em cada etapa.

**Critérios de conclusão:**
- A estrutura contempla catálogo, resultados e detalhes do material.
- Os estados sem resultados e sem materiais cadastrados estão previstos.
- Os cenários de acesso estão representados.
- A estrutura está alinhada aos requisitos e às histórias de usuário.

#### BK-009 — Revisar o fluxo principal do usuário

**Status:** Pendente

**Descrição:** Conferir o fluxo desde a entrada na plataforma até a localização e o acesso a um material.

**Critérios de conclusão:**
- O fluxo contempla busca e filtros.
- Os caminhos com resultados e sem resultados estão representados.
- Os cenários de link externo, arquivo hospedado, ambos e ausência de acesso estão contemplados.
- As decisões ainda pendentes estão identificadas.

#### BK-010 — Consolidar as diretrizes visuais

**Status:** Pendente

**Descrição:** Organizar as diretrizes iniciais do design system e identificar os elementos que ainda precisam ser definidos.

**Critérios de conclusão:**
- A proposta visual está documentada.
- Cores, tipografia, espaçamentos e componentes estão organizados.
- Os valores ainda não confirmados estão identificados como provisórios.
- As diretrizes de acessibilidade e responsividade estão registradas.

### P3 — Prototipação e avaliação futura

#### BK-011 — Criar wireframes do MVP

**Status:** Planejado para etapa futura

**Descrição:** Elaborar representações estruturais das principais telas, sem exigir ainda a implementação do sistema.

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
- Os wireframes correspondem aos requisitos e aos fluxos documentados.
- Os estados alternativos estão contemplados.

#### BK-012 — Desenvolver o protótipo visual

**Status:** Planejado para etapa futura

**Descrição:** Aplicar as diretrizes visuais aos wireframes e elaborar um protótipo navegável.

**Critérios de conclusão:**
- O protótipo representa o fluxo principal.
- Os componentes seguem as diretrizes visuais definidas.
- Os estados alternativos relevantes estão representados.
- As decisões visuais ainda provisórias estão identificadas.

#### BK-013 — Planejar a avaliação com professores

**Status:** Planejado para etapa futura

**Descrição:** Planejar uma avaliação da experiência de uso com professores, público prioritário do EduMaterial.

**Critérios de conclusão:**
- Os objetivos da avaliação estão definidos.
- As tarefas a serem realizadas pelos participantes estão descritas.
- Os critérios de observação e análise estão documentados.
- Os resultados futuros serão registrados somente após a coleta e análise de dados reais.

### P4 — Implementação e qualidade futuras

#### BK-014 — Planejar a implementação do MVP

**Status:** Planejado para etapa futura

**Descrição:** Transformar os requisitos aprovados em tarefas técnicas de implementação.

**Critérios de conclusão:**
- As funcionalidades do MVP estão suficientemente especificadas.
- As decisões técnicas necessárias estão registradas.
- As tarefas de implementação possuem escopo e critérios de aceitação.
- As dependências técnicas estão identificadas.

#### BK-015 — Planejar a verificação de qualidade

**Status:** Planejado para etapa futura

**Descrição:** Definir como será verificado o funcionamento das funcionalidades após sua implementação.

**Aspectos a considerar:**
- Busca e filtros.
- Navegação entre catálogo, resultados e detalhes.
- Acesso por links externos.
- Acesso a arquivos hospedados.
- Estados vazios e mensagens de erro.
- Responsividade e acessibilidade.

**Critérios de conclusão:**
- Os cenários de verificação estão documentados.
- Cada cenário possui um resultado esperado.
- As verificações serão executadas somente quando houver uma implementação disponível.

## 5. Ordem recomendada de execução

A sequência proposta para orientar o andamento do projeto é:

1. Consolidar os documentos e verificar sua presença no repositório.
2. Conferir referências e consistência entre os arquivos.
3. Resolver as principais pendências funcionais do MVP.
4. Atualizar requisitos, histórias de usuário, arquitetura e fluxos conforme as decisões tomadas.
5. Consolidar as diretrizes visuais.
6. Criar wireframes e protótipo visual em uma etapa futura.
7. Planejar e realizar avaliações com professores, quando viável.
8. Planejar a implementação e a verificação de qualidade em etapas posteriores.

A ordem poderá ser ajustada caso alguma decisão dependa de informações ainda indisponíveis.

## 6. Controle de andamento

O backlog deverá ser atualizado conforme as tarefas forem iniciadas, concluídas ou replanejadas.

Os status utilizados são:

- **Pendente:** tarefa identificada, ainda não concluída.
- **Em andamento:** tarefa em execução.
- **Concluído:** tarefa finalizada e com seus critérios de conclusão atendidos.
- **Bloqueado:** tarefa que depende de uma decisão, recurso ou atividade anterior.
- **Planejado para etapa futura:** atividade reconhecida, mas que não pertence à fase atual.

Uma tarefa não deverá ser marcada como concluída apenas por ter sido descrita neste documento.

## 7. Considerações metodológicas

O EduMaterial encontra-se em uma etapa de organização e revisão documental. As hipóteses de produto ainda precisam ser avaliadas adequadamente.

Um formulário de pesquisa foi considerado anteriormente, mas sua aplicação foi abandonada. Portanto, dados simulados não devem ser tratados como respostas reais, evidências empíricas ou validação das necessidades dos professores.

As futuras atividades de avaliação deverão distinguir claramente o planejamento metodológico, a coleta de dados e os resultados efetivamente obtidos.

## 8. Documentos relacionados

- `README.md`
- `docs/product/product-brief.md`
- `docs/product/requisitos.md`
- `docs/product/historias-de-usuario.md`
- `docs/ux-ui/arquitetura-da-informacao.md`
- `docs/ux-ui/design-system.md`
- `docs/ux-ui/objetivos-de-ux.md`
- `docs/ux-ui/user-flow.md`
