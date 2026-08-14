Charters de Teste Exploratório
================================
Formato baseado em Session-Based Test Management (SBTM): Missão | Área | Duração | Notas e riscos observados

## Charter 01 -- Fluxo de autenticação (Mobile - Neon Challenge)
- Missão: explorar o fluxo de login do app buscando falhas de usabilidade, mensagens de erro pouco claras e comportamento em cenários de rede instável.
- Área: tela de login e recuperação de senha
- Duração: 45 minutos
- Notas/riscos observados: validar comportamento ao alternar de rede Wi-Fi para dados móveis durante o login; checar se as mensagens de erro são específicas o suficiente para o usuário corrigir o problema; observar o comportamento do teclado nativo sobrepondo campos de input.

## Charter 02 -- Fluxo de checkout (Web - SauceDemo)
- Missão: explorar o fluxo de checkout buscando inconsistências de cálculo, comportamento em back/forward do navegador e estados inesperados do carrinho.
- Área: carrinho e checkout
- Duração: 40 minutos
- Notas/riscos observados: testar o uso do botão voltar do navegador durante o checkout; verificar se o carrinho mantém o estado após refresh da página; validar o comportamento ao tentar finalizar a compra duas vezes em sequência rápida (duplo clique).

## Charter 03 -- Navegação e responsividade (Web - Velo Configurator)
- Missão: explorar a experiência de configuração do veículo em diferentes resoluções de tela, buscando problemas de layout e perda de dados ao redimensionar.
- Área: fluxo de configuração de opcionais e simulação de financiamento
- Duração: 30 minutos
- Notas/riscos observados: verificar se os valores calculados de financiamento permanecem consistentes ao redimensionar a janela; checar o comportamento de campos de formulário ao usar o zoom do navegador; validar se os opcionais selecionados persistem ao navegar entre as etapas do configurador.

## Charter 04 -- Autenticação e sessão (API/Web)
- Missão: explorar o comportamento de expiração de sessão e o tratamento de tokens inválidos ou expirados.
- Área: autenticação via API e persistência de sessão no front-end
- Duração: 30 minutos
- Notas/riscos observados: testar chamadas à API com token expirado; verificar se o front-end redireciona corretamente para o login ao receber 401; checar se dados sensíveis ficam expostos em respostas de erro.
