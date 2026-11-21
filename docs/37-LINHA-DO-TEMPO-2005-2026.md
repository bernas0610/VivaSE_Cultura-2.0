# 37 — Linha do tempo de 2005 a 2026

Revisão: 21/11/2026. Ajuste solicitado pelo responsável em 20/11/2026: a tela **Cultura → Linha do tempo** (`#/historia`) passa a mostrar somente o período de 2005 a 2026.

## O que mudou

| Item | Antes | Depois |
| --- | --- | --- |
| Marcos exibidos | 15, de 1972 a 2026 | 14, de 2005 a 2026 |
| Filtro “Festival” | 14 marcos | 13 marcos |
| Filtro “Cidade” | 1 marco (2010) | 1 marco (2010), sem alteração |
| Seletor “Edição da linha do tempo” | 18 edições, de 1972 a 2025 | 8 edições: 2005, 2017, 2018, 2019, 2022, 2023, 2024 e 2025 |
| Texto de abertura | “Explore 15 marcos documentados…” | “Explore 14 marcos documentados de 2005 a 2026…” |

O único marco removido da tela é “O primeiro encontro” (1972). As edições de 1972, 1973, 1984, 1985 e de 1988 a 1993 deixam de aparecer no seletor desta tela.

Um endereço antigo que aponte para uma edição fora do período (por exemplo, `#/historia?edicao=1972`) não mostra lista vazia: a tela ignora o parâmetro e abre a trajetória completa de 2005 a 2026.

## O que não mudou

O recorte vale **somente para a tela da linha do tempo**. Nenhum dado foi apagado.

- `src/data/history.ts` continua com o marco de 1972 e as 18 edições.
- A máquina do tempo e o mapa histórico (`#/mapa?modo=historico`) continuam com as 18 edições, de 1972 a 2025.
- A página de artistas (`#/artistas`) continua com trajetórias e filtros que incluem edições anteriores a 2005.
- O formulário de memórias continua aceitando lembranças a partir de 1972.
- A publicação sobre a história do FASC na plataforma (`src/platform/content/posts.ts`) continua citando a criação do festival em 1972.

Se o recorte de 2005 a 2026 precisar valer para o site inteiro, essa é uma decisão nova: afeta mapa histórico, artistas, testes de domínio e documentos 23, 24 e 33.

## Implementação

Arquivo: `src/features/HistoryTimeline.tsx`.

- Constantes `FIRST_YEAR = 2005` e `LAST_YEAR = 2026` definem o período num único lugar.
- `timelineMilestones` e `timelineEditions` filtram `historicalMilestones` e `festivalEditions` por ano.
- O parâmetro `edicao` só é aplicado se a edição pertencer ao período.
- O texto de abertura usa a contagem filtrada e as constantes.

Para mudar o período no futuro, basta alterar as duas constantes.

## Verificação

- `npm run typecheck`: sem erros.
- `npm test`: 52 testes aprovados. Os testes de domínio continuam esperando 1972 nos dados, o que é correto, porque os dados não mudaram.
- Navegador (Vite dev, 21/11/2026): 14 marcos, primeiro ano 2005, nenhum 1972 na lista; seletor com as oito edições do período; `#/historia?edicao=1972` abre os 14 marcos; nenhum erro no console.
- `tests/phase-4.py` foi atualizado para esperar 14 marcos (13 no filtro Festival), primeiro ano 2005 e ausência de 1972. Ele não foi executado neste ambiente, porque o pacote `playwright` não está instalado.
- `npm run build`: aprovado. Continua o aviso de chunk acima de 500 kB do mapa (`MapView`), sem relação com esta mudança.

## Publicação

- Commit `d41758d`: plataforma cultural (registro 36), linha do tempo 2005–2026 e documentação.
- A primeira tentativa de push para `bernas0610/VivaSE_Cultura-2.0` foi recusada (HTTP 403): a conta `andersonsanto09` ainda não tinha permissão de escrita.
- Enquanto isso, um repositório temporário foi publicado em `andersonsanto09/VivaSE_Cultura-2.0`, a pedido do responsável. O workflow dele passou e o site abriu, mas sem o mapa vetorial, porque a variável `VITE_MAPTILER_KEY` não existia lá.
- Com a permissão de escrita concedida, os commits foram enviados para `main` do repositório original, como avanço direto a partir de `bf478f5` (até `f823c98`).
- Workflow de publicação: [execução 44917032378](https://github.com/bernas0610/VivaSE_Cultura-2.0/actions/runs/44917032378), com build (incluindo `npm test`) e deploy concluídos com sucesso em 21/11/2026.
- Repositório temporário: o Pages dele foi desativado e o site temporário saiu do ar. A exclusão do repositório ficou com o responsável, porque a credencial do Git neste computador não tem a permissão `delete_repo`.

Verificação no site público (https://bernas0610.github.io/VivaSE_Cultura-2.0/), em 21/11/2026:

- Home da plataforma abre na raiz, com as 13 imagens carregadas.
- `#/historia`: 14 marcos, primeiro ano 2005, nenhum 1972, texto “de 2005 a 2026”.
- `#/mapa?dia=21`: mapa vetorial do MapTiler carregado (respostas 200), 20 pins e lista com os 20 espaços.
- Nenhum erro no console nas páginas visitadas.
