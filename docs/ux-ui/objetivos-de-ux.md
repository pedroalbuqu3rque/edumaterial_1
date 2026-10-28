# Objetivos de UX — EduMaterial

**Versão:** 0.3  
**Status:** Em revisão documental  
**Escopo:** MVP do EduMaterial

## 1. Objetivo do documento

Este documento define os objetivos de experiência do usuário (UX) para o MVP do EduMaterial, uma proposta de plataforma digital voltada a professores que procuram materiais didáticos para suas aulas.

Os objetivos orientam as decisões de arquitetura da informação, navegação, conteúdo e interface, buscando tornar a descoberta, a seleção e o acesso aos materiais mais claros e compreensíveis.

Os objetivos representam resultados pretendidos. Ainda não foram validados por pesquisa com usuários reais nem avaliados em testes de usabilidade.

## 2. Público prioritário

O público prioritário do EduMaterial é formado por professores que procuram materiais didáticos para utilizar em suas aulas.

A proposta considera que esses professores precisam localizar recursos relacionados aos conteúdos que pretendem trabalhar, compreender as características dos materiais e identificar como acessá-los.

Essas necessidades são hipóteses que orientam o planejamento da experiência. Não devem ser apresentadas como conclusões de entrevistas, questionários ou testes com professores.

## 3. Contexto do problema

O EduMaterial parte da hipótese de que a procura por materiais didáticos pode exigir que os professores consultem diferentes fontes e avaliem os recursos encontrados antes de utilizá-los em suas aulas.

A proposta de experiência consiste em reunir informações sobre materiais em um catálogo organizado, com pesquisa por palavras-chave, filtros e páginas de detalhes.

A plataforma deverá deixar claras as formas de acesso disponíveis: links externos, arquivos hospedados diretamente na plataforma ou ambas as opções.

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

**Avaliação futura:** observar se participantes conseguem localizar e abrir materiais em tarefas definidas para uma avaliação de usabilidade.

### OUX-002 — Tornar a pesquisa compreensível

**Objetivo:** permitir que o professor pesquise materiais por palavras-chave relacionadas ao recurso que procura.

**Diretrizes de UX:**

- Apresentar um campo de pesquisa claramente identificado.
- Tornar compreensível a finalidade do campo.
- Apresentar os resultados de maneira organizada.
- Informar quando uma pesquisa não retornar materiais.
- Permitir que o professor altere os termos da pesquisa.

**Resultado esperado:** o professor compreende como realizar uma pesquisa e interpretar os resultados apresentados.

**Avaliação futura:** observar se participantes conseguem realizar pesquisas com termos fornecidos e compreender as respostas do sistema.

### OUX-003 — Facilitar o uso dos filtros

**Objetivo:** permitir que o professor refine o catálogo por tipo de material e etapa de ensino.

**Diretrizes de UX:**

- Identificar claramente os filtros disponíveis.
- Apresentar as opções de forma compreensível.
- Indicar quais filtros estão ativos.
- Permitir a remoção dos filtros aplicados.
- Informar quando os critérios selecionados não retornarem materiais.

**Resultado esperado:** o professor consegue compreender e alterar os critérios de filtragem.

**Avaliação futura:** observar se participantes conseguem aplicar e remover filtros e interpretar os resultados.

### OUX-004 — Apoiar a avaliação inicial dos materiais

**Objetivo:** apresentar informações suficientes para que o professor compreenda inicialmente as características de um material antes de acessá-lo.

**Diretrizes de UX:**

- Identificar claramente o material na página de detalhes.
- Organizar os metadados e a descrição em uma hierarquia compreensível.
- Apresentar autoria, fonte e condições de utilização quando disponíveis e aplicáveis.
- Evitar depender de uma pré-visualização do conteúdo, pois ela não faz parte do MVP.

**Resultado esperado:** o professor consegue compreender as informações disponíveis sobre o recurso e decidir se deseja acessar o material.

**Avaliação futura:** observar se participantes conseguem identificar características relevantes de materiais apresentados em tarefas de avaliação.

### OUX-005 — Tornar as formas de acesso claras

**Objetivo:** permitir que o professor identifique como acessar cada material.

**Diretrizes de UX:**

- Identificar os links externos como opções de acesso.
- Identificar os arquivos hospedados na plataforma como opções distintas.
- Apresentar ambas as opções quando estiverem disponíveis.
- Informar quando não houver uma forma de acesso cadastrada.
- Evitar apresentar ações indisponíveis como se fossem funcionais.

**Resultado esperado:** o professor consegue reconhecer as opções disponíveis e compreender quando não existe uma forma de acesso cadastrada.

**Avaliação futura:** verificar se participantes identificam corretamente as opções de acesso em diferentes cenários.

### OUX-006 — Facilitar a compreensão de estados sem resultados

**Objetivo:** ajudar o professor a compreender quando não há materiais correspondentes à pesquisa ou aos filtros utilizados.

**Diretrizes de UX:**

- Informar claramente que nenhum material corresponde aos critérios utilizados.
- Permitir alterar os termos da pesquisa.
- Permitir remover ou modificar filtros.
- Diferenciar a ausência de resultados do catálogo vazio.

**Resultado esperado:** o professor compreende o motivo da ausência de resultados e identifica como tentar novamente.

**Avaliação futura:** observar se participantes conseguem recuperar-se de uma pesquisa sem resultados sem confundi-la com um catálogo vazio.

### OUX-007 — Preservar a compreensão em diferentes telas

**Objetivo:** planejar uma experiência legível e utilizável em diferentes tamanhos de tela.

**Diretrizes de UX:**

- Preservar a legibilidade dos títulos e das descrições.
- Adaptar a apresentação do catálogo e dos cartões à largura disponível.
- Manter controles e ações identificáveis.
- Evitar que informações essenciais sejam ocultadas ou apresentadas de forma confusa.

**Resultado esperado:** os elementos essenciais da experiência permanecem compreensíveis em diferentes tamanhos de tela.

**Avaliação futura:** verificar a apresentação dos principais fluxos em diferentes resoluções, caso o projeto avance para implementação.

## 5. Princípios gerais de experiência

Os objetivos de UX são orientados pelos seguintes princípios:

- **Clareza:** o usuário deve compreender as informações e as ações disponíveis.
- **Consistência:** componentes equivalentes devem apresentar comportamentos semelhantes.
- **Orientação:** o usuário deve conseguir entender onde está e como retornar ao catálogo.
- **Transparência:** a interface deve informar as formas de acesso e suas limitações.
- **Recuperação:** estados sem resultados devem permitir que o usuário ajuste os critérios utilizados.
- **Acessibilidade:** as informações e os controles devem ser planejados considerando diferentes formas de interação.
- **Integridade:** hipóteses de experiência não devem ser apresentadas como resultados comprovados.

## 6. Relação com o escopo do MVP

Os objetivos de UX estão relacionados às funcionalidades previstas para o MVP:

| Funcionalidade | Objetivo de UX relacionado |
|---|---|
| Catálogo | OUX-001 |
| Pesquisa por palavras-chave | OUX-002 |
| Filtros | OUX-003 |
| Detalhes do material | OUX-004 |
| Acesso por link ou arquivo | OUX-005 |
| Estados sem resultados | OUX-006 |
| Apresentação em diferentes telas | OUX-007 |

A pré-visualização, a edição e a adaptação de materiais não estão incluídas nos objetivos do MVP, pois estão fora do escopo inicial.

## 7. Decisões, hipóteses e pendências

### Decisões confirmadas

- O público prioritário são professores.
- A experiência contempla exploração do catálogo, pesquisa, filtros, detalhes e acesso.
- O acesso poderá ocorrer por links externos, arquivos hospedados na plataforma ou ambas as opções.
- A pré-visualização não faz parte do MVP.
- O projeto está em fase de revisão documental.

### Hipóteses

- Uma organização consistente pode facilitar a descoberta de materiais.
- Pesquisa e filtros podem ajudar o professor a localizar recursos relevantes.
- Informações claras podem apoiar a avaliação inicial dos materiais.
- A identificação das formas de acesso pode reduzir dúvidas durante a navegação.

Essas hipóteses ainda não foram validadas por pesquisa com usuários reais.

### Pendências

- Definir os campos pesquisáveis e as regras de pesquisa.
- Definir as opções e a combinação dos filtros.
- Definir os campos obrigatórios e opcionais dos materiais.
- Definir os formatos de arquivo aceitos.
- Detalhar os estados de falha de acesso.
- Especificar os critérios de avaliação futura de forma compatível com o protótipo ou sistema que vier a existir.

## 8. Avaliação futura

Caso o projeto avance para uma etapa de avaliação, os objetivos poderão orientar testes de usabilidade com tarefas representativas, como localizar um material, aplicar filtros, consultar detalhes e identificar as formas de acesso.

Essas atividades são possibilidades futuras, não ações já realizadas. Nenhuma conclusão sobre a eficácia da experiência deve ser apresentada sem evidências correspondentes.

## 9. Status da documentação

Este documento estabelece objetivos pretendidos para a experiência do EduMaterial. Ele não comprova que a interface esteja implementada, que os objetivos tenham sido alcançados ou que as hipóteses tenham sido validadas.

Deverá permanecer alinhado ao Product Brief, aos requisitos, às histórias de usuário, à arquitetura da informação, ao fluxo de navegação e ao Design System.
