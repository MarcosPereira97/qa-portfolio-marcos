APIs, Performance e CI/CD
============================

## Testes de API (REST/GraphQL)

- Ferramentas: Postman (coleções e testes automatizados), Newman (execução via CLI/CI).
- Abordagem: validação de contrato (status code, schema de resposta), testes de regras de negócio via API antes mesmo da automação de UI, testes de autenticação/autorização (tokens, permissões).
- Aplicação prática: validação de integrações de gateway de pagamento, testes de endpoints de autenticação e sessão.

## Performance

- Ferramenta: k6.
- Abordagem: testes de carga em endpoints críticos (login, checkout), definição de thresholds de tempo de resposta, identificação de gargalos antes de ir para produção.
- Observação: testes de performance são tratados como parte do pipeline de release, não como atividade isolada pós-incidente.

## CI/CD

- Ferramentas: GitHub Actions, Azure DevOps, Jenkins.
- Abordagem: pipelines que rodam lint, testes unitários, testes E2E e publicam relatórios (Allure, TestDino) como artefato, bloqueando merge/deploy em caso de falha em cenários críticos.
- Exemplo de projeto com CI real: [PerformanceHUB](https://github.com/MarcosPereira97/PerformanceHUB) (projeto de desenvolvimento pessoal, não incluso na vitrine de QA, mas demonstra a mentalidade de qualidade aplicada ao pipeline).

## Observabilidade

- Ferramentas: Kibana, logs estruturados.
- Aplicação: uso de logs e dashboards para investigação de falhas intermitentes (flaky tests) e correlação entre erros de API e comportamento de UI.
