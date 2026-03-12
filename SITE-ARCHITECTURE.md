# SHERSHEN.AI — SITE ARCHITECTURE
## Complete Information Architecture & Implementation Plan
**Date**: 2026-03-13 | **Version**: 1.0

---

## 0. STRATEGIC FOUNDATION (from brand analysis)

Before architecture — the filter everything passes through:

- **Brand formula**: "Рій AI-агентів, що повертає підприємцям їхній час"
- **Sell time, not AI**: Every page answers "Скільки годин це зекономить?"
- **Result, not process**: "Ваш відділ працює 24/7 з завтра" instead of "ми впровадимо AI"
- **Kill two fears**: Fear of complexity + Fear of wasting money → Free 7-day pilot with measurable result
- **Cultural code**: "Wartime Innovation" — created in a country where AI is survival, not hype

---

## 1. THE 80/20 PAGES — 7 Pages That Drive Results

These are the only pages that matter for Phase 1. Everything else is noise until these convert.

| Priority | Page | Why It Matters | Revenue Impact |
|---|---|---|---|
| 1 | **Homepage** `/` | First impression, brand story, funnel entry | 40% of conversions start here |
| 2 | **AI-Assistants Service** `/poslugy/ai-asystenty/` | Highest-margin service, clearest value prop | Primary revenue driver |
| 3 | **Pricing** `/tsiny/` | #1 friction killer — transparency wins in UA market | Converts consideration → decision |
| 4 | **SEO Content Service** `/poslugy/seo-kontent/` | Easiest to demonstrate (show before/after rankings) | Quick-win revenue |
| 5 | **AI Implementation** `/poslugy/vprovadzhennya-ai/` | Highest ticket size | Enterprise/mid-market entry |
| 6 | **Contact/CTA** `/kontakty/` | Conversion endpoint | Every funnel ends here |
| 7 | **Blog (pillar article)** `/blog/` + 1st post | SEO entry point, proves expertise | Long-term organic pipeline |

---

## 2. COMPLETE URL STRUCTURE

### 2.1 Core Pages (Phase 1-2)

```
shershen.ai/
│
├── /                                    # Homepage (pillar landing)
│
├── /poslugy/                            # Services hub page
│   ├── /poslugy/ai-asystenty/           # AI Assistants & Chatbots
│   ├── /poslugy/vprovadzhennya-ai/      # AI Implementation for Business
│   └── /poslugy/seo-kontent/            # SEO Content with AI
│
├── /tsiny/                              # Pricing & Packages
├── /kejsy/                              # Case Studies hub
│   └── /kejsy/[slug]/                   # Individual case study
│
├── /blog/                               # Blog listing
│   └── /blog/[slug]/                    # Individual article
│
├── /pro-nas/                            # About / Team
├── /kontakty/                           # Contact + form + Calendly
├── /faq/                                # Extended FAQ
│
├── /polityka-konfidentsijnosti/         # Privacy Policy
├── /robots.txt
├── /sitemap.xml
└── /404
```

### 2.2 Future Pages (Phase 3+)

```
├── /instrumenty/                        # Interactive tools hub
│   ├── /instrumenty/roi-kalkulyator/    # ROI Calculator
│   └── /instrumenty/ai-audit/           # Free AI Readiness Quiz
│
├── /resursy/                            # Resources hub
│   ├── /resursy/chek-list-ai/           # Lead magnet landing
│   └── /resursy/shablony/               # Templates
│
├── /galuzevi-rishennya/                 # Industry solutions (future)
│   ├── /galuzevi-rishennya/e-commerce/
│   ├── /galuzevi-rishennya/medsfera/
│   └── /galuzevi-rishennya/poslugovy-biznes/
```

### 2.3 URL Design Rationale

- **Ukrainian transliteration** — targeting UA search queries, not EN
- **No `.html` extensions** — clean URLs, CMS-agnostic
- **Shallow depth** — max 2 levels for SEO crawl efficiency
- **Keyword-in-URL** — every slug contains primary keyword

---

## 3. NAVIGATION HIERARCHY

### 3.1 Main Navigation (Desktop Header)

```
[ШЕРШЕНЬ logo]    Послуги ▾    Кейси    Ціни    Блог    Про нас    [🐝 Безкоштовний пілот]
                    ├── AI-асистенти
                    ├── Впровадження AI
                    └── SEO-контент
```

**Rules:**
- Max 6 items + 1 CTA button
- CTA is always amber/yellow, always visible
- "Послуги" dropdown on hover (desktop) / tap (mobile)
- Logo always links to homepage
- CTA text: "Безкоштовний пілот" (not "Консультація" — per CMO audit recommendation)

### 3.2 Mobile Navigation (Burger)

```
× Закрити

Головна
Послуги
  → AI-асистенти
  → Впровадження AI
  → SEO-контент
Кейси
Ціни
Блог
Про нас
FAQ
Контакти

───────────────────
📞 +380 XX XXX XXXX
📱 Написати в Telegram

[Безкоштовний 7-денний пілот] ← sticky amber button
```

### 3.3 Footer Navigation

```
┌─────────────────────────────────────────────────────────────────┐
│                                                                   │
│  ШЕРШЕНЬ                    Послуги           Ресурси              │
│  Рій AI-агентів для         AI-асистенти      Блог                │
│  вашого бізнесу             Впровадження AI   Кейси               │
│                             SEO-контент       FAQ                 │
│  hello@shershen.ai          Ціни              Про нас             │
│  +380 XX XXX XXXX                                                 │
│  Telegram: @shershen_ai                                           │
│                                                                   │
│  ─────────────────────────────────────────────────────────────── │
│  © 2026 Шершень | Політика конфіденційності                      │
│                                                                   │
└─────────────────────────────────────────────────────────────────┘
```

### 3.4 Utility Navigation

- **Sticky mobile CTA**: Fixed bottom bar with "Безкоштовний пілот" button (appears after 30% scroll)
- **Floating Telegram button**: Bottom-right corner on all pages
- **Breadcrumbs**: On all pages except homepage (`Головна > Послуги > AI-асистенти`)

---

## 4. INTERNAL LINKING STRATEGY

### 4.1 Topic Cluster Model

```
                    ┌──────────────┐
                    │   HOMEPAGE   │
                    │  (Hub Page)  │
                    └──────┬───────┘
                           │
          ┌────────────────┼────────────────┐
          │                │                │
    ┌─────▼─────┐    ┌────▼─────┐    ┌────▼──────┐
    │ CLUSTER 1 │    │ CLUSTER 2│    │ CLUSTER 3 │
    │ AI-       │    │ AI       │    │ SEO +     │
    │ Assistants│    │ Implemen-│    │ Content   │
    │ (Pillar)  │    │ tation   │    │ (Pillar)  │
    │           │    │ (Pillar) │    │           │
    └─────┬─────┘    └────┬─────┘    └─────┬─────┘
          │               │                │
    Blog articles   Blog articles    Blog articles
    + Case studies  + Case studies   + Case studies
    (spokes)        (spokes)         (spokes)
```

### 4.2 Cluster 1: AI-Assistants (Pillar: `/poslugy/ai-asystenty/`)

**Pillar page** links to and from:
- Blog: "Як створити чат-бота для бізнесу" → `/blog/chat-bot-dlya-biznesu/`
- Blog: "Telegram бот для бізнесу: 10 прикладів" → `/blog/telegram-bot-biznes/`
- Blog: "AI-асистент vs чат-бот: різниця" → `/blog/ai-asystent-vs-chat-bot/`
- Blog: "Скільки коштує розробка чат-бота 2026" → `/blog/rozrobka-chat-bota-tsina/`
- Blog: "Інтеграція бота з CRM" → `/blog/crm-integratsiya-bot/`
- Case: Relevant client case studies
- Cross-link: Pricing page (package details)
- Cross-link: FAQ (bot-related questions)

### 4.3 Cluster 2: AI Implementation (Pillar: `/poslugy/vprovadzhennya-ai/`)

**Pillar page** links to and from:
- Blog: "Впровадження AI у бізнес: з чого почати" → `/blog/vprovadzhennya-ai-biznes/`
- Blog: "AI для малого бізнесу: 7 кейсів" → `/blog/ai-malyj-biznes/`
- Blog: "ROI від впровадження AI" → `/blog/roi-ai/`
- Blog: "RAG-система для бізнесу" → `/blog/rag-systema-biznes/`
- Case: Implementation case studies
- Cross-link: ROI Calculator tool
- Cross-link: AI Readiness Checklist (lead magnet)

### 4.4 Cluster 3: SEO Content (Pillar: `/poslugy/seo-kontent/`)

**Pillar page** links to and from:
- Blog: "AI для SEO: контент що ранкується" → `/blog/ai-dlya-seo/`
- Blog: "SEO-статті з AI: якість та унікальність" → `/blog/seo-statti-ai/`
- Blog: "Контент-стратегія з AI: план на 12 місяців" → `/blog/kontent-strategiya-ai/`
- Case: Content/SEO case studies
- Cross-link: Pricing (content packages)

### 4.5 Cross-Page Linking Rules

Every page must have:
1. **2-3 contextual links** to other service/blog pages within body text
2. **CTA block** linking to `/kontakty/` or `/tsiny/`
3. **"Related" section** at bottom with 2-3 related articles/cases
4. **Breadcrumbs** linking up the hierarchy

**Link equity flow priority:**
```
Homepage → Service pages → Case studies → Blog posts
              ↑                              │
              └──────────────────────────────┘
              (blog posts link back to services)
```

---

## 5. CONTENT TYPES & TEMPLATES

### 5.1 Landing/Service Pages (3 pages)

**Template structure:**
```
[Breadcrumb]
[H1: Question format — "Як AI-асистент може працювати на ваш бізнес 24/7?"]
[Answer-first paragraph — direct value statement with numbers]
[Trust bar — client logos]

[Section: Problem — "Знайомо? Ви витрачаєте X годин на..."]
[Section: Solution — what Shershen does, with specifics]
[Section: How it works — 3-4 step process, timeline]
[Section: Results/proof — numbers, mini-cases, before/after]
[Section: Pricing preview — starting from, link to full pricing]
[Section: FAQ — 4-5 service-specific questions, schema markup]
[CTA block — "Безкоштовний 7-денний пілот"]
[Related cases + blog posts]
```

### 5.2 Case Studies

**Template structure:**
```
[Breadcrumb]
[H1: "Як [компанія] зекономила [X годин/грн] з AI від Шершня"]
[Hero metrics: 3 key numbers in big cards]
[Challenge section]
[Solution section — what was built]
[Results section — measurable outcomes]
[Client quote/testimonial]
[CTA: "Хочете такий самий результат?"]
```

**Naming convention:** `/kejsy/[industry]-[result]/`
Example: `/kejsy/ecommerce-avtomatyzatsiya-pidtrymky/`

### 5.3 Blog Posts

**Content types within blog:**
- **How-to guides** (1500-3000 words) — SEO workhorses
- **Comparison posts** (GPT vs Claude, etc.) — high commercial intent
- **Cost/pricing articles** — capture bottom-funnel queries
- **Trend pieces** — shareability, thought leadership
- **Mini case studies** — social proof disguised as content

**Template structure:**
```
[Breadcrumb]
[H1: Target keyword as question]
[TL;DR box — 2-3 sentence answer for AI snippets]
[Table of contents]
[Body with H2s as questions]
[Author box — expertise signals]
[CTA: Lead magnet or consultation]
[Related articles — 3 cards]
```

### 5.4 Blog Categories (map to clusters)

| Category | URL | Target |
|---|---|---|
| AI-асистенти | `/blog/category/ai-asystenty/` | Cluster 1 |
| Впровадження AI | `/blog/category/vprovadzhennya-ai/` | Cluster 2 |
| SEO та контент | `/blog/category/seo-kontent/` | Cluster 3 |
| AI тренди | `/blog/category/ai-trendy/` | Awareness/traffic |

### 5.5 Interactive Tools (Phase 3)

| Tool | Purpose | Lead capture |
|---|---|---|
| ROI Calculator | "Скільки ви зекономите з AI" — input hours/costs, output savings | Email for full report |
| AI Readiness Quiz | 5-question assessment — "Чи готовий ваш бізнес до AI" | Email for results PDF |

---

## 6. SEO KEYWORD MAPPING (Ukrainian Focus)

### 6.1 Homepage

| Target Keyword | Search Volume (est.) | Difficulty | Intent |
|---|---|---|---|
| ai для бізнесу україна | Medium | Low | Informational/Commercial |
| штучний інтелект для бізнесу | Medium | Medium | Informational |
| ai автоматизація бізнесу | Low-Med | Low | Commercial |
| ai студія україна | Low | Low | Navigational |

**Title**: Шершень — AI-автоматизація для бізнесу | Повертаємо вам 20 годин на тиждень
**H1**: Рій AI-агентів, що працює на ваш бізнес 24/7

### 6.2 AI Assistants Page

| Target Keyword | Volume | Difficulty | Intent |
|---|---|---|---|
| чат-бот для бізнесу | High | Medium | Commercial |
| ai асистент | Medium | Medium | Informational |
| розробка чат-бота | Medium | Medium | Commercial |
| telegram бот для бізнесу | Medium | Low | Commercial |
| чат-бот для сайту | Medium | Medium | Commercial |

**Title**: AI-асистенти та чат-боти для бізнесу — розробка від 2 тижнів | Шершень
**H1**: Який AI-асистент потрібен вашому бізнесу?

### 6.3 AI Implementation Page

| Target Keyword | Volume | Difficulty | Intent |
|---|---|---|---|
| впровадження ai в бізнес | Low-Med | Low | Commercial |
| автоматизація бізнес-процесів ai | Low | Low | Commercial |
| ai консалтинг україна | Low | Low | Commercial |
| впровадження штучного інтелекту | Low-Med | Low | Informational |

**Title**: Впровадження AI у бізнес: аудит → стратегія → результат за 30 днів | Шершень
**H1**: Як впровадити AI у ваш бізнес без ризику і зайвих витрат?

### 6.4 SEO Content Page

| Target Keyword | Volume | Difficulty | Intent |
|---|---|---|---|
| seo контент | Medium | Medium | Commercial |
| написання seo статей | Medium | Medium | Commercial |
| ai для seo | Low-Med | Low | Informational |
| контент для сайту замовити | Medium | Medium | Transactional |
| seo копірайтинг | Medium | Medium | Commercial |

**Title**: SEO-контент з AI: 30 статей за 7 днів, унікальність від 95% | Шершень
**H1**: Скільки SEO-статей потрібно вашому бізнесу щоб вийти в топ?

### 6.5 Pricing Page

| Target Keyword | Volume | Difficulty | Intent |
|---|---|---|---|
| вартість розробки чат-бота | Medium | Low | Transactional |
| ціна ai рішення | Low | Low | Transactional |
| скільки коштує чат-бот | Medium | Low | Transactional |
| seo статті ціна | Medium | Low | Transactional |

**Title**: Ціни на AI-рішення для бізнесу — від $500 | Шершень
**H1**: Скільки коштує AI для вашого бізнесу? Прозорі ціни без сюрпризів

### 6.6 Blog Posts — First 10 Keyword Targets

| # | Article | Primary Keyword | Secondary Keywords |
|---|---|---|---|
| 1 | Як створити чат-бота для бізнесу | чат-бот для бізнесу | створити чат-бот, бот для продажів |
| 2 | Впровадження AI: з чого почати | впровадження ai в бізнес | ai для компанії, з чого почати ai |
| 3 | Скільки коштує чат-бот в Україні 2026 | розробка чат-бота ціна | вартість чат-бота, бот ціна |
| 4 | AI для SEO: контент що ранкується | ai для seo | ai seo оптимізація, ai контент |
| 5 | Telegram бот для бізнесу: 10 прикладів | telegram бот для бізнесу | telegram бот, бот телеграм |
| 6 | AI для малого бізнесу: 7 кейсів | ai малий бізнес | ai для підприємців, ai smb |
| 7 | GPT vs Claude vs Gemini для бізнесу | gpt vs claude | порівняння ai, який ai обрати |
| 8 | Автоматизація підтримки з AI | автоматизація підтримки ai | ai підтримка клієнтів |
| 9 | ROI від впровадження AI | roi ai впровадження | окупність ai, ai економія |
| 10 | AI тренди 2026 | ai тренди 2026 | штучний інтелект 2026 |

---

## 7. CONVERSION FUNNELS

### 7.1 Primary Funnel: Awareness → Pilot

```
AWARENESS                    CONSIDERATION                 DECISION
─────────────────           ──────────────────           ─────────────────
Blog post (SEO)             Service page                 Pricing page
Social media post    →      Case study           →       Free pilot form
Telegram channel            FAQ                          Calendly booking
Google Ads landing          ROI Calculator               Telegram DM
                            Lead magnet PDF

Entry points:               Engagement signals:           Conversion points:
- Organic search            - 2+ page visits             - Form submission
- Social referral           - >2 min on site             - Calendly booking
- Direct/brand              - Pricing page view          - Telegram message
- Paid ads                  - Case study read            - Phone call
```

### 7.2 Funnel by Page Role

| Page | Funnel Stage | Primary CTA | Secondary CTA |
|---|---|---|---|
| Homepage | Awareness → Consideration | "Безкоштовний 7-денний пілот" | "Наші послуги" |
| Blog posts | Awareness | "Завантажити чек-лист" (lead magnet) | "Детальніше про послугу" (service link) |
| Service pages | Consideration | "Отримати пілот" | "Подивитись ціни" |
| Case studies | Consideration → Decision | "Хочу такий результат" | "Подивитись ціни" |
| Pricing | Decision | "Обрати пакет" (→ form) | "Запитати знижку" (Telegram) |
| FAQ | Consideration | "Залишились питання? Напишіть нам" | Service links |
| Contact | Decision | Form submission | Telegram / Phone |

### 7.3 CTA Hierarchy (every page)

1. **Primary CTA** (amber button): "Безкоштовний 7-денний пілот" or service-specific variant
2. **Secondary CTA** (outline button): Contextual next step
3. **Tertiary CTA** (text link): "Написати в Telegram" or phone number
4. **Exit-intent popup**: Lead magnet download (fires once per session, after 30s+ on site)

### 7.4 Lead Magnet Funnel

```
Blog post → CTA banner in article → Email form → PDF delivery →
→ Email nurture (3 emails over 7 days) → Service page → Pilot request
```

Lead magnets by funnel stage:
- **Awareness**: "5 способів як AI економить бізнесу $10K/міс" (PDF)
- **Consideration**: "Чек-лист: чи готовий ваш бізнес до AI" (interactive/PDF)
- **Decision**: "ROI калькулятор AI-впровадження" (interactive tool)

### 7.5 Retargeting Touchpoints

| Trigger | Action |
|---|---|
| Visited pricing page, no conversion | Retarget with case study ad |
| Downloaded lead magnet | Email sequence → pilot offer |
| Visited 3+ pages | Telegram bot retarget suggestion |
| Started form, abandoned | Exit-intent: "Забронюйте дзвінок за 30 сек" |

---

## 8. TECHNICAL REQUIREMENTS

### 8.1 CMS Recommendation

**Recommended: Astro (SSG) + Decap CMS (headless)**

| Requirement | Why Astro |
|---|---|
| Speed | Static-first, 0 JS by default → LCP < 1.5s |
| SEO | Full control over meta, schema, sitemap generation |
| Blog | Markdown/MDX content collections, built-in |
| Low overhead | No database, no server runtime |
| Team skill | HTML/CSS/JS team can learn in days |
| Cost | $0 hosting on Vercel/Netlify/Cloudflare |

**Alternative options:**

| Option | Pros | Cons | Best for |
|---|---|---|---|
| **Astro + Decap CMS** (recommended) | Fastest, free, SEO-perfect | Non-tech team needs CMS training | Dev-led small team |
| **Next.js** | React ecosystem, ISR | Overkill for brochure site | If future app features planned |
| **WordPress + GeneratePress** | Easy for non-devs, plugins | Speed issues, security surface | Content-first team, no devs |
| **Webflow** | Visual builder, CMS built-in | $29+/mo, vendor lock-in, UA localization limits | Designer-led team |

### 8.2 Hosting

| Component | Recommendation | Cost |
|---|---|---|
| **Hosting** | Vercel (primary) or Cloudflare Pages | Free tier |
| **Domain** | `shershen.ai` via Namecheap/Cloudflare | ~$70/year |
| **SSL** | Auto via Vercel/Cloudflare | Free |
| **CDN** | Built into Vercel/Cloudflare | Free |
| **Email** | Google Workspace or Zoho Mail | $0-6/mo |
| **Form backend** | Formspree (free 50/mo) → Telegram Bot API | Free |
| **Analytics** | GA4 + Google Search Console + Clarity | Free |
| **Email marketing** | MailerLite (free up to 1000 subscribers) | Free |

**Total cost: ~$6-12/month** (domain amortized)

### 8.3 Performance Targets

| Metric | Target | Tool |
|---|---|---|
| Lighthouse Performance | > 95 | Chrome DevTools |
| LCP | < 2.0s (mobile) | PageSpeed Insights |
| FID/INP | < 100ms | PageSpeed Insights |
| CLS | < 0.05 | PageSpeed Insights |
| TTFB | < 200ms | WebPageTest |
| Total page weight | < 500KB (initial load) | DevTools |
| Time to Interactive | < 3s (3G) | Lighthouse |

### 8.4 Technical SEO Checklist

- [ ] Auto-generated `sitemap.xml` (updated on build)
- [ ] `robots.txt` with sitemap reference
- [ ] Canonical URLs on every page
- [ ] hreflang tags (if EN version planned)
- [ ] JSON-LD: Organization (all pages), FAQPage, Service, Article (blog), BreadcrumbList
- [ ] Open Graph + Twitter Card meta on every page
- [ ] Responsive images: WebP + srcset + lazy loading
- [ ] Preload critical fonts (Inter 400, 700, 800)
- [ ] `font-display: swap` for all web fonts
- [ ] Breadcrumb component with schema
- [ ] 301 redirects from old URLs if any
- [ ] Custom 404 page with navigation and search

### 8.5 Analytics Events (GTM)

| Event | Trigger | Priority |
|---|---|---|
| `pilot_form_submit` | 7-day pilot form submission | Critical |
| `cta_click_hero` | Hero CTA click | High |
| `cta_click_service` | Service page CTA click | High |
| `telegram_click` | Telegram link click | High |
| `phone_click` | Phone number click | High |
| `calendly_booking` | Calendly embed interaction | High |
| `pricing_view` | Pricing page load | Medium |
| `case_view` | Case study page load | Medium |
| `lead_magnet_download` | PDF download | Medium |
| `faq_interaction` | FAQ accordion open | Low |
| `scroll_50` | 50% scroll depth | Low |
| `scroll_100` | 100% scroll depth | Low |

---

## 9. PHASE PLAN

### Phase 1: MVP Launch (Weeks 1-2)

**Goal**: Live site that generates first leads.

| Task | Pages/Deliverables | Hours |
|---|---|---|
| Homepage | Full landing with hero, trust bar, services preview, FAQ, CTA | 12-16h |
| Contact page | Form (Formspree → Telegram), Calendly embed, phone, map | 4-6h |
| Pricing page | 3 packages per service, comparison table, CTA | 6-8h |
| Technical setup | Domain, hosting, SSL, GA4, GSC, GTM, sitemap, robots.txt, 404, privacy | 6-8h |
| Design system | Components: buttons, cards, forms, nav, footer, mobile menu | 8-10h |
| **Phase 1 Total** | **4 pages + infrastructure** | **~36-48h** |

**Launch checklist:**
- [ ] Real phone number, real email
- [ ] Form sends to Telegram and email
- [ ] Favicon + OG image
- [ ] Mobile tested on 3 devices
- [ ] PageSpeed > 90
- [ ] GA4 + GSC connected
- [ ] Submit sitemap to Google

### Phase 2: Services + Social Proof (Weeks 3-5)

**Goal**: Complete service pages, start building trust.

| Task | Pages/Deliverables | Hours |
|---|---|---|
| 3 Service pages | AI-assistants, AI Implementation, SEO Content | 12-16h |
| Services hub | `/poslugy/` overview page | 3-4h |
| About page | Team, story, values, "wartime innovation" narrative | 4-6h |
| Case studies | Template + 3 initial cases (can be anonymized) | 8-12h |
| Testimonials | Collect 3-5 real testimonials with photos | 2-3h (design) |
| Trust bar | Client logos section | 2h |
| FAQ page | Extended FAQ with schema markup | 3-4h |
| Lead magnet #1 | PDF: "5 способів як AI економить бізнесу" + landing | 6-8h |
| **Phase 2 Total** | **~8 pages + assets** | **~40-53h** |

### Phase 3: Content Engine + Scale (Weeks 6-12)

**Goal**: Organic traffic machine, lead nurturing.

| Task | Pages/Deliverables | Hours |
|---|---|---|
| Blog template | Post layout, category pages, related posts | 6-8h |
| First 10 blog posts | Per keyword map above (2/week) | 20-30h |
| Email nurture | 3-email sequence for lead magnet subscribers | 4-6h |
| ROI Calculator | Interactive tool with email gate for full report | 8-12h |
| AI Readiness Quiz | 5-question assessment with result email | 6-8h |
| Exit-intent popup | Lead magnet offer on exit | 2-3h |
| Cookie banner | GDPR-compliant consent | 2h |
| A/B testing setup | Google Optimize or Vercel flags | 3-4h |
| **Phase 3 Total** | **10 blog posts + tools + optimization** | **~51-73h** |

### Phase 4: Growth (Month 4+)

- Industry-specific landing pages (`/galuzevi-rishennya/`)
- Guest posting + backlink campaign
- Video content (case study walkthroughs)
- Chatbot on website (eating own dog food)
- English version of key pages (if targeting international)
- Advanced analytics: heatmaps, session recordings (Clarity)

---

## 10. CONTENT PRODUCTION PRIORITIES

### Week-by-week for first 8 weeks:

| Week | Content to Produce | SEO Action |
|---|---|---|
| 1 | Homepage copy, pricing copy | Submit sitemap, set up GSC |
| 2 | Contact page, privacy policy, 404 | Index core pages |
| 3 | AI-assistants service page | Internal linking setup |
| 4 | SEO content service page + AI implementation page | Schema markup audit |
| 5 | 3 case studies + about page + FAQ | Submit to business directories |
| 6 | Blog post #1 + #2 (highest volume keywords) | Start link building outreach |
| 7 | Blog post #3 + #4 + lead magnet PDF | Set up email capture |
| 8 | Blog post #5 + #6 | First A/B test on homepage CTA |

---

## 11. KEY METRICS & MILESTONES

| Milestone | Target Date | KPI |
|---|---|---|
| Site live (MVP) | Week 2 | 4 pages, PageSpeed > 90 |
| First lead from site | Week 3 | 1 form submission |
| All service pages live | Week 5 | 8+ pages indexed |
| First organic keyword ranking | Week 8 | Top 50 for 3+ keywords |
| 15 leads/month from site | Month 3 | Form + Telegram + Calendly |
| 500 organic visits/month | Month 3 | GSC data |
| 2000 organic visits/month | Month 6 | GSC data |
| 40 leads/month | Month 6 | CRM data |

---

## 12. FINAL NOTES

### What to NOT build (common waste for small teams):

- Multi-language support (until 2000+ visits/mo in UA)
- Complex CRM integration (use Telegram + Google Sheets first)
- Chat widget (until you have capacity to respond in < 5 min)
- Newsletter before you have 100+ subscribers
- Video production before written content proves what topics convert
- Industry pages before you have 2+ case studies per industry

### The one thing that matters most:

The **Pricing page** and **Service pages** must answer the question from the CMO audit: "Скільки годин це зекономить?" Every section, every headline, every CTA should connect to time saved, money saved, or revenue gained. Not features. Not technology. Results.
