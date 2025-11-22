# ADR 0004 – Escolha do Backend
**Status**
Decisão aprovada 

## Contexto

O backend do e-commerce B2B é responsável por:

regras de negócio (produtos, pedidos, empresas, usuários);

autenticação e controle de acesso;

processamento de operações de compra;

comunicações futuras com sistemas externos (pagamento e nota fiscal).

A escolha da tecnologia precisava garantir:

produtividade;

comunidade ampla;

facilidade de integração com frontend web;

performance adequada;

curva de aprendizado moderada para a equipe.

## Decisão

A tecnologia escolhida foi Node.js, situada na pasta:

/back-end


com API REST estruturada.

**Alternativas Consideradas**
**1. Java (Spring Boot)**

Rejeitado.

Excelente para grandes aplicações, mas mais complexo.

Maior curva de aprendizado.

Demandaria mais estrutura de devops.

**2. Python (Django/Flask)**

Rejeitado.

Bom para desenvolvimento rápido, mas menos alinhado com stack JS do projeto.

Menor eficiência em alta concorrência comparado ao Node.js.

**3. Node.js**
Escolhido.

Sinergia natural com o frontend (JavaScript em toda stack).

Grande ecossistema.

Fácil integração com APIs e serviços externos.

Bom desempenho em sistemas I/O como e-commerces.

## Consequências
**Positivas**

Desenvolvimento mais rápido.

Mesma linguagem no front e back.

Facilidade para novos desenvolvedores.

Amplo suporte a bibliotecas (express, JWT, ORM…)

**Negativas**

Aplicações muito pesadas podem exigir mais cuidado com performance.

Requer vigilância com callbacks e assíncronos (gerenciável).

## Conclusão

Node.js é a tecnologia que melhor equilibra produtividade, escalabilidade e compatibilidade com o restante do projeto.