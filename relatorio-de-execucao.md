# Relatório de execução

- **Data e hora:** 06/10/2026, aproximadamente 12h13 (horário de Brasília)
- **Navegador e versão:** navegador integrado do Codex; versão não informada pela interface
- **Sistema operacional:** Windows
- **Usuário de demonstração:** `standard_user`
- **URL:** https://www.saucedemo.com/

Executei os casos no site de demonstração, com dados fictícios no checkout. Para os testes de login, usei uma senha incorreta apenas no CT-002; os demais usaram as credenciais de demonstração exibidas pelo site. Os resultados abaixo descrevem o que observei nesta rodada, neste ambiente.

| Caso | Status | Observação / evidência / bug |
| --- | --- | --- |
| CT-001 | Passou | Login abriu o catálogo em `/inventory.html`. |
| CT-002 | Passou | Senha incorreta foi recusada com mensagem de usuário/senha inválidos. |
| CT-003 | Passou | Login vazio foi recusado com a mensagem `Username is required`. |
| CT-004 | Passou | Logout voltou à tela inicial; ao tentar voltar ao catálogo, o site exigiu login. |
| CT-005 | Passou | O catálogo exibiu seis produtos com nome, preço e botão para adicionar. |
| CT-006 | Passou | Detalhes da mochila abriram com o mesmo nome e preço do catálogo: US$ 29,99. |
| CT-007 | Passou | Preços em ordem crescente: 7,99; 9,99; 15,99; 15,99; 29,99; 49,99. |
| CT-008 | Passou | Nomes apareceram em ordem decrescente, de `Test.allTheThings()` até `Sauce Labs Backpack`. |
| CT-009 | Passou | Mochila apareceu no carrinho uma vez, por US$ 29,99; indicador mostrou 1 item. |
| CT-010 | Passou | Mochila e luz de bicicleta apareceram uma vez cada; indicador mostrou 2 itens. |
| CT-011 | Passou | Removi a luz de bicicleta; ela saiu do carrinho e o indicador voltou a 1 item. |
| CT-012 | Passou | `Continue Shopping` voltou ao catálogo e manteve a mochila no carrinho. |
| CT-013 | Passou | Checkout com campos vazios ficou na primeira etapa e mostrou `First Name is required`. |
| CT-014 | Passou | Resumo exibiu os dois itens: 29,99 + 9,99 = 39,98; taxa de 3,20; total de 43,18. |
| CT-015 | Passou | Pedido de uma mochila chegou à tela `Checkout: Complete!` com `Thank you for your order!`; carrinho ficou vazio. |
| CT-016 | Passou | `Cancel` interrompeu o checkout, voltou ao carrinho e manteve a mochila sem confirmar compra. |

## Resumo

| Métrica | Quantidade |
| --- | ---: |
| Planejados | 16 |
| Executados | 16 |
| Passaram | 16 |
| Falharam | 0 |
| Bloqueados | 0 |

**Conclusão desta rodada:** os 16 cenários passaram e não encontrei um defeito reproduzível nos fluxos cobertos. Isso descreve apenas esta execução; não garante ausência de problemas em outros navegadores, contas ou situações. Nenhum relatório de bug foi aberto.
