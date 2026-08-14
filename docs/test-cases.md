Casos de Teste -- SauceDemo (Web)
==================================

Formato: ID | Titulo | Pre-condicao | Passos | Resultado esperado | Prioridade

## Modulo: Autenticacao

TC-01 | Login com credenciais validas
- Pre-condicao: usuario standard_user cadastrado
- Passos: acessar login, preencher usuario e senha validos, clicar em Login
- Resultado esperado: redirecionamento para a pagina de produtos
- Prioridade: Critica

TC-02 | Login com senha invalida
- Pre-condicao: usuario existente
- Passos: preencher usuario valido e senha incorreta, clicar em Login
- Resultado esperado: mensagem de erro "Username and password do not match"
- Prioridade: Alta

TC-03 | Login com usuario bloqueado
- Pre-condicao: usuario locked_out_user
- Passos: preencher credenciais do usuario bloqueado, clicar em Login
- Resultado esperado: mensagem informando que o usuario foi bloqueado
- Prioridade: Alta

TC-04 | Login com campos obrigatorios vazios
- Passos: clicar em Login sem preencher usuario/senha
- Resultado esperado: mensagem de erro indicando campo obrigatorio
- Prioridade: Media

## Modulo: Homepage / Catalogo

TC-05 | Listagem de produtos
- Resultado esperado: todos os produtos cadastrados sao exibidos com nome, preco e imagem

TC-06 | Ordenacao por preco (menor-maior)
- Passos: selecionar filtro Price (low to high)
- Resultado esperado: produtos reordenados corretamente

TC-07 | Ordenacao por preco (maior-menor)
- Resultado esperado: produtos reordenados em ordem decrescente

TC-08 | Ordenacao alfabetica (A-Z)
- Resultado esperado: produtos em ordem alfabetica crescente

TC-09 | Adicionar produto ao carrinho pela homepage
- Resultado esperado: icone do carrinho reflete +1 item

TC-10 | Acessar detalhes do produto
- Passos: clicar no nome do produto
- Resultado esperado: pagina de detalhes exibida com descricao completa

## Modulo: Carrinho

TC-11 | Adicionar multiplos produtos
- Resultado esperado: contador do carrinho reflete a quantidade correta

TC-12 | Remover produto do carrinho
- Resultado esperado: produto removido e contador atualizado

TC-13 | Carrinho vazio nao permite checkout
- Resultado esperado: botao de checkout desabilitado ou redirecionamento bloqueado

## Modulo: Checkout (prioridade critica)

TC-14 | Checkout completo com dados validos
- Passos: preencher nome, sobrenome, CEP, finalizar compra
- Resultado esperado: pedido concluido com mensagem de sucesso

TC-15 | Checkout sem nome preenchido
- Resultado esperado: erro "First Name is required"

TC-16 | Checkout sem sobrenome preenchido
- Resultado esperado: erro "Last Name is required"

TC-17 | Checkout sem CEP preenchido
- Resultado esperado: erro "Postal Code is required"

TC-18 | Cancelar checkout retorna ao carrinho
- Resultado esperado: usuario retorna a tela de carrinho sem perder itens

TC-19 | Resumo do pedido exibe valores corretos (subtotal, taxa, total)
- Resultado esperado: calculo de taxa e total conferem com os itens do carrinho

TC-20 | Finalizar compra limpa o carrinho
- Resultado esperado: apos confirmacao, carrinho fica vazio e contador zera
