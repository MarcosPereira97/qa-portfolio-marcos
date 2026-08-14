Frameworks de Automacao Web
=============================

## Cypress + TypeScript

- Uso: automacao E2E com foco em rapidez de feedback e boa integracao com pipelines de CI.
- Projeto de referencia: [qa.greenn-web-test.cypress](https://github.com/MarcosPereira97/qa.greenn-web-test.cypress) -- inclui reuso de sessao (cy.session), fixtures JSON e relatorios Allure.
- Pontos fortes na minha experiencia: comandos customizados reutilizaveis, estrategia de dados de teste isolada, debugging visual no Test Runner.

## Selenium + Ruby + Cucumber (BDD)

- Uso: automacao E2E com abordagem orientada a comportamento (Gherkin), facilitando comunicacao com stakeholders nao tecnicos.
- Projeto de referencia: [qa.webmotors-web-test.selenium](https://github.com/MarcosPereira97/qa.webmotors-web-test.selenium).
- Pontos fortes na minha experiencia: escrita de cenarios em linguagem de negocio, Page Object Pattern, integracao com Cucumber para rastreabilidade de requisitos.

## Playwright + TypeScript

- Uso: automacao E2E moderna com suporte nativo a multiplos browsers, auto-wait e depuracao via trace viewer.
- Contexto de aplicacao: projetos de estudo e cursos (AutomatizAI, Udemy) para evolucao continua da stack.
- Pontos fortes na minha experiencia: integracao com reporters como TestDino, testes contra ambientes de Preview (Vercel), execucao paralela.

## Observacao geral

Em todos os frameworks acima, minha abordagem prioriza: dados de teste isolados, evidencias (relatorios/screenshots) como parte da entrega, e testes organizados por risco de negocio -- nao apenas por tela ou funcionalidade.
