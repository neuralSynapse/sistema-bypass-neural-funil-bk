# Manifesto Técnico — Funil BK V1.0

## Identidade

Produto: Sistema Bypass Neural
Experiência: Diagnóstico do Ponto de Ruptura da Venda
Versão: V1.0

## Arquitetura

- `index.html`: loader de produção e correções defensivas de navegação
- `source/production/part-00.txt` a `part-08.txt`: nove blocos estáticos que formam o HTML final
- `.github/workflows/pages.yml`: deploy para GitHub Pages
- `.nojekyll`: publicação estática direta

## Regras críticas

- não alterar o checkout oficial sem decisão registrada
- preservar Pixel `341131507668987`
- preservar storage `bypassBK_v1`
- recalcular o diagnóstico a partir das respostas atuais
- não apresentar porcentagens pseudocientíficas
- preservar autonomia do cliente na linguagem pública
- não misturar este repositório com outros projetos ou marcas

## Fonte de verdade de produção

A branch `main` publicada é a fonte de verdade do código em produção. Mudanças futuras devem passar por branch, QA e promoção explícita.
