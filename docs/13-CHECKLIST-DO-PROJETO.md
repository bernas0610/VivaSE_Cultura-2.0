# 13 — Checklist de todas as fases do projeto

Atualizado em 21/11/2026. `[x]` = executado/registrado; `[ ]` = pendente ou ainda depende de aceite. Uma função existente não encerra sua fase sem a validação correspondente. Este é o estado do protótipo desta revisão, não uma promessa de prazo.

**Fases 1 a 4 concluídas no escopo funcional do protótipo. Próxima: fase 5 — qualidade final e preparação do pitch. O teste físico dos novos fluxos foi confirmado sem problemas em 19/11; a revisão final de publicação permanece na fase 5.** Limites e evidências da orientação estão no [relatório da fase 3](15-FASE-3-VALIDACAO.md).

**Revisão estética antes da fase 4:** mescla aprovada de Cartaz vivo e Atlas cultural implementada em 17/11/2026. Evidências e limites no [registro 19](19-DIRECAO-VISUAL-IMPLEMENTADA.md). A avaliação visual desta versão pelo responsável permanece pendente.

- [x] Home com abertura de Cartaz vivo, calendário editorial e categorias em faixa roxa.
- [x] Cabeçalhos amarelos no mapa e na programação; linha do tempo com cards por categoria.
- [x] Hierarquia de ícone/título/ação, CTAs distintos e microinterações curtas com movimento reduzido.
- [x] Filtros recolhíveis, informações práticas antecipadas e estado de “agora” fora do festival.
- [x] Regressão de orientação, gestos e estabilidade dos pins; reflow até 320 px.
- [ ] Aceite visual da versão implementada e nova conferência em celular físico.
- [x] Corrigir o afastamento excessivo dos pins na visão geral, com separação proporcional ao zoom e referências preservadas (registro 20).
- [x] Aprovar a fotografia, sua largura e o dourado da Home; publicação solicitada pelo responsável.
- [x] Commit/push realizados e GitHub Pages publicado; foto, logo, mapa, busca e programação verificados no endereço público (registro 21).

## Fase 1 — Planejamento e definição do produto

**Situação: encerrada como planejamento.**

- [x] Público principal: turista que precisa se orientar durante o FASC.
- [x] Prioridades: orientação, descoberta cultural e preservação da memória.
- [x] Escopo do MVP e critérios de aceite registrados.
- [x] Edição 2026 e distinção entre datas do festival e do ideathon.
- [x] Arquitetura sem backend e decisões técnicas iniciais.
- [x] Jornadas, requisitos de qualidade e estratégia de testes planejados.
- [x] Matriz CSD em texto e PDF.
- [x] Fontes iniciais, riscos, dúvidas e limitações documentados.
- [x] Nome VivaSE Cultura e direção FASC 2026 aceitos provisoriamente.
- [x] Documentação inicial enviada ao GitHub (`6d2bb88`).

Critério cumprido: escopo registrado e dúvidas explícitas. A hipótese de utilidade para turistas ainda precisa de validação com pessoas; planejamento não comprova resultado de campo.

## Fase 2 — Fundação técnica, visual e conteúdo

**Situação: concluída tecnicamente, com revisão do protótipo pelo responsável. O refinamento visual continua nas próximas fases.**

- [x] Ambiente React/TypeScript/Vite e scripts funcionando.
- [x] Dependências corrigidas e build de produção aprovado.
- [x] Entrada com identidade visual do FASC 2026.
- [x] Base responsiva de navegação, mapa/lista, agenda e detalhes.
- [x] Inventário dos 20 espaços/frentes encontrados na v4.
- [x] 144 registros dos três dias reconciliados com as 21 páginas de conteúdo.
- [x] Fontes por página e revisão editorial registradas.
- [x] Referências cartográficas para todos os registros, com precisão declarada.
- [x] Compartilhamento de equipamentos e cortejos tratados sem inventar posições/percurso.
- [x] Endereços fornecidos pelo responsável incorporados.
- [x] Busca, filtros de agenda, intervalos e datas de madrugada.
- [x] Sete testes de domínio, typecheck e build aprovados.
- [x] Fluxos de navegador e inspeção em 1440, 768 e 390 px.
- [x] Lista mestra, limitações e relatório técnico atualizados.
- [x] Apresentar o protótipo ao responsável e aplicar as correções de identidade, ícones, logo e interação solicitadas.
- [x] Substituir Leaflet por MapLibre/react-map-gl e MapTiler, preservando atribuição e lista alternativa.
- [x] Extrair a logo oficial vetorial transparente e aplicá-la ao cabeçalho.
- [x] Retirar a imagem solta e os links de PDF das telas; fonte fora do build público.
- [x] Corrigir zoom dos marcadores e preservar âncoras geográficas em todos os níveis.
- [x] Habilitar roda, inclinação/rotação por arraste e botão de perspectiva; verificar no navegador.
- [x] Avaliar recomendações enviadas por mensagens e registrar escolhas de tecnologias e melhorias. O arquivo `.txt` em si não foi recebido; isso não bloqueia a entrega.

Critério técnico cumprido: base executável, dados coerentes e direção discutida. Precisão de rua/praça continua declarada; não equivale a coordenadas de portas nem a vistoria de acessibilidade.

## Fase 3 — Conclusão e validação dos fluxos de orientação

**Situação: concluída para orientação do protótipo. Testes, revisão e retorno do responsável em celular físico registrados.**

- [x] Entrada abre mapa, e navegação permite voltar.
- [x] Lista e mapa permitem selecionar espaços; cada registro tem marcador individual, inclusive em referências compartilhadas.
- [x] Busca por espaço/atração, categorias e limpeza de filtros.
- [x] Detalhe mostra endereço, agenda, fonte e referência geográfica.
- [x] Programação por dia e lugar, com busca por participantes.
- [x] Localização por ação, recusa tratada e retorno à área do festival.
- [x] Trajeto externo e ação de copiar endereço implementados.
- [x] Lista permanece disponível em falha do mapa.
- [x] Verificar RF-01 a RF-07, RF-12 e RF-13 com automação, inspeção e relato do responsável; registrar métodos e limites no documento 15.
- [x] Cobrir indisponibilidade/timeout do GPS, API ausente, exceção síncrona, resposta tardia e falha da cópia de endereço.
- [x] Conferir filtros, dia, URL, reload, histórico e acesso direto; retornar à agenda original quando o detalhe vier dela.
- [x] Revisar teclado, foco, nomes acessíveis e reflow equivalente a 200% (640 CSS px para uma tela-base de 1280 px); zoom nativo permanece na qualidade final.
- [x] Teste do responsável em celular físico: percurso proposto funcionou, sem cortes ou travamentos; aparelho/navegador não informados.
- [x] Aplicar os ajustes de interação e composição solicitados na avaliação até esta revisão.
- [x] Verificar roda do mouse, arraste com botão do meio/direito e alternância de perspectiva.
- [x] Corrigir falhas encontradas na validação desta fase; refinamentos finais e verificações ampliadas seguem na fase 5.

Critério de saída: percurso completo “encontrar atividade → escolher espaço → entender referência → abrir trajeto” repetível, inclusive sem GPS ou fundo do mapa.

## Fase 4 — Descoberta cultural e preservação da memória

**Situação: concluída no escopo funcional do protótipo em 19/11/2026, com evidências e limites no [relatório 33](33-FECHAMENTO-FASE-4.md). O responsável confirmou o teste dos novos fluxos em aparelho físico, sem problemas, em 19/11/2026.**

- [x] Selecionar lugares e conteúdo cultural com fontes por afirmação.
- [x] Criar roteiros temáticos com ordem e paradas explícitas.
- [x] Integrar parada ao detalhe/mapa e ao trajeto externo.
- [x] Evitar prometer duração, distância ou acessibilidade de percurso não verificado.
- [x] Criar exploração de memórias, distinguindo exemplos fictícios e referências públicas.
- [x] Pesquisar e atribuir relatos publicados que possam entrar na interface.
- [x] Permitir escrever lembrança salva somente no navegador/aparelho.
- [x] Permitir excluir lembrança e verificar persistência ao recarregar.
- [x] Tratar falha, indisponibilidade e limite de armazenamento sem alegar salvamento.
- [x] Informar que apagar dados do navegador pode remover lembranças.
- [x] Criar linha do tempo com marcos históricos documentados e fontes acessíveis.
- [x] Conferir datas e descontinuidades; não inventar edições, públicos ou artistas.
- [x] Revisar fontes, créditos, licenças declaradas e limites de reutilização; casos sem autorização específica registrada estão inventariados para a revisão final de publicação (relatório 33).
- [x] Verificar integração das funções nas larguras móveis e testar as jornadas culturais com automação; teste em aparelho físico confirmado sem problemas pelo responsável em 19/11/2026.

- [x] Fotografias reais no resumo do pin e no detalhe, com crédito, contexto e falha tratada. Cobertura atual: 20/20 registros, sem apresentar fotos antigas como montagem de 2026.
- [x] Referências de fachada de Tsuru e Reurb confirmadas pelo responsável; links de consulta disponíveis.
- [x] Completar os nove registros pendentes com fotografias reais, créditos e legendas; referências de entorno/arquivo identificadas.
- [x] Testar jornadas culturais e reflow em 1440/768/390/320 px; axe sem violações detectadas nas três telas culturais em 390 px.
- [x] Aplicar as revisões solicitadas pelo responsável e consolidar o fechamento funcional; a confirmação dos novos fluxos em aparelho físico foi recebida em 19/11/2026, sem problemas.

Evidências, fontes, cobertura e pendências: [22 — Fase 4](22-FASE-4-CULTURA-E-FOTOS.md). A conferência de atribuição não equivale a uma licença irrestrita de uso.

Critério de saída: roteiros, memórias e linha do tempo utilizáveis, fontes rastreáveis e persistência local testada. RF-08 a RF-11 são parte do MVP e continuam obrigatórios.

### Expansão histórica solicitada — 17/11/2026

- [x] Inspecionar e reutilizar MapLibre, rotas por hash, tokens e componentes existentes.
- [x] Modelar edições, fontes, espaços, artistas e participações com relações tipadas.
- [x] Cadastrar 18 edições do acervo recebido, sem preencher interrupções por inferência.
- [x] Separar mapa de 2026 do modo histórico e preservar a consulta do modo atual.
- [x] Atualizar pins e nomes por edição; manter registros sem coordenadas somente na lista.
- [x] Máquina do tempo sempre visível acima do mapa atual e do histórico, com pontos por edição, anterior/próxima e Play/Pause/reinício.
- [x] Limpar timers, pausar fora da tela e preservar a câmera durante a sequência.
- [x] Preservar os 38 registros anteriores, integrar as 212 entradas recebidas e acrescentar um anúncio verificado no PDF oficial de 2025: 230 registros após o merge. Distinguir cobertura, anúncio, convite e menção sem edição.
- [x] Preservar 191 artistas/grupos no acervo e destacar uma curadoria de 80 nomes, com busca, categoria, edição, ordenação, paginação e trajetória cronológica.
- [x] Expandir a linha do tempo de oito para 15 marcos, com contexto e ligações ao mapa. Em 21/11 a tela passou a mostrar só 2005 a 2026 (14 marcos), a pedido do responsável; o acervo de 1972 foi preservado (registro 37).
- [x] Preservar edição, espaço e busca ao navegar entre Cultura, artista e mapa.
- [x] Testar teclado, trocas rápidas, ausência de registros, mobile, movimento reduzido, build e regressões.
- [x] Incorporar a avaliação dos novos fluxos e as correções solicitadas; teste físico final dos novos fluxos confirmado sem problemas pelo responsável em 19/11/2026.
- [x] Corrigir popup encoberto pelos pins e carregamento tardio após sair do mapa.
- [x] Ampliar o inventário histórico para 125 espaços por edição; usar coordenadas somente nas referências conferidas.
- [x] Consolidar a revisão editorial do recorte do protótipo e o fechamento solicitado pelo responsável, preservando o inventário das lacunas históricas (relatórios 30–33).

Relatório completo: [23 — Mapa histórico e acervo](23-MAPA-HISTORICO-E-ACERVO.md). A revisão atual está em [24 — Pesquisa integrada e máquina do tempo](24-PESQUISA-INTEGRADA-E-MAQUINA-DO-TEMPO.md). O recorte histórico tem cobertura parcial explícita; o seletor não representa todos os anos da trajetória.

## Fase 5 — Qualidade final e preparação do pitch

**Situação: em andamento desde 19/11. Revisão técnica e apoio inicial do pitch preparados; ensaio humano e curadoria continuam abertos. Evidências no [documento 34](34-FASE-5-QUALIDADE-E-PITCH.md).**

- [x] Primeiro conjunto automatizado de verificações e capturas criado.
- [x] Reconferir fonte oficial em 19/11: continua vinculando a v4, idêntica ao PDF arquivado; verificar novos comunicados no dia do pitch.
- [ ] Revisar o conjunto final de dados, créditos, limites e mensagens.
- [x] Medir produção local com perfil de rede/CPU documentado e verificar falha do mapa/lista/agenda independente (documento 34).
- [x] Revisar contraste, teclado, foco e reflow até largura equivalente a 200%; resultados axe e limite sobre fotografia registrados no documento 34.
- [x] Registrar o teste final dos novos fluxos culturais em celular físico: roteiro/parada, salvar/recarregar/excluir memória e programação histórica por data. Em 19/11/2026, o responsável confirmou o teste e relatou “sem problemas”; aparelho e navegador não informados.
- [ ] Verificar condições de reutilização ou substituir mídias sem autorização específica registrada, conforme inventário de proveniência da fase 4.
- [x] Repetir orientação, cultura, planejamento, datas/rolagem histórica e produção; escopo e limites no documento 34.
- [x] Atualizar seletores antigos e repetir testes afetados; nenhuma falha crítica de produto identificada nesta rodada.
- [x] Confirmar duração/equipamento/internet: três minutos, computador/projetor com internet.
- [ ] Confirmar dia/horário específico, critérios da banca e tempo de perguntas.
- [x] Definir roteiro de três minutos para orientação, cultura e memória (documento 35).
- [x] Preparar apoio local com seis capturas reais e navegação por setas, sem prometer mapa offline.
- [x] Preparar material de pitch com tempos e sequência de telas.
- [ ] Fazer ensaio humano cronometrado e conferir legibilidade no projetor.
- [x] Registrar limites e próximos passos desta rodada no documento 34.
- [ ] Fazer commit/push da versão final quando solicitado e conferir sincronização.
- [x] Hospedagem escolhida e protótipo já publicado no GitHub Pages.

### Ajustes de 20 e 21/11/2026

- [x] Plataforma cultural de São Cristóvão: nova Home em `#/`, FASC preservado em `#/fasc` e nas rotas originais, publicações e experiência Senhor dos Passos (registro 36).
- [x] Linha do tempo restrita a 2005–2026 na tela `#/historia`, sem apagar dados do acervo (registro 37).
- [x] Typecheck e 52 testes de domínio aprovados após os dois ajustes; testes de navegador afetados atualizados.
- [ ] Executar os testes Playwright atualizados (`phase-3`, `phase-4`, `phase-5`, `art-polish`, `visual-review`) num ambiente com Python e Playwright.
- [x] Enviar os ajustes ao repositório `bernas0610/VivaSE_Cultura-2.0` após a permissão de escrita e conferir a nova publicação no Pages (registros 21 e 37).
- [ ] Excluir o repositório temporário `andersonsanto09/VivaSE_Cultura-2.0` (registro 37).

Critério de saída: demo repetível, material de apoio, limitações conhecidas e versão de apresentação identificada.

## Pós-MVP — Fora das cinco fases da primeira apresentação

Não são requisitos para concluir o protótipo acordado. Só entram com nova decisão de escopo.

- [ ] Administração de programação, login e controle de acesso.
- [ ] Backend e sincronização de lembranças entre aparelhos.
- [ ] Publicação compartilhada de memórias e moderação.
- [ ] Comparação estatística de edições com dados comprovados.
- [ ] Roteiro pessoal com seleção/remoção de paradas (RF-14, melhoria P1).
- [ ] Operação pública: infraestrutura, provedor de mapas, monitoramento e manutenção.
- [ ] Expansão para outros eventos e funcionalidades além do escopo inicial.

## Dependências que não devem ser confundidas com fases concluídas

- O responsável revisou o protótipo e as correções pedidas foram aplicadas. Isso não equivale à validação do MVP completo ou à aprovação de funções ainda não implementadas.
- Recomendações recebidas por mensagens já foram avaliadas. Eventual `.txt` adicional será novo material de revisão.
- Banheiros, emergências, bloqueios e acessibilidade: dependem de fonte específica da edição; não serão inventados.
- Pesquisa histórica: bibliografia localizada não equivale a livros integralmente lidos.
- Pitch: três minutos, computador/projetor com internet confirmados; banca e horário específico ainda não informados.

Referências: [roadmap](09-ROADMAP.md), [requisitos](02-REQUISITOS.md), [fundação](11-FASE-2-FUNDACAO.md) e [inventário](12-INVENTARIO-E-PROGRAMACAO.md).

## Ajustes após avaliação do responsável — 16/11/2026

- Removida a lista agrupada do mapa; 20 marcadores individuais abrem diretamente seus espaços. Separação visual não altera as coordenadas de origem.
- Removidos links do PDF das telas. Fonte preservada em `docs/fontes/`, sem PDF no build público.
- Sete testes, typecheck, build e suíte de navegador aprovados após os ajustes; capturas desktop/mobile revistas.

Revisão após feedback: [14 — Mapa vetorial, ícones e identidade FASC](14-MAPA-VETORIAL-E-REVISAO-VISUAL.md).

## Snapshot solicitado para o GitHub

O responsável solicitou commit e push desta revisão. O snapshot reúne fundação, inventário/agenda, mapa vetorial, identidade e correções de interação. Configuração real do MapTiler fica em `.env.local`, ignorado pelo Git; apenas `.env.example` é versionado. A confirmação de envio e o identificador do commit são conferidos no Git e informados na entrega.

Próximo trabalho: construir roteiros, memórias locais e linha do tempo na fase 4. Nenhuma dessas funções culturais deve ser marcada como entregue antecipadamente.

Encerramento da orientação: [15 — Validação da fase 3](15-FASE-3-VALIDACAO.md). O relato em celular físico é do responsável; testes de GPS real por HTTPS e em campo continuam na revisão final.

Revisão da entrada/agenda: [16](16-REVISAO-MAPA-AGENDA-E-LANDING.md). A experiência agrupada foi substituída pela decisão mais recente em [17 — Pins individuais](17-PINS-INDIVIDUAIS-E-PROXIMOS-PASSOS.md). Cards filtram categorias; agenda inclui categoria e modo “agora” por intervalos publicados.

## Última revisão — mapa e publicação do snapshot

- [x] Sem cluster: um pin por espaço, sem ocultar os outros ao selecionar.
- [x] Pins menores; número somente no selecionado e na lista.
- [x] Afastamento apenas quando há colisão, limitado em pixels, com traço à âncora original.
- [x] Abertura no Centro Histórico; visão geral inclui a Bica.
- [x] Lista de vizinhos para sobreposição residual, sem zoom automático.
- [x] Preservar chips/legenda, precisão aproximada, cards que filtram, cores dos dias, Radix e agenda “agora”.
- [x] Revalidar domínio, jornadas, foco/teclado, gestos, fallback e larguras de tela.
- [x] Preparar snapshot solicitado para commit/push, com configuração real fora do Git.

Fases 1, 2 e 3 concluídas no escopo do protótipo; fase 4 é o próximo trabalho. Confirmação do push e hash do snapshot são informados após a checagem do remoto. Próximos passos detalhados no documento 17.

## Manutenção antes da fase 4 — 17/11

- [x] Analisar o vídeo e confirmar o bug com o responsável.
- [x] Eliminar redistribuição de pins durante o zoom; manter afastamento estável e pins individuais.
- [x] Preservar câmera ao redimensionar e manter enquadramento ao revelar mapa oculto.
- [x] Refinar contornos, detalhe, controles, aviso de precisão e legenda móvel.
- [x] Nove testes de domínio, teste de estabilidade por quadros, regressões e build.
- [ ] Avaliar a nova versão com o responsável; este ajuste não inicia a fase 4.

Detalhes: [18 — Correção do zoom e acabamento](18-CORRECAO-ZOOM-E-ACABAMENTO.md).

## Revisão integrada e publicação solicitada — 17/11/2026

- [x] Aplicar os seis pontos de revisão: máquina do tempo aberta, curadoria, popup, fotografias, espaços por edição e trajetórias de artistas.
- [x] Preservar os registros existentes, deduplicar e testar o merge das pesquisas.
- [x] 27 testes de domínio, build e jornadas históricas/culturais aprovados; estabilidade em 1.131 quadros com desvio máximo de 1,142 px.
- [x] Preparar a revisão para commit, push e publicação autorizados pelo responsável.
- [ ] Aceite das novas telas e conferência final em aparelho físico.

Registro detalhado: [24 — Pesquisa integrada](24-PESQUISA-INTEGRADA-E-MAQUINA-DO-TEMPO.md).

### Memória dos palcos — Quem já passou por aqui

- [x] Seção nos detalhes dos palcos musicais atuais, destacando a curadoria de grandes nomes com apresentação documentada naquele palco.
- [x] Anos por artista, acesso à trajetória completa e retorno ao palco original.
- [x] Distinguir identidade do palco de uma referência geográfica compartilhada; anúncios não aparecem como shows executados.
- [x] Estado explícito quando o recorte ainda não contém um grande nome documentado para o palco.
- [x] 28 testes de domínio, build e verificação no navegador de navegação e reflow 390/320 px.

### Revisão estética completa — Home, acervo, lugares, agenda e mapa

- [x] Home com fotografia da cidade, memória atribuída e destaque do acervo.
- [x] Nove fotografias identificadas de artistas, créditos, cartazes tipográficos e seleção editorial.
- [x] Fotografias maiores e hierarquia própria nos detalhes dos locais.
- [x] Agenda compacta com horários fortes e destaques editoriais estáveis ao filtrar.
- [x] Miniaturas nos 20 espaços e ano selecionado mais visível na máquina do tempo.
- [x] Verificar navegação, filtros, fotos, contraste, reflow e build.
- [ ] Aceite visual e teste final em aparelho físico.

Detalhes: [25 — Refinamento visual](25-REFINAMENTO-VISUAL-E-ACERVO-FOTOGRAFICO.md).

### Footer da Home

- [x] Chamada final, CTA, marca, navegação e referência à cidade na identidade FASC.
- [x] Fontes, créditos e identificação de projeto independente.
- [x] Desktop/mobile, contraste, teclado e build conferidos.


## Expansão de Programação e Cultura — 17/11/2026

- [x] Minha programação local, persistência e resumo por dia com conflitos sustentados por horários informados.
- [x] Visões por horário e palco/espaço; filtros de período, Agora e A seguir.
- [x] Detalhe e compartilhamento individual da atividade; navegação entre anúncio de 2026, espaço e artista histórico.
- [x] Entrada própria para Cultura com três caminhos e acesso aos artistas.
- [x] Mapa das paradas e progresso manual persistido por roteiro.
- [x] Editar/cancelar, filtrar e exportar lembranças sem alterar identidade/criação dos registros existentes.
- [x] Aviso de retorno ao festival temporário, fechamento manual e limpeza do temporizador.
- [x] Testes de domínio e jornadas de navegador; regressões e reflow móveis.
- [ ] Aceite do responsável e nova conferência em aparelho físico desses fluxos.

Detalhes, testes e limites: [26 — Programação pessoal e Cultura](26-PROGRAMACAO-PESSOAL-E-CULTURA.md). A fase 4 permanece em revisão; esta expansão não encerra automaticamente a fase 5.


## Revisão da aba Sobre — 18/11/2026

- [x] Abertura editorial com fotografia identificada e propósito do projeto.
- [x] História da proposta e três pilares com navegação funcional.
- [x] Autoria coletiva como Equipe VivaSE, conforme decisão do responsável.
- [x] Fontes, créditos, fotografias, precisão e dados locais organizados em acordeões.
- [x] Perguntas frequentes e caminho público para sugerir correções pelo GitHub.
- [x] Encerramento com mapa/Cultura, preservação do dia e atalhos acessíveis.
- [x] Verificar foto/fallback, teclado, foco, reflow móvel, contraste e build.
- [ ] Aceite visual e conferência da nova página em aparelho físico.

Evidências e limites: [27 — Sobre editorial e transparência](27-SOBRE-EDITORIAL-E-TRANSPARENCIA.md).


## Auditoria dos retratos — 18/11/2026

- [x] Corrigir a associação de Gaby Amarantos e reassociar o arquivo anterior a Edcity.
- [x] Revisar os demais retratos; corrigir Marina Lima e BaianaSystem.
- [x] Registrar imagem original e evidência de legenda/contexto por retrato.
- [x] Inventariar ausências: 72 destaques sem foto cadastrada; 181 no catálogo completo.
- [x] Distinguir ausência de foto e falha de carregamento; recuperar ao mudar de artista.
- [x] Verificar arquivos, carregamento, navegação, acessibilidade e build.
- [x] Ampliar a seleção com fotografias para todos os 80 destaques, com atribuição conferida (ver expansão abaixo).

Detalhes e inventário: [28 — Auditoria dos retratos](28-AUDITORIA-DOS-RETRATOS.md).


## Revisão das participações históricas — 18/11/2026

- [x] Conferir João Gomes e Pabllo Vittar nas coberturas posteriores aos shows.
- [x] Incorporar confirmação de realização a 47 registros, preservando IDs e pesquisa recebida.
- [x] Distinguir a substituição documentada de Itamar Vieira Jr. em 2024.
- [x] Priorizar fontes de cobertura e atualizar o contexto das edições revisadas.
- [x] Apresentar fonte de programação como natureza do registro, sem sugerir que não houve show.
- [x] Preservar horários anunciados, precisão dos lugares e separação da edição futura de 2026.
- [x] Verificar domínio, lista/trajetória, fontes, teclado/acessibilidade, reflow e build.
- [ ] Ampliar a pesquisa de cobertura dos 98 registros que ainda usam fontes de programação.

Inventário e critérios: [29 — Revisão das participações](29-REVISAO-DAS-PARTICIPACOES.md).

## Expansão das fotografias — 18/11/2026

- [x] Fotografias para os 80 nomes em destaque; 130 dos 191 nomes no catálogo completo.
- [x] Priorizar registros do FASC; identificar fotos externas, divulgação e entrevista.
- [x] Conferir legendas e contexto, rejeitando homônimos e associações automáticas equivocadas.
- [x] Exibir crédito, fonte e licença das imagens do Commons.
- [x] Identificar os dois participantes nas fotografias conjuntas.
- [x] Preservar registros históricos e as dez imagens corrigidas na auditoria anterior.
- [x] Inventariar as 61 pendências sem substituir fotografias por imagens de outra pessoa.
- [x] Verificar carregamento, recuperação após falha, acessibilidade, domínio e build.
- [ ] Encontrar fotografias identificadas dos 61 nomes restantes; conferir os direitos e créditos antes de incorporar.

Detalhes: [30 — Expansão das fotos dos artistas](30-EXPANSAO-DAS-FOTOS-DOS-ARTISTAS.md).

## Programação no mapa histórico — 18/11/2026

- [x] Resumo ao clicar no pin, com ações diretas para programação e detalhes.
- [x] Agenda do espaço primeiro, com datas, horários destacados e filtro por data.
- [x] Separar informações do local e contexto geral da edição, eliminando repetições.
- [x] Preservar fontes, status históricos, datas civis, dias de programação e lacunas.
- [x] Abrir a programação diretamente ao tocar no pin no celular.
- [x] Verificar links diretos, troca de edição, estados vazios, teclado e acessibilidade.
- [x] Testar as 18 edições, reflow em quatro larguras e build de produção.

Detalhes: [31 — Programação no mapa histórico](31-PROGRAMACAO-NO-MAPA-HISTORICO.md).

## Datas e rolagem do mapa histórico — 18/11/2026

- [x] Conferir e preencher 156 datas com fontes e evidência por participação.
- [x] Eliminar datas ausentes nas participações cadastradas de 2005 e 2017–2025.
- [x] Preservar dias de programação, datas civis, horários anunciados e status históricos.
- [x] Registrar divergências de horário e programação, sem inventar valores.
- [x] Corrigir a área branca ao rolar o painel até o fim.
- [x] Corrigir o conflito de altura em tablet e preservar a rolagem no celular.
- [x] Testar datas, rolagem, acessibilidade, fluxo histórico e build.
- [ ] Recuperar o dia individual das 42 participações antigas ainda sem comprovação suficiente.

Detalhes e inventário: [32 — Datas históricas e rolagem](32-DATAS-HISTORICAS-E-ROLAGEM.md).

## Encerramento funcional da fase 4 — 19/11/2026

- [x] Reexecutar os 42 testes do domínio e as jornadas culturais/de planejamento.
- [x] Consolidar escopo entregue, evidências, inventário de proveniência e limites do acervo.
- [x] Preparar passagem para qualidade final e pitch, sem ampliar funcionalidades.
- [x] Registrar as pendências de teste físico e revisão final de publicação na fase 5, sem declará-las realizadas.

Referência atual: [33 — Fechamento da fase 4](33-FECHAMENTO-FASE-4.md).

## Confirmação do teste físico cultural — 19/11/2026

- [x] Receber confirmação do responsável de que realizou o roteiro de teste solicitado.
- [x] Registrar o resultado informado: “sem problemas”.
- [x] Concluir essa pendência de validação da fase 4, mantendo as demais verificações finais da fase 5.
