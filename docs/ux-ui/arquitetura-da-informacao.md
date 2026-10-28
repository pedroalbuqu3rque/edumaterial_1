# Arquitetura da Informação — EduMaterial

**Versão:** 0.3  
**Status:** Em revisão documental  
**Escopo:** MVP do EduMaterial

## 1. Objetivo

Definir como os materiais didáticos serão organizados, apresentados e acessados no EduMaterial.

A arquitetura da informação busca facilitar a localização dos recursos, tornar suas características compreensíveis e permitir que os professores naveguem entre o catálogo, os resultados da pesquisa e os detalhes de cada material.

Esta estrutura representa uma proposta para o MVP. Não corresponde a uma interface implementada ou validada com usuários reais.

## 2. Estrutura geral

O MVP está organizado em três áreas principais:

1. **Catálogo:** apresenta os materiais disponíveis e permite explorar os recursos, pesquisar por palavras-chave e aplicar filtros.
2. **Resultados:** apresenta os materiais correspondentes à pesquisa e aos filtros selecionados.
3. **Detalhes do material:** reúne as informações de um recurso específico e apresenta suas formas de acesso, quando disponíveis.

Pesquisa e filtros são mecanismos de exploração do catálogo. Eles não precisam corresponder a páginas independentes: sua disposição visual definitiva será definida em uma etapa posterior de design da interface.

## 3. Hierarquia de navegação

```text
EduMaterial
└── Catálogo
    ├── Estado inicial
    │   ├── Catálogo com materiais
    │   │   └── Explorar materiais
    │   └── Catálogo vazio
    │       └── Informar ausência de materiais cadastrados
    │
    ├── Pesquisa por palavras-chave
    │   └── Resultados
    │       ├── Materiais encontrados
    │       │   └── Selecionar material
    │       └── Nenhum resultado
    │           └── Ajustar pesquisa
    │
    ├── Filtros
    │   ├── Tipo de material
    │   └── Etapa de ensino
    │       └── Resultados filtrados
    │           ├── Materiais encontrados
    │           │   └── Selecionar material
    │           └── Nenhum resultado
    │               └── Ajustar ou remover filtros
    │
    └── Detalhes do material
        ├── Identificação
        │   ├── Título
        │   ├── Tipo de material
        │   └── Etapa de ensino, quando disponível
        │
        ├── Informações descritivas
        │   ├── Resumo
        │   ├── Descrição
        │   └── Orientações de uso, quando disponíveis
        │
        ├── Origem e utilização
        │   ├── Autoria ou fonte, quando disponível
        │   └── Condições de uso, quando conhecidas
        │
        └── Formas de acesso
            ├── Link externo, quando disponível
            ├── Arquivo hospedado na plataforma, quando disponível
            ├── Link e arquivo, quando ambas as opções existirem
            └── Ausência de forma de acesso cadastrada
```

A pré-visualização do conteúdo dos materiais não está incluída nessa hierarquia, pois não faz parte do MVP.

## 4. Organização das informações dos materiais

A tabela apresenta os campos propostos e suas finalidades. A definição de quais campos serão obrigatórios ou opcionais permanece pendente.

| Informação | Finalidade |
|---|---|
| Título | Identificar o material. |
| Tipo de material | Informar a categoria do recurso. |
| Etapa de ensino | Indicar a etapa educacional a que o recurso se destina, quando aplicável. |
| Resumo | Apresentar brevemente a proposta do material. |
| Descrição | Explicar o conteúdo, a finalidade ou as características do recurso. |
| Orientações de uso | Fornecer informações sobre como o material pode ser utilizado, quando disponíveis. |
| Autoria ou origem | Identificar o responsável pela produção ou a fonte do recurso, quando disponível. |
| Condições de uso | Informar licenças ou restrições de utilização, quando conhecidas e aplicáveis. |
| Link externo | Permitir o acesso ao material hospedado em outro endereço, quando disponível. |
| Arquivo hospedado | Identificar o arquivo disponibilizado diretamente na plataforma, quando existente. |

Os campos devem ser apresentados de acordo com sua disponibilidade e com as regras que forem definidas para o cadastro dos materiais. A documentação não pressupõe que todas as informações já estejam preenchidas.

## 5. Estados da interface

### 5.1. Catálogo com materiais

O catálogo apresenta os materiais cadastrados e permite que o usuário explore os itens, pesquise ou aplique filtros.

### 5.2. Catálogo vazio

Ocorre quando não existem materiais cadastrados para exibição. A interface deve informar essa situação.

### 5.3. Resultados encontrados

Ocorre quando a exploração, a pesquisa ou a filtragem apresenta um ou mais materiais. Cada item deve permitir a consulta aos detalhes.

### 5.4. Pesquisa ou filtragem sem resultados

Ocorre quando existem materiais no catálogo, mas nenhum corresponde aos critérios utilizados. A interface deve informar a situação e permitir alterar a pesquisa ou remover filtros.

### 5.5. Detalhes do material

Apresenta as informações descritivas disponíveis e as formas de acesso cadastradas.

### 5.6. Ausência de forma de acesso

Ocorre quando o material não possui link externo nem arquivo cadastrado. As informações descritivas permanecem disponíveis, acompanhadas de uma indicação clara de que não existe uma forma de acesso cadastrada.

### 5.7. Falha de acesso

Pode ocorrer quando um link externo ou arquivo cadastrado não está disponível. O comportamento específico para comunicar essa falha permanece pendente de definição.

## 6. Navegação e orientação

A organização proposta deve permitir que o professor:

- Entenda onde está no catálogo;
- Explore materiais sem precisar iniciar uma pesquisa;
- Identifique os critérios de pesquisa e filtragem ativos;
- Acesse os detalhes de um material;
- Identifique as formas de acesso disponíveis;
- Retorne ao catálogo após consultar um recurso.

A disposição visual, os componentes e os padrões de navegação serão especificados em etapas posteriores de design da interface.

## 7. Decisões, hipóteses e pendências

### Decisões confirmadas

- O catálogo é o ponto central de descoberta.
- Pesquisa e filtros são mecanismos de exploração do catálogo.
- Os filtros previstos são tipo de material e etapa de ensino.
- A página de detalhes apresenta informações sobre o material e suas formas de acesso.
- O acesso pode ocorrer por link externo, arquivo hospedado na plataforma ou ambas as opções.
- A pré-visualização não faz parte do MVP.

### Hipóteses

Uma organização consistente das informações pode ajudar os professores a localizar e avaliar inicialmente os materiais. Essa expectativa ainda não foi validada por pesquisa com usuários reais.

### Pendências

- Definir os campos obrigatórios e opcionais;
- Definir os campos pesquisáveis;
- Definir as opções dos filtros;
- Definir a combinação entre pesquisa e filtros;
- Definir os formatos de arquivo aceitos;
- Definir o tratamento de falhas de acesso.

## 8. Documentos relacionados

- [`product-brief.md`](../product/product-brief.md)
- [`requisitos.md`](../product/requisitos.md)
- [`historias-de-usuario.md`](../product/historias-de-usuario.md)
- [`user-flow.md`](./user-flow.md)
- [`objetivos-de-ux.md`](./objetivos-de-ux.md)
- [`design-system.md`](./design-system.md)

## 9. Status da documentação

Esta arquitetura representa a organização proposta para o MVP. Ela ainda não corresponde a uma implementação ou validação com usuários reais.

O documento deverá permanecer alinhado aos requisitos, às histórias de usuário e ao fluxo de navegação durante a consolidação documental.
