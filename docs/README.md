# VivaSE Cultura — Fase 1

Data de referência: 16/11/2026; estado atualizado em 21/11/2026. Fase 1 encerrada como planejamento; fase 2 concluída tecnicamente e revisada pelo responsável. Fases 3 e 4 encerradas no escopo funcional do protótipo. Fase 5 em andamento: qualidade final e pitch de três minutos. Em 20/11 o VivaSE ganhou uma camada de plataforma cultural sobre o FASC ([36](36-PLATAFORMA-CULTURAL.md)) e, em 21/11, a linha do tempo passou a mostrar só 2005 a 2026 ([37](37-LINHA-DO-TEMPO-2005-2026.md)). Consulte o [checklist atualizado](13-CHECKLIST-DO-PROJETO.md) e a [migração do mapa e correções](14-MAPA-VETORIAL-E-REVISAO-VISUAL.md).

## Objetivo

Planejar um protótipo para apresentação no ideathon: um guia para turistas que não conhecem São Cristóvão se orientarem durante o FASC, com acesso ao contexto cultural dos lugares.

## Documentos da Fase 1

| Documento | Pergunta principal | Estado |
| --- | --- | --- |
| [01 — Visão do produto](01-VISAO-DO-PRODUTO.md) | Para quem e para que estamos construindo? | Escopo consolidado |
| [02 — Requisitos](02-REQUISITOS.md) | O que o primeiro protótipo precisa fazer? | P0/P1 e critérios planejados |
| [03 — Arquitetura](03-ARQUITETURA.md) | Como organizar a aplicação e os dados? | Proposta sem backend |
| [04 — Direção visual e design system](04-DIRECAO-VISUAL.md) | Como o VivaSE deve se apresentar? | Direção aceita provisoriamente; refinamento no protótipo |
| [05 — Experiência e jornadas](05-EXPERIENCIA-E-JORNADAS.md) | Como o visitante encontra o que procura? | Seis jornadas propostas |
| [06 — Mapa, localização e roteiros](06-MAPA-LOCALIZACAO-E-ROTEIROS.md) | Como orientar o visitante com informações confiáveis? | Inventário, precisão e trajeto externo |
| [07 — Performance, descoberta e acessibilidade](07-QUALIDADE-E-ACESSIBILIDADE.md) | Como tornar a experiência legível e utilizável? | Metas propostas; sem medições |
| [08 — Estratégia de testes](08-ESTRATEGIA-DE-TESTES.md) | Que evidências demonstram que o protótipo funciona? | 20 cenários planejados; não executados |
| [09 — Roadmap, riscos e dúvidas](09-ROADMAP.md) | Qual a sequência e o que falta decidir? | Janela de 16 a 21/11 e pendências |
| [10 — Decisões técnicas](10-DECISOES-TECNICAS.md) | O que foi decidido, por quem e por quê? | Decisões confirmadas e propostas distintas |

## Acompanhamento da implementação

- [11 — Fundação e verificações](11-FASE-2-FUNDACAO.md).
- [12 — Inventário e programação](12-INVENTARIO-E-PROGRAMACAO.md).
- [13 — Checklist de todas as fases](13-CHECKLIST-DO-PROJETO.md).

## Materiais de apoio

- [Matriz CSD em texto](MATRIZ-CSD.md).
- [Matriz CSD em PDF](../output/pdf/VivaSE-Matriz-CSD.pdf).
- [Fontes e critérios de pesquisa](FONTES-E-CURADORIA.md).
- Materiais recebidos: pitch Oxente Labs, Business Model Canvas e 15 prints da versão anterior.

Os materiais anteriores são referências para o produto; alegações históricas, horários, estatísticas e depoimentos neles presentes precisam de verificação individual.

## Escopo confirmado

1. FASC 2026, de 20 a 22/11, com programação oficial como base. O ideathon é de 19 a 21/11; são calendários diferentes.
2. Todos os espaços com atividades do evento, identificados pela pesquisa, com pendências registradas.
3. Entrada, mapa, localização, busca, programação, detalhes, roteiros culturais, memórias e linha do tempo.
4. Trajetos em aplicativo externo. Memórias pessoais no próprio navegador e exemplos fictícios identificados.
5. Área administrativa e comparação estatística entre edições fora desta primeira entrega.
6. Prioridade: orientação durante o festival, descoberta cultural e preservação da memória, nesta ordem.

Perfil da banca, duração e recursos do pitch ainda desconhecidos. A cobertura integral do conteúdo é um requisito, não uma pesquisa já concluída. Próximo passo: revisar o protótipo com o responsável, concluir a validação dos fluxos e construir roteiros, memórias e linha do tempo.

## Repositório

Destino: [VivaSE_Cultura-2.0](https://github.com/bernas0610/VivaSE_Cultura-2.0), publicado em [bernas0610.github.io/VivaSE_Cultura-2.0](https://bernas0610.github.io/VivaSE_Cultura-2.0/). O envio de 21/11/2026 está registrado no [documento 21](21-PUBLICACAO-GITHUB-PAGES.md). A configuração local aponta `origin` para a nova versão e preserva o repositório antigo como `legacy`. A documentação inicial foi enviada no commit `6d2bb88`. O responsável solicitou um novo snapshot de implementação e documentação; o resultado da sincronização deve ser conferido no Git. A pasta local mantém o nome `VivaSE_Cultura`.

## Forma de trabalho

Registrar separadamente decisões confirmadas, recomendações, hipóteses e perguntas. Perguntar ao responsável quando faltar contexto que altere o produto. Discutir a direção visual antes de fechar o design system e de começar a implementação das telas. Não atribuir resultados de testes ou validação com turistas a esta documentação.

Revisão após feedback: [14 — Mapa vetorial, ícones e identidade FASC](14-MAPA-VETORIAL-E-REVISAO-VISUAL.md).

- [15 — Encerramento, evidências e limites da fase 3](15-FASE-3-VALIDACAO.md).

Revisão histórica da orientação/visual: [16 — Mapa, agenda e entrada](16-REVISAO-MAPA-AGENDA-E-LANDING.md). A proposta intermediária de agrupamento foi substituída pela decisão de pins individuais do registro 17. Cards filtram categorias; agenda inclui categoria e modo “agora” por intervalos publicados.

- [17 — Decisão final de pins individuais e próximos passos](17-PINS-INDIVIDUAIS-E-PROXIMOS-PASSOS.md).

- [18 — Correção do zoom e acabamento antes da fase 4](18-CORRECAO-ZOOM-E-ACABAMENTO.md), revisão de 17/11/2026.

- [19 — Implementação da direção visual aprovada](19-DIRECAO-VISUAL-IMPLEMENTADA.md): Cartaz vivo + Atlas cultural, refinamentos e validação de 17/11/2026.

- [20 — Correção da visão geral e proposta com fotografia](20-ZOOM-GERAL-E-PROPOSTA-FOTOGRAFICA.md): separação proporcional ao zoom e fotografia aplicada após avaliação.

- [21 — Publicação no GitHub Pages](21-PUBLICACAO-GITHUB-PAGES.md): endereço do projeto, build e configuração do domínio do mapa.

- [22 — Fase 4: roteiros, memórias, história e fotografias](22-FASE-4-CULTURA-E-FOTOS.md): implementação local, evidências e pendências de curadoria.

- [23 — Mapa histórico interativo e acervo de artistas](23-MAPA-HISTORICO-E-ACERVO.md): nove edições, 15 marcos, 36 artistas/grupos, reprodução, integração e evidências. A tela da linha do tempo hoje mostra 14 marcos (registro 37).

- [24 — Pesquisa integrada e máquina do tempo](24-PESQUISA-INTEGRADA-E-MAQUINA-DO-TEMPO.md): merge das seis pesquisas, curadoria, trajetórias, fotografias e correções de interação.

- [25 — Refinamento visual e acervo fotográfico](25-REFINAMENTO-VISUAL-E-ACERVO-FOTOGRAFICO.md): Home editorial, retratos, detalhes, agenda e mapa.

- [26 — Programação pessoal, Cultura e aviso do mapa](26-PROGRAMACAO-PESSOAL-E-CULTURA.md).
- [27 — Sobre: propósito, equipe e transparência](27-SOBRE-EDITORIAL-E-TRANSPARENCIA.md).
- [28 — Auditoria dos retratos do acervo](28-AUDITORIA-DOS-RETRATOS.md).
- [29 — Revisão da realização das participações históricas](29-REVISAO-DAS-PARTICIPACOES.md).
- [30 — Expansão das fotografias dos artistas](30-EXPANSAO-DAS-FOTOS-DOS-ARTISTAS.md).
- [31 — Programação no mapa histórico](31-PROGRAMACAO-NO-MAPA-HISTORICO.md).
- [32 — Datas históricas e rolagem](32-DATAS-HISTORICAS-E-ROLAGEM.md).
- [33 — Fechamento da fase 4](33-FECHAMENTO-FASE-4.md): descoberta cultural e memória.

- [34 — Fase 5: qualidade e apresentação](34-FASE-5-QUALIDADE-E-PITCH.md).
- [35 — Roteiro do pitch de três minutos](35-ROTEIRO-PITCH-3-MINUTOS.md) e [apoio local com capturas reais](apresentacao/index.html).
- [36 — Plataforma cultural de São Cristóvão](36-PLATAFORMA-CULTURAL.md): nova Home, rotas, preservação do FASC, Senhor dos Passos, publicações e fontes.
- [37 — Linha do tempo de 2005 a 2026](37-LINHA-DO-TEMPO-2005-2026.md): recorte da tela, o que foi preservado no acervo e verificação.
