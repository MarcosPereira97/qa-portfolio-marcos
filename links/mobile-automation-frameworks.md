Frameworks de Automacao Mobile
=================================

## Appium + Ruby + Cucumber

- Uso: automacao de testes E2E para aplicativos Android nativos, com cenarios escritos em BDD (Gherkin).
- Projeto de referencia: [qa.neon-mobile-test.appium](https://github.com/MarcosPereira97/qa.neon-mobile-test.appium).
- Pontos fortes na minha experiencia: configuracao de capabilities de dispositivo/emulador, localizacao de elementos nativos, integracao com Cucumber para cenarios de negocio.

## Em construcao: Appium / Mobilewright / Taqwright

- Contexto: novo ciclo de estudo usando um app de referencia mais moderno ([Taqwright demo app](https://github.com/Taqwright/taqwright-demo/tree/main/app)) para evoluir a stack mobile.
- Objetivo: comparar abordagens entre Appium tradicional e ferramentas mais recentes como Mobilewright e Taqwright, avaliando produtividade, estabilidade e velocidade de execucao.
- Status: planejado no roadmap (ver [roadmap.md](../roadmap.md)).

## Observacao geral

Em automacao mobile, priorizo: estabilidade de localizadores (evitar XPath fragil), isolamento de dados de teste por execucao, e cobertura de cenarios de rede instavel/interrupcoes, que sao riscos comuns e pouco testados em apps moveis.
