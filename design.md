# Nova Rental — Design System & Guia de Imagens

Landing page de movimentação e içamento de cargas pesadas.
Arquivo de referência: `nova-rental-landing.html`

---

## 1. Design System (tokens)

### Cores
| Token | Hex | Uso |
|---|---|---|
| `--bg` | `#EEF1F6` | Fundo claro das seções |
| `--surface` | `#FFFFFF` | Cards |
| `--ink` | `#0E1726` | Texto principal |
| `--ink-soft` | `#5A6678` | Texto secundário |
| `--navy` | `#081123` | Seções escuras / hero / footer |
| `--navy-2 / navy-3` | `#0C1A33` / `#11254a` | Gradientes escuros |
| `--brand` | `#0E5FE6` | Azul principal (CTAs, ícones, links) |
| `--brand-deep` | `#0A3FA8` | Azul profundo (gradiente de botão) |
| `--brand-bright` | `#3E8BFF` | Azul de brilho / destaque sobre escuro |
| `--line` | `#E2E7EF` | Bordas e divisores |

> A marca é **mono-azul**, como a referência da Cruzeiro é mono-vermelho. O azul é o único acento — usado em CTAs, ícones, badges numeradas e links. Não introduzir uma segunda cor de acento.

### Tipografia
- **Display / títulos:** Archivo (700–900), uppercase em eyebrows, peso 800/900 em headlines. Headline usa duas tonalidades: branco + 1 palavra em azul.
- **Corpo / UI:** DM Sans (400/500/700).

### Forma e estilo
Cantos arredondados (`14px`), cards com sombra suave, faixa marquee animada, corte diagonal no hero, brilho azul (glow) nos elementos-chave, grade forte, bastante espaço negativo. Tom geral: **industrial, técnico, confiável, ousado mas sóbrio.**

### Motion
Reveal no scroll (fade + subida leve), hover lift nos cards, marquee infinito. Respeita `prefers-reduced-motion`.

---

## 2. Mapa de Imagens

**Princípio:** cada imagem ilustra o assunto da seção em que aparece — a foto deve mostrar exatamente a situação descrita ao lado. Mantenha **consistência visual**: fotos reais de operação, tratamento escuro/azulado (blue grading), trabalhadores com EPI/colete hi-vis, céu dramático ou ambiente industrial.

**Padrões técnicos para todas as fotos**
- Tratamento: contraste alto, sombras azuladas frias, levemente dessaturado (exceto o colete hi-vis, que pode permanecer vibrante).
- Formato: `.webp` (fallback `.jpg`), comprimidas, com `loading="lazy"` exceto a do hero.
- Nada de marca d'água ou logo de banco de imagens.

**Como substituir no HTML:** cada slot é um `<div class="ph">…</div>`. Troque por:
```html
<img src="img/NOME-DO-ARQUIVO.webp" alt="DESCRIÇÃO" class="ph-img">
```
e adicione no CSS: `.ph-img{width:100%;height:100%;object-fit:cover;display:block}`

---

### 2.1 HERO — `img/hero-icamento.webp`
- **Seção:** topo / "Precisão para grandes operações"
- **Tamanho:** 1200×900 px (retrato cortado em diagonal), alta resolução. **Não usar lazy-load.**
- **Cena ideal:** guindaste ou caminhão munck içando uma carga pesada (equipamento industrial, viga ou contêiner) ao entardecer/noite, céu dramático. A imagem mais "heróica" do portfólio.
- **Prompt IA (EN):** `Heavy mobile crane lifting a large industrial machine against a dramatic dusk sky, blue color grading, low angle, cinematic, workers in hi-vis vests, photorealistic, high detail`

### 2.2 SEGMENTOS — grade de 6 (`.seg-card .ph`), 600×360 px cada
Cada foto deve mostrar **a aplicação específica** do card ao lado:

| Arquivo | Assunto do card | Cena ideal | Prompt IA (EN) |
|---|---|---|---|
| `img/seg-obras.webp` | Obras e construção civil | Munck/guindaste posicionando peça em canteiro de obras, estrutura de concreto ao fundo | `articulated crane lifting concrete beam at a construction site, daytime, workers with helmets` |
| `img/seg-industria.webp` | Indústria | Içamento de máquina dentro de galpão industrial, pontes rolantes ao fundo | `industrial machinery being lifted inside a factory hall, overhead cranes, sling rigging` |
| `img/seg-logistica.webp` | Logística e armazenagem | Empilhadeira/munck carregando paletes em pátio ou centro de distribuição | `forklift and crane truck loading pallets in a logistics yard, containers, sunny` |
| `img/seg-montagem.webp` | Montagens industriais | Guindaste içando estrutura metálica em montagem industrial | `crane lifting steel structure during industrial assembly, blue sky, steel frame building` |
| `img/seg-parada.webp` | Paradas de manutenção | Equipe removendo/posicionando equipamento dentro de planta industrial | `maintenance team removing heavy equipment inside an industrial plant, tubes and tanks` |
| `img/seg-especiais.webp` | Operações especiais | Içamento crítico de carga de grande porte, rigging complexo, dois guindastes | `complex heavy lift operation with two cranes and rigging, oversized load, dusk` |

### 2.3 FROTA — grade de 4 (`.equip-card .ph`), 520×300 px cada
Foto do equipamento limpo, em destaque, idealmente com a marca Nova Rental:

| Arquivo | Equipamento | Prompt IA (EN) |
|---|---|---|
| `img/equip-guindaste.webp` | Guindaste | `mobile hydraulic crane on a construction site, clean, three-quarter view, blue sky` |
| `img/equip-munck.webp` | Caminhão Munck | `truck-mounted articulated knuckle-boom crane (munck), white truck, three-quarter view` |
| `img/equip-plataforma.webp` | Plataforma elevatória | `blue scissor lift / aerial work platform extended, worker on top, clear sky` |
| `img/equip-empilhadeira.webp` | Empilhadeira | `industrial forklift carrying a pallet of materials in a warehouse, yellow forklift` |

> Dica: para a frota, fundo **mais claro/dia** ajuda o equipamento a "saltar" do card. Mantenha enquadramento consistente entre os 4 (mesmo ângulo 3/4).

### 2.4 OPERAÇÕES (seção escura) — 3 cards (`.case-card .ph`), 560×320 px
Fotos de **ação real**, fechadas no detalhe da operação:

| Arquivo | Assunto | Cena ideal | Prompt IA (EN) |
|---|---|---|---|
| `img/op-icamento.webp` | Içamento e movimentação | Carga suspensa por cabos/lingas, gancho em primeiro plano | `heavy load suspended by crane slings, hook close-up, motion, blue industrial grading` |
| `img/op-remocao.webp` | Remoção técnica de máquinas | Máquina industrial sendo retirada de dentro de uma planta | `industrial machine being removed from a factory by crane, technical operation` |
| `img/op-transporte.webp` | Transporte e posicionamento | Carga sendo posicionada com precisão por operador sinalizando | `worker signaling crane operator positioning a heavy load precisely, hand signals` |

### 2.5 CAPACIDADE TÉCNICA — `img/capacidade-bg.webp` (`.cap-card .ph`)
- **Uso:** fundo do card escuro com o logo da Nova Rental por cima (a foto fica com 45% de opacidade, então escolha algo com boa silhueta).
- **Cena ideal:** silhueta de guindaste/lança contra o céu, ou frota perfilada.
- **Prompt IA (EN):** `silhouette of a crane boom against a moody blue sky, dark, atmospheric, space for logo overlay`

### 2.6 DEPOIMENTOS — opcional
Hoje usam iniciais coloridas (`RS`, `MA`, `JC`). Se tiver fotos reais dos clientes, substitua o `.test-avatar` por `<img>` 96×96 px, recorte circular. **Não use rostos genéricos de banco de imagens** em depoimentos — soa falso. Sem foto real, mantenha as iniciais.

### 2.7 LOGO
O logo atual é um ícone SVG vetorial (guindaste estilizado) + wordmark "NOVA RENTAL". Para usar o logo oficial, substitua o `<span class="mark">…</span>` por `<img src="img/logo-nova-rental.svg">`. Preferir SVG/PNG transparente.

---

## 3. Prompt para finalizar o design na Stitch

Cole o bloco abaixo na Stitch (modo de maior qualidade, formato **web app**). Suba a página 1 do PDF da Nova Rental e/ou um print desta landing como **imagem de referência** para o style matching. Depois, refine **uma coisa por vez**.

```
You are a senior UI/UX designer. Design a polished, high-converting single-page B2B landing page (web/desktop, 1440px) for "Nova Rental", a heavy-load handling and crane-lifting company in Brazil.

=== HARD RULE ===
All visible text MUST be in Brazilian Portuguese, exactly as written below. Do NOT translate to English. Keep accents.

=== DESIGN SYSTEM ===
Mood: industrial, engineered, premium, confident — an engineering firm that owns the operation, not a flyer.
Single accent color = cobalt blue (use only for CTAs, icons, numbered badges, links).
Colors: page bg #EEF1F6; cards #FFFFFF; dark sections/hero/footer #081123 with #0C1A33 gradients; primary blue #0E5FE6; deep blue #0A3FA8; bright blue glow #3E8BFF; borders #E2E7EF.
Type: headlines in Archivo (800/900), uppercase eyebrows in Archivo 700 with letter-spacing; body in DM Sans. Headlines are white with ONE keyword in cobalt blue.
Shape language: 14px rounded cards, soft shadows, animated marquee strip, diagonal cut on hero photo, subtle blue edge-glow on key elements, blueprint-style faint grid, strong 12-col grid, generous whitespace.
Buttons: gradient cobalt→deep-blue pill with a small circular arrow icon. Hover lift.

=== SECTIONS (top to bottom) ===
1) Thin top bar (dark): left "Atendimento em obras, indústrias e logística — todo o estado de São Paulo"; right phone "(19) 99427-6272" + "comercial@novarental.com.br".
2) Sticky nav: logo "NOVA RENTAL" (crane icon); links Início · Segmentos · Equipamentos · Operações · Processo; right cobalt button "Solicitar orçamento".
3) HERO (dark, photo right with diagonal cut): kicker "MOVIMENTAÇÃO E IÇAMENTO DE CARGAS PESADAS"; H1 "Precisão para grandes operações" (with "operações" in cobalt); subhead "A Nova Rental movimenta, iça e posiciona cargas pesadas para obras, indústrias e logística — com planejamento técnico, equipe qualificada e frota moderna onde o erro não é uma opção."; primary CTA "Solicitar orçamento"; ghost CTA "Ver operações".
4) MARQUEE strip (cobalt gradient, scrolling): "Segurança operacional · Frota moderna · Equipe certificada · Atendimento ágil · Análise de risco · Suporte técnico".
5) SEGMENTOS — section title "Soluções de movimentação para diferentes operações", eyebrow "Segmentos de atuação". 6 photo cards (3x2), each photo + title + 1-line + "Ver solução →": Obras e construção civil; Indústria; Logística e armazenagem; Montagens industriais; Paradas de manutenção; Operações especiais. CTA below.
6) FROTA E EQUIPAMENTOS — title "Estrutura versátil para cada operação". 4 cards (numbered 01–04) photo + title + 3 bullets: Guindaste; Caminhão Munck; Plataforma elevatória; Empilhadeira.
7) DIFERENCIAIS — 2-col: left title "Por que a Nova Rental é a escolha de quem não pode errar" + paragraph + CTA; right 6 icon cards (3x2): Segurança operacional; Equipe qualificada; Frota moderna; Atendimento ágil; Suporte técnico; Compromisso com o cliente.
8) OPERAÇÕES (dark section) — title "Movimentação técnica aplicada em projetos de alta exigência". 3 glass cards over photos, each with title + checkmark bullets + "Solicitar operação →": Içamento e movimentação de cargas pesadas; Remoção técnica de máquinas e equipamentos; Transporte e posicionamento técnico.
9) PROCESSO — title "Um processo estruturado para movimentar com mais segurança". 6 numbered step cards (3x2): 1 Entendimento da necessidade; 2 Análise técnica e de risco; 3 Planejamento da operação; 4 Mobilização; 5 Execução segura; 6 Entrega com acompanhamento.
10) CAPACIDADE TÉCNICA — 2-col: left dark image card with Nova Rental logo overlay; right title "Operação que não abre mão da segurança e da precisão" + paragraph + 6 checkmark items (Análise técnica do projeto; Operadores qualificados; Equipamentos revisados; Planejamento com análise de risco; Atendimento focado em cada operação; Suporte do início ao fim) + CTA.
11) DEPOIMENTOS — title "Credibilidade construída em operações reais e relações de confiança". 3 testimonial cards with 5 stars, quote, avatar with initials + name + role.
12) CONTATO — two-column card: left dark panel "Sua operação merece a segurança da Nova Rental" + phone (19) 99427-6272 + e-mail comercial@novarental.com.br + responsável Gabriel Dourado; right white form "Solicite um orçamento" with fields Nome, Empresa, E-mail, WhatsApp, dropdown "Tipo de operação", Mensagem, and cobalt submit "Solicitar orçamento".
13) FOOTER (dark): logo + description + slogan "Movimentamos cargas. Entregamos soluções." (last 2 words in cobalt); Navegação links; Contato (região de Sumaré/Campinas, phone, e-mail, novarental.net.br); social icons (Instagram, Facebook, WhatsApp). Bottom bar "© 2026 Nova Rental. Todos os direitos reservados."

Do NOT include an FAQ section.
Make the cobalt "Solicitar orçamento" button the single most prominent action across the page. Use dramatic crane/lifting photos with dark-blue color grading and hi-vis workers as imagery placeholders.
```

**Versão mobile (rode depois, na mesma sessão):**
```
Now create the MOBILE version (390px) of this same Nova Rental landing, keeping the EXACT design system and all Portuguese copy (do not translate). Sticky top bar with logo + hamburger + persistent cobalt "Orçamento" button. Hero single column, photo as full-bleed background, CTAs full-width stacked. All grids become single column. Add a FIXED bottom action bar always visible: cobalt "Solicitar orçamento" + WhatsApp icon. Large tap targets (min 48px). No FAQ.
```

> Depois de gerar, refine com pedidos pontuais, ex.: *"Deixe o botão de orçamento maior e adicione brilho azul na borda dos cards de equipamento"*. Exporte para Figma (camadas editáveis) ou HTML/CSS quando aprovar.
