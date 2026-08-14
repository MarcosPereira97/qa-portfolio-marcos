Charters de Teste Exploratorio
================================

Formato baseado em Session-Based Test Management (SBTM): Missao | Area | Duracao | Notas e riscos observados

## Charter 01 -- Fluxo de autenticacao (Mobile - Neon Challenge)

- Missao: Explorar o fluxo de login do app buscando falhas de usabilidade, mensagens de erro pouco claras e comportamento em cenarios de rede instavel.
- Area: Tela de login e recuperacao de senha
- Duracao: 45 minutos
- Notas/riscos observados: validar comportamento ao alternar de rede Wi-Fi para dados moveis durante o login; checar se mensagens de erro sao especificas o suficiente para o usuario corrigir o problema; observar comportamento do teclado nativo sobrepondo campos de input.

## Charter 02 -- Fluxo de checkout (Web - SauceDemo)

- Missao: Explorar o fluxo de checkout buscando inconsistencias de calculo, comportamento em back/forward do navegador e estados inesperados do carrinho.
- Area: Carrinho e checkout
- Duracao: 40 minutos
- Notas/riscos observados: testar uso do botao voltar do navegador durante o checkout; verificar se o carrinho mantem estado apos refresh da pagina; validar comportamento ao tentar finalizar compra duas vezes em sequencia rapida (duplo clique).

## Charter 03 -- Navegacao e responsividade (Web - Velo Configurator)

- Missao: Explorar a experiencia de configuracao do veiculo em diferentes resolucoes de tela, buscando problemas de layout e perda de dados ao redimensionar.
- Area: Fluxo de configuracao de opcionais e simulacao de financiamento
- Duracao: 30 minutos
- Notas/riscos observados: verificar se os valores calculados de financiamento permanecem consistentes ao redimensionar a janela; checar comportamento de campos de formulario ao usar zoom do navegador; validar se opcionais selecionados persistem ao navegar entre etapas do configurador.

## Charter 04 -- Autenticacao e sessao (API/Web)

- Missao: Explorar o comportamento de expiracao de sessao e tratamento de tokens invalidos ou expirados.
- Area: Autenticacao via API e persistencia de sessao no front-end
- Duracao: 30 minutos
- Notas/riscos observados: testar chamadas a API com token expirado; verificar se o front-end redireciona corretamente para login ao receber 401; checar se dados sensiveis ficam expostos em respostas de erro.
