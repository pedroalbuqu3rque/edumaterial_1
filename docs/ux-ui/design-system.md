# Design System — EduMaterial

## 1. Objetivo

Documentar os padrões visuais e os componentes utilizados na interface do EduMaterial, garantindo consistência entre as telas do produto.

Este documento descreve a direção visual inicial do MVP. Os valores devem ser conferidos e ajustados conforme os estilos efetivamente utilizados no Figma.

## 2. Direção visual

A interface segue uma abordagem minimalista, com predominância de preto, branco e tons de cinza.

Os princípios visuais são:

- **Clareza:** priorizar a leitura e a identificação das informações.
- **Simplicidade:** evitar elementos decorativos sem função.
- **Consistência:** utilizar os mesmos padrões para componentes semelhantes.
- **Hierarquia:** destacar títulos, ações principais e informações relevantes.
- **Responsividade:** preservar a legibilidade em diferentes tamanhos de tela.

## 3. Cores

| Token | Valor inicial | Aplicação |
|---|---|---|
| `color-background` | `#FFFFFF` | Fundo principal |
| `color-surface` | `#FFFFFF` | Cartões e superfícies |
| `color-text-primary` | `#111111` | Títulos e textos principais |
| `color-text-secondary` | `#666666` | Descrições e informações auxiliares |
| `color-border` | `#E5E5E5` | Bordas e divisórias |
| `color-surface-muted` | `#F5F5F5` | Fundos secundários |
| `color-action` | `#111111` | Ações principais |
| `color-action-text` | `#FFFFFF` | Texto sobre ações principais |

**Nota:** estes são valores de referência propostos. Antes da implementação, confirme se correspondem às cores usadas nas telas do Figma.

## 4. Tipografia

A tipografia deve facilitar a leitura e estabelecer uma hierarquia visual clara.

| Estilo | Uso |
|---|---|
| Título principal | Nome da página ou mensagem principal |
| Título de seção | Organização dos grupos de conteúdo |
| Título de cartão | Identificação do material |
| Texto de corpo | Descrições e informações |
| Texto auxiliar | Categorias, metadados e orientações |

A família tipográfica e os tamanhos exatos devem ser definidos a partir dos estilos existentes no Figma, evitando divergências entre o protótipo e o código.

## 5. Espaçamento e organização

O layout deve utilizar espaçamentos consistentes para organizar os elementos.

Recomenda-se adotar uma escala baseada em múltiplos de 4 px, ajustada conforme a necessidade dos componentes.

Exemplos de aplicação:

- Pequenos intervalos entre ícones e textos.
- Espaçamento interno uniforme em botões e campos.
- Distância consistente entre cartões.
- Separação maior entre seções da página.

Os valores finais devem ser conferidos no arquivo de design.

## 6. Componentes

### 6.1. Cabeçalho

Responsável pela identificação do EduMaterial e pela navegação principal.

Deve manter alinhamento, espaçamento e hierarquia visual consistentes entre as telas.

### 6.2. Campo de pesquisa

Permite informar palavras-chave para localizar materiais.

Deve apresentar um rótulo ou indicação compreensível, além de um estado visual claro de foco.

### 6.3. Filtros

Permitem restringir os materiais por critérios disponíveis, como tipo de material e etapa de ensino.

Os estados selecionado e não selecionado devem ser visualmente distinguíveis.

### 6.4. Cartão de material

Apresenta um resumo do recurso no catálogo.

Deve priorizar o título e informações úteis para identificar o material. Quando clicável, sua aparência e seu comportamento devem indicar essa possibilidade.

### 6.5. Botões

Devem diferenciar ações principais de ações secundárias.

O texto precisa descrever claramente o resultado esperado, como pesquisar, limpar filtros ou abrir um material.

### 6.6. Estado sem resultados

Informa que a pesquisa não encontrou materiais correspondentes.

Deve apresentar uma mensagem clara e, quando aplicável, orientar o usuário a alterar os termos ou limpar os filtros.

### 6.7. Página de detalhes

Organiza as informações de um material selecionado e destaca a ação de acesso ao recurso, quando houver um link disponível.

## 7. Estados dos componentes

Os componentes interativos devem considerar, conforme sua função:

- Padrão.
- Hover.
- Foco por teclado.
- Selecionado.
- Desabilitado.
- Carregamento ou erro, quando aplicável.

Os estados devem ser implementados e verificados durante o desenvolvimento, não apenas representados visualmente.

## 8. Acessibilidade

A interface deve buscar:

- Contraste adequado entre texto e fundo.
- Textos legíveis e hierarquia de títulos consistente.
- Navegação por teclado nos elementos interativos.
- Indicação visível de foco.
- Rótulos compreensíveis para campos e botões.
- Informações que não dependam exclusivamente de cores para serem compreendidas.

## 9. Responsividade

A interface deve se adaptar a computadores e dispositivos móveis.

Durante a implementação, verificar:

- Reorganização dos cartões em telas menores.
- Adaptação dos filtros e do campo de pesquisa.
- Ausência de rolagem horizontal desnecessária.
- Legibilidade dos textos.
- Facilidade para acionar botões e links em telas sensíveis ao toque.

## 10. Evolução do Design System

Este documento representa a primeira versão do Design System do EduMaterial.

Os tokens, componentes e estados deverão ser revisados conforme a implementação e os testes do produto. Alterações relevantes devem ser registradas para manter a documentação alinhada à interface.
