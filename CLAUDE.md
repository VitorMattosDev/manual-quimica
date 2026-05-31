# CLAUDE.md — Manual de Química

Livro aberto em **Quarto**, terceiro título da série *Manuais de Ciências* (irmão
dos manuais de Matemática e Física). Vai da matéria à química quântica. Publicado
no GitHub Pages.

## Comandos

```bash
quarto preview          # site local com hot-reload (só HTML) — uso diário
quarto render           # gera site + PDF em _book/ (PDF exige TeX)
quarto publish gh-pages # render + deploy manual (raramente necessário)
```

- Deploy normal é **automático**: todo `push` na `main` dispara o GitHub Action
  (`.github/workflows/publish.yml`), que renderiza e publica (PDF via TinyTeX na nuvem).
- **PDF exige TeX local** (`quarto install tinytex`). Sem TeX, render do PDF falha
  com `No TeX installation was detected`. Para trabalhar só no site numa máquina sem
  TeX, comente o bloco `pdf:` em `_quarto.yml`.
- **CI:** o grafo `mermaid` do `index.qmd` exige Chromium headless para virar imagem
  no PDF. O `publish.yml` já roda `quarto install chrome-headless-shell` antes do
  render — sem isso, o deploy trava em `index.qmd` no runner Ubuntu.

## Estrutura

```
_quarto.yml    configuração do livro (lang: pt no topo; mhchem em HTML e PDF; rótulos PT)
index.qmd      apresentação + grafo de pré-requisitos (mermaid)
constantes.qmd apêndice: constantes físico-químicas + formulário
PLANO.md       guia de estilo (COMO escrever)
ROADMAP.md     fila executável capítulo a capítulo (O QUÊ / em que ordem)
volumes/       capítulos, em volumes/vN-tema/NN-nome.qmd
```

Divisão de papéis: **ROADMAP.md = o quê/ordem · PLANO.md = como escrever ·
CLAUDE.md = as regras que amarram os dois.**

## O que construir (roadmap)

Ao receber "escreva o próximo capítulo": abra o `ROADMAP.md`, pegue o **primeiro
item não marcado** (`[ ]` ou `[~]`), siga o protocolo de execução do topo do
arquivo e, ao terminar, **marque `[x]` e comite**. Feche um volume inteiro antes
de abrir o próximo (fatia vertical).

## Convenções de escrita (sempre seguir)

- Capítulo-gabarito: `volumes/v4-estequiometria/04-estequiometria.qmd`. Espelhe-o.
- Estrutura padrão: Motivação → Definições/Leis → Exemplos resolvidos → Exercícios
  → Soluções (em `callout-tip collapse="true"`).
- Idioma **português**; tom didático antes de formal — motivar antes de definir.
- Ambientes que numeram/referenciam sozinhos:
  - `#thm-` teorema · `lem-` · `cor-` · `prp-` proposição
  - `#def-` definição · `#exm-` exemplo · `#exr-` exercício · `.proof` demonstração
  - Referência cruzada: `@def-nome` → "Definição 4.1". **Nunca** escreva o número à mão.
- **Química:** fórmulas e equações **sempre** com `mhchem` — `\ce{2 H2 + O2 -> 2 H2O}`,
  `\ce{[Cu(NH3)4]^2+}`, equilíbrio com `<=>`. Unidades: `\pu{...}` ou `\mathrm{}`+`\,`.
- **Estruturas moleculares:** padrão = imagem `.svg`/`.png` embutida (vale em HTML e
  PDF). `chemfig` só para PDF e nunca por padrão (quebra o `quarto preview`).
- Matemática: `$...$` em linha, `$$...$$` em destaque; equação importante com `{#eq-nome}`.

## Regras do projeto

- **Não** edite numerações, sumário do `_quarto.yml` ou rótulos manualmente sem
  necessidade — o Quarto gera tudo.
- Ao adicionar capítulo: criar o `.qmd` **E** registrá-lo em `chapters:` do
  `_quarto.yml`. Para abrir um volume novo, criar/descomentar o bloco `part:`.
- Atualize `constantes.qmd` ao introduzir constante ou fórmula nova.
- Antes de propor reestruturação grande, consulte `PLANO.md` e `ROADMAP.md`.
- Commits pequenos e descritivos, **um por capítulo/seção concluída**.

## Estado atual

Volume I em construção. Capítulo-gabarito (Vol. IV, estequiometria) pronto como
referência. Capítulos 1 (Matéria) e 2 (Medidas) do Vol. I são esboços a preencher.
Prioridade: fechar o Volume I inteiro antes de abrir o Volume II.
