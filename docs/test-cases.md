Casos de Teste -- SauceDemo (Web)
==================================

Formato: ID | Título | Pré-condição | Passos | Resultado esperado | Prioridade

## Módulo: Autenticação

TC-01 | Login com credenciais válidas
- Pré-condição: usuário standard_user cadastrado
- Passos: acessar login, preencher usuário e senha válidos, clicar em Login
- Resultado esperado: redirecionamento para a página de produtos
- Prioridade: Crítica

TC-02 | Login com senha inválida
- Pré-condição: usuário existente
- Passos: preencher usuário válido e senha incorreta, clicar em Login
- Resultado esperado: mensagem de erro "Username and password do not match"
- Prioridade: Alta

TC-03 | Login com usuário bloqueado
- Pré-condição: usuário locked_out_user
- Passos: preencher credenciais do usuário bloqueado, clicar em Login
- Resultado esperado: mensagem informando que o usuário foi bloqueado
- Prioridade: Alta

TC-04 | Login com campos obrigatórios vazios
- Passos: clicar em Login sem preencher usuário/senha
- Resultado esperado: mensagem de erro indicando campo obrigatório
- Prioridade: Média

## Módulo: Homepage / Catálogo

TC-05 | Listagem de produtos
- Resultado esperado: todos os produtos cadastrados são exibidos com nome, preço e imagem

TC-06 | Ordenação por preço (menor-maior)
- Passos: selecionar filtro Price (low to high)
- Resultado esperado: produtos reordenados corretamente

TC-07 | Ordenação por preço (maior-menor)
- Resultado esperado: produtos reordenados em ordem decrescente

TC-08 | Ordenação alfabética (A-Z)
- Resultado esperado: produtos em ordem alfabética crescente

TC-09 | Adicionar produto ao carrinho pela homepage
- Resultado esperado: ícone do carrinho reflete +1 item

TC-10 | Acessar detalhes do produto
- Passos: clicar no nome do produto
- Resultado esperado: página de detalhes exibida com descrição completa

## Módulo: Carrinho

TC-11 | Adicionar múltiplos produtos
- Resultado esperado: contador do carrinho reflete a quantidade correta

TC-12 | Remover produto do carrinho
- Resultado esperado: produto removido e contador atualizado

TC-13 | Carrinho vazio não permite checkout
- Resultado esperado: botão de checkout desabilitado ou redirecionamento bloqueado

## Módulo: Checkout (prioridade crítica)

TC-14 | Checkout completo com dados válidos
- Passos: preencher nome, sobrenome, CEP, finalizar compra
- Resultado esperado: pedido concluído com mensagem de sucesso

TC-15 | Checkout sem nome preenchido
- Resultado esperado: erro "First Name is required"

TC-16 | Checkout sem sobrenome preenchido
- Resultado esperado: erro "Last Name is required"

TC-17 | Checkout sem CEP preenchido
- Resultado esperado: erro "Postal Code is required"

TC-18 | Cancelar checkout retorna ao carrinho
- Resultado esperado: usuário retorna à tela de carrinho sem perder itens

TC-19 | Resumo do pedido exibe valores corretos (subtotal, taxa, total)
- Resultado esperado: cálculo de taxa e total conferem com os itens do carrinho

TC-20 | Finalizar compra limpa o carrinho
- Resultado esperado: após confirmação, carrinho fica vazio e contador zera
