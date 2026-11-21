# VivaSE Cultura 2.0

Nova versão do guia cultural e mapa do FASC, planejada para o ideathon de 19 a 21/11/2026. Repositório: [VivaSE_Cultura-2.0](https://github.com/bernas0610/VivaSE_Cultura-2.0). Site: [bernas0610.github.io/VivaSE_Cultura-2.0](https://bernas0610.github.io/VivaSE_Cultura-2.0/).

**Estado atual (21/11/2026):** fases 1 a 4 concluídas no escopo do protótipo. Fase 5 em andamento: qualidade final e pitch de três minutos. Orientação, roteiros, memórias locais, linha do tempo, mapa histórico e acervo de artistas estão implementados e testados. [Fechamento da fase 4](docs/33-FECHAMENTO-FASE-4.md) · [Fase 5](docs/34-FASE-5-QUALIDADE-E-PITCH.md) · [Checklist](docs/13-CHECKLIST-DO-PROJETO.md).

A máquina do tempo fica visível acima do mapa: 18 edições históricas e retorno a 2026. O acervo preserva 191 artistas/grupos e 230 participações, com uma seleção pública de 80 nomes, trajetórias cronológicas e 125 registros de espaços por edição. [Pesquisa integrada, critérios e lacunas](docs/24-PESQUISA-INTEGRADA-E-MAQUINA-DO-TEMPO.md).

**Plataforma cultural (20/11/2026):** a raiz do site (`#/`) agora abre a Home do VivaSE sobre São Cristóvão, com experiências, publicações e lugares. A Home original do FASC está em `#/fasc`, e todas as rotas do FASC (`#/mapa`, `#/programacao`…) continuam iguais. Nova experiência: Festa de Nosso Senhor dos Passos (`#/senhor-dos-passos`). [Arquitetura, rotas e fontes](docs/36-PLATAFORMA-CULTURAL.md).

**Linha do tempo (21/11/2026):** a tela Cultura → Linha do tempo (`#/historia`) mostra apenas o período de 2005 a 2026: 14 marcos e oito edições no seletor. O acervo completo, desde 1972, continua no mapa histórico e na página de artistas. [Registro da mudança](docs/37-LINHA-DO-TEMPO-2005-2026.md).

## Executar a nova versão

Usar Node.js 22.18 ou superior (ambiente validado: Node 26.10.0).

```sh
npm install
npm run dev
```

Antes de usar o mapa vetorial, copie `.env.example` para `.env.local` e configure sua chave pública MapTiler com origens permitidas. Reinicie o servidor após alterar esse arquivo.

Abrir o endereço local impresso pelo Vite. Verificações: `npm test` (52 testes de domínio), `npm run typecheck` e `npm run build`. O build verifica tipos e gera `dist/`. O mapa é carregado sob demanda. Os testes de navegador ficam em `tests/*.py` e exigem Python com Playwright.

Principais endereços: `#/` (Home da plataforma), `#/fasc` (Home do FASC), `#/mapa`, `#/programacao`, `#/cultura`, `#/historia`, `#/artistas`, `#/publicacoes` e `#/senhor-dos-passos`.

A fundação tem 20 registros de espaços/frentes com referências geográficas de precisão declarada e 144 registros de agenda reconciliados com as 21 páginas de conteúdo da v4. As funções culturais estão implementadas e testadas localmente; as fotos distinguem arquivo, equipamento e entorno, e a revisão do responsável continua pendente; o PDF v4 é mantido apenas na documentação interna do repositório. A abertura de “Como chegar” é externa.

[Checklist de todas as fases](docs/13-CHECKLIST-DO-PROJETO.md) · [Documentação da Fase 1](docs/README.md) · [Matriz CSD em PDF](output/pdf/VivaSE-Matriz-CSD.pdf) · [Fontes e curadoria](docs/FONTES-E-CURADORIA.md)

Escopo completo do MVP: FASC 2026, todos os espaços levantados pela pesquisa, mapa, localização, programação, detalhes, roteiros, memórias no próprio navegador e linha do tempo. Trajetos em aplicativo externo; administração adiada. O escopo completo não equivale ao incremento já implementado.

## Referência da versão anterior

O texto a seguir foi preservado do repositório original como referência histórica de proposta e instalação.

# 🗺️ Mapa Vivo do FASC

Mapa interativo e histórico do Festival de Artes de São Cristóvão (FASC), unindo tecnologia, memória coletiva e patrimônio cultural sergipano.

---

## 📋 Pré-requisitos

Antes de começar, você precisa ter instalado no computador:

### 1. Node.js
Baixe e instale:

https://nodejs.org/

Para verificar se instalou corretamente, abra o terminal e digite:

```bash
node -v
npm -v
```

Se aparecer um número de versão, está tudo certo.

---

## 🚀 Como baixar e rodar o projeto

### 1. Baixar o projeto

Clique no botão verde:

```text
Code → Download ZIP
```

ou clone pelo Git:

```bash
git clone URL_DO_REPOSITORIO
```

---

### 2. Abrir a pasta do projeto

Extraia o `.zip` (se baixou) e abra a pasta no VS Code.

---

### 3. Instalar as dependências

No terminal, dentro da pasta do projeto, rode:

```bash
npm install
```

Esse comando irá baixar automaticamente todas as bibliotecas necessárias e criar a pasta:

```text
node_modules/
```

---

### 4. Rodar o projeto

Se o projeto usa **Vite**, execute:

```bash
npm run dev
```

Se o projeto usa **Create React App**, execute:

```bash
npm start
```

---

### 5. Abrir no navegador

Após iniciar, aparecerá algo parecido com:

```text
Local: http://localhost:5173/
```

ou

```text
Local: http://localhost:3000/
```

Abra esse endereço no navegador.

---

## 📁 Estrutura do projeto

```text
src/            # Código principal
public/         # Arquivos públicos
package.json    # Dependências e scripts
README.md       # Instruções
```

---

## ⚠️ Importante

A pasta abaixo **não vem no GitHub**, e isso é normal:

```text
node_modules/
```

Ela é recriada automaticamente com:

```bash
npm install
```

---

## 🛠️ Tecnologias usadas

- React
- Leaflet
- OpenStreetMap
- JavaScript
- CSS

---

## 🎭 Sobre o projeto

O **Mapa Vivo do FASC** é uma plataforma digital que permite explorar o Festival de Artes de São Cristóvão através de:

- mapa interativo;
- memória histórica;
- depoimentos e lembranças;
- comparação entre edições;
- valorização do patrimônio cultural sergipano.

---

## ❤️ Sergipe vive aqui

Tecnologia a serviço da cultura e da memória.

Mapa e identidade da nova versão: [registro da migração MapLibre/MapTiler](docs/14-MAPA-VETORIAL-E-REVISAO-VISUAL.md).

Experiência atual do mapa: [pins individuais, precisão e próximos passos](docs/17-PINS-INDIVIDUAIS-E-PROXIMOS-PASSOS.md).

Direção visual atual: [Cartaz vivo + Atlas cultural e validação](docs/19-DIRECAO-VISUAL-IMPLEMENTADA.md).

Site: [VivaSE Cultura no GitHub Pages](https://bernas0610.github.io/VivaSE_Cultura-2.0/). [Configuração da publicação](docs/21-PUBLICACAO-GITHUB-PAGES.md).

Revisão visual de 17/11: Home editorial, nove fotografias identificadas de artistas, cartazes tipográficos, miniaturas dos locais e agenda com destaques editoriais. [Registro e verificação](docs/25-REFINAMENTO-VISUAL-E-ACERVO-FOTOGRAFICO.md).
