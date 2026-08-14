Bug Reports -- Exemplos
=========================
Exemplos estruturados de bugs que encontrei durante execução de testes automatizados e sessões exploratórias. Formato: Título orientado a impacto, Severidade, Ambiente, Passos para reprodução, Resultado atual, Resultado esperado, Evidência.

## BUG-01 -- Checkout permite duplo submit e gera pedido duplicado
- Severidade: Alta
- Ambiente: SauceDemo (Chrome 126, ambiente de staging)
- Passos para reprodução:
  1. Adicionar produto ao carrinho
  2. Preencher dados de checkout
  3. Clicar duas vezes rapidamente no botão "Finish"
- Resultado atual: dois pedidos são registrados para a mesma compra
- Resultado esperado: apenas um pedido deve ser criado, com o botão desabilitado após o primeiro clique
- Evidência: vídeo da sessão exploratória (Charter 02) que gravei mostrando o duplo clique e o retorno de duas confirmações
- Risco de negócio: cobrança duplicada ao cliente, gerando chargeback e retrabalho de suporte

## BUG-02 -- Mensagem de erro genérica ao perder conexão durante login (Mobile)
- Severidade: Média
- Ambiente: App Neon, Android 13, emulador Pixel 5
- Passos para reprodução:
  1. Abrir a tela de login
  2. Desativar a rede (modo avião) após preencher as credenciais
  3. Tocar em "Entrar"
- Resultado atual: o aplicativo exibe apenas "Erro desconhecido", sem orientar o usuário
- Resultado esperado: mensagem específica informando falha de conexão e sugestão de verificar a rede
- Evidência: charter exploratório 01 (mobile) que conduzi, com print da tela de erro
- Risco de negócio: usuário pode abandonar o cadastro/login por não entender o problema

## BUG-03 -- Valores de financiamento não recalculam ao redimensionar a janela
- Severidade: Baixa
- Ambiente: Velo Configurator, Chrome desktop, resolução 1024x768
- Passos para reprodução:
  1. Acessar o configurador do veículo
  2. Selecionar opcionais e simular financiamento
  3. Redimensionar a janela do navegador para uma resolução menor
- Resultado atual: o valor da parcela exibido não é recalculado, mostrando dado desatualizado em relação aos opcionais selecionados
- Resultado esperado: o valor deve permanecer consistente com os opcionais selecionados, independentemente do redimensionamento
- Evidência: charter exploratório 03 que executei, com prints antes/depois do redimensionamento
- Risco de negócio: pode gerar expectativa de preço incorreta para o cliente antes da compra
