# 21 — Publicação no GitHub Pages

Publicação solicitada em 17/11/2026, após os ajustes visuais aprovados. O responsável autorizou tornar o repositório público porque o plano atual não oferece Pages para este repositório privado.

## Destino

- Repositório: `bernas0610/VivaSE_Cultura-2.0`.
- Site: https://bernas0610.github.io/VivaSE_Cultura-2.0/
- O projeto usa um subdiretório próprio. O repositório e o site do portfólio não são substituídos.
- Fonte de publicação: workflow `.github/workflows/pages.yml` em pushes para `main`, também executável manualmente.

## Configuração

Vite utiliza base relativa (`./`), com logo resolvida por `import.meta.env.BASE_URL`. Imagens de fundo, chunks e worker seguem os caminhos do build. A navegação por hash permite abrir mapa/programação sem regras especiais de servidor.

O workflow instala pelo lockfile, executa os testes de domínio, gera `dist` e publica o artefato oficial de Pages. Os arquivos locais `.env.local`, `tmp`, `node_modules` e `dist` não entram no commit.

`VITE_MAPTILER_KEY` é uma variável do repositório usada no build. Trata-se da chave de navegador do mapa, que faz parte do cliente público. Nenhuma credencial de autenticação do GitHub foi gravada no projeto.

O domínio `bernas0610.github.io` (sem protocolo ou caminho) precisa estar em **Allowed HTTP Origins** da chave MapTiler, além das origens locais existentes. Essa configuração libera as requisições do mapa no domínio; não modifica páginas ou conteúdo do portfólio. No teste inicial, a origem pública retornou 403; o responsável confirmou ter salvo o domínio em 17/11/2026.

## Verificação da publicação

Conferir o resultado do workflow, o carregamento em `/VivaSE_Cultura-2.0/`, a foto, a logo, os chunks e o worker do mapa. A confirmação de que o mapa público carrega depende também da origem permitida no MapTiler.

Build e dez testes de domínio aprovados. Teste local do build no subdiretório `/VivaSE_Cultura-2.0/` confirmou foto, logo, chunks/worker, 20 marcadores e a agenda, sem respostas HTTP locais de erro. A verificação pública será feita após a conclusão do workflow.

## Publicação confirmada

- Commit de implementação: `60a024b`, enviado para `main`.
- Workflow de publicação: [execução 44141859082](https://github.com/bernas0610/VivaSE_Cultura-2.0/actions/runs/44141859082), concluída com sucesso.
- Site público respondeu HTTP 200 em 17/11/2026.
- Foto e logo carregaram a partir do subdiretório do projeto.
- MapTiler respondeu HTTP 200 para a origem pública após salvar `bernas0610.github.io` nas origens permitidas.
- Conferidos 20 pins, busca por Péricles, detalhes e 51 atividades no sábado, 21/11.
- Agenda em 390 px sem rolagem horizontal; nenhum erro JavaScript ou resposta HTTP de falha na verificação.
- Evidências locais: `tmp/pages-public/result.json` e capturas na mesma pasta.

O site do portfólio não foi modificado. A revisão em aparelho físico continua sendo uma validação distinta da automação em navegador.

## Envio das atualizações de 20 e 21/11/2026

Atualizações: plataforma cultural (registro 36) e linha do tempo 2005–2026 (registro 37).

- A primeira tentativa de envio para `bernas0610/VivaSE_Cultura-2.0` foi recusada com HTTP 403: a conta `andersonsanto09`, usada pelo Git neste computador, ainda não tinha permissão de escrita.
- Enquanto isso, um repositório temporário foi criado no perfil `andersonsanto09`, com Pages, a pedido do responsável.
- Depois que a permissão de escrita foi concedida, as atualizações foram enviadas para `main` do repositório original, como avanço direto a partir de `bf478f5`. O workflow existente publicou o site no mesmo endereço.
- O responsável pediu a remoção do repositório temporário. A situação da remoção está no [registro 37](37-LINHA-DO-TEMPO-2005-2026.md).
- A variável `VITE_MAPTILER_KEY` e a origem `bernas0610.github.io` no MapTiler já estavam configuradas desde 17/11; nada mudou nelas.
