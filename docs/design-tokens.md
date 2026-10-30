# 🎨 Tokens de Design

**Projeto:** Gestão de Caronas na UTFPR
**Versão:** 1.1 · decisões de design
**Última atualização:** Outubro de 2026

> 🤖 **Este documento existe para a IA parar de inventar um botão diferente a cada
> tela.** Não é um design system — é o mínimo que dá à prototipagem assistida algo a
> que obedecer.

---

## Paleta

Nome semântico, nunca `azul-2` — a cor muda, o papel dela não. Os nomes ficam em
inglês porque viram classes do Tailwind (`bg-primary`, `text-foreground`).

| Token | Valor | Onde se usa |
| --- | --- | --- |
| `primary` | `#FFC700` | ações principais e identidade visual |
| `secondary` | `#121212` | contraste, textos e ícones |
| `tertiary` | `#FFF8E1` | fundo claro e identidade PWA |
| `neutral` | `#F8F9FA` | superfícies e áreas neutras |
| `surface` | `#FFFFFF` | fundo de cartões, formulários e painéis |
| `foreground` | `#121212` | títulos, conteúdo principal e rótulos |
| `muted` | `#6B6B6B` | descrições, metadados, legendas e informações secundárias |
| `danger` | `#B42318` | erros de validação, alertas críticos e ações destrutivas |
| `success` | `#087443` | confirmações, verificações e estados positivos |
| `disabled` | `#D9D9D9` | botões indisponíveis, campos inativos e controles bloqueados |

## Escala de espaçamento

Uma progressão só, usada em tudo.

| Token | Valor |
| --- | --- |
| `xs` | `4px` |
| `sm` | `8px` |
| `md` | `16px` |
| `lg` | `24px` |
| `xl` | `32px` |

## Tipografia

| Token | Família · tamanho · peso | Papel |
| --- | --- | --- |
| `heading-xl` | Inter, sans-serif · `32px` · `700` (Bold) | título principal |
| `heading-lg` | Inter, sans-serif · `24px` · `700` (Bold) | títulos de seção |
| `heading-md` | Inter, sans-serif · `20px` · `700` (Bold) | títulos de cartões |
| `body` | Inter, sans-serif · `14px` · `400` (Regular) | texto de corpo |
| `label` | Inter, sans-serif · `12px` · `500` (Medium) | rótulos |
| `caption` | Inter, sans-serif · `10px` · `400` (Regular) | legendas |

Escala complementar: `xs` `10px`, `sm` `12px`, `md` `14px`, `lg` `16px`,
`xl` `20px`, `2xl` `24px` e `3xl` `32px`. Pesos disponíveis: Regular `400`,
Medium `500`, Semibold `600` e Bold `700`.

## Estados de botão

| Estado | Aparência |
| --- | --- |
| normal | Fundo `#FFC700`, texto e ícone `#121212`, borda arredondada de `12px` e sombra leve |
| hover | Fundo `#E5B200`, texto escuro e sombra sutil; transição de `150ms` |
| foco (teclado) | Fundo amarelo original; contorno `#121212` de `2px`, afastado `2px`; aplicar com `:focus-visible` |
| desabilitado | Fundo `#D9D9D9`, texto e ícones em cinza escuro, sem sombra ou hover; ação indisponível para