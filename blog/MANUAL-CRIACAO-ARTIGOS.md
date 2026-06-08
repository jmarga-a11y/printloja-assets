# Manual de Criação de Artigos — Blog PrintLoja

> Documento vivo. A cada rodada o cliente refina as regras. Sempre ler antes de gerar um artigo.
> Última atualização: 2026-06-08

## 1. Objetivo
Criar autoridade de domínio para **printloja.com.br** no Google, ranquear para palavras‑chave específicas e ultrapassar concorrentes. Conteúdo otimizado para **SEO clássico** e para a **busca por IA do Google (AI Overviews / SGE)**. O Google **não pode perceber** que é conteúdo automatizado.

## 2. Fonte das pautas
Google Sheet (id `1sr1wESx9_H6WOJUDtHeuCf6Wz9KBfqs_m6SqgJZhgfc`). Colunas: Página destino/autoridade | Título | Palavras‑Chave | Página de Concorrente.

### Tipos de linha
- **Tipo A** — pauta completa (título + keywords). Posso sugerir keywords secundárias coerentes (baseadas em dados, nunca inventadas).
- **Tipo B** — só keyword + URL de destino do nosso site (sem título). **Eu crio o título/pauta** para ranquear naquela keyword.
- **Tipo C** — URL de concorrente. Entrar na página, extrair temas e as keywords que ele usa, e **reescrever melhor/mais completo**. **NUNCA** copiar texto, dados ou links do concorrente. Todos os links são printloja.com.br.

## 3. Regra de ouro do fluxo
- **Sempre perguntar antes de gerar.** Nunca gerar a fila inteira de uma vez.
- Basear-se em **dados reais** (pesquisa). Nada inventado.
- **Eu não publico.** Salvo o arquivo na pasta do Drive; outra ferramenta varre e publica.

## 4. Saída e hospedagem
- **Formato:** HTML pronto.
- **Pasta (Drive):** `Blog PrintLoja - Fila de Publicação` (folder id `1jX5qgAgwNHa7IJfOUly-oa3ZEqE1y1u2`). 1 arquivo por artigo.
- **Imagens:** repositório GitHub `jmarga-a11y/printloja-assets`, pasta `blog/printloja-blog-imagens/`. Servidas por jsDelivr: `https://cdn.jsdelivr.net/gh/jmarga-a11y/printloja-assets@main/blog/printloja-blog-imagens/ARQUIVO.jpg`.
- **Limitação:** o conector do Drive só cria/lê (não edita nem apaga). Para corrigir um HTML, recrio o arquivo e o cliente apaga o antigo.

## 5. Cadência de publicação
- **3x por semana** (seg/qua/sex ~09h), com **minuto aleatório** e variação de estrutura entre artigos, para não parecer automação. Data no campo `data_publicacao` dos metadados.

## 6. Estrutura obrigatória de cada artigo (SEO + AEO)
- `meta_title` + `meta_description` (≤ ~155 caracteres).
- **1 único H1**; hierarquia H2/H3 correta.
- **Resposta direta no topo** (answer-first) + bloco de **FAQ**.
- **Dados estruturados JSON-LD**: `Article` + `FAQPage` (e `Product`/`BreadcrumbList` quando fizer sentido).
- **Links internos** para categorias/produtos do printloja.com.br (mínimo 2; ideal 4–6). Lembrar: **a loja vende SUPRIMENTOS, não impressoras** — linkar para tinta/toner/cartucho/papel.
- **Imagem de topo** (hero) em 1200px, arte original (Canva/Gemini), com `alt` descritivo. Crédito quando necessário — **nunca** de concorrente.
- `alt` em **todas** as imagens. Open Graph, canonical.
- Texto **leve e gostoso de ler**, porém informativo. Parágrafos curtos, listas e tabelas comparativas (formatos que a IA cita).

## 7. Diretrizes de imagem (atualizado 2026-06-08)
- **Imagens no meio do artigo** para deixar a leitura mais agradável — com moderação. **Não pode pesar a leitura**; se ficar pesado, pode reduzir/remover (não é 100% obrigatório).
- Ao citar um **modelo específico** (ex.: Epson L3250), usar **imagem do produto real**. Como não vendemos impressoras, **relacionar com o suprimento que vendemos** para aquele modelo (ex.: kit de tinta que serve na L3250) e linkar para a página de venda.
- Preferir **imagens reais e nossas** (CDN da loja `images.tcdn.com.br`, store 1041864) — são produtos que vendemos, sem risco de direitos e reforçam a marca.
- Imagens inline em tamanho moderado (~300px, com `loading="lazy"`), float esquerda/direita para o texto fluir.

## 8. "Leia Mais" do WordPress (atualizado 2026-06-08)
- Inserir a tag **`<!--more-->`** logo após o parágrafo de abertura. É o corte "Leia Mais" do WordPress: na listagem do blog, mostra a introdução e o botão para continuar lendo, incentivando a navegação por todo o conteúdo.

## 9. Checklist final (vai nos metadados do HTML)
`h1_unico` · `alt_em_todas_imagens` · `meta_description_chars` · `links_internos` · `faq_schema` · `article_schema` · `leia_mais` · `imagens_inline` · controle de canibalização (não competir com artigo nosso na mesma keyword).
