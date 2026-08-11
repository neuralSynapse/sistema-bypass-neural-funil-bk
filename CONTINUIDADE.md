# Continuidade Operacional — Sistema Bypass Neural — Funil BK

## Repositório oficial

`neuralSynapse/sistema-bypass-neural-funil-bk`

## Produção

Branch publicada: `main`

Entrada: `index.html`

Build: nove blocos em `source/production/`.

## Antes de qualquer alteração

1. criar ou usar branch de trabalho;
2. preservar checkout, Pixel e storage salvo;
3. testar recálculo de diagnóstico ao editar respostas;
4. conferir sequência de 28 telas;
5. validar tracking e checkout;
6. promover para `main` somente após QA.

## Pontos de atenção

O loader de produção aplica duas correções defensivas ao HTML montado:

- Resultado segue para a Ponte antes da oferta;
- checkout automático dispara quando a etapa final é `27`.

Essas correções devem ser incorporadas diretamente ao código-fonte numa futura refatoração, evitando removê-las sem substituir a lógica equivalente.

## URL esperada do GitHub Pages

Quando o Pages estiver ativo, o endereço padrão é:

`https://neuralsynapse.github.io/sistema-bypass-neural-funil-bk/`
