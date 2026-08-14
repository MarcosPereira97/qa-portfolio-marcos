Frameworks de Automação Mobile
=================================

## Appium + Ruby + Cucumber

- Uso: automação de testes E2E para aplicativos Android nativos, com cenários escritos em BDD (Gherkin).
- Projeto de referência: [qa.neon-mobile-test.appium](https://github.com/MarcosPereira97/qa.neon-mobile-test.appium).
- Pontos fortes na minha experiência: configuração de capabilities de dispositivo/emulador, localização de elementos nativos, integração com Cucumber para cenários de negócio.

## Em construção: Appium / Mobilewright / Taqwright

- Contexto: novo ciclo de estudo usando um app de referência mais moderno ([Taqwright demo app](https://github.com/Taqwright/taqwright-demo/tree/main/app)) para evoluir a stack mobile.
- Objetivo: comparar abordagens entre Appium tradicional e ferramentas mais recentes como Mobilewright e Taqwright, avaliando produtividade, estabilidade e velocidade de execução.
- Status: planejado no roadmap (ver [roadmap.md](../roadmap.md)).

## Observação geral

Em automação mobile, priorizo: estabilidade de localizadores (evitar XPath frágil), isolamento de dados de teste por execução, e cobertura de cenários de rede instável/interrupções, que são riscos comuns e pouco testados em apps móveis.
