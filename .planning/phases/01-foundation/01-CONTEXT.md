# Phase 1: Foundation - Context

**Gathered:** 2026-03-25
**Status:** Ready for planning

<domain>
## Phase Boundary

Criar o sistema de design CSS completo, esqueleto do documento HTML, barra de navegação estática, seção hero full-viewport e footer com aviso LGPD. Tudo estático — sem JavaScript (JS vem na Fase 3). Output: arquivo `lp pixt.html` browsável e responsivo.

</domain>

<decisions>
## Implementation Decisions

### Hero — Tratamento Visual
- **D-01:** Fundo branco puro (`#ffffff`) com acento da cor brand — uma forma ou bloco geométrico em `#c6f432` como elemento visual de destaque no hero
- **D-02:** Hero contém: headline + subtítulo + botão CTA + elemento gráfico abstrato (linhas, grade ou forma geométrica em verde/preto) — sem foto ou imagem de produto na Fase 1
- **D-03:** Headline muito grande, estilo Apple — entre 5rem e 7rem no desktop; hierarquia tipográfica marcante

### Decisões Travadas (PROJECT.md + REQUIREMENTS.md)
- **D-04:** Visual white/clean — fundo predominantemente branco, sem modo dark
- **D-05:** Arquivo HTML único autocontido — sem build step, sem frameworks
- **D-06:** Fontes: Space Grotesk (display/headlines) + Work Sans (body) via Google Fonts com `preconnect` + `display=swap`
- **D-07:** Hero usa `min-height: 100dvh` com fallback `min-height: 100vh` para iOS Safari
- **D-08:** Smooth scroll via CSS `scroll-behavior: smooth` no `<html>`
- **D-09:** Todas as animações futuras usam apenas `transform` e `opacity` — zero layout recalculation

### Claude's Discretion
- Cinzas/neutros do sistema de design (texto secundário, bordas, muted) — usar escala razoável baseada em `#111211` e `#ffffff`
- Estrutura exata do elemento gráfico abstrato no hero (linhas, grade ou forma)
- Layout desktop do nav (logo + CTA; links de âncora opcionais)
- Conteúdo do footer além do aviso LGPD (logo, copyright, redes sociais)
- Espaçamento e padding do sistema de design

</decisions>

<specifics>
## Specific Ideas

- Referência visual principal: https://www.apple.com/br/airpods/ — espaçamento generoso, tipografia grande e bold, seções limpas, muito branco
- Brand PIXT: verde neon `#c6f432`, preto `#111211`
- O elemento gráfico abstrato no hero deve usar as cores da brand (verde e/ou preto) — geométrico, não orgânico
- A LP é um arquivo NOVO e independente do `site oficial.html` — o site oficial é apenas fonte de conteúdo textual, não base de código

</specifics>

<canonical_refs>
## Canonical References

**Downstream agents MUST read these before planning or implementing.**

### Requisitos da Fase 1
- `.planning/REQUIREMENTS.md` — Requirements NAV-01, NAV-02, HERO-01, HERO-02, FOOT-01, FOOT-02, FONT-01, PERF-01 com critérios de aceite detalhados

### Contexto do Projeto
- `.planning/PROJECT.md` — Decisões chave (white/clean, arquivo único, formulário como CTA), constraints de stack, referência Apple AirPods
- `.planning/STATE.md` — Histórico de decisões e contexto de sessão

### Fonte de Conteúdo
- `site oficial.html` — Fonte de verdade para textos, copy e conteúdo da PIXT (NÃO clonar o código — apenas extrair texto quando necessário)

</canonical_refs>

<code_context>
## Existing Code Insights

### Reusable Assets
- Nenhum componente reutilizável direto — LP é arquivo novo e independente

### Established Patterns (do site oficial e arquivos existentes)
- Google Fonts já usado em todos os arquivos existentes: `Space Grotesk` + `Work Sans` com os pesos 400/500/600/700
- CSS custom properties (variáveis) é o padrão estabelecido nos arquivos existentes — usar `--color-accent: #c6f432`, `--color-bg: #fff`, etc.
- Nav com `position: fixed` + `backdrop-filter: blur()` é padrão nos arquivos existentes

### Integration Points
- Nenhum — Phase 1 cria o documento base do zero

</code_context>

<deferred>
## Deferred Ideas

- Tokens de cor detalhados do sistema de design (cinzas, bordas, muted) — Claude decide durante implementação
- Links de âncora no nav para seções — as seções ainda não existem na Fase 1; nav terá logo + CTA apenas
- Interatividade do nav (scroll behavior, hide/show) — Fase 3
- Conteúdo real extraído do `site oficial.html` para o hero — Fase 2; Fase 1 usa placeholder copy

</deferred>

---

*Phase: 01-foundation*
*Context gathered: 2026-03-25*
