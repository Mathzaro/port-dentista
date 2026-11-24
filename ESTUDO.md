# Anotações de estudo

Cada etapa do projeto ganha uma seção aqui: o que mudou, por quê e perguntas que podem aparecer numa entrevista.

---

## 24/11/2026 · Estrutura HTML e CSS responsivo

### O que foi feito
- Página única com cabeçalho, apresentação (hero), sobre, tratamentos, primeira consulta, depoimentos, horários/endereço e rodapé.
- CSS escrito **mobile first**: o estilo base é para celular e os `@media (min-width: ...)` adicionam colunas em telas maiores.
- Cores, fontes e espaçamentos guardados em **variáveis CSS** no `:root`.

### Por que assim
- **Tags semânticas** (`header`, `main`, `section`, `address`) dizem ao navegador, ao Google e aos leitores de tela o que cada parte é. Uma `div` não diz nada.
- **Tratamentos em `<dl>`** (lista de definições): cada tratamento é um termo (`dt`) com a sua explicação (`dd`).
- **Passos da consulta em `<ol>`**: é uma sequência de verdade, então a lista é numerada. O número vem de um `counter` do CSS.
- **Horários em `<table>`**: são dados em linhas e colunas. O `th scope="row"` avisa ao leitor de tela que a célula é o título da linha.
- **`prefers-reduced-motion`**: a animação dos dentes só roda se a pessoa não pediu ao sistema para reduzir animações.

### Conceitos para revisar
`display: grid`, `grid-template-columns`, `clamp()`, `position: sticky`, `:focus-visible`, `counter-reset` / `counter-increment`, `@keyframes`.

### Perguntas de entrevista
1. **O que é mobile first e por que usar?**
   Escrever o CSS primeiro para telas pequenas e ir adicionando regras para telas maiores com `min-width`. O celular carrega só o necessário, e é mais fácil acrescentar colunas do que tirar.

2. **Qual a diferença entre `<section>` e `<div>`?**
   `<section>` é um bloco temático do conteúdo, normalmente com um título. `<div>` é só um contêiner, sem significado, usado para estilo ou agrupamento.
