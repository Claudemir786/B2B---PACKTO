# ADR 0003 – Escolha do Banco de Dados
**Status**
Decisão aprovada

# Contexto

O e-commerce B2B Packed requer:

armazenamento persistente de usuários, empresas, produtos e pedidos;

integridade relacional;

consultas estruturadas;

suporte a operações transacionais.

A equipe também possui vivência com bancos relacionais e precisa de uma solução madura para e-commerce.

## Decisão

A escolha foi utilizar um banco de dados relacional, armazenado na pasta:

/database


Possíveis motores utilizados (dependendo do ambiente): MySQL.

A estrutura foi projetada com tabelas normalizadas e relacionamentos claros.

## Alternativas Consideradas
**1. Banco NoSQL (MongoDB, Firebase, etc.)**

Rejeitado.

Não atende tão bem cenários com alto nível de relação entre entidades.

Validação e integridade ficariam por conta da aplicação.

Mais adequado a outros contextos (ex.: análises, documentos, streaming).

**2. Banco Relacional**

Escolhido.

Modelagem clara para e-commerce.

Suporta integridade referencial.

Ampla compatibilidade com ORMs ou queries nativas.

Fácil de manter e escalar verticalmente.

## Consequências
**Positivas**

Consultas mais eficientes para dados tabulares.

Suporte nativo a relacionamentos (JOINs).

Segurança e confiabilidade para operações críticas.

Facilidade de manutenção.

**Negativas**

Escalabilidade horizontal mais complexa do que NoSQL.

Migração para microserviços futuros exigirá divisão do schema (normal).

## Conclusão

Um banco relacional atende perfeitamente as necessidades atuais do e-commerce B2B, oferecendo consistência, segurança e boa performance.