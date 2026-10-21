# HZM Soluções — Grand Chase Classic

Painel pessoal para organizar personagens, desafios semanais e pedidos de serviços do Grand Chase Classic.

## Como usar
- Abra `index.html` em um navegador ou publique o repositório com GitHub Pages.
- Na aba **Minha conta**, cadastre cada conta do jogo e os personagens que pertencem a ela.
- O catálogo de personagens inclui Elesis, Lire, Arme, Lass, Ryan, Ronan, Amy, Jin, Sieghart, Mari, Dio, Zero, Rey, Lupus, Lin, Azin, Holy, Edel, Veigas, Uno, Decanee, Ai, Kallia e Iris.
- Na aba **Controle de vendas**, crie um pedido, adicione cada fase/material como um serviço, informe a quantidade contratada e o valor atribuído a esse serviço.
- Registre o tempo de cada ida individualmente com o formato `mm:ss`, ou use **Colar tempos** para inserir uma lista separada por vírgulas ou linhas.
- O painel calcula tempo total, média por ida, valor por hora/minuto e ranking por serviço. As taxas/custos informados no pedido são distribuídos proporcionalmente entre os serviços para estimar o retorno líquido.
- Use **Exportar backup** regularmente para guardar uma cópia JSON dos dados.

## Armazenamento e limitações atuais
Esta primeira versão salva os dados no `localStorage` do navegador e do dispositivo em que for usada. Os registros não são sincronizados entre computadores ou navegadores. Para sincronização entre dispositivos e autenticação, será necessário integrar um banco de dados, como Supabase.

Os retratos padrão são carregados de URLs do site Grand Chase Creator. Se uma imagem externa deixar de estar disponível, o painel exibe as iniciais do personagem; também é possível informar outra URL ou carregar uma imagem do computador. Imagens carregadas do computador ficam apenas no navegador atual e podem aumentar o tamanho do backup.

## Publicar com GitHub Pages
1. Abra **Settings → Pages** neste repositório.
2. Em **Build and deployment**, selecione **Deploy from a branch**.
3. Selecione a branch `main` e a pasta `/ (root)`, depois salve.
4. Aguarde a publicação e abra o endereço informado pelo GitHub Pages.

Este é um projeto pessoal de organização e análise. Não é afiliado oficialmente à KOG ou à GGMAX.
