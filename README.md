# Manual de Química

Livro aberto em [Quarto](https://quarto.org), terceiro título da série *Manuais de
Ciências*. Da matéria à química quântica — básico ao avançado.

## Setup em uma máquina nova

1. **Quarto** (obrigatório): instale de <https://quarto.org/docs/get-started/>.
2. **TeX** (só para gerar PDF): `quarto install tinytex`.
   - O conteúdo do livro vem do Git, mas **Quarto e TeX precisam ser instalados
     localmente** — eles não são versionados.
3. Troque `SEU-USUARIO` no `_quarto.yml` pelo seu usuário/organização do GitHub.

## Rodar o livro

```bash
quarto preview     # site local com hot-reload (só HTML) — uso diário
quarto render      # gera site + PDF em _book/ (PDF exige TeX)
```

### Rodar apenas o site, sem PDF

Numa máquina sem TeX, comente o bloco `pdf:` dentro de `format:` no `_quarto.yml`.
O `quarto preview` passa a rodar sem exigir nenhuma instalação de TeX.

## Equações químicas

As fórmulas usam `mhchem` (`\ce{...}`), já configurado para **HTML e PDF**:

- HTML: o `_quarto.yml` carrega a extensão mhchem no MathJax.
- PDF: o pacote `mhchem` é incluído no cabeçalho LaTeX.

## Publicação (GitHub Pages)

1. O deploy é **automático**: todo `push` na `main` dispara o Action em
   `.github/workflows/publish.yml`, que renderiza (com PDF, via TinyTeX na nuvem)
   e publica.
2. **Primeiro deploy:** inicialize a branch `gh-pages` rodando uma vez
   `quarto publish gh-pages` (isso renderiza o PDF e portanto pede TeX local), ou
   deixe o Action criá-la no primeiro push.
3. No GitHub: **Settings → Pages → Build and deployment → Source: Deploy from a
   branch**, branch **`gh-pages`**, pasta **`/ (root)`**.

## Trabalhando com o Claude Code

O `CLAUDE.md` na raiz é lido no início de toda sessão e carrega setup, convenções e
estado do projeto. Os três arquivos de controle:

- **`ROADMAP.md`** — o quê escrever e em que ordem (fila de 99 capítulos).
- **`PLANO.md`** — como escrever (guia de estilo).
- **`CLAUDE.md`** — as regras que amarram os dois.
