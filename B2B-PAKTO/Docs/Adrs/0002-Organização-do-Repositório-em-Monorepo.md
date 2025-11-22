# ADR 0002 – Organização do Repositório em Monorepo
**Status**

Decisão aprovada e implementada.

## Contexto

O projeto B2B PACKTO inclui frontend, backend, scripts de banco e documentação. Inicialmente, existia a dúvida se cada área deveria usar repositórios separados (multirepo) ou se tudo deveria ser centralizado.

Como o sistema está em fase inicial e desenvolvido por uma equipe enxuta, é essencial manter organização clara, integração simplificada e menor overhead de configuração.

## Decisão

O repositório foi organizado como monorepo, contendo as pastas:

/front-end
/back-end
/database
/docs


Toda a base de código é versionada e gerenciada em um único repositório.

## Alternativas Consideradas
**1. Multirepo (um repositório para cada módulo)**

Rejeitado por enquanto.

Exige mais gerência (mais repositórios, permissões, pipelines).

Aumenta a complexidade do CI/CD.

Dificulta o desenvolvimento sincronizado entre front e back.

Não necessário para o tamanho atual da equipe.

**2. Monorepo (escolhido)**

Atende melhor os requisitos atuais do projeto.

## Consequências
**Positivas**

Menos complexidade operacional.

Facilita colaboração entre frontend e backend.

CI/CD mais simples.

Melhor visibilidade do projeto como um todo.

Padronização centralizada.

**Negativas**

O repositório tende a ficar grande com o tempo.

Para equipes enormes, poderia causar conflitos frequentes (não é o caso atual).

## Conclusão

O monorepo é a escolha mais adequada para a fase atual do sistema, garantindo simplicidade, organização e integração eficiente entre todas as áreas do projeto.