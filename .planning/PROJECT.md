# LP PIXT

## What This Is

Uma landing page de alta conversão para a PIXT — agência de Agentes de IA — construída com visual e comportamento inspirados na página da Apple (AirPods). A LP captura leads qualificados via formulário de contato e apresenta os quatro agentes da PIXT (Vendas+, LeadFlow, Booker, ExpertAI) com design minimalista, tipografia impactante e animações scroll-driven.

## Core Value

Converter visitantes em leads qualificados através de uma experiência visual premium que transmite a seriedade e inovação da PIXT no primeiro scroll.

## Requirements

### Validated

(Nenhum ainda — entregar para validar)

### Active

- [ ] Hero section com headline impactante, subtítulo e CTA principal (formulário ou âncora)
- [ ] Seção "O que é a PIXT" explicando a proposta de Força de Trabalho Sintética
- [ ] Seção de produtos com cards de Vendas+, LeadFlow, Booker e ExpertAI
- [ ] Formulário de contato com campos de nome, e-mail e empresa
- [ ] Visual white/clean predominante com tipografia sans-serif hierárquica (estilo Apple)
- [ ] Scroll-driven animations: fade-in e slide-up nos elementos ao rolar
- [ ] Sticky positioning para criar narrativa visual fluida
- [ ] Smooth scroll e hover effects sutis em CTAs e links
- [ ] Totalmente responsivo (mobile-first)
- [ ] Arquivo único HTML com CSS/JS embutidos (sem dependências externas além de fontes)
- [ ] Conteúdo extraído exclusivamente do arquivo "site oficial.html"

### Out of Scope

- Three.js / WebGL / cubos 3D — complexidade desnecessária para LP de conversão
- Modo dark — decisão consciente: visual white/clean foi escolhido
- Cópia direta do "site oficial" — a LP é um arquivo novo e independente
- Backend / servidor — apenas HTML estático

## Context

- **Código existente:** `site oficial.html` na mesma pasta — única fonte de conteúdo (textos, produtos, argumentos de venda)
- **Referência visual:** https://www.apple.com/br/airpods/ — espaçamento generoso, tipografia grande e bold, transições suaves, seções modularizadas
- **Brand PIXT:** Verde neon `#c6f432`, preto `#111211`, fontes Space Grotesk (display) e Work Sans (body)
- **Output:** Arquivo `lp pixt.html` em `C:\Users\T-GAMER\Desktop\Claude pojeto`
- **Sem build step:** Arquivo HTML autocontido, aberto diretamente no browser

## Constraints

- **Stack**: HTML + CSS + JS vanilla em arquivo único — sem frameworks, sem build
- **Conteúdo**: Apenas "site oficial.html" como fonte de verdade para textos
- **Visual**: Fundo branco predominante com acentos da brand PIXT (#c6f432)
- **Performance**: Sem Three.js; animações via CSS transitions + Intersection Observer

## Key Decisions

| Decision | Rationale | Outcome |
|----------|-----------|---------|
| White/clean visual (não dark) | Diferencia da hero do site oficial e aproxima do padrão Apple premium | — Pending |
| Arquivo HTML único autocontido | Facilita entrega e uso imediato sem servidor | — Pending |
| Formulário como CTA principal | Objetivo da LP é capturar leads qualificados | — Pending |

## Evolution

Este documento evolui nas transições de fase e milestones.

**Após cada fase:**
1. Requisitos invalidados? → Mover para Out of Scope com motivo
2. Requisitos validados? → Mover para Validated com referência da fase
3. Novos requisitos? → Adicionar em Active
4. Decisões a registrar? → Adicionar em Key Decisions

---
*Last updated: 2026-03-25 após inicialização*
