# HZM Soluções — Grand Chase Classic

Painel pessoal para organizar personagens, desafios e pedidos de serviços do Grand Chase Classic.

## Organização dos dados

- **Minha conta:** contas do jogo, personagens, desafios semanais e marcações pessoais ficam no navegador atual.
- **Controle de vendas:** clientes/pedidos, itens vendidos, taxas da plataforma, tempos individuais e observações de melhoria são salvos no Supabase do projeto `hzm-solutions`.
- Os pedidos exigem login. Cada conta autenticada só pode acessar seus próprios registros por meio das políticas de segurança do banco (RLS).
- O catálogo inicial é criado automaticamente no primeiro acesso autenticado, sem valores fixos.

## Registrar um pedido

1. Entre na aba **Controle de vendas** e crie uma conta de acesso com seu e-mail e uma senha, ou entre com a conta existente.
2. Informe o cliente ou identificador do pedido, data, status, plataforma e a taxa cobrada pela plataforma (se houver).
3. Escolha o modo de cobrança:
   - **Cobrar por item:** informe o valor de cada serviço.
   - **Cobrar por pacote:** informe um único valor para o pedido inteiro; os itens e seus tempos continuam registrados, mas o sistema não inventa uma divisão de receita entre eles.
4. Adicione os serviços do catálogo, a quantidade, o personagem usado e, se quiser, uma observação sobre melhorias no personagem.
5. Registre cada tempo individualmente, use o cronômetro ou cole uma lista no formato `mm:ss`.
6. Salve o pedido. Os pedidos e os tempos de execução ficam no banco, permitindo consultar o histórico em outro dispositivo depois de entrar na mesma conta.

O catálogo inclui Void 1, Void 2, Void 3, Void 4, pacotes Void semanal e mensal, Torre das Ilusões, Eclipse, Harrier, Kricktria, Farm Abyssal e opções de up de personagem. Os valores não são predefinidos: você os informa ao criar cada pedido.

## Análises

O painel calcula faturamento, taxas, tempo registrado, retorno geral por hora e ranking de serviços. Para pedidos cobrados por item, estima o retorno por serviço descontando uma parte proporcional da taxa do pedido. Em pedidos por pacote, não atribui receita artificialmente a cada serviço; os tempos continuam sendo usados para comparar desempenho.

Os tempos de execução são associados ao personagem informado na linha do serviço. A observação de melhoria permite registrar marcos como troca de arma ou evolução de equipamento e comparar os tempos antes e depois.

## Limitações e backup

- Dados da área **Minha conta** ficam no navegador e não são sincronizados. Limpar os dados do site pode apagá-los; o botão **Exportar backup** pode ser usado para guardar uma cópia.
- Os pedidos ficam no Supabase e não dependem do armazenamento local do navegador.
- Imagens locais dos personagens ficam apenas no navegador atual.
- Se o Supabase exigir confirmação de e-mail, confirme a mensagem recebida antes de entrar.

## Publicar com GitHub Pages

1. Abra **Settings → Pages** neste repositório.
2. Em **Build and deployment**, selecione **Deploy from a branch**.
3. Selecione a branch `main` e a pasta `/ (root)`, depois salve.
4. Aguarde a publicação e abra o endereço informado pelo GitHub Pages.

Este é um projeto pessoal de organização e análise. Não é afiliado oficialmente à KOG ou à GGMAX.
