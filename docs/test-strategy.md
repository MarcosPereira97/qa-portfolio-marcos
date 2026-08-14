Estrategia de Testes -- SauceDemo (Greenn Challenge)
=====================================================

## Contexto

Aplicacao de e-commerce de referencia (SauceDemo) usada em desafio tecnico. Fluxo de negocio: login, navegacao/catalogo, carrinho e checkout -- o funil de compra, onde qualquer falha tem impacto direto em receita.

## Objetivo da estrategia

Garantir que o fluxo critico de compra funcione ponta a ponta, priorizando cenarios de maior risco de negocio em vez de cobertura exaustiva de UI.

## Analise de risco

| Area | Risco de negocio | Prioridade de teste |
|---|---|---|
| Login | Bloqueia acesso total ao sistema | Alta |
| Catalogo/Homepage | Impacta descoberta de produto | Media |
| Carrinho | Erros geram compra incorreta | Alta |
| Checkout | Erro = perda direta de venda | Critica |

## Tipos de teste aplicados

- E2E automatizado (Cypress): cobre os 4 fluxos acima, com foco nos caminhos felizes e principais caminhos de erro (credenciais invalidas, campos obrigatorios, carrinho vazio).
- Dados de teste: centralizados em fixtures JSON, evitando hardcode e facilitando manutencao.
- Comandos customizados: reuso de login via cy.session(), reduzindo tempo de execucao e duplicacao.
- Evidencias: relatorios Allure com screenshots automaticos em falhas e historico de execucao.

## Cobertura atual

- Autenticacao: 4 casos (login valido/invalido, campos obrigatorios)
- Homepage: 6 casos (navegacao, produtos, ordenacao)
- Checkout: 10 casos (fluxo completo, validacoes)
- Total: 20 casos automatizados

## Fora de escopo (documentado propositalmente)

- Testes de performance/carga (nao fazem parte deste desafio)
- Testes de acessibilidade
- Testes cross-browser alem de Chrome/Electron (limitacao conhecida)

## Criterios de saida

- 100% dos cenarios criticos (checkout) passando antes de considerar a suite pronta para CI
- Zero flakiness tolerada em cenarios de autenticacao
