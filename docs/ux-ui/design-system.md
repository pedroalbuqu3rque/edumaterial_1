# Design System — EduMaterial

**Versão:** 0.2  
**Status:** Proposta documental revisada  
**Escopo:** MVP do EduMaterial

## 1. Objetivo

Documentar os princípios visuais, os tokens de design e os componentes previstos para a interface do EduMaterial, buscando manter consistência entre as diferentes áreas da plataforma.

Este documento estabelece uma direção visual inicial para o MVP. Os valores e padrões apresentados são propostas de referência e deverão ser confrontados com o protótipo visual existente, caso aplicável, antes de serem tratados como definições finais.

A documentação descreve uma interface planejada. Não significa que os componentes tenham sido implementados, verificados ou validados com usuários reais.

## 2. Direção visual

A direção visual proposta para o EduMaterial é minimalista, com predominância de preto, branco e tons de cinza.

A interface deve priorizar a organização das informações, a leitura dos materiais e a identificação das ações disponíveis, evitando elementos decorativos que não contribuam para a experiência de uso.

### Princípios visuais

- **Clareza:** apresentar informações e ações de maneira compreensível.
- **Simplicidade:** evitar elementos visuais desnecessários.
- **Consistência:** utilizar padrões semelhantes para componentes que desempenham funções equivalentes.
- **Hierarquia:** destacar títulos, informações relevantes e ações principais.
- **Legibilidade:** favorecer a leitura de descrições e metadados dos materiais.
- **Responsividade:** preservar a compreensão e a utilização da interface em diferentes tamanhos de tela.
- **Acessibilidade:** considerar contraste, foco visível, navegação por teclado e identificação textual das ações.

## 3. Cores

A paleta inicial proposta utiliza preto, branco e tons de cinza.

| Token | Valor de referência | Aplicação prevista |
|---|---|---|
| `color-background` | `#FFFFFF` | Fundo principal das páginas |
| `color-surface` | `#FFFFFF` | Cartões e superfícies de conteúdo |
| `color-text-primary` | `#111111` | Títulos e textos principais |
| `color-text-secondary` | `#666666` | Descrições e informações auxiliares |
| `color-border` | `#E5E5E5` | Bordas e divisórias |
| `color-surface-muted` | `#F5F5F5` | Fundos secundários e áreas de apoio |
| `color-action` | `#111111` | Ações principais |
| `color-action-text` | `#FFFFFF` | Texto sobre ações principais |

Os valores são referências iniciais, não uma declaração de que as cores já foram implementadas ou verificadas no protótipo.

Antes de serem tratados como definitivos, os tokens deverão ser conferidos em relação ao arquivo de design e avaliados quanto à legibilidade e ao contraste.

### 3.1. Uso das cores

- O fundo principal deve favorecer a leitura dos conteúdos.
- Os tons de cinza devem auxiliar na separação de áreas e na apresentação de informações secundárias.
- As ações principais devem apresentar contraste suficiente com o fundo.
- As cores não devem ser o único meio de indicar estados, erros ou diferenças entre componentes.
- Estados como selecionado, desabilitado e erro devem ser identificáveis também por rótulos, ícones, contornos ou outras indicações visuais apropriadas.

## 4. Tipografia

A tipografia deve estabelecer uma hierarquia clara entre títulos, informações dos materiais, descrições e elementos de apoio.

| Estilo | Finalidade |
|---|---|
| Título principal | Identificar a página ou destacar sua mensagem principal |
| Título de seção | Organizar grupos de conteúdo |
| Título de cartão | Identificar um material no catálogo |
| Texto de corpo | Apresentar descrições e informações principais |
| Texto auxiliar | Apresentar categorias, metadados e orientações |
| Texto de controle | Identificar campos, filtros e ações |

A família tipográfica, os tamanhos, os pesos e as alturas de linha ainda precisam ser confirmados no arquivo de design.

Até essa confirmação, os estilos tipográficos devem ser tratados como categorias semânticas propostas, e não como especificações finais de fonte e tamanho.

## 5. Espaçamento e organização

O layout deve utilizar espaçamentos consistentes para estabelecer relações entre elementos e facilitar a leitura.

Como referência inicial, propõe-se uma escala baseada em múltiplos de 4 px.

Exemplos de aplicação:

- Espaçamento entre ícones e seus rótulos.
- Distância interna entre o conteúdo e as bordas de botões.
- Espaçamento entre campos de pesquisa e filtros.
- Separação entre cartões do catálogo.
- Distância entre seções e blocos de conteúdo.
- Margens laterais adequadas em telas menores.

Os valores finais devem ser definidos a partir do protótipo visual e aplicados de maneira consistente entre os componentes.

## 6. Componentes

Os componentes descritos nesta seção representam elementos previstos para a interface do MVP. Seus comportamentos e estados deverão ser especificados de acordo com os requisitos e a arquitetura da informação.

### 6.1. Cabeçalho

**Finalidade:** identificar o EduMaterial e oferecer acesso à navegação principal prevista para o produto.

**Diretrizes:**
- Manter alinhamento e espaçamento consistentes.
- Apresentar os elementos de navegação com hierarquia visual clara.
- Preservar a legibilidade em diferentes tamanhos de tela.
- Evitar elementos de navegação que não correspondam às funcionalidades previstas no MVP.

### 6.2. Campo de pesquisa

**Finalidade:** permitir que o professor informe palavras-chave para localizar materiais.

**Diretrizes:**
- Apresentar um rótulo ou indicação textual compreensível.
- Tornar clara a finalidade do campo.
- Exibir um estado de foco identificável.
- Permitir que o usuário compreenda como iniciar uma pesquisa.
- Manter consistência com os demais campos da interface.

A aparência do campo não define, por si só, as regras de pesquisa. Os campos pesquisáveis e o comportamento da busca permanecem especificados na documentação de requisitos.

### 6.3. Filtros

**Finalidade:** permitir o refinamento do catálogo por tipo de material e etapa de ensino.

**Diretrizes:**
- Identificar claramente cada critério de filtragem.
- Diferenciar visualmente os estados selecionado e não selecionado.
- Indicar os filtros ativos.
- Tornar possível identificar como remover ou alterar filtros.
- Preservar a legibilidade em telas menores.

A apresentação visual dos filtros deverá acompanhar as regras funcionais definidas para sua utilização em conjunto com a pesquisa.

### 6.4. Cartão de material

**Finalidade:** apresentar um resumo do recurso no catálogo ou nos resultados da pesquisa.

**Diretrizes:**
- Priorizar o título do material.
- Apresentar as informações resumidas definidas para o catálogo.
- Organizar metadados, como tipo e etapa de ensino, de maneira consistente.
- Evitar excesso de informações no cartão.
- Indicar claramente como consultar os detalhes do recurso, quando o cartão ou uma de suas áreas for interativa.
- Não exibir informações que não estejam disponíveis no cadastro do material.

O cartão não deve sugerir que existe uma visualização prévia do conteúdo, pois essa funcionalidade está fora do MVP.

### 6.5. Botões e ações

**Finalidade:** permitir a execução das ações disponíveis na interface.

**Diretrizes:**
- Diferenciar ações principais e secundárias.
- Utilizar rótulos que descrevam o resultado esperado.
- Manter consistência visual entre ações equivalentes.
- Apresentar estados identificáveis de foco e desabilitação.
- Evitar rótulos ambíguos.

Exemplos de ações previstas incluem pesquisar, limpar filtros, consultar detalhes e acessar um material.

### 6.6. Estado sem resultados

**Finalidade:** informar que a pesquisa ou os filtros aplicados não retornaram materiais correspondentes.

**Diretrizes:**
- Apresentar uma mensagem direta e compreensível.
- Diferenciar a ausência de resultados de uma falha técnica.
- Orientar o usuário, quando apropriado, a alterar os termos ou remover filtros.
- Não sugerir que o catálogo está vazio quando existem materiais cadastrados, mas nenhum corresponde aos critérios utilizados.

### 6.7. Estado de catálogo vazio

**Finalidade:** informar que não há materiais cadastrados para apresentar no catálogo.

**Diretrizes:**
- Utilizar uma mensagem diferente daquela empregada para uma pesquisa sem resultados.
- Não sugerir que o usuário precisa corrigir a pesquisa quando não há materiais cadastrados.
- Manter a apresentação visual consistente com os demais estados informativos da interface.

### 6.8. Página de detalhes do material

**Finalidade:** organizar as informações de um recurso selecionado e permitir que o professor identifique sua forma de acesso.

**Diretrizes:**
- Apresentar o título e as informações descritivas em uma hierarquia clara.
- Organizar os metadados de maneira consistente.
- Distinguir as informações do material das ações de acesso.
- Não depender de uma visualização prévia para apresentar os detalhes.
- Não exibir dados fictícios ou presumidos como se fossem informações cadastradas.

### 6.9. Acesso por link externo

**Finalidade:** permitir que o professor identifique e acesse um material disponível em um endereço externo.

**Diretrizes:**
- Utilizar uma ação com rótulo claro, como “Acessar material”.
- Informar, quando necessário, que o acesso direciona o usuário para um ambiente externo.
- Manter a ação visualmente distinguível das informações descritivas.
- Não exibir a ação quando não houver link externo cadastrado.

O comportamento de links indisponíveis deverá ser definido nos requisitos e considerado no detalhamento posterior da interface.

### 6.10. Acesso a arquivo hospedado na plataforma

**Finalidade:** permitir que o professor acesse ou baixe um arquivo disponibilizado diretamente na plataforma.

**Diretrizes:**
- Identificar claramente a ação de acesso ao arquivo.
- Distinguir o acesso ao arquivo do acesso por link externo.
- Apresentar informações sobre o arquivo quando esses dados estiverem disponíveis e forem relevantes.
- Não exibir uma ação de acesso a arquivo quando não houver arquivo disponível.

Os formatos aceitos, os limites de tamanho e as regras de armazenamento permanecem pendentes de definição.

### 6.11. Estado sem forma de acesso

**Finalidade:** informar que o material não possui link externo nem arquivo disponível para acesso.

**Diretrizes:**
- Apresentar uma mensagem clara sobre a ausência de uma forma de acesso cadastrada.
- Não exibir botões que prometam abrir um recurso inexistente.
- Preservar as informações descritivas do material.
- Manter uma apresentação consistente com os demais estados informativos.

## 7. Estados dos componentes

Os componentes interativos deverão considerar os estados aplicáveis à sua função.

| Estado | Aplicação prevista |
|---|---|
| Padrão | Aparência habitual do componente |
| Hover | Indicação visual ao posicionar o ponteiro sobre um elemento interativo, quando aplicável |
| Foco | Indicação visual do elemento que recebeu foco, incluindo navegação por teclado |
| Selecionado | Indicação de uma opção ou filtro ativo |
| Desabilitado | Indicação de uma ação temporariamente indisponível |
| Carregamento | Indicação de que uma operação está em andamento, quando aplicável |
| Sem resultados | Indicação de que uma pesquisa ou filtragem não retornou materiais |
| Erro | Indicação de falha em uma operação, quando identificada |
| Sem acesso | Indicação de que não existe link ou arquivo disponível para o material |

Nem todos os estados se aplicam a todos os componentes. O detalhamento deve considerar a função de cada elemento e o comportamento previsto nos requisitos.

A descrição desses estados não significa que já tenham sido implementados ou verificados.

## 8. Acessibilidade

A interface deve considerar princípios de acessibilidade desde o planejamento visual.

Diretrizes propostas:

- Utilizar contraste adequado entre texto, fundo, bordas e controles.
- Manter uma hierarquia consistente de títulos.
- Utilizar textos legíveis e rótulos compreensíveis.
- Permitir a identificação visual do foco dos elementos interativos.
- Considerar a navegação por teclado nos controles interativos.
- Evitar que informações dependam exclusivamente de cores.
- Utilizar rótulos que expressem a finalidade dos campos e das ações.
- Distinguir mensagens informativas de mensagens de erro.
- Preservar a compreensão das informações em diferentes tamanhos de tela.

Os critérios técnicos específicos de acessibilidade ainda deverão ser definidos conforme as necessidades do produto. A presença dessas diretrizes no documento não representa uma certificação ou validação de acessibilidade.

## 9. Responsividade

A interface deve adaptar sua organização a computadores e dispositivos móveis.

Diretrizes propostas:

- Reorganizar os cartões conforme a largura disponível.
- Adaptar o campo de pesquisa e os filtros para telas menores.
- Evitar rolagem horizontal desnecessária.
- Preservar a legibilidade dos títulos, descrições e metadados.
- Manter as ações principais identificáveis e utilizáveis em telas sensíveis ao toque.
- Evitar que informações ou ações de acesso sejam ocultadas em telas menores.

Os pontos de quebra e os valores específicos de espaçamento ainda deverão ser definidos no detalhamento visual.

## 10. Decisões confirmadas, hipóteses e pendências

### 10.1. Decisões confirmadas

- A direção visual inicial será minimalista, com predominância de preto, branco e tons de cinza.
- O MVP terá catálogo, pesquisa, filtros e detalhes dos materiais.
- O acesso poderá ocorrer por links externos ou arquivos hospedados na plataforma.
- A visualização prévia dos materiais está fora do MVP.
- A interface deve contemplar estados de ausência de resultados e ausência de forma de acesso.

### 10.2. Hipóteses de design

- Uma interface visualmente simples poderá facilitar a leitura das informações.
- Uma hierarquia clara poderá ajudar os professores a identificar materiais e ações.
- A distinção visual entre as modalidades de acesso poderá reduzir ambiguidades.
- Estados informativos bem definidos poderão facilitar a compreensão de situações sem resultados ou sem acesso.

Essas hipóteses são princípios de planejamento, não resultados comprovados por testes com usuários.

### 10.3. Pendências

- Confirmar se os tokens de cor correspondem ao protótipo visual existente.
- Definir a família tipográfica e os estilos tipográficos finais.
- Confirmar a escala definitiva de espaçamento.
- Detalhar a apresentação dos filtros em diferentes tamanhos de tela.
- Definir os rótulos finais das ações de acesso.
- Especificar os estados visuais para links e arquivos indisponíveis.
- Detalhar os critérios de acessibilidade aplicáveis ao produto.
- Definir os pontos de quebra do layout responsivo.

As pendências deverão ser resolvidas e registradas antes de os valores correspondentes serem tratados como especificações definitivas.

## 11. Evolução do Design System

Este documento representa uma proposta inicial de Design System para o EduMaterial.

A evolução deverá acompanhar as decisões documentadas de produto, a arquitetura da informação e os fluxos de uso. Alterações nos tokens, componentes ou estados deverão ser registradas para preservar a coerência entre os artefatos de design.

A confirmação de que os componentes estão implementados ou funcionando deverá ocorrer apenas quando houver evidências correspondentes nas etapas futuras do projeto.

## 12. Status da documentação

**Status atual:** proposta de Design System em revisão documental.

O projeto está concentrado na consolidação da documentação de produto e UX/UI. A implementação, a verificação técnica e os testes com usuários não são considerados concluídos nem fazem parte desta etapa.

A coleta de respostas por meio do Google Forms foi abandonada. Portanto, as diretrizes deste documento não devem ser apresentadas como resultados de pesquisa com professores. Eventuais dados ou cenários simulados devem ser identificados como fictícios e não podem ser tratados como evidências empíricas.
