# Arquitetura da Informação — EduMaterial

**Versão:** 0.2  
**Status:** Proposta documental revisada  
**Escopo:** MVP do EduMaterial

## 1. Objetivo

Definir como os materiais didáticos serão organizados, apresentados e acessados no EduMaterial.

A arquitetura da informação busca facilitar a localização dos recursos, tornar suas características compreensíveis e permitir que os professores naveguem entre o catálogo, os resultados de pesquisa e os detalhes de cada material.

Esta estrutura representa uma proposta para o MVP. Não corresponde a uma interface implementada ou validada com usuários reais.

## 2. Estrutura geral

O MVP está organizado em três áreas principais:

1. **Catálogo:** apresenta os materiais disponíveis e permite explorar os recursos, pesquisar por palavras-chave e aplicar filtros.
2. **Resultados da pesquisa:** apresenta os materiais correspondentes aos termos pesquisados e aos filtros selecionados.
3. **Detalhes do material:** reúne as informações de um recurso específico e apresenta sua forma de acesso, quando disponível.

A pesquisa e os filtros são mecanismos de exploração do catálogo, e não áreas independentes que exijam necessariamente páginas separadas. Sua disposição visual definitiva será estabelecida durante o planejamento da interface.

## 3. Hierarquia de navegação

A hierarquia proposta para o MVP é representada a seguir:

```text
EduMaterial
│
└── Catálogo
    ├── Campo de pesquisa
    ├── Filtros
    │   ├── Tipo de material
    │   └── Etapa de ensino
    │
    ├── Lista de materiais
    │   └── Selecionar material
    │
    ├── Resultados da pesquisa
    │   ├── Materiais encontrados
    │   │   └── Selecionar material
    │   └── Estado sem resultados
    │       └── Ajustar pesquisa ou filtros
    │
    └── Detalhes do material
        ├── Identificação
        │   ├── Título
        │   ├── Tipo de material
        │   └── Etapa de ensino
        │
        ├── Informações descritivas
        │   ├── Resumo
        │   ├── Descrição
        │   └── Orientações de uso, quando disponíveis
        │
        └── Acesso ao material
            ├── Link externo, quando disponível
            ├── Arquivo hospedado na plataforma, quando disponível
            └── Informação de ausência de acesso, quando aplicável
```

A visualização prévia do conteúdo dos materiais não está incluída nessa hierarquia, pois não faz parte do MVP.

## 4. Organização das informações dos materiais

Cada material deve possuir informações que permitam identificá-lo e compreender suas características.

A tabela abaixo apresenta os campos propostos e sua finalidade. A definição de quais campos serão obrigatórios ou opcionais permanece pendente.

| Informação | Finalidade |
|---|---|
| Título | Identificar o material. |
| Tipo de material | Informar a categoria do recurso. |
| Etapa de ensino | Indicar a etapa educacional à qual o recurso se destina, quando aplicável. |
| Resumo | Apresentar brevemente a proposta do material. |
| Descrição | Explicar o conteúdo, a finalidade ou as características do recurso. |
| Orientações de uso | Fornecer informações sobre como o material pode ser utilizado, quando disponíveis. |
| Autoria ou origem | Identificar o responsável pela produção ou a fonte do recurso, quando essa informação estiver disponível. |
| Condições de uso | Informar licenças ou restrições de utilização, quando conhecidas e devidamente registradas. |
| Link externo | Permitir o acesso ao material hospedado em outro endereço, quando disponível. |
| Arquivo na plataforma | Identificar o arquivo disponibilizado diretamente na plataforma, quando existente. |

As informações apresentadas devem corresponder aos dados efetivamente cadastrados. A ausência de um campo opcional não deve levar o sistema a inventar ou presumir informações sobre o material.

### 4.1. Identificação e descrição

O título é a informação básica para identificar cada recurso no catálogo e nos resultados da pesquisa.

O tipo de material e a etapa de ensino também devem ser apresentados de maneira consistente, pois fazem parte dos critérios de filtragem previstos para o MVP.

O resumo e a descrição devem ajudar o professor a compreender o recurso sem depender de uma visualização prévia do conteúdo.

### 4.2. Formas de acesso

O acesso aos materiais pode ocorrer por duas modalidades:

- **Link externo:** direciona o professor para um endereço fora da plataforma.
- **Arquivo hospedado na plataforma:** disponibiliza um arquivo associado ao material para acesso ou download, conforme o comportamento que vier a ser definido.

Um material poderá apresentar uma dessas modalidades ou, caso o cadastro e as regras futuras permitam, ambas.

Quando não houver link nem arquivo disponível, a página de detalhes deverá informar que o recurso não possui uma forma de acesso cadastrada.

A apresentação de informações sobre o material deve ser independente da existência de uma forma de acesso.

### 4.3. Campos obrigatórios e opcionais

A definição dos campos obrigatórios e opcionais ainda está pendente.

Como diretriz inicial, cada material precisa ter um título identificável e informações suficientes para ser apresentado no catálogo. Os demais campos deverão ser especificados de acordo com sua função na pesquisa, na filtragem, na identificação e no acesso ao recurso.

A obrigatoriedade de autoria, licença, resumo e orientações de uso deverá ser definida antes da implementação, considerando a disponibilidade e a confiabilidade dessas informações.

## 5. Pesquisa e filtros

A pesquisa por palavras-chave permite localizar materiais a partir dos termos informados pelo professor.

Os filtros complementam a pesquisa, permitindo restringir os resultados por tipo de material e etapa de ensino.

### 5.1. Estados de pesquisa e navegação

A arquitetura deve distinguir os seguintes estados:

- **Catálogo inicial:** exibição dos materiais disponíveis sem uma pesquisa ativa ou filtros aplicados.
- **Resultados encontrados:** exibição dos materiais correspondentes à pesquisa e aos filtros utilizados.
- **Pesquisa sem resultados:** indicação de que nenhum material corresponde aos termos ou critérios selecionados.
- **Catálogo vazio:** indicação de que não existem materiais cadastrados para exibição.
- **Detalhes do material:** exibição das informações do recurso selecionado.
- **Material sem forma de acesso:** exibição dos detalhes com informação explícita de que não há link ou arquivo disponível.
- **Falha de acesso:** situação em que um link ou arquivo cadastrado não pode ser acessado, caso essa condição seja identificada pelo sistema.

A pesquisa sem resultados e o catálogo vazio são situações distintas e não devem utilizar mensagens que sugiram a mesma causa.

Da mesma forma, a ausência de uma forma de acesso não significa que o material não exista ou que suas informações descritivas estejam indisponíveis.

### 5.2. Combinação entre pesquisa e filtros

A combinação entre pesquisa por palavras-chave e filtros deverá permitir que o professor refine os materiais encontrados.

A regra exata de combinação ainda precisa ser definida, incluindo como o sistema deve responder quando diferentes filtros estiverem ativos simultaneamente.

Também permanecem pendentes a definição dos campos pesquisáveis e as regras de correspondência dos termos.

Essas decisões deverão ser documentadas nos requisitos do produto antes da implementação.

## 6. Navegação entre áreas

O usuário deverá conseguir:

- Explorar os materiais disponíveis no catálogo.
- Pesquisar por palavras-chave.
- Aplicar e remover filtros.
- Abrir um material a partir do catálogo ou dos resultados da pesquisa.
- Consultar os detalhes do material selecionado.
- Identificar a forma de acesso disponível.
- Acessar o recurso por um link externo ou por um arquivo hospedado na plataforma, quando disponível.
- Retornar ao catálogo ou aos resultados anteriores.
- Ajustar a pesquisa ou remover filtros quando não encontrar resultados.

A navegação deverá manter uma relação clara entre o catálogo, os resultados e os detalhes do material.

A organização visual definitiva desses elementos será especificada na etapa de design da interface.

## 7. Considerações para a interface

A interface deverá representar fielmente as informações disponíveis no catálogo e utilizar rótulos claros para identificar as ações possíveis.

As seguintes diretrizes devem orientar o planejamento da experiência:

- Os materiais devem apresentar informações consistentes no catálogo, nos resultados e nos detalhes.
- A pesquisa e os filtros devem ser identificáveis e compreensíveis.
- Os filtros ativos devem ser distinguíveis dos filtros não selecionados.
- Os estados de catálogo vazio e pesquisa sem resultados devem ser diferenciados.
- Links externos e arquivos hospedados na plataforma devem possuir ações de acesso claramente identificadas.
- Materiais sem forma de acesso cadastrada não devem apresentar ações que prometam abrir um recurso inexistente.
- A ausência de informações opcionais não deve resultar na apresentação de dados fictícios.
- A organização deve permanecer compreensível em dispositivos móveis.
- A interface não deve sugerir que existe visualização prévia do material no MVP.

Estados de carregamento e falha de acesso deverão ser considerados no detalhamento posterior da interface, conforme os comportamentos definidos para cada modalidade de acesso.

## 8. Decisões confirmadas, hipóteses e pendências

### 8.1. Decisões confirmadas

- O público prioritário é formado por professores que procuram materiais para suas aulas.
- O catálogo será a área central da plataforma.
- A pesquisa por palavras-chave fará parte do MVP.
- Os filtros por tipo de material e etapa de ensino farão parte do MVP.
- Cada material terá uma área de detalhes.
- O acesso poderá ocorrer por links externos ou arquivos hospedados diretamente na plataforma.
- A visualização prévia não fará parte do MVP.

### 8.2. Hipóteses de organização

- A apresentação de informações resumidas no catálogo poderá facilitar a exploração dos materiais.
- A separação entre catálogo, resultados e detalhes poderá tornar a navegação mais compreensível.
- A apresentação de informações descritivas poderá ajudar o professor a avaliar inicialmente a adequação de um recurso.

Essas hipóteses orientam a proposta de arquitetura, mas ainda não foram validadas por pesquisa ou testes com usuários reais.

### 8.3. Pendências

- Definir os campos obrigatórios e opcionais de cada material.
- Definir os campos utilizados na pesquisa por palavras-chave.
- Especificar as regras de combinação entre pesquisa e filtros.
- Definir os valores disponíveis para cada filtro.
- Definir os formatos e limites de arquivos aceitos.
- Definir as regras de armazenamento e disponibilização dos arquivos.
- Determinar como links e arquivos indisponíveis serão tratados.
- Definir quais informações de autoria, origem e condições de uso serão necessárias.
- Detalhar a disposição visual da pesquisa, dos filtros e dos resultados.

## 9. Limites e status da documentação

Esta arquitetura descreve a organização proposta para o MVP do EduMaterial. Ela deverá permanecer alinhada ao Product Brief, aos requisitos, às histórias de usuário, aos objetivos de UX e ao fluxo de uso.

As decisões ainda pendentes devem ser registradas antes de serem tratadas como requisitos definidos.

A coleta de respostas por meio do Google Forms foi abandonada. Portanto, esta arquitetura não deve ser apresentada como resultado de uma pesquisa com professores. Caso sejam utilizados dados ou cenários simulados para ilustrar o catálogo, eles deverão ser identificados explicitamente como fictícios.

**Status atual:** proposta de arquitetura da informação em revisão documental. A implementação e a validação com usuários não são consideradas concluídas e não fazem parte desta etapa.
