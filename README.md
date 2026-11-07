# Garagem — Controle de Manutenção V2

Aplicação 100% HTML/CSS/JavaScript, pronta para GitHub Pages.

## Recursos

- Cadastro de veículos.
- Cadastro de componentes com intervalo em km e/ou dias.
- Cálculo automático da próxima manutenção quando um componente é selecionado.
- Alertas quando faltam até 7 dias ou até 50 km.
- Registro de manutenções, custos e quilometragem.
- Histórico e painel geral.
- Cadastro de celular por veículo.
- Botões de envio de lembrete por WhatsApp ou SMS a partir do alerta.
- Backup e restauração em JSON.
- Dados armazenados no navegador via localStorage.

## Publicar no GitHub Pages

1. Crie um repositório no GitHub.
2. Envie todos os arquivos desta pasta para a raiz do repositório.
3. No GitHub, abra **Settings → Pages**.
4. Em **Build and deployment**, selecione **Deploy from a branch**.
5. Selecione a branch `main` e a pasta `/ (root)`.
6. Salve e aguarde a publicação.

## Como funciona o cálculo automático

Ao cadastrar uma manutenção e escolher um componente:

- `Próxima troca (km) = km da manutenção + intervalo do componente`.
- `Próxima troca (data) = data da manutenção + intervalo em dias`.

Se você preencher manualmente a próxima data ou km, o sistema preserva o valor informado.

## Avisos por WhatsApp/SMS

O sistema identifica automaticamente os alertas de **7 dias ou 50 km** e mostra os botões WhatsApp e SMS.

O número deve ser cadastrado no campo **Celular para avisos** do veículo, preferencialmente com DDD. O WhatsApp abre a conversa com a mensagem pronta e o SMS abre o aplicativo de mensagens com o texto preenchido.

### Importante sobre envio automático

O GitHub Pages é hospedagem estática. Por segurança, ele não deve guardar credenciais de APIs de WhatsApp/SMS nem executar um agendador no servidor. Por isso, esta V2 faz o disparo com um clique pelo celular.

Para a próxima versão, podemos conectar um serviço de backend/banco de dados e uma API oficial de mensagens para que o sistema envie automaticamente os avisos sem precisar abrir o site.

## Dados

Os dados desta V2 ficam no navegador do aparelho. Use **Exportar dados** regularmente. A próxima evolução pode usar banco de dados online para sincronizar celular, computador e outros usuários.
