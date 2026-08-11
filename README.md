# Sistema Bypass Neural — Funil BK

Repositório oficial e independente do **Funil BK do Sistema Bypass Neural**.

## Produção

- Entrada pública: `index.html`
- Arquitetura de produção: loader + 9 blocos estáticos em `source/production/`
- Fluxo: 28 telas, uma decisão por etapa
- Diagnóstico determinístico em quatro eixos:
  - Diagnóstico Fraco
  - Valor Difuso
  - Objeção Reativa
  - Fechamento Aberto
- Recalcula o diagnóstico a partir das respostas atuais, inclusive após voltar e editar
- Desempate ponderado e tratamento de cenário sem ruptura dominante
- Persistência local: `bypassBK_v1`
- Meta Pixel: `341131507668987`
- Checkout oficial Hotmart com preservação de UTMs e `fbclid`
- Ativos canônicos reais do produto, otimizados para web

## Sequência comercial

O diagnóstico cobre contexto, abertura, diagnóstico, construção de valor, preço, objetivo, objeções, follow-up e fechamento. O resultado entrega ponto principal, ponto secundário, manifestações, consequência, primeiro ajuste e nível qualitativo de estrutura.

O núcleo operacional apresentado é o IPAC: **Identificar, Perguntar, Apresentar e Conduzir**.

## QA da V1.0

- 28 etapas verificadas
- lógica original validada em 33/33 testes automatizados
- 9/9 blocos de produção com integridade verificada antes da publicação
- Pixel, checkout, storage e eventos obrigatórios conferidos
- navegação Resultado → Ponte corrigida antes do deploy
- redirecionamento automático do checkout corrigido antes do deploy
- auditoria pública sem referências a projetos externos ao Sistema Bypass Neural

Detalhes em [`QA.md`](QA.md).

## Deploy

GitHub Pages é publicado a partir da branch `main` por GitHub Actions usando `.github/workflows/pages.yml`.

Versão atual: **V1.0**
