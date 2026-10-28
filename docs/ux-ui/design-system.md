# Design System — EduMaterial

**Versão:** 0.3  
**Status:** Em revisão documental  
**Escopo:** MVP do EduMaterial

## 1. Objetivo

Documentar a direção visual, os tokens de design e os componentes previstos para a interface do EduMaterial, buscando manter consistência entre as diferentes áreas da plataforma.

Este documento estabelece uma proposta inicial para o MVP. Os valores e padrões apresentados são referências de planejamento e deverão ser conferidos com o protótipo visual existente, caso aplicável, antes de serem tratados como definições finais.

A documentação descreve uma interface planejada. Não significa que os componentes tenham sido implementados, verificados ou validados com usuários reais.

## 2. Direção visual

A direção visual proposta é minimalista, com predominância de preto, branco e tons de cinza.

A interface deve priorizar a organização das informações, a leitura dos materiais e a identificação das ações disponíveis, evitando elementos decorativos que não contribuam para a experiência de uso.

### Princípios visuais

- **Clareza:** apresentar informações e ações de maneira compreensível.
- **Simplicidade:** evitar elementos visuais desnecessários.
- **Consistência:** utilizar padrões semelhantes para componentes equivalentes.
- **Hierarquia:** destacar títulos, informações relevantes e ações principais.
- **Legibilidade:** favorecer a leitura de descrições e metadados.
- **Responsividade:** preservar a compreensão e a utilização em diferentes tamanhos de tela.
- **Acessibilidade:** considerar contraste, foco visível, navegação por teclado e identificação textual das ações.

## 3. Cores

A paleta inicial proposta utiliza preto, branco e tons de cinza.

| Token | Valor de referência | Aplicação prevista |
|---|---|---|
| `color-background` | `#FFFFFF` | Fundo principal |
| `color-surface` | `#FFFFFF` | Cartões e superfícies de conteúdo |
| `color-text-primary` | `#111111` | Títulos e textos principais |
| `color-text-secondary` | `#666666` | Descrições e informações auxiliares |
| `color-border` | `#E5E5E5` | Bordas e divisórias |
| `color-surface-muted` | `#F5F5F5` | Fundos secundários |
| `color-action` | `#111111` | Ações principais |
| `color-action-text` | `#FFFFFF` | Texto sobre ações principais |

Os valores são referências iniciais. Antes de serem tratados como definitivos, deverão ser confrontados com o arquivo de design e avaliados quanto à legibilidade e ao contraste.

### 3.1. Uso das cores

- O fundo principal deve favorecer a leitura.
- Tons de cinza podem separar áreas e destacar informações secundárias.
- As ações principais devem apresentar contraste suficiente com o fundo.
- A cor não deve ser o único meio de indicar erros, estados ou diferenças entre componentes.
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

A família tipográfica, os tamanhos, os pesos e a altura de linha deverão ser definidos ou confirmados durante a consolidação do design visual.

## 5. Espaçamento e organização

O espaçamento deve contribuir para a leitura, a separação dos conteúdos e a consistência entre componentes.

As diretrizes iniciais são:

- Manter espaçamentos consistentes entre elementos equivalentes.
- Separar visualmente o conteúdo principal das informações auxiliares.
- Evitar cartões excessivamente densos.
- Preservar áreas clicáveis adequadas para controles e ações.
- Ajustar a disposição dos componentes para diferentes tamanhos de tela.

A escala numérica de espaçamento, os raios de borda e outras medidas ainda precisam ser confirmados no design visual.

## 6. Componentes previstos

### 6.1. Cabeçalho

Deve identificar a plataforma e disponibilizar os elementos de navegação definidos para o MVP.

### 6.2. Campo de pesquisa

Deve possuir identificação compreensível, permitir a inserção de palavras-chave e apresentar uma ação clara para iniciar ou atualizar a pesquisa.

### 6.3. Filtros

Devem permitir selecionar tipo de material e etapa de ensino. A interface deve indicar os critérios ativos e permitir removê-los.

As opções disponíveis e o comportamento da combinação com a pesquisa ainda precisam ser definidos.

### 6.4. Cartão de material

Deve apresentar informações resumidas para identificar o recurso e permitir o acesso aos detalhes.

O conjunto definitivo de informações do cartão depende da definição dos campos do catálogo.

### 6.5. Botões e links

As ações devem possuir rótulos compreensíveis e aparência consistente. Links externos e ações relacionadas a arquivos devem ser identificáveis como formas de acesso distintas.

### 6.6. Estado sem resultados

Deve informar quando uma pesquisa ou filtragem não encontrar materiais e orientar o usuário a ajustar os critérios.

### 6.7. Estado de catálogo vazio

Deve informar que não existem materiais cadastrados para exibição. Esse estado não deve ser confundido com uma pesquisa sem resultados.

### 6.8. Detalhes do material

Deve organizar os metadados, a descrição, as orientações de uso e as informações de origem disponíveis.

### 6.9. Acesso ao material

Deve apresentar as opções cadastradas para o recurso: link externo, arquivo hospedado na plataforma ou ambas as opções.

### 6.10. Estado sem forma de acesso

Deve informar quando não houver link externo nem arquivo disponível, sem apresentar uma ação de acesso indisponível.

### 6.11. Estado de falha de acesso

A apresentação de mensagens para links ou arquivos indisponíveis deverá ser definida posteriormente, mantendo a clareza sobre a impossibilidade de concluir a ação.

## 7. Estados dos componentes

Os componentes interativos deverão considerar, conforme sua função, estados como:

- Padrão;
- Foco;
- Selecionado;
- Desabilitado;
- Erro ou indisponibilidade;
- Carregamento, quando aplicável;
- Ausência de resultados.

A aparência e o comportamento específicos de cada estado ainda deverão ser detalhados na fase de design.

## 8. Acessibilidade e responsividade

A proposta visual deverá considerar:

- Contraste suficiente entre texto e fundo;
- Hierarquia de títulos compreensível;
- Rótulos claros para campos e controles;
- Foco visível durante a navegação por teclado;
- Identificação textual de ações;
- Estados que não dependam exclusivamente de cor;
- Adaptação dos componentes a diferentes larguras de tela;
- Legibilidade das informações em cartões e páginas de detalhes.

Essas diretrizes são critérios de planejamento. Sua conformidade deverá ser verificada em uma etapa posterior, caso o projeto avance para implementação.

## 9. Decisões, hipóteses e pendências

### Decisões confirmadas

- A direção visual proposta é minimalista.
- A paleta institucional de referência utiliza preto, branco e tons de cinza.
- A interface deve priorizar clareza, consistência, legibilidade e acessibilidade.
- Os componentes devem apoiar catálogo, pesquisa, filtros, detalhes e acesso aos materiais.

### Hipóteses

Uma interface visualmente consistente pode facilitar a compreensão das informações e das ações disponíveis. Essa expectativa ainda não foi validada por testes com usuários reais.

### Pendências

- Confirmar os tokens de cor no design visual;
- Definir família tipográfica, tamanhos e pesos;
- Definir a escala de espaçamento e outros valores visuais;
- Confirmar os campos dos cartões e dos detalhes;
- Especificar visualmente os estados dos componentes;
- Verificar os critérios de acessibilidade em uma etapa posterior.

## 10. Documentos relacionados

- [`product-brief.md`](../product/product-brief.md)
- [`requisitos.md`](../product/requisitos.md)
- [`arquitetura-da-informacao.md`](./arquitetura-da-informacao.md)
- [`user-flow.md`](./user-flow.md)
- [`objetivos-de-ux.md`](./objetivos-de-ux.md)

## 11. Status da documentação

Este Design System descreve uma direção visual inicial para o MVP. Os valores de referência não devem ser tratados como implementados ou validados até que sejam confirmados no design visual e verificados na etapa apropriada.

O documento deverá permanecer alinhado à arquitetura da informação, aos requisitos e aos fluxos previstos para o produto.
