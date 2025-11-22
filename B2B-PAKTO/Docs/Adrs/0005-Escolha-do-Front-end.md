## ADR 0005 – Escolha do Frontend
**Status**
Decisão aprovada e implementada.

## Contexto

A plataforma de compras B2B precisa oferecer ao usuário:

interface responsiva;

experiência moderna;

componentes reutilizáveis;

boa performance;

integração fluida com a API backend.

A equipe também precisava de uma tecnologia acessível e com curva de aprendizado adequada.

## Decisão

A tecnologia escolhida para o frontend foi HTML + CSS + JavaScript, estruturada na pasta:

/front-end


A decisão favoreceu simplicidade, compatibilidade universal e velocidade de entrega.

## Alternativas Consideradas
**1. React, Vue ou Angular**

Rejeitados por enquanto.

São excelentes, mas exigem build, bundlers, componentes, roteamento.

Maiores exigências de conhecimento da equipe.

A plataforma não exigia SPAs completas no estágio inicial.

**2. HTML/CSS/JS**

Escolhido.

Entrega rápida.

Baixa complexidade.

Compatível com qualquer servidor web.

Fácil de integrar com backend via fetch/axios.

Facilita manutenção por equipes pequenas.

## Consequências
**Positivas**

Menos dependências.

Projeto mais leve.

Desenvolvimento mais rápido no início.

Fácil para novos membros compreenderem.

**Negativas**

Escalabilidade limitada em termos de interatividade avançada.

Se futuramente virar uma SPA, será necessário migrar o front.

## Conclusão

O uso de HTML/CSS/JS é a escolha mais apropriada para o estágio atual do projeto, focado em simplicidade e velocidade de desenvolvimento, sem comprometer a capacidade de evolução futura.