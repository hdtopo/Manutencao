# Garagem — Controle de Manutenção Veicular (GitHub Pages)

Aplicação estática feita em HTML, CSS e JavaScript puro. Não precisa de Python, PHP ou servidor próprio.

## Publicar no GitHub Pages
1. Crie um repositório no GitHub (por exemplo `garagem`).
2. Envie os arquivos `index.html`, `style.css`, `app.js` e `README.md` para a raiz do repositório.
3. Abra **Settings → Pages**.
4. Em **Build and deployment**, escolha **Deploy from a branch**.
5. Selecione a branch `main` e a pasta `/ (root)`, depois clique em **Save**.
6. Aguarde o GitHub informar o endereço do site.

## Recursos
- Cadastro, edição e exclusão de veículos.
- Cadastro de componentes com intervalo por km e/ou dias.
- Registro de manutenção, peças, mão de obra, observações e próxima revisão.
- Atualização de hodômetro e histórico.
- Alertas visuais: vencida, atenção (até 7 dias ou até 50 km) e em dia.
- Exportação e importação de backup JSON.
- Layout adaptado para celular.

## Limitação importante desta versão
Os dados são guardados no `localStorage` do navegador. Portanto:
- ficam neste navegador e neste aparelho;
- não há login real nem sincronização entre aparelhos;
- limpar os dados do navegador pode apagar os registros;
- exporte backups regularmente.

O GitHub Pages hospeda apenas os arquivos estáticos. Para login, banco de dados online, sincronização e notificações automáticas, será necessário conectar um serviço externo (por exemplo Supabase ou Firebase) e configurar as credenciais com segurança. Não publique senhas ou chaves privadas no repositório.
