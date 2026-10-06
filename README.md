# Testando uma compra no SauceDemo

Este é meu primeiro projeto de QA. Escolhi o [SauceDemo](https://www.saucedemo.com/) porque ele permite acompanhar uma jornada de compra do começo ao fim: entrar na conta, escolher produtos, conferir o carrinho e finalizar o pedido.

Organizei aqui o que pretendo testar, os passos de cada cenário e um espaço para registrar o que realmente acontecer durante a execução. Quero que qualquer pessoa consiga entender meu raciocínio e repetir os testes.

> **Onde o projeto está agora:** preparei 16 casos de teste, mas ainda não executei os cenários. O [relatório](relatorio-de-execucao.md) está em branco de propósito. Só vou marcar um resultado ou abrir um bug depois de observar o comportamento no site.

## O que estou cobrindo

- Login e logout
- Visualização e ordenação dos produtos
- Inclusão e remoção de itens no carrinho
- Preenchimento do checkout e confirmação do pedido

Não incluí cadastro, busca, pagamento real, API ou testes de carga neste primeiro ciclo.

## Como repetir os testes

1. Abra o [SauceDemo](https://www.saucedemo.com/) em uma janela privada.
2. Use uma das contas de demonstração mostradas na página de login.
3. Leia o [plano](plano-de-testes.md) e siga os [casos de teste](casos-de-teste.md).
4. Anote cada resultado no [relatório](relatorio-de-execucao.md), junto com o navegador e a data.
5. Se encontrar um problema, tente reproduzi-lo mais uma vez. Depois, use o [modelo de bug](bugs/MODELO-BUG.md) e salve a evidência em `evidencias/`.

## O que você vai encontrar aqui

| Arquivo | Para que serve |
| --- | --- |
| [Plano de testes](plano-de-testes.md) | Explica o objetivo, o escopo e como vou conduzir a execução. |
| [Casos de teste](casos-de-teste.md) | Traz os passos e o resultado esperado de cada cenário. |
| [Relatório de execução](relatorio-de-execucao.md) | Reúne os resultados observados e um resumo da rodada. |
| [Modelo de bug](bugs/MODELO-BUG.md) | Ajuda a descrever uma falha de forma que outra pessoa consiga reproduzi-la. |
| [Evidências](evidencias/README.md) | Guarda capturas de tela e vídeos relacionados aos testes. |

## Próximo passo

Executar os 16 casos, preencher o relatório e acrescentar apenas os bugs que forem confirmados. O repositório está em [YannSantana/qa-manual-saucedemo](https://github.com/YannSantana/qa-manual-saucedemo).

## Referência

A [documentação da Sauce Labs](https://docs.saucelabs.com/web-apps/automated-testing/selenium/sample-scripts/) usa o SauceDemo em exemplos de teste de login e acesso ao catálogo.
