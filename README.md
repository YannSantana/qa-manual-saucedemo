# Projeto de QA | SauceDemo

Portfólio de testes manuais da aplicação de demonstração [SauceDemo](https://www.saucedemo.com/). O objetivo é demonstrar planejamento, criação de casos, execução e comunicação de defeitos em um fluxo de compra.

> **Estado:** casos preparados; execução manual ainda não realizada. Os resultados devem ser preenchidos após testar a aplicação. Nenhum defeito é declarado sem reprodução e evidência.

## Escopo

- Login e logout
- Catálogo e ordenação de produtos
- Carrinho
- Checkout e confirmação do pedido

Não fazem parte deste ciclo: cadastro, busca, pagamento real, API e testes de carga. Esses recursos não foram incluídos no fluxo escolhido.

## Como executar

1. Abra [SauceDemo](https://www.saucedemo.com/) em uma janela privada do navegador.
2. Use as credenciais de demonstração exibidas na página. Registre a conta utilizada no relatório.
3. Leia o [plano de testes](plano-de-testes.md) e execute os [casos de teste](casos-de-teste.md) na ordem indicada.
4. Para cada caso, preencha uma linha em [relatorio-de-execucao.md](relatorio-de-execucao.md) com **Passou**, **Falhou** ou **Bloqueado**.
5. Se encontrar uma falha, copie o [modelo de bug](bugs/MODELO-BUG.md), salve como `BUG-001.md` e adicione capturas em `evidencias/`.
6. Atualize este estado com a data, navegador, total de testes e links para os bugs confirmados.

## Organização

| Arquivo | Finalidade |
| --- | --- |
| `plano-de-testes.md` | Estratégia, escopo, riscos e critérios |
| `casos-de-teste.md` | Passos e resultados esperados |
| `relatorio-de-execucao.md` | Registro dos resultados observados |
| `bugs/MODELO-BUG.md` | Estrutura para relatar defeitos reproduzidos |
| `evidencias/` | Capturas ou vídeos dos testes |

## Repositório e próximos passos

Este projeto está publicado em [YannSantana/qa-manual-saucedemo](https://github.com/YannSantana/qa-manual-saucedemo). Para completar a parte prática do portfólio, execute os testes, preencha o relatório e substitua o estado acima pelos resultados reais. Não publique dados pessoais nem credenciais próprias nas evidências.

## Referência

A [documentação oficial da Sauce Labs](https://docs.saucelabs.com/web-apps/automated-testing/selenium/sample-scripts/) usa o SauceDemo como aplicação de exemplo para login e acesso ao catálogo.
