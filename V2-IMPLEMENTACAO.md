# FUNIL BK V2 — IMPLEMENTAÇÃO

Data: 2026-08-11

## Aplicado

- entrada com Diagnóstico do Ponto de Ruptura;
- duas boas notícias antes das perguntas;
- 28 etapas no total;
- perguntas de contexto, abertura, diagnóstico, valor, preço, objetivo, quatro objeções, follow-up e fechamento;
- microganhos visuais ao longo do percurso;
- feedback sonoro curto e opcional;
- progresso persistente em localStorage (`bypassBK_v2`);
- diagnóstico adaptativo em quatro eixos: Diagnóstico Fraco, Valor Difuso, Objeção Reativa e Fechamento Aberto;
- comunicação do resultado em linguagem de cliente, sem expor lógica interna de classificação;
- recomendação personalizada conforme respostas;
- explicação do IPAC;
- apresentação da plataforma e do ecossistema de materiais;
- recomendação de produtos conforme o ponto de ruptura;
- VSL oficial integrada;
- oferta principal de R$37;
- preservação de UTMs e `fbclid`;
- Meta Pixel 341131507668987;
- exit-intent do livro por R$17 no funil;
- página editorial do livro criada em `livro.html`;
- vetores individuais do BK V2 em `/v2/`.

## Checkout

Checkout principal ativo:
`https://pay.hotmart.com/A98424225S?bid=1773208589822&checkoutMode=10&off=njqo49xj`

O checkout dedicado do livro de R$17 ainda não foi localizado entre os ativos canônicos. Por isso o botão de compra na página do livro permanece sem redirecionamento de pagamento para evitar cobrar R$37 ou apontar para uma oferta errada. Assim que existir a URL do checkout do livro, conectar somente esse CTA e registrar o evento `BK_Book17_Checkout`.

## Arquivos principais

- `index.html` — entrada/loader da V2;
- `index-v2.html` — experiência completa do diagnóstico;
- `livro.html` — recuperação editorial R$17;
- `/v2/*.svg` — vetores responsivos.
