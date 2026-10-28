# Design System — EduMaterial

**Versão:** 0.3  
**Status:** Em revisão documental

## 1. Objetivo

Documentar os princípios visuais, os tokens de design, os componentes e os estados de interface previstos para o EduMaterial, promovendo consistência visual, clareza de navegação, acessibilidade e responsividade.

Este documento descreve a direção visual proposta para o MVP. Os valores apresentados são referências iniciais e deverão ser conferidos com os estilos efetivamente utilizados no Figma antes de serem tratados como definitivos.

A documentação do design system não significa que os componentes já estejam implementados ou que sua acessibilidade tenha sido verificada.

## 2. Direção visual

A identidade visual inicial do EduMaterial adota uma abordagem minimalista, com predominância de preto, branco e tons de cinza.

A interface deve priorizar a organização das informações e a facilidade de uso, evitando elementos decorativos que não contribuam para a compreensão ou a navegação.

### 2.1 Princípios visuais

- **Clareza:** apresentar informações e ações de maneira compreensível.
- **Simplicidade:** reduzir elementos desnecessários e evitar sobrecarga visual.
- **Consistência:** utilizar padrões semelhantes para componentes que desempenham funções equivalentes.
- **Hierarquia:** destacar títulos, ações principais e informações relevantes.
- **Legibilidade:** manter textos e controles fáceis de identificar e utilizar.
- **Acessibilidade:** considerar contraste, navegação por teclado, foco visível e identificação compreensível dos controles.
- **Responsividade:** adaptar a organização dos elementos a diferentes tamanhos de tela.

## 3. Cores

A paleta inicial é monocromática. Os tokens abaixo representam valores de referência, ainda sujeitos à confirmação no arquivo de design.

| Token | Valor de referência | Aplicação |
|---|---|---|
| `color-background` | `#FFFFFF` | Fundo principal das páginas. |
| `color-surface` | `#FFFFFF` | Cartões e superfícies de conteúdo. |
| `color-text-primary` | `#111111` | Títulos e textos principais. |
| `color-text-secondary` | `#666666` | Descrições e informações auxiliares. |
| `color-border` | `#E5E5E5` | Bordas, divisórias e separadores. |
| `color-surface-muted` | `#F5F5F5` | Fundos secundários e áreas de apoio. |
| `color-action` | `#111111` | Fundo de ações principais. |
| `color-action-text` | `#FFFFFF` | Texto de ações principais. |

### 3.1 Regras de aplicação

- Utilizar o contraste entre fundo e texto para estabelecer hierarquia.
- Manter consistência na aplicação das cores em componentes equivalentes.
- Não depender exclusivamente da cor para comunicar estados, erros, seleção ou disponibilidade.
- Utilizar rótulos, ícones ou outros indicadores complementares quando necessário.
- Conferir o contraste dos pares de cores antes da implementação.

A paleta não deve ser considerada final até que os valores sejam comparados com o Figma e verificados em relação aos requisitos de acessibilidade.

## 4. Tipografia

A tipografia deve favorecer a leitura de textos informativos, descrições de materiais, metadados e orientações de acesso.

### 4.1 Hierarquia tipográfica

| Estilo | Aplicação |
|---|---|
| Título principal | Nome da página ou mensagem principal. |
| Título de seção | Organização dos grupos de conteúdo. |
| Título de cartão | Identificação do material no catálogo. |
| Texto de corpo | Descrições e informações principais. |
| Texto auxiliar | Categorias, metadados e orientações complementares. |
| Texto de controle | Rótulos de campos, filtros e botões. |

### 4.2 Regras tipográficas

- Manter uma hierarquia consistente entre títulos e textos.
- Priorizar a legibilidade em diferentes tamanhos de tela.
- Evitar textos auxiliares excessivamente pequenos.
- Utilizar pesos tipográficos de forma consistente.
- Não utilizar apenas o tamanho ou o peso visual para transmitir informações essenciais.
- Definir família tipográfica, tamanhos, pesos e alturas de linha a partir dos estilos efetivamente utilizados no Figma.

Os valores tipográficos exatos permanecem pendentes de confirmação.

## 5. Espaçamento e organização

A interface deve utilizar uma escala de espaçamento consistente para estabelecer relações entre elementos, organizar seções e manter o alinhamento visual.

Recomenda-se utilizar uma escala baseada em múltiplos de 4 px como referência inicial.

| Referência | Aplicação típica |
|---|---|
| 4 px | Pequenos intervalos entre elementos relacionados. |
| 8 px | Espaçamento entre ícones, textos e controles próximos. |
| 16 px | Espaçamento interno de componentes e separação entre elementos. |
| 24 px | Separação entre grupos de conteúdo. |
| 32 px | Separação entre seções ou áreas principais. |

Esses valores são referências propostas, não medidas confirmadas do projeto. A escala final deverá ser compatibilizada com o Figma.

O espaçamento deve refletir a hierarquia da informação, evitando tanto a aglomeração de elementos quanto distâncias que prejudiquem a compreensão das relações entre eles.

## 6. Componentes de interface

### 6.1 Cabeçalho

**Finalidade:** identificar o EduMaterial e oferecer acesso à navegação principal.

**Diretrizes:**

- Manter alinhamento e espaçamento consistentes.
- Apresentar os elementos de navegação de forma compreensível.
- Evitar excesso de elementos que disputem atenção.
- Adaptar a organização do conteúdo a telas menores.

### 6.2 Campo de pesquisa

**Finalidade:** permitir que o usuário informe palavras-chave para localizar materiais educacionais.

**Diretrizes:**

- Apresentar um rótulo ou indicação compreensível.
- Utilizar texto de orientação que ajude a entender a finalidade do campo.
- Exibir um estado de foco claramente identificável.
- Permitir a edição da consulta.
- Apresentar uma ação de pesquisa identificável, quando aplicável ao comportamento definido para a interface.

A busca deverá ser compatível com as regras funcionais documentadas: campos pesquisáveis, correspondência parcial, tratamento de maiúsculas e minúsculas, acentuação e ordenação por relevância.

Essas regras funcionais pertencem à especificação do produto; o design system define como os controles e seus estados serão apresentados visualmente.

### 6.3 Filtros

**Finalidade:** restringir os materiais apresentados de acordo com critérios selecionados.

Os filtros previstos para o MVP são:

- Tipo de material.
- Etapa de ensino.

**Diretrizes:**

- Identificar cada filtro com um rótulo compreensível.
- Diferenciar visualmente os estados selecionado e não selecionado.
- Indicar de maneira clara quais critérios estão ativos.
- Tornar as ações de alteração ou remoção de filtros compreensíveis.
- Adaptar os controles a telas menores sem prejudicar sua utilização.

O comportamento exato de combinação e remoção dos filtros deverá seguir as regras estabelecidas nos requisitos funcionais.

### 6.4 Cartão de material

**Finalidade:** apresentar informações resumidas sobre um recurso no catálogo ou nos resultados da busca.

**Conteúdo prioritário:**

- Título.
- Tipo de material.
- Etapa de ensino, quando disponível.
- Resumo ou descrição curta, quando disponível.

**Diretrizes:**

- Priorizar o título e as informações necessárias à identificação do recurso.
- Manter a hierarquia tipográfica consistente.
- Evitar que metadados secundários concorram visualmente com o título.
- Indicar de maneira compreensível quando o cartão ou um de seus elementos for interativo.
- Não presumir a existência de arquivo ou link externo apenas pela apresentação do cartão.

### 6.5 Botões e ações

**Finalidade:** permitir a execução de ações, como pesquisar, limpar filtros, retornar aos resultados ou acessar um material.

**Diretrizes:**

- Diferenciar ações principais de ações secundárias.
- Utilizar rótulos que descrevam o resultado esperado.
- Manter dimensões e espaçamentos consistentes.
- Apresentar estados visuais distintos para foco, interação e desabilitação.
- Garantir que a finalidade de cada ação seja compreensível sem depender exclusivamente de um ícone.

A interface não deve apresentar como disponível uma ação cuja funcionalidade não exista ou não se aplique ao estado atual.

### 6.6 Página de detalhes

**Finalidade:** apresentar as informações de um material selecionado e as formas de acesso disponíveis.

**Conteúdo previsto:**

- Título.
- Tipo de material.
- Etapa de ensino, quando disponível.
- Resumo e descrição.
- Orientações complementares, quando disponíveis.
- Informações de autoria, origem e condições de uso, quando disponíveis e previstas.
- Ações de acesso aplicáveis ao material.

A página de detalhes não implica visualização prévia do conteúdo do material. Essa funcionalidade está fora do escopo atual do MVP.

### 6.7 Ações de acesso

A interface deve distinguir visualmente as formas de acesso disponíveis.

| Situação do material | Apresentação esperada |
|---|---|
| Apenas link externo | Ação identificada como acesso à fonte externa. |
| Apenas arquivo hospedado | Ação identificada como acesso ou download do arquivo, conforme a implementação definida. |
| Link externo e arquivo hospedado | Duas ações claramente diferenciadas. |
| Nenhuma forma de acesso | Informações do material sem ação de acesso indisponível. |

Os rótulos devem ajudar o usuário a compreender para onde será direcionado ou qual recurso será aberto.

### 6.8 Estado sem resultados

**Finalidade:** informar que uma pesquisa ou combinação de filtros não encontrou materiais correspondentes.

**Diretrizes:**

- Apresentar uma mensagem clara.
- Diferenciar a ausência de resultados de um catálogo sem materiais cadastrados.
- Orientar o usuário a revisar a consulta ou os filtros, quando apropriado.
- Evitar mensagens que atribuam o problema ao usuário.

### 6.9 Estado de catálogo vazio

**Finalidade:** informar que não existem materiais disponíveis para exibição.

A mensagem deve refletir a situação real do catálogo. Não deve ser utilizada para representar uma busca sem correspondências quando existem materiais cadastrados.

### 6.10 Estados de erro e acesso indisponível

**Finalidade:** comunicar falhas que impeçam o carregamento ou o acesso a um recurso.

**Diretrizes:**

- Informar o problema em linguagem compreensível.
- Evitar mensagens técnicas desnecessárias para o usuário.
- Oferecer nova tentativa quando essa ação for viável.
- Não indicar sucesso quando o acesso falhar.
- Diferenciar a ausência de uma forma de acesso cadastrada de uma falha ao tentar utilizar um link ou arquivo disponível.

## 7. Estados dos componentes

Os componentes interativos devem considerar os estados relevantes para sua função.

| Estado | Diretriz visual e funcional |
|---|---|
| Padrão | Apresentação normal do componente. |
| Hover | Indicação complementar de interação em dispositivos compatíveis. |
| Foco por teclado | Destaque visível para o elemento que recebeu foco. |
| Selecionado | Indicação clara da opção ativa, especialmente nos filtros. |
| Desabilitado | Aparência que indique indisponibilidade e comportamento coerente com essa condição. |
| Carregamento | Indicação de processamento quando houver uma operação em andamento. |
| Erro | Comunicação clara da falha e, quando possível, orientação para recuperação. |

O estado de hover não deve ser o único indicador de interatividade, pois não está disponível da mesma forma em todos os dispositivos.

Os estados devem ser definidos no design e verificados durante a implementação futura.

## 8. Acessibilidade

O design system deve apoiar uma experiência acessível, considerando os seguintes aspectos:

- Contraste adequado entre texto, fundo, bordas e controles.
- Hierarquia tipográfica consistente.
- Rótulos compreensíveis para campos, filtros e botões.
- Indicação visível de foco.
- Navegação por teclado nos elementos interativos.
- Identificação clara de estados selecionados, desabilitados e de erro.
- Informações que não dependam exclusivamente de cores.
- Textos legíveis em diferentes tamanhos de tela.
- Links e ações com finalidades compreensíveis.
- Mensagens de erro e estados vazios com linguagem clara.

Sempre que possível, a verificação de contraste deve utilizar os critérios aplicáveis das diretrizes WCAG. A conformidade não deve ser declarada sem avaliação apropriada.

## 9. Responsividade

A interface deverá adaptar-se a computadores, tablets e dispositivos móveis.

Durante o design e a implementação futura, deverão ser considerados:

- Reorganização dos cartões em telas menores.
- Adaptação do campo de pesquisa e dos filtros.
- Preservação da hierarquia das informações.
- Ausência de rolagem horizontal desnecessária.
- Legibilidade dos textos.
- Espaçamento adequado entre controles interativos.
- Facilidade para acionar botões e links em telas sensíveis ao toque.
- Apresentação compreensível dos estados vazios e das mensagens de erro.

Os pontos de quebra e as regras exatas de adaptação ainda precisam ser definidos a partir do layout e do protótipo.

## 10. Relação com a arquitetura da informação

O design system deve oferecer componentes capazes de representar a estrutura prevista na arquitetura da informação:

- Catálogo de materiais.
- Campo de pesquisa.
- Filtros por tipo de material e etapa de ensino.
- Cartões de resultados.
- Página de detalhes.
- Ações de acesso.
- Estados de catálogo vazio e pesquisa sem resultados.
- Estados de carregamento, erro e acesso indisponível.

Os componentes devem refletir os requisitos funcionais sem introduzir comportamentos que não tenham sido definidos para o produto.

## 11. Itens pendentes de definição

Antes de considerar o design system consolidado, será necessário:

- Conferir a paleta de cores com o Figma.
- Definir a família tipográfica e os tamanhos de texto.
- Confirmar a escala de espaçamento.
- Definir dimensões, variações e estados dos componentes.
- Estabelecer os pontos de quebra para responsividade.
- Verificar os contrastes dos pares de cores utilizados.
- Detalhar a apresentação das ações de acesso.
- Definir padrões visuais para carregamento, erros e indisponibilidade.
- Registrar eventuais alterações em relação ao protótipo.

Os itens pendentes não devem ser tratados como decisões confirmadas até que sejam revisados.

## 12. Evolução do design system

Este documento representa a direção inicial do design system do EduMaterial.

Os tokens, componentes e estados deverão evoluir conforme as decisões de design forem consolidadas e o produto avançar para prototipação e implementação.

Alterações relevantes deverão ser registradas e refletidas nos documentos relacionados, de modo a manter a consistência entre a interface planejada, o Figma e a implementação futura.

## 13. Considerações metodológicas

Este documento descreve diretrizes visuais propostas. Não comprova que os componentes estejam implementados, que a interface esteja acessível ou que tenha sido avaliada por usuários.

A revisão atual é documental. A verificação técnica, a avaliação de acessibilidade e os testes de usabilidade deverão ocorrer em etapas futuras, caso sejam executados.

## 14. Documentos relacionados

- `README.md`
- `docs/product/product-brief.md`
- `docs/product/requisitos.md`
- `docs/product/historias-de-usuario.md`
- `docs/product/backlog.md`
- `docs/ux-ui/arquitetura-da-informacao.md`
- `docs/ux-ui/objetivos-de-ux.md`
- `docs/ux-ui/user-flow.md`
