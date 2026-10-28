# Arquitetura da Informação — EduMaterial

## 1. Objetivo

Definir como os materiais educacionais são organizados, apresentados e acessados no EduMaterial.

A arquitetura da informação busca tornar a navegação compreensível e facilitar a localização dos recursos disponíveis.

## 2. Estrutura geral

O MVP é organizado em três áreas principais:

1. **Catálogo:** apresenta os materiais disponíveis e permite explorar, pesquisar e filtrar os recursos.
2. **Resultados da busca:** apresenta os materiais correspondentes à pesquisa realizada.
3. **Detalhes do material:** reúne as informações de um recurso específico e disponibiliza seu acesso, quando houver um link.

## 3. Hierarquia de navegação

```text
EduMaterial
│
├── Catálogo
│   ├── Campo de pesquisa
│   ├── Filtros
│   └── Lista de materiais
│       └── Selecionar material
│
├── Resultados da busca
│   ├── Resultados encontrados
│   │   └── Selecionar material
│   └── Estado sem resultados
│       └── Ajustar pesquisa ou filtros
│
└── Detalhes do material
    ├── Título
    ├── Tipo de material
    ├── Etapa de ensino
    ├── Descrição e informações de uso
    └── Link de acesso, quando disponível
```

## 4. Organização dos materiais

Cada material deve possuir informações que ajudem o usuário a identificá-lo e avaliar sua relevância.

| Informação | Finalidade |
|---|---|
| Título | Identificar o recurso |
| Tipo de material | Informar a categoria do recurso |
| Etapa de ensino | Indicar o público educacional previsto |
| Resumo | Apresentar rapidamente a proposta |
| Descrição | Explicar o conteúdo e a finalidade |
| Orientações de uso | Apoiar a compreensão de como utilizar o recurso |
| Link de acesso | Permitir abrir o material, quando disponível |

A disponibilidade e o preenchimento desses campos devem ser consistentes com os dados cadastrados no catálogo.

## 5. Pesquisa e filtros

A pesquisa por palavras-chave permite localizar materiais a partir de termos informados pelo usuário.

Os filtros complementam a pesquisa e ajudam a restringir os resultados conforme os critérios disponíveis no MVP, como tipo de material e etapa de ensino.

A interface deve diferenciar claramente:

- Catálogo sem pesquisa ativa.
- Resultados encontrados.
- Pesquisa sem resultados.

## 6. Navegação entre áreas

O usuário deve conseguir:

- Abrir um material a partir do catálogo ou dos resultados.
- Consultar os detalhes do material selecionado.
- Retornar ao catálogo.
- Ajustar a pesquisa quando não encontrar resultados.

A navegação deve manter uma relação clara entre a lista de materiais e a página de detalhes.

## 7. Considerações para implementação

- A estrutura visual deve representar fielmente as informações disponíveis nos dados.
- Materiais sem link de acesso não devem apresentar uma ação que prometa abrir um recurso inexistente.
- Os estados de carregamento, erro e ausência de resultados devem ser considerados durante o desenvolvimento.
- A organização deve continuar compreensível em dispositivos móveis.

## 8. Limites e validação

Esta arquitetura representa a organização proposta para o MVP. Ela deverá ser revisada durante o desenvolvimento para garantir consistência com os requisitos, o modelo de dados e as funcionalidades efetivamente implementadas.
