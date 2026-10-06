# Plano de testes

## Objetivo

Verificar se um usuário de demonstração consegue entrar, selecionar produtos, revisar o carrinho e concluir um pedido no SauceDemo.

## Ambiente e dados

- Aplicação: https://www.saucedemo.com/
- Plataforma: navegador desktop; registrar nome e versão no relatório
- Conta: usuário de demonstração informado pela aplicação; registrar qual foi utilizado
- Estado inicial: nova janela privada para evitar carrinho ou sessão anterior
- Dados de checkout: dados fictícios, como `Ana`, `Teste`, `12345`

## Estratégia

Executar testes funcionais manuais dos fluxos principais e de validações negativas. Observar mensagens exibidas, mudança de página, conteúdo do carrinho e confirmação final. Registrar cada resultado e uma evidência para falhas. Os valores monetários devem ser conferidos conforme os números exibidos na execução, sem pressupor preços fixos.

## Prioridades

- **Alta:** login, inclusão/remoção no carrinho, checkout e pedido concluído.
- **Média:** ordenação, navegação e mensagens de validação.

## Critérios de entrada

Aplicação acessível, navegador disponível e conta de demonstração funcional.

## Critérios de saída

Todos os casos com status registrado; falhas documentadas com passos reproduzíveis; resumo com quantidade de casos que passaram, falharam ou ficaram bloqueados. Se o ambiente estiver indisponível, registrar o bloqueio em vez de marcar falha do produto.

## Riscos e limites

O site é uma demonstração pública e pode mudar. Mensagens e comportamento esperados neste projeto são hipóteses de teste; divergências precisam ser avaliadas antes de abrir um bug. O projeto não valida transações financeiras reais.
