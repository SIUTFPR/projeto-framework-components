# 🎨 Tokens de Design

**Projeto:** Gestão de Caronas na UTFPR
**Versão:** 1.0 · decisões de design
**Última atualização:** Outubro de 2026

> 🤖 **Este documento existe para a IA parar de inventar um botão diferente a cada
> tela.** Não é um design system — é o mínimo que dá à prototipagem assistida algo a
> que obedecer.

---

## Paleta

Nome semântico, nunca `azul-2` — a cor muda, o papel dela não.

| Token | Valor | Onde se usa |
| --- | --- | --- |
| `primaria` | `#FFC700` | ações principais e identidade visual |
| `secundaria` | `#121212` | contraste, textos e ícones |
| `terciaria` | `#FFF8E1` | fundo claro e identidade PWA |
| `neutra` | `#F8F9FA` | superfícies e áreas neutras |
| `superficie` | `#FFFFFF` | fundo de cartões, formulários e painéis |
| `texto` | `#121212` | títulos, conteúdo principal e rótulos |
| `texto-suave` | `#6B6B6B` | descrições, metadados, legendas e informações secundárias |
| `perigo` | `#B42318` | erros de validação, alertas críticos e ações destrutivas |
| `sucesso` | `#087443` | confirmações, verificações e estados positivos |
| `desabilitado` | `#D9D9D9` | botões indisponíveis, campos inativos e controles bloqueados |

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
| desabilitado | Fundo `#D9D9D9`, texto e ícones em cinza escuro, sem sombra ou hover; ação indisponível para clique e teclado |
| carregando | Mantém o fundo amarelo, mostra indicador animado e texto descritivo (ex.: “Enviando...”); impede envios repetidos |

## Breakpoints (Mobile-First)

O design nasce para a menor tela e cresce (ID2). Toda tela do protótipo tem
versão mobile antes da versão desktop.

| Token | Largura mínima | Vale para |
| --- | --- | --- |
| `sm` | `576px` | celulares grandes; mais espaço para formulários e cartões |
| `md` | `768px` | tablets; cartões em duas colunas e navegação ampliada |
| `lg` | `992px` | desktops; múltiplas colunas, navegação horizontal e áreas laterais |

## Identidade PWA

Os valores abaixo alimentam o `manifest.webmanifest` no `/utf-setup` (ID3).

| Campo | Valor |
| --- | --- |
| Nome curto (`short_name`) | `UTFPR Caronas` |
| Cor de tema (`theme_color`) | `#FFC700` |
| Cor de fundo (`background_color`) | `#FFF8E1` |
| Ícone | Amarelo com símbolo escuro |
| Modo de exibição (`display`) | `standalone` |
| Comportamento visual offline | Exibir faixa discreta e persistente sem conexão; manter disponíveis as últimas informações de caronas armazenadas localmente; desabilitar ações que dependem do servidor com explicação; atualizar dados e remover a faixa automaticamente ao reconectar. Manter a identidade amarela `#FFC700`, escura `#121212` e clara `#FFF8E1`; reservar vermelho para erros importantes. |

## Protótipo

**Link:** [Protótipo no Stitch](https://stitch.google.com/projects/328477196056609722)
**Telas:** Início (Home), Listagem de caronas, Oferecer uma carona e Detalhes da viagem.
