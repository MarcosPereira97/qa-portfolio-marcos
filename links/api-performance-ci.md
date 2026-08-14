APIs, Performance e CI/CD
============================

## Testes de API (REST/GraphQL)

- Ferramentas: Postman (colecoes e testes automatizados), Newman (execucao via CLI/CI).
- Abordagem: validacao de contrato (status code, schema de resposta), testes de regras de negocio via API antes mesmo da automacao de UI, testes de autenticacao/autorizacao (tokens, permissoes).
- Aplicacao pratica: validacao de integracoes de gateway de pagamento, testes de endpoints de autenticacao e sessao.

## Performance

- Ferramenta: k6.
- Abordagem: testes de carga em endpoints criticos (login, checkout), definicao de thresholds de tempo de resposta, identificacao de gargalos antes de ir para producao.
- Observacao: testes de performance sao tratados como parte do pipeline de release, nao como atividade isolada pos-incidente.

## CI/CD

- Ferramentas: GitHub Actions, Azure DevOps, Jenkins.
- Abordagem: pipelines que rodam lint, testes unitarios, testes E2E e publicam relatorios (Allure, TestDino) como artefato, bloqueando merge/deploy em caso de falha em cenarios criticos.
- Exemplo de projeto com CI real: [PerformanceHUB](https://github.com/MarcosPereira97/PerformanceHUB) (projeto de desenvolvimento pessoal, nao incluso na vitrine de QA, mas demonstra a mentalidade de qualidade aplicada ao pipeline).

## Observabilidade

- Ferramentas: Kibana, logs estruturados.
- Aplicacao: uso de logs e dashboards para investigacao de falhas intermitentes (flaky tests) e correlacao entre erros de API e comportamento de UI.
