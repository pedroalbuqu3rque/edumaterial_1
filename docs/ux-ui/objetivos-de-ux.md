# Objetivos de UX — EduMaterial

**Versão:** 0.4  
**Status:** Em revisão documental  
**Escopo:** MVP do EduMaterial

## 1. Objetivo do documento

Este documento define os objetivos de experiência do usuário (UX) para o MVP do EduMaterial, uma proposta de plataforma digital voltada prioritariamente a professores que procuram materiais educacionais para suas aulas.

Os objetivos orientam as decisões de arquitetura da informação, navegação, conteúdo e interface, buscando tornar a descoberta, a seleção e o acesso aos materiais mais claros e compreensíveis.

Os objetivos representam resultados pretendidos. Ainda não foram validados por pesquisas com usuários reais nem avaliados em testes de usabilidade.

## 2. Público prioritário

O público prioritário do EduMaterial é formado por professores que procuram materiais educacionais para preparar, complementar ou desenvolver suas aulas.

A experiência deverá apoiar o professor a:

- Localizar recursos relacionados aos conteúdos que pretende trabalhar.
- Compreender as características dos materiais disponíveis.
- Refinar os resultados conforme suas necessidades.
- Identificar as formas de acesso disponíveis.
- Recuperar-se de situações em que a busca não retorna resultados ou o acesso falha.

Essas necessidades orientam o planejamento da experiência, mas não devem ser apresentadas como conclusões de entrevistas, questionários ou testes com professores.

## 3. Contexto do problema

O EduMaterial parte da hipótese de que a procura por materiais educacionais pode exigir que professores consultem diferentes fontes e avaliem os recursos encontrados antes de utilizá-los em suas aulas.

A proposta de experiência consiste em reunir informações sobre materiais em um catálogo organizado, com pesquisa por palavras-chave, filtros, páginas de detalhes e opções de acesso claramente identificadas.

A plataforma deverá distinguir materiais acessíveis por links externos, arquivos hospedados diretamente na plataforma, materiais com ambas as opções e materiais sem uma forma de acesso disponível.

A coleta de respostas por meio do Google Forms foi abandonada. Portanto, dados simulados não devem ser utilizados como evidência empírica para confirmar a existência, a frequência ou a intensidade das dificuldades descritas.

## 4. Objetivos de experiência

### OUX-001 — Facilitar a descoberta de materiais

**Objetivo:** permitir que o professor explore o catálogo e identifique materiais potencialmente relevantes para suas aulas.

**Diretrizes de UX:**

- Organizar os materiais de maneira consistente.
- Destacar o título e as informações essenciais de cada recurso.
- Manter uma hierarquia visual que facilite a exploração do catálogo.
- Permitir a navegação dos materiais para suas respectivas páginas de detalhes.
- Apresentar de forma distinta um catálogo vazio e uma lista de resultados de pesquisa.

**Resultado esperado:** o professor consegue compreender a organização do catálogo e identificar como consultar um material.

**Avaliação futura:** observar se participantes conseguem localizar e abrir materiais em tarefas definidas para uma avaliação de usabilidade.

### OUX-002 — Tornar a pesquisa compreensível e previsível

**Objetivo:** permitir que o professor pesquise materiais por palavras-chave e compreenda como os resultados são encontrados e ordenados.

**Diretrizes de UX:**

- Apresentar um campo de pesquisa claramente identificado.
- Tornar compreensível a finalidade do campo.
- Permitir a alteração dos termos pesquisados.
- Apresentar os resultados em ordem de relevância.
- Informar quando uma pesquisa não retornar materiais.
- Manter o comportamento da pesquisa consistente com as regras funcionais definidas.

**Regras funcionais estabelecidas para a busca:**

A pesquisa considera os campos:

1. Título.
2. Tipo de material.
3. Resumo.
4. Descrição.

O comportamento esperado é:

- Ignorar diferenças entre letras maiúsculas e minúsculas.
- Ignorar diferenças de acentuação.
- Aceitar correspondências parciais.
- Ordenar os resultados por relevância, priorizando título, tipo de material, resumo e descrição, nessa ordem.

Por exemplo, pesquisar `historia` deverá permitir localizar materiais com o termo `história`, e pesquisar `geog` deverá permitir localizar materiais que contenham `geografia`.

A fórmula exata de pontuação, os critérios de desempate e o tratamento de consultas com múltiplas palavras ainda precisam ser especificados.

**Resultado esperado:** o professor compreende como pesquisar, interpreta os resultados e consegue ajustar a consulta quando necessário.

**Avaliação futura:** observar se participantes conseguem realizar pesquisas com termos fornecidos, compreender a ordenação dos resultados e modificar consultas que não retornem materiais.

### OUX-003 — Facilitar o uso dos filtros

**Objetivo:** permitir que o professor refine o catálogo por tipo de material e etapa de ensino.

**Diretrizes de UX:**

- Identificar claramente os filtros disponíveis.
- Apresentar as opções de forma compreensível.
- Indicar quais filtros estão ativos.
- Permitir que o usuário compreenda como modificar ou remover critérios aplicados.
- Informar quando os critérios selecionados não retornarem materiais.
- Manter a apresentação dos filtros consistente com os resultados exibidos.

**Resultado esperado:** o professor consegue compreender e alterar os critérios de filtragem.

**Avaliação futura:** observar se participantes conseguem aplicar e remover filtros e interpretar os resultados obtidos.

A combinação de filtros e sua interação com a pesquisa deverão seguir as regras funcionais definidas nos requisitos do produto.

### OUX-004 — Apoiar a avaliação inicial dos materiais

**Objetivo:** apresentar informações suficientes para que o professor compreenda as características de um material antes de acessá-lo.

**Diretrizes de UX:**

- Identificar claramente o material na página de detalhes.
- Organizar os metadados e a descrição em uma hierarquia compreensível.
- Apresentar título, tipo de material, etapa de ensino, resumo e descrição conforme a disponibilidade das informações.
- Apresentar autoria, fonte e condições de utilização quando disponíveis e aplicáveis.
- Evitar depender de uma pré-visualização do conteúdo, pois ela não faz parte do MVP.
- Não apresentar informações ausentes como se fossem conhecidas.

**Resultado esperado:** o professor consegue compreender as informações disponíveis sobre o recurso e decidir se deseja acessar o material.

**Avaliação futura:** observar se participantes conseguem identificar características relevantes dos materiais apresentados em tarefas de avaliação.

### OUX-005 — Tornar as formas de acesso claras

**Objetivo:** permitir que o professor identifique como acessar cada material e compreenda quais opções estão disponíveis.

**Diretrizes de UX:**

- Identificar links externos como opções de acesso à fonte externa.
- Identificar arquivos hospedados na plataforma como opções distintas.
- Apresentar ambas as opções quando estiverem disponíveis.
- Informar quando não houver uma forma de acesso cadastrada.
- Evitar apresentar ações indisponíveis como se fossem funcionais.
- Diferenciar o acesso a um recurso hospedado de um redirecionamento para outro site.

**Cenários que devem ser contemplados:**

1. Material com link externo, sem arquivo hospedado.
2. Material com arquivo hospedado, sem link externo.
3. Material com link externo e arquivo hospedado.
4. Material sem link externo ou arquivo hospedado disponível.

**Resultado esperado:** o professor reconhece as opções de acesso e compreende quando não existe uma forma de acesso cadastrada.

**Avaliação futura:** verificar se participantes identificam corretamente as opções disponíveis nos diferentes cenários.

### OUX-006 — Facilitar a compreensão e a recuperação de estados sem resultados

**Objetivo:** ajudar o professor a compreender quando não há materiais correspondentes à pesquisa ou aos filtros utilizados e permitir que ele tente novamente.

**Diretrizes de UX:**

- Informar claramente que nenhum material corresponde aos critérios utilizados.
- Permitir a alteração dos termos da pesquisa.
- Permitir a modificação ou remoção dos filtros.
- Diferenciar a ausência de resultados de um catálogo vazio.
- Evitar mensagens que culpem o usuário pela ausência de resultados.
- Apresentar orientações simples para continuar a navegação.

**Resultado esperado:** o professor compreende o motivo da ausência de resultados e identifica como ajustar a pesquisa ou os filtros.

**Avaliação futura:** observar se participantes conseguem recuperar-se de uma pesquisa sem resultados sem confundi-la com um catálogo vazio.

### OUX-007 — Preservar a compreensão em diferentes telas

**Objetivo:** planejar uma experiência legível e utilizável em diferentes tamanhos de tela.

**Diretrizes de UX:**

- Preservar a legibilidade dos títulos e das descrições.
- Adaptar a apresentação do catálogo e dos cartões à largura disponível.
- Manter os controles e as ações identificáveis.
- Evitar que informações essenciais sejam ocultadas ou apresentadas de forma confusa.
- Manter a distinção entre links externos e arquivos hospedados.
- Permitir que os filtros e a pesquisa continuem compreensíveis em dispositivos móveis.

**Resultado esperado:** os elementos essenciais da experiência permanecem compreensíveis em diferentes tamanhos de tela.

**Avaliação futura:** verificar a apresentação dos principais fluxos em diferentes resoluções, caso o projeto avance para prototipação ou implementação.

### OUX-008 — Comunicar falhas de acesso de maneira clara

**Objetivo:** ajudar o professor a compreender quando não consegue acessar um material e identificar o que pode fazer em seguida.

**Diretrizes de UX:**

- Informar quando uma tentativa de acesso falhar.
- Diferenciar a ausência de uma forma de acesso cadastrada de uma falha ao abrir um recurso disponível.
- Utilizar mensagens compreensíveis, sem detalhes técnicos desnecessários.
- Oferecer uma nova tentativa quando essa ação for viável.
- Não indicar que o acesso foi concluído com sucesso quando houver falha.
- Manter as informações do material acessíveis quando possível, mesmo que o recurso não possa ser aberto.

**Resultado esperado:** o professor compreende que ocorreu uma falha e consegue identificar as alternativas disponíveis, quando houver.

**Avaliação futura:** verificar se participantes compreendem as mensagens apresentadas e conseguem identificar ações de recuperação apropriadas.

## 5. Princípios gerais de experiência

Os objetivos de UX são orientados pelos seguintes princípios:

- **Clareza:** o usuário deve compreender as informações e as ações disponíveis.
- **Consistência:** componentes equivalentes devem apresentar comportamentos semelhantes.
- **Orientação:** o usuário deve conseguir entender onde está e como retornar ao catálogo ou aos resultados.
- **Transparência:** a interface deve informar as formas de acesso e suas limitações.
- **Recuperação:** estados sem resultados e falhas devem permitir que o usuário identifique alternativas.
- **Acessibilidade:** as informações e os controles devem considerar diferentes formas de interação.
- **Responsividade:** a organização das informações deve permanecer compreensível em diferentes telas.
- **Integridade metodológica:** hipóteses de experiência não devem ser apresentadas como resultados comprovados.

## 6. Relação com o escopo do MVP

| Funcionalidade | Objetivo de UX relacionado |
|---|---|
| Catálogo de materiais | OUX-001 |
| Pesquisa por palavras-chave | OUX-002 |
| Filtros por tipo de material e etapa de ensino | OUX-003 |
| Detalhes do material | OUX-004 |
| Acesso por link externo ou arquivo hospedado | OUX-005 |
| Estados sem resultados | OUX-006 |
| Apresentação em diferentes telas | OUX-007 |
| Falhas e indisponibilidade de acesso | OUX-008 |

A pré-visualização, a edição, a adaptação e o envio de materiais pelos usuários não fazem parte dos objetivos do MVP, pois estão fora do escopo inicial.

## 7. Decisões, hipóteses e pendências

### 7.1 Decisões confirmadas

- O público prioritário é formado por professores.
- A experiência contempla catálogo, pesquisa, filtros, detalhes e acesso aos materiais.
- A pesquisa considera título, tipo de material, resumo e descrição.
- A busca ignora diferenças de caixa e acentuação e aceita correspondências parciais.
- Os resultados são ordenados por relevância, com prioridade para título, tipo de material, resumo e descrição.
- Os filtros previstos são tipo de material e etapa de ensino.
- Os materiais podem ser acessados por link externo, arquivo hospedado, ambos ou nenhum.
- A pré-visualização, a edição, a adaptação e o envio de materiais não fazem parte do MVP atual.
- O projeto está em fase de revisão documental.

### 7.2 Hipóteses

- Uma organização consistente pode facilitar a descoberta de materiais.
- Pesquisa e filtros podem ajudar o professor a localizar recursos relevantes.
- Informações claras podem apoiar a avaliação inicial dos materiais.
- A identificação das formas de acesso pode reduzir dúvidas durante a navegação.
- Mensagens claras de erro podem facilitar a recuperação após falhas de acesso.

Essas hipóteses ainda não foram validadas por pesquisas com usuários reais.

### 7.3 Pendências

- Definir a fórmula de relevância e os critérios de desempate.
- Especificar o tratamento de consultas com múltiplas palavras.
- Definir as opções dos filtros e as regras para sua combinação.
- Definir os campos obrigatórios e opcionais dos materiais.
- Definir os formatos de arquivo aceitos e os limites aplicáveis.
- Detalhar os estados e as mensagens de falha de acesso.
- Definir critérios de avaliação futura compatíveis com o protótipo ou sistema que vier a existir.
- Confirmar os critérios de acessibilidade e responsividade que serão utilizados.

## 8. Avaliação futura

Caso o projeto avance para uma etapa de avaliação, os objetivos poderão orientar testes de usabilidade com tarefas representativas, como:

- Localizar um material por meio do catálogo.
- Pesquisar utilizando diferentes termos.
- Aplicar e remover filtros.
- Consultar os detalhes de um recurso.
- Identificar as formas de acesso disponíveis.
- Compreender uma pesquisa sem resultados.
- Interpretar uma falha de acesso.
- Navegar pelas principais áreas em diferentes tamanhos de tela.

Os critérios de sucesso deverão ser definidos antes da avaliação, de acordo com os objetivos e as tarefas propostas.

Essas atividades são possibilidades futuras, não ações já realizadas. Nenhuma conclusão sobre a eficácia da experiência deve ser apresentada sem evidências correspondentes.

## 9. Status da documentação

Este documento estabelece objetivos pretendidos para a experiência do EduMaterial. Ele não comprova que a interface esteja implementada, que os objetivos tenham sido alcançados ou que as hipóteses tenham sido validadas.

A revisão atual é documental. A avaliação com usuários, os testes de usabilidade e as verificações de acessibilidade deverão ocorrer em etapas futuras, caso sejam executados.

O documento deverá permanecer alinhado ao Product Brief, aos requisitos, às histórias de usuário, ao backlog, à arquitetura da informação, ao fluxo de navegação e ao Design System.
