# PLANO.md — Guia de estilo do Manual de Química

Este arquivo define **como escrever**. O **que** escrever e **em que ordem** está
no `ROADMAP.md`. As regras que amarram os dois estão no `CLAUDE.md`.

> Fonte da verdade para convenções de estilo. Em caso de conflito sobre *como*
> redigir um capítulo, este arquivo manda.

## Capítulo-gabarito

`volumes/v4-estequiometria/04-estequiometria.qmd` é o **modelo**. Todo capítulo
novo espelha sua estrutura, ambientes e tom.

## Estrutura padrão de um capítulo

1. **Motivação** — por que o assunto importa, em prosa, antes de qualquer definição.
2. **Definições / leis / resultados** — em ambientes numerados (ver abaixo).
3. **Exemplos resolvidos** — sempre com números e unidades.
4. **Exercícios**.
5. **Soluções selecionadas** — em `callout-tip` colapsável.

Tom **didático antes de formal**: sempre motivar antes de definir.

## Ambientes (numeram e referenciam sozinhos)

Use o atributo `#tipo-nome`; um `## Título` interno é opcional.

- `::: {#thm-nome}` teorema · `lem-` lema · `cor-` corolário · `prp-` proposição
- `::: {#def-nome}` definição · `exm-` exemplo · `exr-` exercício
- `::: {.proof}` demonstração (termina com `$\square$`)
- Caixas: `.callout-note` (nota), `.callout-warning` (cuidado/erro comum),
  `.callout-tip collapse="true"` (soluções).
- Referência cruzada: `@def-nome` → "Definição 4.1" automático.
  **Nunca** escreva "Definição 4.1" na mão.

## Química: equações e fórmulas (a convenção mais importante)

- **Sempre** use `mhchem` para fórmulas e equações químicas: `\ce{2 H2 + O2 -> 2 H2O}`,
  `\ce{CO2}`, `\ce{H+}`, `\ce{[Cu(NH3)4]^2+}`. Funciona no site (MathJax, já
  configurado no `_quarto.yml`) **e** no PDF (pacote `mhchem`).
- Estados de agregação e setas: `\ce{CaCO3(s) ->[\Delta] CaO(s) + CO2(g)}`,
  equilíbrio com `<=>`.
- Grandezas físicas e unidades: `\pu{36 g}`, `\pu{8,314 J/mol/K}` (pacote `siunitx`
  no PDF; `\pu` do mhchem no site). Em texto corrido também vale `\mathrm{}` + `\,`.
- Matemática: `$...$` em linha, `$$...$$` em destaque; equações importantes recebem
  rótulo `{#eq-nome}`.

## Estruturas moleculares e diagramas

- **Padrão seguro (HTML + PDF):** imagem embutida (`.svg` ou `.png`) na pasta do
  capítulo, inserida com `![legenda](caminho){#fig-nome}`. Gere as estruturas
  externamente (ex.: RDKit, ferramenta de desenho) e versione o arquivo.
- **Opcional, só PDF:** `chemfig` para estruturas vetoriais nativas. **Não** ative
  por padrão — quebra o `quarto preview` (HTML) numa máquina recém-configurada.
  Se for usar, documente e isole no formato PDF.
- Diagramas de processo/aparato podem usar `mermaid` (já suportado no Quarto).

## Idioma e notação

- Português em todo o texto.
- Decimais com vírgula no texto corrido em prosa; em código LaTeX use o que
  renderizar corretamente (`6{,}022` para sair com vírgula).
- Ao introduzir uma constante ou fórmula nova, **atualize `constantes.qmd`**.

## O roadmap

A fila executável capítulo a capítulo está em `ROADMAP.md`. Este `PLANO.md`
**não** duplica o roadmap — só aponta para ele.
