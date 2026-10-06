# Casos de teste

Preparei estes cenários para acompanhar uma compra de ponta a ponta e conferir algumas situações de erro. Cada caso tem uma ação concreta e algo que espero ver na tela. Ainda preciso executá-los para saber o resultado real.

**Antes de começar:** abra uma janela privada. Nos casos após o login, use uma conta de demonstração válida. Antes de testar o carrinho, remova os itens deixados por outro cenário. Anote no relatório qualquer diferença entre o esperado e o observado.

## Login e sessão

### CT-001 — Login válido | Alta
1. Abra a página inicial.
2. Informe usuário e senha válidos da demonstração.
3. Selecione **Login**.

**Esperado:** o catálogo de produtos é exibido e a sessão fica ativa.

### CT-002 — Senha inválida | Média
1. Abra a página inicial.
2. Informe um usuário de demonstração válido e uma senha incorreta.
3. Selecione **Login**.

**Esperado:** a entrada é recusada, há mensagem de erro e o catálogo não é aberto.

### CT-003 — Campos de login vazios | Média
1. Abra a página inicial sem preencher os campos.
2. Selecione **Login**.

**Esperado:** a entrada é recusada e a interface informa o dado necessário.

### CT-004 — Logout | Alta
1. Entre com credenciais válidas.
2. Abra o menu e selecione **Logout**.

**Esperado:** a página de login volta a ser exibida; uma página protegida não deve permanecer acessível pela navegação comum.

## Catálogo

### CT-005 — Lista de produtos | Alta
1. Faça login.
2. Observe o catálogo.

**Esperado:** produtos são exibidos com nome, preço e ação para adicionar ao carrinho.

### CT-006 — Detalhes de um produto | Média
1. Faça login.
2. Abra um produto pelo nome ou imagem.
3. Compare nome e preço com os exibidos na lista.

**Esperado:** a página de detalhes abre para o produto selecionado, com dados consistentes.

### CT-007 — Ordenar por preço crescente | Média
1. Faça login.
2. Selecione a opção de ordenar por preço do menor para o maior.
3. Leia os preços na ordem apresentada.

**Esperado:** cada preço é maior ou igual ao anterior.

### CT-008 — Ordenar por nome decrescente | Média
1. Faça login.
2. Selecione a opção de ordenar por nome de Z a A.
3. Leia os nomes na ordem apresentada.

**Esperado:** os nomes aparecem em ordem alfabética decrescente.

## Carrinho

### CT-009 — Adicionar um produto | Alta
1. Faça login com carrinho vazio.
2. Adicione um produto.
3. Abra o carrinho.

**Esperado:** o produto correto aparece no carrinho; nome e preço correspondem ao catálogo.

### CT-010 — Adicionar dois produtos | Alta
1. Faça login com carrinho vazio.
2. Adicione dois produtos diferentes.
3. Abra o carrinho.

**Esperado:** ambos aparecem uma vez; o indicador do carrinho representa a quantidade de itens.

### CT-011 — Remover produto | Alta
1. Faça login e adicione um produto.
2. Abra o carrinho e remova o produto.

**Esperado:** o item deixa de aparecer no carrinho; o indicador é atualizado.

### CT-012 — Continuar comprando | Média
1. Faça login e abra o carrinho.
2. Selecione **Continue Shopping**.

**Esperado:** o catálogo volta a ser exibido, sem perda indevida dos itens mantidos no carrinho.

## Checkout

### CT-013 — Campos obrigatórios | Alta
1. Adicione um produto e inicie o checkout.
2. Deixe os campos de identificação vazios e selecione **Continue**.

**Esperado:** a próxima etapa não abre e a interface indica um campo obrigatório.

### CT-014 — Resumo do pedido | Alta
1. Adicione dois produtos diferentes.
2. Inicie o checkout e preencha dados fictícios válidos.
3. Avance ao resumo e compare itens, preços e total exibidos.

**Esperado:** os itens correspondem ao carrinho e o total é coerente com subtotal e taxas exibidas.

### CT-015 — Concluir pedido | Alta
1. Adicione um produto.
2. Preencha dados fictícios válidos e avance ao resumo.
3. Selecione **Finish**.

**Esperado:** a aplicação mostra uma confirmação de pedido concluído.

### CT-016 — Cancelar checkout | Média
1. Adicione um produto e inicie o checkout.
2. Selecione **Cancel** antes de concluir o pedido.

**Esperado:** o checkout é interrompido sem confirmação de compra; os itens do carrinho continuam disponíveis.
