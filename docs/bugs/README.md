Bug Reports -- Exemplos
=========================

Exemplos estruturados de bugs encontrados durante execucao de testes automatizados e sessoes exploratorias. Formato: Titulo orientado a impacto, Severidade, Ambiente, Passos para reproducao, Resultado atual, Resultado esperado, Evidencia.

## BUG-01 -- Checkout permite duplo submit e gera pedido duplicado

- Severidade: Alta
- Ambiente: SauceDemo (Chrome 126, ambiente de staging)
- Passos para reproducao:
  1. Adicionar produto ao carrinho
  2. Preencher dados de checkout
  3. Clicar duas vezes rapidamente no botao "Finish"
- Resultado atual: dois pedidos sao registrados para a mesma compra
- Resultado esperado: apenas um pedido deve ser criado, com o botao desabilitado apos o primeiro clique
- Evidencia: video da sessao exploratoria (Charter 02) mostrando o duplo clique e o retorno de duas confirmacoes
- Risco de negocio: cobranca duplicada ao cliente, gerando chargeback e retrabalho de suporte

## BUG-02 -- Mensagem de erro generica ao perder conexao durante login (Mobile)

- Severidade: Media
- Ambiente: App Neon, Android 13, emulador Pixel 5
- Passos para reproducao:
  1. Abrir a tela de login
  2. Desativar a rede (modo aviao) apos preencher as credenciais
  3. Tocar em "Entrar"
- Resultado atual: aplicativo exibe apenas "Erro desconhecido", sem orientar o usuario
- Resultado esperado: mensagem especifica informando falha de conexao e sugestao de verificar a rede
- Evidencia: charter exploratorio 01 (mobile), print da tela de erro
- Risco de negocio: usuario pode abandonar o cadastro/login por nao entender o problema

## BUG-03 -- Valores de financiamento nao recalculam ao redimensionar a janela

- Severidade: Baixa
- Ambiente: Velo Configurator, Chrome desktop, resolucao 1024x768
- Passos para reproducao:
  1. Acessar o configurador do veiculo
  2. Selecionar opcionais e simular financiamento
  3. Redimensionar a janela do navegador para uma resolucao menor
- Resultado atual: o valor da parcela exibido nao é recalculado, mostrando dado desatualizado em relacao aos opcionais selecionados
- Resultado esperado: o valor deve permanecer consistente com os opcionais selecionados, independentemente do redimensionamento
- Evidencia: charter exploratorio 03, prints antes/depois do redimensionamento
- Risco de negocio: pode gerar expectativa de preco incorreta para o cliente antes da compra
