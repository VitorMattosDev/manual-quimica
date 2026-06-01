# ROADMAP.md — Fila executável do Manual de Química

Este arquivo é **a fila de trabalho**: o quê escrever e em que ordem. Cada item
tem o **caminho exato do arquivo**, o **escopo** em uma linha e o **status**.

## Protocolo de execução

- A **próxima tarefa** é sempre o **primeiro item não marcado** (`[ ]` ou `[~]`)
  na ordem deste arquivo.
- Ao concluir um capítulo: marque `[x]`, registre o `.qmd` em `chapters:` do
  `_quarto.yml` (e abra o bloco `part:` do volume, se for o primeiro do volume),
  atualize `constantes.qmd` se introduziu constantes/fórmulas, e faça **um commit**.
- **Fatia vertical:** feche um volume inteiro antes de abrir o próximo.
- Legenda: `[x]` pronto · `[~]` esboço a completar · `[ ]` a fazer.

Estado atual: **1 pronto · 2 esboços · 96 pendentes.**

---

## FASE 1 — Química Geral

### Volume I — Fundamentos da Química
*Objetivo:* a linguagem e as ferramentas básicas. *Pré-requisito:* nenhum.

- [x] `volumes/v1-fundamentos/01-materia.qmd` — Matéria, propriedades e estados.
- [x] `volumes/v1-fundamentos/02-medidas.qmd` — Medidas, unidades (SI) e algarismos significativos.
- [x] `volumes/v1-fundamentos/03-metodo.qmd` — Método científico e modelagem em química.
- [x] `volumes/v1-fundamentos/04-misturas.qmd` — Substâncias puras, misturas e separação de misturas.
- [x] `volumes/v1-fundamentos/05-transformacoes.qmd` — Fenômenos físicos e químicos.
- [x] `volumes/v1-fundamentos/06-modelos-atomicos.qmd` — Modelos atômicos: de Dalton a Bohr.
- [x] `volumes/v1-fundamentos/07-linguagem.qmd` — Símbolos, fórmulas e equações químicas.

### Volume II — Estrutura Atômica e Periodicidade
*Objetivo:* o átomo quântico e a periodicidade. *Pré-requisito:* Vol. I.

- [x] `volumes/v2-atomistica/01-modelo-quantico.qmd` — Modelo quântico; dualidade; orbitais.
- [x] `volumes/v2-atomistica/02-numeros-quanticos.qmd` — Números quânticos e exclusão de Pauli.
- [x] `volumes/v2-atomistica/03-config-eletronica.qmd` — Configuração eletrônica (Aufbau, Hund).
- [x] `volumes/v2-atomistica/04-tabela-periodica.qmd` — Organização e história da tabela periódica.
- [x] `volumes/v2-atomistica/05-propriedades-periodicas.qmd` — Raio, ionização, afinidade, eletronegatividade.
- [x] `volumes/v2-atomistica/06-grupos.qmd` — Periodicidade e reatividade dos grupos.

### Volume III — Ligações Químicas e Estrutura Molecular
*Objetivo:* como átomos se unem e que forma adquirem. *Pré-requisito:* Vol. II.

- [x] `volumes/v3-ligacoes/01-ionica.qmd` — Ligação iônica e energia reticular.
- [x] `volumes/v3-ligacoes/02-covalente.qmd` — Ligação covalente e estruturas de Lewis.
- [x] `volumes/v3-ligacoes/03-ressonancia.qmd` — Ressonância e carga formal.
- [x] `volumes/v3-ligacoes/04-vsepr.qmd` — Geometria molecular (VSEPR).
- [x] `volumes/v3-ligacoes/05-polaridade.qmd` — Polaridade molecular.
- [x] `volumes/v3-ligacoes/06-hibridizacao.qmd` — Ligação de valência e hibridização.
- [x] `volumes/v3-ligacoes/07-intermoleculares.qmd` — Forças intermoleculares e propriedades.

### Volume IV — Estequiometria e Reações
*Objetivo:* contabilidade da matéria nas reações. *Pré-requisito:* Vols. I, III.

- [x] `volumes/v4-estequiometria/01-mol-massa.qmd` — Massa atômica/molecular e o conceito de mol.
- [x] `volumes/v4-estequiometria/02-formulas.qmd` — Fórmula mínima e molecular; composição percentual.
- [x] `volumes/v4-estequiometria/03-balanceamento.qmd` — Equações químicas e balanceamento.
- [x] `volumes/v4-estequiometria/04-estequiometria.qmd` — Cálculos, reagente limitante e rendimento. **(GABARITO)**
- [x] `volumes/v4-estequiometria/05-tipos-reacoes.qmd` — Tipos de reações químicas.
- [x] `volumes/v4-estequiometria/06-solucao-aquosa.qmd` — Reações em solução aquosa e equações iônicas.
- [x] `volumes/v4-estequiometria/07-nox.qmd` — Números de oxidação e introdução à oxirredução.

### Volume V — Estados da Matéria e Soluções
*Objetivo:* fases e misturas homogêneas. *Pré-requisito:* Vol. IV.

- [x] `volumes/v5-estados-solucoes/01-gases-ideais.qmd` — Leis dos gases e equação do gás ideal.
- [x] `volumes/v5-estados-solucoes/02-cinetica-gases.qmd` — Teoria cinética e gases reais.
- [x] `volumes/v5-estados-solucoes/03-liquidos-solidos.qmd` — Líquidos, sólidos e diagramas de fase.
- [x] `volumes/v5-estados-solucoes/04-solucoes.qmd` — Solubilidade e unidades de concentração.
- [x] `volumes/v5-estados-solucoes/05-diluicao.qmd` — Preparo e diluição de soluções.
- [x] `volumes/v5-estados-solucoes/06-coligativas.qmd` — Propriedades coligativas.
- [x] `volumes/v5-estados-solucoes/07-coloides.qmd` — Coloides e dispersões.

---

## FASE 2 — Físico-Química

### Volume VI — Termodinâmica Química
*Objetivo:* energia e espontaneidade das reações. *Pré-requisito:* Vol. V.

- [x] `volumes/v6-termodinamica/01-energia-1lei.qmd` — Energia, calor, trabalho e 1ª lei.
- [x] `volumes/v6-termodinamica/02-entalpia.qmd` — Entalpia e termoquímica.
- [x] `volumes/v6-termodinamica/03-hess.qmd` — Lei de Hess e entalpias de formação.
- [x] `volumes/v6-termodinamica/04-entropia.qmd` — Entropia e a 2ª lei.
- [x] `volumes/v6-termodinamica/05-gibbs.qmd` — Energia livre de Gibbs e espontaneidade.
- [x] `volumes/v6-termodinamica/06-gibbs-equilibrio.qmd` — Relação entre ΔG e a constante de equilíbrio.

### Volume VII — Cinética Química
*Objetivo:* velocidade e mecanismo das reações. *Pré-requisito:* Vol. VI.

- [x] `volumes/v7-cinetica/01-velocidade.qmd` — Velocidade de reação e fatores.
- [x] `volumes/v7-cinetica/02-leis-velocidade.qmd` — Leis de velocidade e ordem de reação.
- [x] `volumes/v7-cinetica/03-integradas.qmd` — Equações integradas e tempo de meia-vida.
- [x] `volumes/v7-cinetica/04-arrhenius.qmd` — Teoria das colisões, estado de transição e Arrhenius.
- [x] `volumes/v7-cinetica/05-mecanismos.qmd` — Mecanismos de reação e catálise.

### Volume VIII — Equilíbrio Químico
*Objetivo:* o estado de equilíbrio e suas aplicações iônicas. *Pré-requisito:* Vols. VI–VII.

- [x] `volumes/v8-equilibrio/01-equilibrio-k.qmd` — Equilíbrio químico e a constante K.
- [x] `volumes/v8-equilibrio/02-le-chatelier.qmd` — Quociente reacional e Le Chatelier.
- [x] `volumes/v8-equilibrio/03-acidos-bases.qmd` — Teorias ácido-base.
- [x] `volumes/v8-equilibrio/04-ph.qmd` — Autoionização da água, pH e pOH.
- [x] `volumes/v8-equilibrio/05-fracos.qmd` — Equilíbrio de ácidos e bases fracos (Ka, Kb).
- [x] `volumes/v8-equilibrio/06-tampao.qmd` — Hidrólise salina e soluções-tampão.
- [x] `volumes/v8-equilibrio/07-titulacao.qmd` — Titulação ácido-base e indicadores.
- [x] `volumes/v8-equilibrio/08-kps.qmd` — Equilíbrio de solubilidade (Kps).

### Volume IX — Eletroquímica
*Objetivo:* reações redox e energia elétrica. *Pré-requisito:* Vol. VIII.

- [x] `volumes/v9-eletroquimica/01-balanceamento-redox.qmd` — Balanceamento de reações redox.
- [x] `volumes/v9-eletroquimica/02-pilhas.qmd` — Células galvânicas e potenciais-padrão.
- [x] `volumes/v9-eletroquimica/03-nernst.qmd` — Equação de Nernst.
- [x] `volumes/v9-eletroquimica/04-eletrolise.qmd` — Eletrólise e leis de Faraday.
- [x] `volumes/v9-eletroquimica/05-aplicacoes.qmd` — Corrosão, baterias e aplicações.

---

## FASE 3 — Química Orgânica

### Volume X — Fundamentos de Química Orgânica
*Objetivo:* o carbono, as funções e a estrutura espacial. *Pré-requisito:* Vol. III.

- [x] `volumes/v10-organica-fund/01-carbono-cadeias.qmd` — O carbono e as cadeias carbônicas.
- [x] `volumes/v10-organica-fund/02-hidrocarbonetos.qmd` — Hidrocarbonetos: classificação e nomenclatura.
- [x] `volumes/v10-organica-fund/03-funcoes-oxigenadas.qmd` — Funções oxigenadas.
- [x] `volumes/v10-organica-fund/04-funcoes-nitrogenadas.qmd` — Funções nitrogenadas e demais.
- [x] `volumes/v10-organica-fund/05-nomenclatura.qmd` — Nomenclatura IUPAC sistemática.
- [x] `volumes/v10-organica-fund/06-isomeria-plana.qmd` — Isomeria constitucional (plana).
- [x] `volumes/v10-organica-fund/07-estereoquimica.qmd` — Estereoquímica: isomeria geométrica e óptica.

### Volume XI — Reações Orgânicas
*Objetivo:* mecanismos e transformações. *Pré-requisito:* Vol. X.

- [x] `volumes/v11-reacoes-org/01-efeitos-intermediarios.qmd` — Efeitos eletrônicos e intermediários.
- [x] `volumes/v11-reacoes-org/02-substituicao.qmd` — Reações de substituição (SN1/SN2, radicalar).
- [x] `volumes/v11-reacoes-org/03-adicao.qmd` — Reações de adição (alcenos, alcinos).
- [x] `volumes/v11-reacoes-org/04-eliminacao.qmd` — Reações de eliminação (E1/E2).
- [x] `volumes/v11-reacoes-org/05-oxi-red-funcoes.qmd` — Oxidação, redução e reações de funções.
- [x] `volumes/v11-reacoes-org/06-acidez-basicidade.qmd` — Acidez e basicidade em orgânica.

### Volume XII — Compostos Aromáticos e Biomoléculas
*Objetivo:* aromaticidade, polímeros e bioquímica. *Pré-requisito:* Vol. XI.

- [x] `volumes/v12-aromaticos-bio/01-aromaticidade.qmd` — Aromaticidade e benzeno.
- [x] `volumes/v12-aromaticos-bio/02-sea.qmd` — Substituição eletrofílica aromática.
- [x] `volumes/v12-aromaticos-bio/03-polimeros.qmd` — Polímeros: adição e condensação.
- [x] `volumes/v12-aromaticos-bio/04-carboidratos-lipidios.qmd` — Carboidratos e lipídios.
- [ ] `volumes/v12-aromaticos-bio/05-proteinas.qmd` — Aminoácidos, peptídeos e proteínas.
- [ ] `volumes/v12-aromaticos-bio/06-acidos-nucleicos.qmd` — Ácidos nucleicos e introdução à bioquímica.

---

## FASE 4 — Inorgânica e Analítica

### Volume XIII — Química Inorgânica Descritiva e de Coordenação
*Objetivo:* os elementos e os complexos. *Pré-requisito:* Vol. II.

- [ ] `volumes/v13-inorganica/01-representativos.qmd` — Hidrogênio e elementos representativos (s, p).
- [ ] `volumes/v13-inorganica/02-descritiva.qmd` — Halogênios, calcogênios, nitrogênio, carbono.
- [ ] `volumes/v13-inorganica/03-transicao.qmd` — Metais de transição: propriedades gerais.
- [ ] `volumes/v13-inorganica/04-coordenacao.qmd` — Compostos de coordenação: nomenclatura e isomeria.
- [ ] `volumes/v13-inorganica/05-campo-ligante.qmd` — Teorias de ligação em complexos (TCC / campo ligante).
- [ ] `volumes/v13-inorganica/06-organometalicos.qmd` — Organometálicos e catálise (introdução).

### Volume XIV — Química Analítica
*Objetivo:* identificar e quantificar. *Pré-requisito:* Vol. VIII.

- [ ] `volumes/v14-analitica/01-qualitativa.qmd` — Análise qualitativa: identificação de íons.
- [ ] `volumes/v14-analitica/02-quantitativa-dados.qmd` — Fundamentos quantitativos e tratamento de dados.
- [ ] `volumes/v14-analitica/03-gravimetria.qmd` — Gravimetria.
- [ ] `volumes/v14-analitica/04-volumetria.qmd` — Volumetria (ácido-base, redox, complexação, precipitação).
- [ ] `volumes/v14-analitica/05-instrumental.qmd` — Introdução à análise instrumental.

---

## FASE 5 — Química Avançada / Fronteira

### Volume XV — Química Quântica e Espectroscopia
*Objetivo:* a base quântica da ligação e da análise espectral.
*Pré-requisito:* Vol. II + mecânica quântica (Manual de Física) + álgebra linear (Manual de Matemática).

- [ ] `volumes/v15-quantica/01-fundamentos-mq.qmd` — Fundamentos da mecânica quântica para a química.
- [ ] `volumes/v15-quantica/02-atomos.qmd` — Átomo de hidrogênio e átomos polieletrônicos.
- [ ] `volumes/v15-quantica/03-tom.qmd` — Teoria do orbital molecular (TOM).
- [ ] `volumes/v15-quantica/04-simetria.qmd` — Simetria molecular e teoria de grupos *(ver álgebra do Manual de Matemática)*.
- [ ] `volumes/v15-quantica/05-espectroscopia.qmd` — Princípios; espectroscopias UV-Vis e IR.
- [ ] `volumes/v15-quantica/06-rmn-massas.qmd` — RMN e espectrometria de massas.

### Volume XVI — Química Nuclear, Materiais e Estado Sólido
*Objetivo:* o núcleo e a matéria condensada. *Pré-requisito:* Vols. II, XV.

- [ ] `volumes/v16-nuclear-materiais/01-radioatividade.qmd` — Radioatividade e decaimento nuclear.
- [ ] `volumes/v16-nuclear-materiais/02-reacoes-nucleares.qmd` — Fissão, fusão e aplicações.
- [ ] `volumes/v16-nuclear-materiais/03-estado-solido.qmd` — Química do estado sólido e estruturas cristalinas.
- [ ] `volumes/v16-nuclear-materiais/04-materiais.qmd` — Materiais: semicondutores, cerâmicas, polímeros avançados.
- [ ] `volumes/v16-nuclear-materiais/05-nanoquimica.qmd` — Nanoquímica e tópicos de fronteira.
