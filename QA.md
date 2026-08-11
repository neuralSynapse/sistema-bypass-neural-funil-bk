# QA — Sistema Bypass Neural — Funil BK V1.0

## Status

Build de produção validado para publicação no GitHub Pages.

## Estrutura

- 28 telas executáveis
- mobile-first
- uma decisão por tela
- voltar e editar respostas
- reiniciar diagnóstico
- persistência em `localStorage` com chave `bypassBK_v1`

## Diagnóstico

- quatro eixos: Diagnóstico Fraco, Valor Difuso, Objeção Reativa e Fechamento Aberto
- score recalculado integralmente após cada edição
- sem soma cega de pontuação
- desempate ponderado
- ponto secundário preservado
- caso com score total zero tratado como ausência de ruptura dominante
- níveis qualitativos: Estrutura Inicial, Parcial, Funcional e Consolidada

## Tracking

Meta Pixel: `341131507668987`

Eventos verificados no build:

- PageView
- BK_ViewEntry
- BK_StartDiagnostic
- BK_ContextComplete
- BK_OpeningComplete
- BK_DiagnosisComplete
- BK_ValueComplete
- BK_PriceComplete
- BK_ObjectionsComplete
- BK_FollowupComplete
- BK_ClosingComplete
- BK_DiagnosticComplete
- BK_ResultViewed
- BK_OfferViewed
- BK_CTA_Click
- InitiateCheckout

## Checkout

Base oficial:

`https://pay.hotmart.com/A98424225S?bid=1773208589822&checkoutMode=10&off=njqo49xj`

Preserva quando disponíveis:

- `utm_source`
- `utm_medium`
- `utm_campaign`
- `utm_content`
- `utm_term`
- `fbclid`

Adiciona `sck` com eixo principal e canal.

## Integridade de produção

- 9/9 blocos em `source/production/` verificados antes da promoção para `main`
- loader configurado para exatamente 9 blocos
- navegação Resultado → Ponte corrigida no loader de produção
- redirecionamento automático do checkout corrigido no loader de produção
- ativos reais do Sistema Bypass Neural incorporados em versões otimizadas para web

## Testes de lógica

A implementação original passou 33/33 testes automatizados, cobrindo classificação forçada dos quatro eixos, desempate, cenário consolidado, recálculo após edição, parâmetros de checkout, deduplicação de eventos e presença dos identificadores obrigatórios.

## Gate final

Após o GitHub Pages ficar público, realizar verificação do URL publicado, carregamento dos nove blocos e fluxo de entrada. QA visual real em diferentes larguras de tela é o último gate externo.
