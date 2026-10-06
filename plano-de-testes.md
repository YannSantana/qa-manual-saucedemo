# Plano de testes

## Por que escolhi esse fluxo

Quero verificar se uma pessoa consegue fazer uma compra de demonstração sem se perder ou encontrar um bloqueio: entrar, escolher produtos, revisar o carrinho e chegar à confirmação do pedido. Também incluí situações em que falta informação ou a senha está errada, porque mensagens claras fazem parte de uma boa experiência.

## Onde vou testar

- Site: https://www.saucedemo.com/
- Ambiente: navegador desktop; vou anotar nome, versão e sistema operacional no relatório.
- Conta: uma das contas de demonstração exibidas na página. Vou registrar qual usei em cada rodada.
- Início de cada rodada: janela privada, para evitar que uma sessão ou carrinho antigo altere o resultado.
- Checkout: dados fictícios (`Ana`, `Teste`, `12345`).

## O que entra neste ciclo

Login, logout, catálogo, ordenação, detalhes de produto, carrinho, checkout e confirmação. Os casos estão em [casos-de-teste.md](casos-de-teste.md).

Ficam de fora cadastro, busca, pagamento real, API, desempenho e acessibilidade. São assuntos importantes, mas este primeiro ciclo está focado no fluxo funcional de compra.

## Como vou avaliar

Vou seguir os passos de cada caso, comparar o que aparece na tela com o resultado esperado e registrar **Passou**, **Falhou** ou **Bloqueado**. Se algo parecer errado, vou repetir o cenário antes de abrir um bug. Para conferir valores, usarei os preços e taxas mostrados pelo site no momento da execução, sem depender de preços fixos.

Os fluxos de login, carrinho e finalização têm prioridade alta porque impedem a compra quando falham. Ordenação, navegação e mensagens de validação têm prioridade média neste ciclo.

## Quando a rodada estará concluída

Todos os 16 casos terão um status no relatório. Cada falha confirmada terá passos para reprodução e evidência. Se o site estiver indisponível ou algum teste não puder começar, vou marcar **Bloqueado** e explicar o motivo.

O SauceDemo é uma aplicação pública de demonstração e pode mudar. Por isso, os resultados esperados são hipóteses de teste: uma diferença observada não vira bug automaticamente. Primeiro preciso entender o comportamento e confirmar que o problema é reproduzível.
