# Biblioteca de Doutrina Guilherme Nascimento — Plugin

Plugin de biblioteca doutrinária de **Guilherme Nascimento**.
Reúne **11 obras** (7 de Recuperação Judicial/Falência e 4 de Processo Civil), extraídas
na íntegra dos PDFs, com cabeçalhos/rodapés e numeração de página removidos, e **fatiadas em trechos
pesquisáveis** (`references/sec-NN.md`) com intervalo de páginas no cabeçalho.

Cada obra é uma **skill** independente. Quando uma tarefa de RJ ou Processo Civil exigir fundamentação
doutrinária, a skill correspondente é acionada, o assistente localiza o trecho pelo índice/mapa de temas
e **lê o texto** antes de redigir — evitando citações de memória.

## Como instalar

1. Descompacte este `.zip`.
2. No Cowork/Claude Code, adicione a pasta como marketplace e instale o plugin `biblioteca-doutrina-gn`
   (o arquivo `.claude-plugin/marketplace.json` já aponta para o próprio plugin), **ou** copie a pasta
   `biblioteca-doutrina-gn-plugin` para o diretório de plugins locais.
3. As 11 skills ficam disponíveis automaticamente.

## Como usar (fluxo de pesquisa)

1. Identifique a âncora jurídica ou tema (artigo de lei, instituto, palavra-chave).
2. Abra a skill da obra desejada e localize o trecho no **Mapa de temas** ou no **Índice de trechos**.
3. **Leia por inteiro** o `references/sec-NN.md` correspondente antes de escrever.
4. Cite usando o intervalo de páginas do cabeçalho do trecho e a referência completa da obra.
5. Se o tema não estiver mapeado, faça **busca textual (grep)** nos arquivos de `references/`.

## Obras — Recuperação Judicial e Falência

| Skill | Obra | Autor(es) | Trechos |
| --- | --- | --- | --- |
| `negrao-falencia-recuperacao` | Falência e Recuperação de Empresas | Ricardo Negrão | 19 |
| `resumo-viciodeumaestudante` | Falência e Recuperação Judicial (Resumo) | @viciodeumaestudante | 1 |
| `rj-falencia-metodos-solucao-conflitos` | Recuperação Judicial e Falência — Métodos de Solução de Conflitos | — | 19 |
| `sacramone-comentarios-lref` | Comentários à Lei de Recuperação de Empresas e Falência | Marcelo Barbosa Sacramone | 66 |
| `sacramone-manual-empresarial` | Manual de Direito Empresarial | Marcelo Barbosa Sacramone | 44 |
| `sacramone-nunes-societario-recuperacao` | Direito Societário e Recuperação de Empresas | Marcelo Barbosa Sacramone e Marcelo Guedes Nunes (coord.) | 27 |
| `sacramone-rj-falencia` | Recuperação Judicial e Falência | Marcelo Barbosa Sacramone | 36 |

## Obras — Processo Civil

| Skill | Obra | Autor(es) | Trechos |
| --- | --- | --- | --- |
| `araujo-junior-processo-civil-pratica` | Processo Civil na Prática | Gediel Claudino de Araújo Júnior | 38 |
| `donizetti-curso-processual-civil` | Curso de Direito Processual Civil | Elpídio Donizetti | 74 |
| `incentivos-processuais-economia-comportamental` | Processo Civil, Incentivos Processuais e Economia Comportamental | — | 8 |
| `nery-cpc-comentado` | Código de Processo Civil Comentado | Nelson Nery Jr. e Rosa Maria de Andrade Nery | 146 |

## Referências completas (para citação)

- **araujo-junior-processo-civil-pratica** — ARAÚJO JÚNIOR, Gediel Claudino de. Processo Civil na Prática. 22. ed. São Paulo: Atlas.
- **donizetti-curso-processual-civil** — DONIZETTI, Elpídio. Curso de Direito Processual Civil. 23. ed. São Paulo: Atlas, 2020.
- **incentivos-processuais-economia-comportamental** — Processo Civil, Incentivos Processuais e Economia Comportamental.
- **negrao-falencia-recuperacao** — NEGRÃO, Ricardo. Falência e Recuperação de Empresas. São Paulo: Saraiva, 2022.
- **nery-cpc-comentado** — NERY JUNIOR, Nelson; NERY, Rosa Maria de Andrade. Código de Processo Civil Comentado. São Paulo: RT, 2018.
- **resumo-viciodeumaestudante** — Resumo de estudos — Falência e Recuperação Judicial (@viciodeumaestudante).
- **rj-falencia-metodos-solucao-conflitos** — Recuperação Judicial e Falência — Métodos de Solução de Conflitos.
- **sacramone-comentarios-lref** — SACRAMONE, Marcelo Barbosa. Comentários à Lei de Recuperação de Empresas e Falência. São Paulo: Saraiva, 2021.
- **sacramone-manual-empresarial** — SACRAMONE, Marcelo Barbosa. Manual de Direito Empresarial. 3. ed. São Paulo: Saraiva, 2022.
- **sacramone-nunes-societario-recuperacao** — SACRAMONE, Marcelo Barbosa; NUNES, Marcelo Guedes (coord.). Direito Societário e Recuperação de Empresas. São Paulo: Quartier Latin, 2021.
- **sacramone-rj-falencia** — SACRAMONE, Marcelo Barbosa. Recuperação Judicial e Falência. São Paulo: Saraiva.

## Observações

- Os números de página nos cabeçalhos dos trechos referem-se à **paginação do arquivo PDF de origem**,
  que pode diferir da paginação impressa da obra. Confira no PDF quando a citação exigir a página impressa.
- Material de pesquisa interna. Confira sempre a **redação vigente da lei** e a **jurisprudência atual**,
  pois os textos refletem o estado da arte à época de cada publicação.
- Total de trechos indexados: **478**.

## Integração com o peticionamento (usar como fonte em qualquer peça)

As 11 skills desta biblioteca têm gatilho para **disparar automaticamente ao minutar qualquer peça**
(petição inicial, contestação, réplica, manifestação, memoriais, recursos, embargos, exceção de
pré-executividade, impugnação, objeção ao plano, plano de recuperação e aditivos). O fluxo pretendido:

1. Ao redigir uma peça, identifique a âncora jurídica (artigo, instituto, tese).
2. A skill da(s) obra(s) pertinente(s) é acionada; localize o trecho no índice/mapa de temas.
3. **Leia o `references/sec-NN.md`** e fundamente a peça, citando a obra e o intervalo de páginas.

### Tornar permanente nas skills de peticionamento (`peticionador` e `peticionador-rj`)

Para que as skills de peticionamento **sempre** consultem esta biblioteca, adicione o bloco abaixo à
seção de instruções de cada uma, em **Configurações → Capacidades**:

```
## Fontes de pesquisa doutrinária (obrigatório)
Antes de redigir qualquer peça, consulte a biblioteca "biblioteca-doutrina-gn":
- Recuperação Judicial/Falência: sacramone-comentarios-lref, sacramone-manual-empresarial,
  sacramone-rj-falencia, sacramone-nunes-societario-recuperacao, negrao-falencia-recuperacao,
  rj-falencia-metodos-solucao-conflitos.
- Processo Civil: nery-cpc-comentado, donizetti-curso-processual-civil,
  araujo-junior-processo-civil-pratica, incentivos-processuais-economia-comportamental.
Localize o tema no índice da skill, LEIA o references/sec-NN.md correspondente e fundamente a peça
citando a obra e o intervalo de páginas. Não cite de memória.
```
