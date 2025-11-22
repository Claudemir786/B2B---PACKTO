 # ADR 0001 – Escolha da Arquitetura Monolítica Modular
**Status**
Decisão aprovada e implementada.

## Contexto

O projeto B2B PACKTO é um e-commerce B2B que envolve:

plataforma de compras online (frontend),

API e regras de negócio (backend),

scripts e estrutura de banco de dados (database),

documentação do sistema (docs).

A equipe possui tamanho reduzido, o projeto está em fase inicial e existem necessidades de desenvolvimento ágil, com menor complexidade operacional. Embora exista a perspectiva futura de um sistema separado para pagamentos e emissão de nota fiscal, essa funcionalidade ainda não foi implementada.

Surgiu a necessidade de escolher uma arquitetura para suportar a organização, manutenção e evolução do projeto.

## Decisão

A arquitetura escolhida foi a Arquitetura Monolítica Modular, organizada em camadas e estruturada em um monorepo.
O projeto é dividido em:

/front-end
/back-end
/database
/docs


Essas pastas representam módulos internos, mas todo o sistema funciona como um único artefato no deploy e no versionamento, caracterizando um monólito modular.

## Alternativas Consideradas
**1. Microsserviços**

Rejeitado por enquanto.

Demandaria alta complexidade operacional.

Necessitaria de mais infraestrutura (kubernetes, mensageria, CI/CD distribuído).

Requer times maiores e escalabilidade mais avançada.

A demanda atual não justifica essa divisão.

**2. Arquitetura SOA**

Rejeitada por enquanto.

Só seria válida com um serviço externo real para pagamentos e notas fiscais.

A implementação atual não possui serviços independentes.

A complexidade seria desnecessária na fase atual do projeto.

**3. Monólito Clássico (tudo junto em uma única pasta)**

Rejeitado.

Baixa organização.

Dificuldade de manutenção.

Estrutura inadequada para expansão futura.

## Consequências
**Consequências Positivas**

Estrutura simples e intuitiva.

Desenvolvimento mais rápido para a equipe atual.

Deploy unificado e fácil de gerenciar.

Custos menores de hospedagem e manutenção.

Organização modular facilita futuras refatorações.

Melhor tempo de entrega durante o desenvolvimento inicial.

**Consequências Negativas**

Escalabilidade horizontal mais limitada que microsserviços.

O backend concentra toda a lógica de negócio, podendo crescer demais no futuro.

Migração futura para SOA/Microsserviços exigirá refatoração gradual.

## Conclusão

A arquitetura Monolítica Modular é a abordagem mais adequada para o estágio atual do projeto B2B PACKTO, oferecendo simplicidade, organização e excelente custo-benefício para desenvolvimento e manutenção.
Ela também serve como base sólida para uma possível evolução futura para serviços independentes, caso o sistema de pagamentos e emissão de nota se torne um módulo separado.