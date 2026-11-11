# Palestras

Site estático com a lista das minhas palestras. Abro a página inicial, escolho uma e apresento.
Não precisa de instalação nem build: basta abrir o `index.html` no navegador.

## Estrutura

```
palestras/
├── index.html      # página inicial: lê o talks.js e mostra um card por palestra
├── talks.js        # cadastro das palestras (título, descrição, pasta, data, tags)
├── img/            # imagens compartilhadas entre as palestras
└── talks/
    └── <pasta>/
        └── index.html   # um deck reveal.js completo
```

## Como funciona

1. `index.html` carrega `talks.js`, que define `window.TALKS`.
2. Cada item vira um card, ordenado da data mais recente para a mais antiga.
3. Clicar no card abre `talks/<pasta>/index.html`, que é a apresentação (reveal.js).

## Apresentando

- `←` / `→` ou espaço: navegar pelos slides
- `F`: tela cheia
- `S`: visão do apresentador (notas)
- `Esc`: visão geral dos slides

Os decks carregam reveal.js e fontes por CDN, então é preciso internet.

## Adicionando uma palestra

1. Crie `talks/<nome-da-pasta>/index.html` (pode copiar uma palestra existente).
2. Imagens compartilhadas ficam em `img/` e são referenciadas como `../../img/arquivo.jpg`.
3. Cadastre em `talks.js`:

```js
{
  title: "Título da palestra",
  description: "Uma frase sobre ela.",
  folder: "nome-da-pasta",
  date: "2026-12-01",
  tags: ["Tag"],
},
```

## Palestras atuais

- **Esteira de produtos (roteiro)**: versão enxuta
