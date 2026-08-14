Estratégia de Testes -- SauceDemo (Greenn Challenge)
=====================================================

## Contexto

Aplicação de e-commerce de referência (SauceDemo) usada em desafio técnico. Fluxo de negócio: login, navegação/catálogo, carrinho e checkout -- o funil de compra, onde qualquer falha tem impacto direto em receita.

## Objetivo da estratégia

Garantir que o fluxo crítico de compra funcione ponta a ponta, priorizando cenários de maior risco de negócio em vez de cobertura exaustiva de UI.

## Análise de risco

| Área | Risco de negócio | Prioridade de teste |
|---|---|---|
| Login | Bloqueia acesso total ao sistema | Alta |
| Catálogo/Homepage | Impacta descoberta de produto | Média |
| Carrinho | Erros geram compra incorreta | Alta |
| Checkout | Erro = perda direta de venda | Crítica |

## Tipos de teste aplicados

- E2E automatizado (Cypress): cobre os 4 fluxos acima, com foco nos caminhos felizes e principais caminhos de erro (credenciais inválidas, campos obrigatórios, carrinho vazio).
- Dados de teste: centralizados em fixtures JSON, evitando hardcode e facilitando manutenção.
- Comandos customizados: reuso de login via cy.session(), reduzindo tempo de execução e duplicação.
- Evidências: relatórios Allure com screenshots automáticos em falhas e histórico de execução.

## Cobertura atual

- Autenticação: 4 casos (login válido/inválido, campos obrigatórios)
- Homepage: 6 casos (navegação, produtos, ordenação)
- Checkout: 10 casos (fluxo completo, validações)
- Total: 20 casos automatizados

## Fora de escopo (documentado propositalmente)

- Testes de performance/carga (não fazem parte deste desafio)
- Testes de acessibilidade
- Testes cross-browser além de Chrome/Electron (limitação conhecida)

## Critérios de saída

- 100% dos cenários críticos (checkout) passando antes de considerar a suíte pronta para CI
- Zero flakiness tolerada em cenários de autenticação
