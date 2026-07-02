# Padrão da capa — Apresentação

Referência visual do slide 1 (capa) de `apresentacao.html`. Use este documento
como parâmetro para todos os novos temas de capa (título, subtítulo e cores
podem variar; o resto se mantém).

---

## Fundo

- Cor: `#35383F` (variável `--carbon`).
- Variante escura (slide 9 · encerramento): `#000000`.

## Fontes

Ambas do Google Fonts, já pré-carregadas no `<head>`.

- **Título:** DM Sans (pesos 400, 500, 600, 700).
- **Subtítulo & labels em caixa alta:** DM Mono (pesos 300, 400, 500).

## Logo

- Base64 embutido no HTML (PNG original 1414×2000, ícone + wordmark).
- Exibe **só o ícone** (hexágono). Wordmark "TATÁ SUSHI" é recortado.
  - `aspect-ratio: 1414 / 1250`
  - `object-fit: cover`
  - `object-position: top center`
- **Tamanho:** `width: 12.67%` do slide, `max-width: 104px`.
- **Espaço abaixo (gap até o título):** `margin-bottom: 4%`.

## Título

- Fonte: **DM Sans 700**.
- Cor: `#CFFF00` (variável `--citric`).
- Tamanho: `clamp(24px, 4.54vw, 65px)`.
- Line-height: `0.9`.
- Letter-spacing: `0.03em`.
- Alinhamento: horizontal e vertical central. O grupo (logo + título +
  subtítulo) é elevado com `padding-bottom: 26%` no `.slide-inner` para o
  **título** ficar no centro vertical do slide.

## Subtítulo

- Fonte: **DM Mono 400**.
- Cor: `rgba(255, 255, 255, .42)` (~42% de branco).
- Tamanho: `clamp(9px, 1vw, 12px)`.
- Letter-spacing: `0.32em`.
- Transform: `uppercase`.
- Margem acima (gap até o título): `margin-top: 2%`.

## Estrutura HTML

```html
<section class="slide slide-cover is-active" aria-label="Slide 1 · Capa">
  <div class="slide-inner">
    <img src="data:image/png;base64,..." alt="TATÁ SUSHI" class="cover-logo">
    <h1 class="cover-title">Reunião de líderes</h1>
    <p class="cover-subtitle">Um novo começo</p>
  </div>
</section>
```

## Como trocar o tema

1. **Título** — edite o texto do `<h1 class="cover-title">`.
2. **Subtítulo** — edite o texto do `<p class="cover-subtitle">`.
3. **Cor do fundo** — troque `--carbon` ou adicione uma variante (ex.: para o
   encerramento existe a classe `.slide-cover.is-dark` com `background: #000`).
4. **Cor do título** — mantenha `--citric` para permanecer no sistema, ou crie
   uma variante temática.
5. **Tudo o mais permanece igual** (logo, fontes, tamanhos, alinhamento).
