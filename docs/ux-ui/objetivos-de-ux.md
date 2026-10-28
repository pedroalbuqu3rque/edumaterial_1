# Objetivos de UX — EduMaterial

**Versão:** 0.2  
**Status:** Proposta documental revisada  
**Escopo:** MVP do EduMaterial

## 1. Objetivo do documento

Este documento define os objetivos de experiência do usuário (UX) para o MVP do EduMaterial, uma proposta de plataforma digital voltada a professores que procuram materiais didáticos para suas aulas.

Os objetivos orientam as decisões de arquitetura da informação, navegação, conteúdo e interface, buscando tornar a descoberta, a seleção e o acesso aos materiais mais claros e compreensíveis.

Os objetivos descritos representam resultados pretendidos. Eles ainda não foram validados por pesquisa com usuários reais nem avaliados por testes de usabilidade.

## 2. Público prioritário

O público prioritário do EduMaterial é formado por professores que procuram materiais didáticos para utilizar em suas aulas.

A proposta considera que esses professores precisam encontrar recursos relacionados aos conteúdos que pretendem trabalhar, compreender as características dos materiais e identificar como acessá-los.

Essas necessidades são hipóteses que orientam o planejamento da experiência. Não devem ser apresentadas como conclusões de entrevistas, questionários ou testes com professores.

## 3. Contexto do problema

O EduMaterial parte da hipótese de que a procura por materiais didáticos pode exigir que os professores consultem diferentes fontes e avaliem os recursos encontrados antes de utilizá-los em suas aulas.

A proposta de experiência consiste em reunir informações sobre materiais em um catálogo organizado, com busca por palavras-chave, filtros e páginas de detalhes.

A plataforma também deverá deixar claras as formas de acesso disponíveis: links externos ou arquivos hospedados diretamente na plataforma.

A coleta de respostas por meio do Google Forms foi abandonada. Portanto, não existem resultados desse questionário que possam ser utilizados como evidência empírica para confirmar a existência, a frequência ou a intensidade das dificuldades descritas.

## 4. Objetivos de experiência

### OUX-001 — Facilitar a descoberta de materiais

**Objetivo:** permitir que o professor explore o catálogo e identifique materiais potencialmente relevantes para suas aulas.

**Diretrizes de UX:**
- Organizar os materiais de maneira consistente.
- Destacar o título e as informações essenciais de cada recurso.
- Manter uma hierarquia visual que facilite a exploração do catálogo.
- Permitir a navegação dos materiais para suas respectivas páginas de detalhes.

**Resultado esperado:** o professor consegue compreender a organização do catálogo e identificar como consultar um material.

**Como avaliar futuramente:** observar se participantes conseguem localizar e abrir materiais em tarefas definidas para uma avaliação de usabilidade.

### OUX-002 — Tornar a pesquisa compreensível

**Objetivo:** permitir que o professor pesquise materiais por palavras-chave relacionadas ao recurso que procura.

**Diretrizes de UX:**
- Apresentar um campo de pesquisa claramente identificado.
- Tornar compreensível a finalidade do campo.
- Apresentar os resultados de maneira organizada.
- Informar quando uma pesquisa não retornar materiais.
- Permitir que o professor altere os termos da pesquisa.

**Resultado esperado:** o professor compreende como realizar uma pesquisa e interpretar os resultados apresentados.

**Como avaliar futuramente:** observar se participantes conseguem realizar pesquisas com termos fornecidos em tarefas de avaliação e compreender as respostas do sistema.

### OUX-003 — Facilitar o refinamento dos resultados

**Objetivo:** permitir que o professor refine os materiais apresentados por tipo de material e etapa de ensino.

**Diretrizes de UX:**
- Identificar claramente os critérios de filtragem.
- Diferenciar filtros ativos de filtros não selecionados.
- Tornar compreensível como remover ou alterar os filtros.
- Apresentar os resultados de acordo com os critérios aplicados.
- Informar quando não houver materiais correspondentes aos filtros.

**Resultado esperado:** o professor consegue compreender quais critérios estão ativos e como eles afetam os resultados.

**Como avaliar futuramente:** observar se participantes conseguem aplicar, combinar e remover filtros em tarefas de avaliação.

### OUX-004 — Apoiar a avaliação inicial de um material

**Objetivo:** fornecer informações que ajudem o professor a compreender as características de um recurso antes de acessá-lo.

**Diretrizes de UX:**
- Apresentar o título e as informações descritivas em uma hierarquia clara.
- Organizar os metadados de maneira consistente.
- Distinguir informações essenciais de informações complementares.
- Apresentar os dados disponíveis sem presumir informações ausentes.
- Permitir que o professor identifique a forma de acesso cadastrada.

**Resultado esperado:** o professor consegue compreender as informações apresentadas e identificar se possui elementos suficientes para decidir se deseja acessar o recurso.

**Como avaliar futuramente:** observar se participantes conseguem identificar informações relevantes em uma página de detalhes e explicar o que compreenderam sobre o material.

**Limite do MVP:** a visualização prévia do conteúdo dentro da plataforma não está incluída. A avaliação inicial dependerá das informações descritivas disponíveis.

### OUX-005 — Tornar claras as formas de acesso

**Objetivo:** permitir que o professor identifique como acessar um material e compreenda quando não existe uma forma de acesso cadastrada.

**Diretrizes de UX:**
- Distinguir visualmente o acesso por link externo do acesso a arquivo hospedado na plataforma.
- Utilizar rótulos claros para as ações de acesso.
- Informar quando o recurso direcionar o professor para um ambiente externo, quando pertinente.
- Não apresentar ações de acesso para recursos inexistentes.
- Informar quando não houver link nem arquivo disponível.
- Preservar as informações descritivas mesmo quando o material não tiver uma forma de acesso cadastrada.

**Resultado esperado:** o professor consegue identificar a modalidade de acesso disponível e compreender eventuais limitações.

**Como avaliar futuramente:** observar se participantes conseguem identificar a forma de acesso de um material e distinguir um link externo de um arquivo disponibilizado na plataforma.

### OUX-006 — Comunicar situações sem resultados ou sem acesso

**Objetivo:** ajudar o professor a compreender as situações em que não encontra materiais ou em que um material não possui uma forma de acesso disponível.

**Diretrizes de UX:**
- Diferenciar catálogo vazio de pesquisa sem resultados.
- Diferenciar ausência de acesso cadastrado de falha técnica.
- Utilizar mensagens diretas e compreensíveis.
- Orientar o usuário sobre ações possíveis quando isso for apropriado.
- Evitar mensagens que atribuam uma causa que não foi identificada.

**Resultado esperado:** o professor compreende a situação apresentada e consegue identificar o próximo passo disponível.

**Como avaliar futuramente:** observar se participantes interpretam corretamente mensagens de ausência de resultados, catálogo vazio e ausência de forma de acesso.

### OUX-007 — Manter a experiência compreensível em diferentes telas

**Objetivo:** preservar a compreensão das informações e a utilização das principais funcionalidades em computadores e dispositivos móveis.

**Diretrizes de UX:**
- Adaptar a organização dos materiais à largura disponível.
- Preservar a legibilidade de títulos, descrições e metadados.
- Manter a pesquisa e os filtros acessíveis.
- Evitar que as ações de consulta e acesso fiquem ocultas ou difíceis de identificar.
- Considerar a navegação por teclado e a identificação visual do foco.

**Resultado esperado:** a estrutura de navegação e as ações principais permanecem compreensíveis em diferentes tamanhos de tela.

**Como avaliar futuramente:** examinar a experiência em diferentes larguras de tela e realizar avaliações específicas de acessibilidade e usabilidade.

## 5. Princípios orientadores da experiência

Os seguintes princípios devem orientar as decisões de UX do EduMaterial.

### 5.1. Clareza

As informações, os controles e as mensagens devem comunicar suas finalidades de maneira direta.

### 5.2. Consistência

A nomenclatura e a apresentação dos materiais devem permanecer coerentes entre catálogo, resultados e detalhes.

### 5.3. Autonomia do professor

A plataforma deve apoiar a decisão do professor, oferecendo informações para que ele avalie a adequação do recurso aos seus objetivos pedagógicos, sem presumir que um material seja adequado a todas as situações.

### 5.4. Transparência

As informações apresentadas devem corresponder aos dados disponíveis. Ausências de informação e limitações de acesso devem ser comunicadas sem criar expectativas indevidas.

### 5.5. Simplicidade

A interface deve priorizar as ações essenciais do MVP, evitando elementos que não contribuam para a descoberta, a seleção ou o acesso aos materiais.

### 5.6. Acessibilidade

A experiência deve considerar legibilidade, contraste, navegação por teclado, foco visível e identificação textual das ações desde o planejamento da interface.

## 6. Relação com o escopo do MVP

Os objetivos de UX devem corresponder às funcionalidades previstas para a primeira versão.

| Funcionalidade | Objetivo de UX relacionado |
|---|---|
| Catálogo de materiais | OUX-001 — Facilitar a descoberta |
| Busca por palavras-chave | OUX-002 — Tornar a pesquisa compreensível |
| Filtros por tipo e etapa de ensino | OUX-003 — Facilitar o refinamento |
| Detalhes do material | OUX-004 — Apoiar a avaliação inicial |
| Acesso por link externo ou arquivo | OUX-005 — Tornar claras as formas de acesso |
| Mensagens de ausência de resultados ou acesso | OUX-006 — Comunicar situações sem resultados ou sem acesso |
| Adaptação a diferentes telas | OUX-007 — Manter a experiência compreensível |

A visualização prévia dos materiais, a edição de recursos e as funcionalidades de personalização não fazem parte dos objetivos de experiência do MVP.

## 7. Avaliação futura da experiência

Os objetivos definidos neste documento poderão orientar uma avaliação de usabilidade em uma etapa posterior do projeto.

Essa avaliação deverá ser planejada com tarefas relacionadas às funcionalidades do MVP, critérios de observação e formas de registro dos resultados.

Exemplos de tarefas futuras:

- Encontrar um material relacionado a determinado conteúdo.
- Pesquisar utilizando palavras-chave.
- Aplicar e remover filtros.
- Consultar as informações de um material.
- Identificar e utilizar a forma de acesso disponível.
- Interpretar uma situação sem resultados ou sem acesso.

Os resultados de uma eventual avaliação deverão ser documentados somente depois que ela for efetivamente realizada. Não devem ser antecipadas taxas de sucesso, níveis de satisfação ou conclusões sobre a facilidade de uso.

## 8. Decisões confirmadas, hipóteses e pendências

### 8.1. Decisões confirmadas

- O público prioritário é formado por professores que procuram materiais para suas aulas.
- A experiência deve contemplar catálogo, busca, filtros e detalhes dos materiais.
- Os filtros iniciais serão por tipo de material e etapa de ensino.
- O acesso aos materiais poderá ocorrer por links externos ou arquivos hospedados na plataforma.
- A visualização prévia não fará parte do MVP.
- A experiência deverá contemplar mensagens para ausência de resultados e ausência de forma de acesso.
- A implementação e o QA não fazem parte da etapa atual de revisão documental.

### 8.2. Hipóteses de experiência

- Um catálogo organizado poderá facilitar a descoberta de materiais.
- A pesquisa por palavras-chave poderá tornar a localização de recursos mais prática.
- Os filtros poderão ajudar o professor a refinar os resultados.
- Informações descritivas poderão apoiar a avaliação inicial dos materiais.
- A distinção entre formas de acesso poderá reduzir ambiguidades.

Essas hipóteses orientam o planejamento da experiência, mas não foram confirmadas por dados de pesquisa com professores.

### 8.3. Pendências

- Definir os campos de informação necessários para a avaliação inicial dos materiais.
- Definir as regras de busca e combinação de filtros.
- Definir os rótulos finais das ações de acesso.
- Especificar as mensagens para links e arquivos indisponíveis.
- Definir critérios observáveis e tarefas para uma futura avaliação de usabilidade.
- Estabelecer os critérios específicos de acessibilidade a serem considerados.

## 9. Limitações metodológicas

O EduMaterial está sendo desenvolvido como um estudo de caso de planejamento de produto digital.

A coleta de respostas por meio do Google Forms foi abandonada. Portanto, não existem resultados desse questionário que possam ser apresentados como evidência empírica sobre as necessidades, preferências ou comportamentos dos professores.

As necessidades e os problemas descritos neste documento são hipóteses de produto. Caso sejam utilizados dados ou cenários simulados para ilustrar tarefas ou situações de uso, eles deverão ser identificados explicitamente como fictícios.

Nenhum objetivo deste documento deve ser descrito como alcançado sem evidências correspondentes. A definição de objetivos não equivale à comprovação de que a experiência atende às necessidades dos usuários.

## 10. Status da documentação

**Status atual:** objetivos de UX em revisão documental.

Este documento deverá permanecer alinhado ao Product Brief, aos requisitos, às histórias de usuário, à arquitetura da informação, ao fluxo de uso e ao Design System.

A implementação, os testes de software, as atividades de QA e a avaliação com usuários pertencem a etapas posteriores e não fazem parte do trabalho documental atual.
