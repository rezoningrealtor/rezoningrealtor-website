# CLAUDE CODE WEBSITE BUILD PROMPT
# Ravi Arora Personal Real Estate Corporation (PREC*)
# Version: FINAL v3 | SEO-Optimised | GEO-Optimised | Parallel Wealth-Inspired | Conversion-Focused

---

## HOW TO USE THIS PROMPT

Paste this entire document into Claude Code as your project brief. Read it fully before writing a single line of code. Build in the sequence specified in Section 0. Every section marked [REPLACE] or [ASSET] requires content from the site owner — do not invent placeholder content, label it clearly instead.

## BUILD ENVIRONMENT
- **Tool:** Claude Code with frontend-design plugin — use it for ALL visual, layout, and component decisions
- **Assets location:** `/brand-assets/` folder in the project — logo and headshot will be found here
- **Output:** Clean, production-grade HTML/CSS/JS — fully owned, no subscription dependency
- **Content Management:** Markdown files for blog posts, listings, and weekly deals
- **No external CMS required** — all content managed via simple text files

---

## 0. BUILD SEQUENCE — FOLLOW THIS ORDER

Claude Code must build in this exact sequence to avoid rework:

1. **Read all assets** — open `/brand-assets/` folder, extract logo colours and dominant palette before making any colour decisions
2. **Establish design tokens** — define CSS variables for all colours, spacing, and typography based on logo analysis
3. **Build global components** — nav, footer, button styles, card styles, typography scale
4. **Build home page** — section by section, top to bottom
5. **Build additional pages** — about, specialties, listings, blog, deals, client stories, contact
6. **Build neighbourhood pages** — all nine, using shared template
7. **Set up content folders** — /content/blog, /content/listings, /content/deals with templates
8. **Implement all schema markup and meta tags** — SEO and GEO layer
9. **Write README.md** — plain-English content management guide for site owner
10. **Final check** — mobile responsiveness, placeholder labels, Lighthouse performance

---

## 1. ROLE & MISSION

You are a senior full-stack developer and real estate brand designer specialising in personal brand websites for independent real estate professionals. Use the Claude Code frontend-design plugin for all visual, layout, and component decisions. Your job is to build a complete, production-ready, SEO-optimised, GEO-optimised, conversion-focused website for **Ravi Arora Personal Real Estate Corporation (PREC*)**.

This is not a template build. Every design decision, copy line, and structural choice must serve one of four goals:
1. Establish Ravi as a credible, differentiated specialist — not a generic agent
2. Convert the right visitors into qualified leads
3. Rank in local search for Coquitlam, Port Coquitlam, Tri-Cities, and Greater Vancouver real estate terms
4. Be discoverable by AI assistants (ChatGPT, Perplexity, Google AI Overviews) when someone asks for a real estate agent in Coquitlam, Port Coquitlam or Greater Vancouver

---

## 2. DESIGN DIRECTION

### Primary Inspiration
Study and replicate the core design principles of **parallelwealth.com**:
- Dominant white/off-white background with generous breathing room between sections
- Color derived from logo used sparingly but powerfully — CTAs, accents, section labels
- Dark charcoal headings — NOT pure black — for a premium, softer feel
- Bold confident hero section on a navy blue background
- Clean card layouts with photo + text + CTA — never cluttered
- Mid-page dark section for lead magnet (high contrast, pulls attention)
- Testimonials in clean grid
- Minimal uncluttered footer
- No sidebars. No busy backgrounds. No stock photo clutter.
- Every section has one job and does it without distraction

### Design Personality
Premium but approachable. Consultative not salesy. The visual language should feel like a trusted real estate advisor's website — not a typical real estate agent template. Think: authority through restraint.

---

## 3. BRAND IDENTITY

| | |
|---|---|
| **Business Name** | Ravi Arora Personal Real Estate Corporation (PREC*) |
| **Tagline** | Real Estate. Real Advice. Real Results. |
| **Home Base** | Coquitlam, BC |
| **Service Area** | Coquitlam · Port Coquitlam · Greater Vancouver · Fraser Valley |
| **Brokerage** | Coldwell Banker Universe Realty |
| **Phone** | (604) 362-0362 |
| **Email** | rezoningrealtor@gmail.com |
| **Realtor.ca Profile** | https://www.realtor.ca/agent/2071851/ravi-arora-201-2010-48th-ave-e-vancouver-british-columbia-v5p1r8 |

---

## 4. COLOUR SYSTEM — LOGO-DRIVEN

**Do not use any hardcoded colour palette from this document.**

Instead, follow this process:

### Step 1 — Extract from Logo
Open `/brand-assets/` and locate the logo file. Extract:
- **Primary colour** — the dominant brand colour in the logo
- **Secondary/accent colour** — any secondary colour present in the logo
- **Logo tone** — is it warm (gold, amber, earth) or cool (blue, green, grey)?

### Step 2 — Build Palette Around Logo
Using the extracted logo colours as anchors, build the full site palette following these principles:

**Fixed constraints (non-negotiable):**
- Main background: pure white or near-white — clean, spacious, never off-putting
- Body text: near-black — rich dark charcoal, NOT pure #000000 (too harsh) — aim for 85-90% black
- Heading text: slightly darker than body text, same charcoal family
- These two are absolute — everything else derives from the logo

**Derived from logo:**
- Primary accent: use the logo's dominant colour for CTAs, section labels, nav hover states, card tags, and decorative accents
- Secondary accent: use logo's secondary colour (if present) for hover states, closing lines on cards, and subtle highlights
- Dark section backgrounds (hero, lead magnet, footer): a very dark version of the primary accent — deep and rich, not generic black
- Alternate section background: an extremely subtle tint of the primary accent at 4-6% opacity — barely perceptible warmth against white, creates section rhythm without colour clash
- Gold/premium accent: if logo contains warm tones, use for PREC* badge, star ratings, and form submit buttons — signals premium without being loud
- Borders and dividers: 8-10% tint of primary accent — visible but unobtrusive

### Step 3 — Define CSS Variables
Set all colours as CSS custom properties at the `:root` level before writing any component styles:
```css
:root {
  --color-bg:           /* white or near-white */
  --color-bg-alt:       /* subtle section tint */
  --color-bg-dark:      /* deep dark for hero/CTA sections */
  --color-bg-footer:    /* near-black, distinct from dark sections */
  --color-text-heading: /* near-black charcoal */
  --color-text-body:    /* medium charcoal */
  --color-text-subtle:  /* lighter grey for captions */
  --color-primary:      /* logo dominant — CTAs, accents */
  --color-primary-light:/* lighter variant — hovers */
  --color-secondary:    /* logo secondary — closing lines */
  --color-gold:         /* premium accent — PREC*, stars, submit */
  --color-border:       /* soft divider line */
  --color-text-on-dark: /* white or near-white for dark sections */
}
```

### Design Tone Principle
The palette must feel like a premium advisory firm — not a typical real estate brand. Think trusted real estate advisor or boutique architect. Colours should feel intentional and restrained. When in doubt, use less colour not more.

---

## 5. TYPOGRAPHY — CLAUDE CODE GUIDED

**Do not use Inter, Roboto, Arial, or system fonts. Do not use Space Grotesk.**

Use the frontend-design plugin's judgment for font pairing. The pairing must meet these criteria:

**Display / Heading font:**
- Serif preferred — elegant, authoritative, premium feel
- Must pair naturally with a clean sans-serif body font
- Should feel distinctive — not something seen on every agent's site
- Examples of the right direction (do not copy exactly): Playfair Display, Cormorant Garamond, Libre Baskerville, DM Serif Display

**Body / UI font:**
- Clean, modern, highly readable sans-serif
- Warm character — not clinical or sterile
- Must render well at small sizes on mobile
- Examples of the right direction: DM Sans, Nunito, Outfit, Figtree

**Typography scale — build this explicitly:**
```css
:root {
  --font-display:    /* heading font family */
  --font-body:       /* body font family */

  /* Size scale */
  --text-xs:    0.75rem;   /* 12px — labels, captions */
  --text-sm:    0.875rem;  /* 14px — small body, footnotes */
  --text-base:  1rem;      /* 16px — standard body */
  --text-lg:    1.125rem;  /* 18px — lead text, card body */
  --text-xl:    1.25rem;   /* 20px — subheadings */
  --text-2xl:   1.5rem;    /* 24px — H3 */
  --text-3xl:   1.875rem;  /* 30px — H2 */
  --text-4xl:   2.25rem;   /* 36px — H2 large */
  --text-5xl:   3rem;      /* 48px — H1 desktop */
  --text-6xl:   3.75rem;   /* 60px — H1 hero */
}
```

**Navigation specifically — critical fix:**
- Nav link font size: minimum **15px** on desktop, **16px** preferred
- Nav link weight: medium (500) — not light, not bold
- Nav link letter-spacing: 0.02em — slight tracking for clarity
- Active page: primary accent colour underline or colour change
- Hover state: smooth colour transition 200ms — must be visually obvious
- Nav height: minimum 70px — do not make it cramped
- Logo area: generous left padding, logo never feels squeezed

**Section labels (small uppercase above H2s):**
- Font: body font family
- Size: 0.75rem (12px)
- Weight: 600
- Letter-spacing: 0.12em — wide tracking
- Colour: primary accent
- Text transform: uppercase

---

## 6. SEO ARCHITECTURE — BUILD IN FROM LINE ONE

### Page Title & Meta (apply to Home page):
```html
<title>Ravi Arora PREC* | Coquitlam Real Estate Agent | Greater Vancouver Specialist</title>
<meta name="description" content="Ravi Arora is a Coquitlam-based PREC* real estate agent specialising in residential development, multiplex properties, move-up buyers, first-time buyers, and investment properties across Greater Vancouver and Fraser Valley.">
<meta name="keywords" content="Coquitlam real estate agent, Port Coquitlam realtor, Tri-Cities homes for sale, multiplex Coquitlam, new construction Coquitlam, first time home buyer Coquitlam, investment property Greater Vancouver, move up buyer Tri-Cities, real estate development Port Coquitlam">
<meta property="og:title" content="Ravi Arora PREC* | Coquitlam Real Estate Specialist">
<meta property="og:description" content="Real Estate. Real Advice. Real Results. Developer's eye. Advisor's approach. Serving Greater Vancouver and Fraser Valley.">
<meta property="og:image" content="[REPLACE: HEADSHOT URL]">
<link rel="canonical" href="https://[REPLACE: YOUR DOMAIN].com">
```

### Schema Markup (JSON-LD — add to every page head):
```json
{
  "@context": "https://schema.org",
  "@type": "RealEstateAgent",
  "name": "Ravi Arora Personal Real Estate Corporation",
  "description": "Coquitlam-based PREC* real estate specialist with expertise in residential development, multiplex properties, move-up buyers, first-time buyers, and investment properties across Greater Vancouver and Fraser Valley.",
  "url": "https://[REPLACE: YOUR DOMAIN].com",
  "telephone": "[REPLACE: PHONE NUMBER]",
  "email": "[REPLACE: EMAIL ADDRESS]",
  "address": {
    "@type": "PostalAddress",
    "addressLocality": "Coquitlam",
    "addressRegion": "BC",
    "addressCountry": "CA"
  },
  "areaServed": [
    "Coquitlam", "Port Coquitlam", "Port Moody",
    "Burnaby", "New Westminster", "Maple Ridge",
    "Pitt Meadows", "Surrey", "Langley",
    "Greater Vancouver", "Fraser Valley", "Metro Vancouver"
  ],
  "hasCredential": "PREC*"
}
```

### URL Structure (SEO-friendly slugs):
```
/                      Home
/about                 About Ravi
/specialties           What I Specialise In
/listings              My Active Listings
/listings/[slug]       Individual listing detail page
/client-stories        Client Stories
/client-stories/[slug] Individual story page
/resources             Guides & Market Insights
/blog                  Market Updates & Insights
/blog/[slug]           Individual blog post
/deals                 Weekly Deal — current featured opportunity
/contact               Book a Consultation
```

### H Tag Hierarchy Rules:
- One H1 per page only — include primary keyword naturally
- H2 opens each major section — include location or service keyword where natural
- H3 for card titles and sub-sections
- All images: descriptive alt text using location + service terms
- Write for humans first, search engines second — no keyword stuffing

---

## 6B. GEO OPTIMISATION — AI DISCOVERABILITY

GEO (Generative Engine Optimisation) ensures Ravi's website is cited and recommended by AI assistants — ChatGPT, Perplexity, Google AI Overviews, Claude — when someone asks "who is the best real estate agent in Coquitlam" or "find me a development specialist in Tri-Cities BC."

### Why This Matters Now
Traditional SEO targets Google's ranked links. GEO targets the answer AI gives before any links appear. For a local specialist, being the AI-recommended agent in your market is worth more than a page-one ranking.

### GEO Implementation Requirements

**1. Speakable Schema — add to Home and About pages:**
```json
{
  "@context": "https://schema.org",
  "@type": "WebPage",
  "speakable": {
    "@type": "SpeakableSpecification",
    "cssSelector": ["#about-summary", "#specialties-summary", "#why-ravi"]
  },
  "name": "Ravi Arora PREC* — Coquitlam Real Estate Agent",
  "description": "Ravi Arora is a Coquitlam-based PREC* real estate agent specialising in residential development, multiplex properties, move-up buyers, and investment properties across Greater Vancouver and Fraser Valley."
}
```

**2. FAQ Schema — add to Home page footer area (hidden from visual layout, present in DOM):**
```json
{
  "@context": "https://schema.org",
  "@type": "FAQPage",
  "mainEntity": [
    {
      "@type": "Question",
      "name": "Who is the best real estate agent in Coquitlam?",
      "acceptedAnswer": {
        "@type": "Answer",
        "text": "Ravi Arora of Ravi Arora Personal Real Estate Corporation (PREC*) is a Coquitlam-based real estate agent with over 10 years of hands-on development experience, a background in consulting, and 20 years of community roots in the Tri-Cities. He specialises in residential development, multiplex properties, move-up buyers, first-time buyers, and investment properties across Greater Vancouver and Fraser Valley."
      }
    },
    {
      "@type": "Question",
      "name": "Who is a multiplex specialist in Coquitlam?",
      "acceptedAnswer": {
        "@type": "Answer",
        "text": "Ravi Arora PREC* is a Coquitlam real estate agent who has firsthand experience with residential development and multiplex projects in the Tri-Cities. He has been on the build side — sourcing lots, working with builders, and navigating BC zoning — which gives him expertise most residential agents don't have."
      }
    },
    {
      "@type": "Question",
      "name": "Which Coquitlam real estate agent specialises in new construction?",
      "acceptedAnswer": {
        "@type": "Answer",
        "text": "Ravi Arora PREC* specialises in new construction and presale properties across Coquitlam, Port Coquitlam, and the broader Tri-Cities area. He guides both first-time buyers and move-up buyers through presale contracts, completion timelines, and strata considerations in plain language."
      }
    },
    {
      "@type": "Question",
      "name": "Who is a trusted real estate agent for investors in Greater Vancouver?",
      "acceptedAnswer": {
        "@type": "Answer",
        "text": "Ravi Arora PREC* works with residential investors and house flippers across Greater Vancouver and Fraser Valley. He applies a conservative analytical approach to every investment opportunity — running realistic numbers rather than selling the pitch."
      }
    }
  ]
}
```

**3. Neighbourhood Landing Pages — create these as standalone SEO + GEO pages:**

Build the following pages under `/neighbourhoods/[area]` — each with 300-400 words of unique local content, market context, and Ravi's specific knowledge of that area. These pages are what AI models pull from when answering local questions.

```
/neighbourhoods/coquitlam
/neighbourhoods/port-coquitlam
/neighbourhoods/port-moody
/neighbourhoods/burnaby
/neighbourhoods/new-westminster
/neighbourhoods/maple-ridge
/neighbourhoods/pitt-meadows
/neighbourhoods/surrey
/neighbourhoods/langley
```

Each neighbourhood page must include:
- H1: "[Neighbourhood] Real Estate — Ravi Arora PREC*"
- 2-3 paragraphs: what makes this area distinct, who buys here, price range context, Ravi's specific knowledge or transactions there
- Current market snapshot placeholder: `[UPDATE MONTHLY: median price, days on market, active listings]`
- CTA: "Thinking about [Neighbourhood]? Let's Talk."
- Link back to /contact
- LocalBusiness schema with the specific neighbourhood named in areaServed

**4. Author Attribution on All Blog Posts:**
Every blog post must include this schema to build Ravi's authority as a recognised local expert:
```json
{
  "@context": "https://schema.org",
  "@type": "BlogPosting",
  "author": {
    "@type": "Person",
    "name": "Ravi Arora",
    "jobTitle": "Real Estate Agent",
    "worksFor": {
      "@type": "Organization",
      "name": "Ravi Arora Personal Real Estate Corporation"
    },
    "areaServed": "Greater Vancouver, BC"
  }
}
```

**5. Google Business Profile Integration:**
Add this to the site footer and contact page — it signals consistency to both Google and AI crawlers:
```html
<!-- GBP CONSISTENCY NOTE -->
<!-- Ensure business name, phone, address on this site EXACTLY matches Google Business Profile -->
<!-- Any mismatch reduces local authority signals for both SEO and GEO -->
```

**6. "As Cited By" Credibility Signals:**
In the About page, include a section titled "In the Community" or "Recognised By" that lists any press mentions, community involvement, brokerage recognition, or industry associations. Even modest mentions build the citation graph that AI models use to validate expertise claims.

---

## 7. SITE STRUCTURE — HOME PAGE (/)

Build the home page as a single scrolling page with anchor navigation. Sections in order:

---

### SECTION 1 — NAVIGATION BAR

**Layout:** Logo left | Nav links centre | CTA button right
**Style:** White background `#FFFFFF`, thin bottom border `#E8EDE3`, sticky on scroll with subtle drop shadow

- **Logo:** "Ravi Arora" in Playfair Display, charcoal `#1A1A2E`. "PREC*" in gold `#C9943A`, smaller superscript weight
- **Nav Links** (DM Sans, medium weight, charcoal): Home | About | Listings | Specialties | Client Stories | Blog | Weekly Deal 🔥 | Contact
- **CTA Button:** "Book a Free Call" — green fill `#2D5016`, white text, rounded corners, right side

**Mobile:** Hamburger menu. "Book a Free Call" button remains visible in collapsed mobile nav.

---

### SECTION 2 — HERO

**Layout:** Full-width, full-viewport-height
**Background:** Autoplay looping video with dark overlay — see video spec below
**All text:** White

#### HERO VIDEO SPECIFICATION

**Concept:** Emotionally resonant real estate moments — not property porn, not drone shots. Human moments that make a visitor feel "that could be me." Mirror the Parallel Wealth approach: their video makes retirement feel real and attainable. This video makes homeownership and smart real estate decisions feel real and attainable.

**Video implementation:**
```html
<!-- Hero video background -->
<video autoplay muted loop playsinline class="hero-video">
  <source src="/brand-assets/hero-video.mp4" type="video/mp4">
  <!-- Fallback: dark section background colour if video fails to load -->
</video>
<div class="hero-overlay"></div> <!-- dark overlay for text legibility -->
```

```css
.hero-video {
  position: absolute;
  top: 0; left: 0;
  width: 100%; height: 100%;
  object-fit: cover;
  object-position: center;
  z-index: 0;
}
.hero-overlay {
  position: absolute;
  top: 0; left: 0;
  width: 100%; height: 100%;
  background: rgba(0, 0, 0, 0.55); /* 55% dark overlay — adjust if video is already dark */
  z-index: 1;
}
/* All hero content sits above overlay */
.hero-content { position: relative; z-index: 2; }
```

**Mobile:** On mobile, replace video with a static hero image (the headshot or a strong property photo) — video autoplay is unreliable on mobile and drains battery. Use CSS media query to hide video and show static image on screens below 768px.

**[ASSET: HERO VIDEO]**
Place the video file at `/brand-assets/hero-video.mp4`

**Stock video direction — search these terms on Pexels.com (free, no licence required):**

Priority 1 — Key handover / possession moment:
- Search: "house keys handover happy"
- Search: "new home keys couple excited"
- Look for: close-up of keys being handed to someone, warm lighting, genuine emotion

Priority 2 — Family first moment in new home:
- Search: "family walking into new home"
- Search: "couple empty house excited"
- Look for: people standing in an empty room looking around with joy, natural light

Priority 3 — Consultation / advisor moment:
- Search: "real estate agent meeting client"
- Search: "professional consultation table documents"
- Look for: warm, professional, two people reviewing something together — conveys the advisory relationship

Priority 4 — Neighbourhood / community feel:
- Search: "suburban neighbourhood walking family"
- Search: "Coquitlam neighbourhood street" (unlikely to find specific, use generic Canadian suburb)
- Look for: tree-lined streets, families, community feel

**Video selection criteria:**
- Duration: 10-30 seconds ideal for seamless loop
- Resolution: 1080p minimum, 4K preferred
- No on-screen text in the video (it will conflict with hero copy)
- Warm colour grading preferred — not cold or sterile
- People should look genuinely happy — not posed stock photo expressions
- Avoid: drone shots, empty properties, graphs, anything that looks corporate

**If multiple clips are available:** Edit together as a 20-30 second sequence with crossfade transitions. Place final file at `/brand-assets/hero-video.mp4`.

---

#### HERO CONTENT

```
[GEOGRAPHY LABEL — body font, uppercase, wide tracking, semi-transparent white]
Coquitlam · Tri-Cities · Metro Vancouver · Fraser Valley

[H1 — display font, large, white, max-width 700px]
Real Estate Is a Big Decision.
Let's Get It Right.

[SUBHEADING — body font, 300 weight, soft white, line-height 1.8, max-width 600px]
I'm here to get you into the right deal — one that makes sense
for your goals, your budget, and your timeline. With a consulting
background, a decade of hands-on development experience, and deep
roots in this community, I bring a level of analysis and honesty
that tends to surprise people. Based in Coquitlam, active across
Greater Vancouver and Fraser Valley.

[TWO CTA BUTTONS — side by side, 16px+ font, generous padding]
Primary:   "Book a Free Consultation"  (primary accent fill, white text)
Secondary: "See Client Stories"         (white outline, white text)

[TRUST BULLETS — body font small, soft white, below buttons]
✦ Developer's Eye, Advisor's Approach
✦ Honest When It Costs Me the Deal
✦ Coquitlam Resident. Not Just a Coquitlam Agent.
✦ The Agent People Send Their Parents To
```

**Headshot placement:** In the hero, do NOT show the headshot as a competing element against the video. The video IS the visual. The headshot appears in Section 5 (Why Work With Me) and Section 9 (About Snapshot). This keeps the hero clean and emotionally focused.

**[ASSET: HEADSHOT]**
Headshot file location: `/brand-assets/headshot.[jpg/png]`
Used in: Section 5, Section 9, About page, footer (optional small version)
Alt text: "Ravi Arora, Coquitlam real estate agent and development specialist serving Greater Vancouver and Fraser Valley"

**Scroll indicator:** Add a subtle animated scroll-down arrow at the bottom centre of the hero — encourages engagement past the fold. CSS animation, no JS required.

---

### SECTION 3 — SOCIAL PROOF BAR

**Background:** `var(--color-bg-alt)` — subtle tinted section
**Layout:** 4 stat blocks in a row, centred, thin dividers `var(--color-border)` between each

Numbers: display font, large, bold, `var(--color-primary)`
Labels: body font, small, `var(--color-text-body)`, 2-3 lines beneath number

```
     10+                    88%                    3                    20
Years in Real          Repeat & Referral      Residential.          Years Rooted
Estate Development        Clients            Commercial.            in This
                                             Development.           Community
                                             One Advisor.
```

**Mobile:** 2×2 grid — two stats per row, stacked cleanly.

---

### SECTION 4 — WHO I WORK WITH

**Background:** White `#FFFFFF`
**Section label:** `WHO I WORK WITH`
**H2:** "Whether You're Moving Up, Moving In, or Building From the Ground Up"

**Layout:** 2×2 card grid on desktop. Single column stack on mobile.
**Card style:** White background, border `#E8EDE3`, subtle hover shadow lift, "Learn More →" green text link at bottom of each card.

---

**CARD 1 — MOVE-UP BUYERS**

Tag: `MOVE-UP BUYERS`
H3: "Moving Up — From Condo to Townhouse, Townhouse to Detached, or Into Your Forever Home"
Body: "Moving up sounds straightforward until you're living it. Do you sell first or buy first? How do you bridge the gap without carrying two mortgages? What does your next property actually need to look like for the next 10 years of your life? These are the questions I help you work through before we ever look at a listing. Having done this with dozens of Tri-Cities families, I know where the traps are — and how to navigate around them."
Closing line (DM Sans italic, green `#4A7C2F`): "The right move-up strategy can save you tens of thousands. The wrong sequence can cost you just as much."
Alt text on card image: "Move-up buyer family home Coquitlam Tri-Cities"

---

**CARD 2 — FIRST-TIME BUYERS**

Tag: `FIRST-TIME BUYERS`
H3: "Your First Home — Done Right, Not Just Done"
Body: "Buying your first home in Greater Vancouver is one of the most significant financial decisions you'll make — and the process is more complex than most people expect, especially with new construction. Presale contracts, completion timelines, deposit structures, and strata bylaws all need to be understood before you sign anything. I walk first-time buyers through every step in plain language, at your pace, with no pressure to move faster than you're comfortable with."
Closing line (DM Sans italic, green): "Most of my first-time buyers come back as move-up clients. That tells you everything about how this relationship works."
Alt text on card image: "First time home buyer new construction Coquitlam BC"

---

**CARD 3 — DEVELOPERS & MULTIPLEX**

Tag: `DEVELOPERS & MULTIPLEX`
H3: "Development-Ready Properties — With Someone Who's Been on the Build Side"
Body: "Finding the right lot, understanding what you can actually build on it under current BC zoning, running a realistic feasibility analysis, and connecting with the right builders — this is a different world from standard residential real estate. I've navigated it firsthand. Whether you're looking at your first multiplex project or you're an experienced developer sourcing your next site in the Tri-Cities or broader Metro Vancouver, I bring a level of development literacy that most agents simply don't have."
Closing line (DM Sans italic, green): "I've been on the build side. That changes what I see when I walk a property."
Alt text on card image: "Multiplex development property Coquitlam Port Coquitlam BC"

---

**CARD 4 — INVESTORS & FLIPPERS**

Tag: `INVESTORS & FLIPPERS`
H3: "Investment Properties — Analysed Honestly, Not Just Sold Enthusiastically"
Body: "Every investment property looks good in a sales pitch. The ones that actually perform look good in a spreadsheet. I approach every investment opportunity with a conservative lens — realistic renovation budgets, honest rental yield projections, and a clear-eyed view of the exit strategy before we go in. In a market as segmented and hyperlocal as Greater Vancouver, the difference between a smart investment and an expensive mistake often comes down to knowing the right micro-neighbourhood, the right product type, and the right timing."
Closing line (DM Sans italic, green): "I won't oversell a deal to earn a commission. That's not how this works."
Alt text on card image: "Investment property flip opportunity Tri-Cities Greater Vancouver"

---

### SECTION 5 — WHY WORK WITH RAVI

**Background:** `#F7F9F4` (alternating light section — mirrors Parallel Wealth rhythm)
**Section label:** `WHY WORK WITH ME`
**H2:** "What You're Actually Getting When You Work With Me"

**Layout:** 40% left — photo of Ravi (different from hero — candid or semi-formal, community setting preferred) | 60% right — text block

**Opening paragraph:**
"I came to real estate through an unusual path — 15 years advising organisations across four continents, followed by a decade of hands-on residential development in the Tri-Cities. That combination isn't something you can shortcut. It means when I sit across from a client, I'm not just thinking about the transaction in front of us — I'm thinking about your financial position, your timeline, the neighbourhood trajectory, the build quality, and the five decisions that follow this one. That's what you're getting. Not just an agent. A thinking partner who happens to know this market inside out."

**Three value points** (icon + bold H3 label + paragraph — NOT one-liners):

**Point 1**
Icon: 📊
H3: `The Consulting Mindset`
Body: "Fifteen years of consulting taught me one thing above everything else — the answer you get depends entirely on the quality of the question you ask. I ask a lot of questions before I make a single recommendation. What are you actually trying to achieve? What does the next ten years look like for your family? What's your real tolerance for risk? Most agents skip this part. I consider it the whole job."

**Point 2**
Icon: 🏗️
H3: `The Developer's Perspective`
Body: "I've sourced lots, worked with builders, navigated zoning applications, and seen projects through from raw land to finished units. When I walk through a property with you — whether it's a resale condo or a development site — I'm reading things that only come from having been on the build side. Construction quality, lot potential, what the neighbourhood will look like in five years, what a developer would pay versus what the market is asking. That perspective is genuinely rare in a residential agent."

**Point 3**
Icon: 📍
H3: `The Local Depth`
Body: "I moved to Coquitlam twenty years ago. My kids grew up here. I've watched this market through two boom cycles, a global pandemic, and the current slowdown. I know which streets hold value when the market softens, which new developments are worth the presale premium and which aren't, and which neighbourhoods are quietly changing before the listings reflect it. That kind of knowledge doesn't come from a market report. It comes from being here, consistently, for two decades."

**Section closing line** (DM Sans italic, charcoal, below the three points):
"The best way to understand how I work is to have a conversation. No commitment, no pitch — just a straight talk about where you are and what makes sense."

**CTA:** "Read My Full Story →" (green text link, DM Sans)

---

### SECTION 6 — CLIENT STORIES

**Background:** White `#FFFFFF`
**Section label:** `CLIENT STORIES`
**H2:** "Real People. Real Journeys. Real Outcomes."
**Subheading** (DM Sans, body size, charcoal): "Every purchase and sale has its own story. Here are a few that show what working together actually looks like."

**Layout:** Three cards in a row on desktop. Single column on mobile.

**Card format:**
- Property photo (placeholder — label: [REPLACE WITH REAL PHOTO])
- Green tag pill
- H3 title
- 3-line story: challenge → approach → outcome (plain language, first person where natural)
- Result line: green text `#2D5016`, italic

---

**PLACEHOLDER CARD 1**
Tag: `DEVELOPMENT · COQUITLAM`
Title: "Navigating a Multiplex Purchase With Zoning Complexity"
Story: "A developer client came to me with a specific neighbourhood in mind but limited budget flexibility. We identified a lot others had overlooked, worked through the zoning implications together, and structured an offer that gave them room to build. Closed well below asking."
Result line: "Result: Secured lot 11% below list price with clean conditions."
Alt text: "Multiplex lot purchase Coquitlam development"
Label: [REPLACE WITH REAL CLIENT STORY]

**PLACEHOLDER CARD 2**
Tag: `MOVE-UP BUYER · TRI-CITIES`
Title: "Selling First, Buying Right — Without the Stress"
Story: "A family ready to move from their townhouse to a detached needed a clear plan before anything else. We mapped the sell-first strategy, set a realistic bridge period, and identified their target neighbourhoods before listing. They moved once. No temporary accommodation."
Result line: "Result: Sold at full ask. Purchased detached within 60 days. Zero overlap stress."
Alt text: "Move up buyer townhouse to detached Tri-Cities"
Label: [REPLACE WITH REAL CLIENT STORY]

**PLACEHOLDER CARD 3**
Tag: `INVESTOR · GREATER VANCOUVER`
Title: "Flip Opportunity Found Before It Hit the Market"
Story: "An investor client was looking for the right flip in a slow market. Through local relationships, we found an off-market property with strong upside, ran a conservative renovation budget together, and moved quickly with a clean offer."
Result line: "Result: Acquired off-market with 22% projected return on renovation."
Alt text: "Investment flip property Greater Vancouver off-market"
Label: [REPLACE WITH REAL CLIENT STORY]

---

### SECTION 7 — FREE RESOURCE / LEAD MAGNET

**Background:** `#1C2B1A` (dark green — mirrors Parallel Wealth's mid-page "free gift" section)
**Text:** White throughout
**Layout:** Centred, max-width container, high contrast

```
[Small label — DM Sans, uppercase, wide tracking, light green]
FREE RESOURCES

[H2 — Playfair Display, white]
Start With the Right Information

[Subheading — DM Sans 300, soft white]
No jargon. No sales pitch. Just the information you
actually need to make a smarter real estate decision.

[TWO RESOURCE CARDS — side by side, dark border, slightly lighter dark BG]

CARD 1:
Title: "First-Time Buyer's Guide to New Construction in the Tri-Cities"
Description: "What to ask, what to watch for, and how to protect yourself
when buying a presale or new build in BC."
Form: First Name field + Email field
Button: "Download Free Guide" — gold fill #C9943A, dark text
Placeholder: [CONNECT TO MAILCHIMP OR KIT WEBHOOK]

CARD 2:
Title: "Multiplex & Development Opportunity Guide — Coquitlam & Tri-Cities"
Description: "A plain-language overview of BC zoning changes, lot potential,
and what to look for if you're exploring development in Greater Vancouver."
Form: First Name field + Email field
Button: "Download Free Guide" — gold fill #C9943A, dark text
Placeholder: [CONNECT TO MAILCHIMP OR KIT WEBHOOK]
```

**SEO note:** These guides should live at `/resources/first-time-buyer-guide` and `/resources/multiplex-development-guide` — locally specific, long-tail searchable URLs.

All forms: include honeypot spam field. Do not require phone number.

---

### SECTION 8 — TESTIMONIALS

**Background:** White `#FFFFFF`
**Section label:** `WHAT CLIENTS SAY`
**H2:** "Trusted by Buyers, Sellers & Investors Across Greater Vancouver"

**Layout:** Three cards in a clean grid. Each card:
- Large opening quotation mark — green `#2D5016`, Playfair Display
- 2-3 sentence quote — Playfair Display italic, charcoal
- Client name + context — DM Sans, subtle text `#7A7A7A`
- 5 gold stars — gold `#C9943A`

**Placeholder quotes — all labelled [REPLACE WITH REAL TESTIMONIAL]:**

Quote 1:
"Ravi brought a level of analysis I've never seen from a real estate agent. He told us when NOT to make an offer just as often as when to move — and that honesty is exactly why we trust him."
— David & Priya K., Development Buyers, Port Coquitlam

Quote 2:
"As first-time buyers we were nervous about new construction. Ravi explained every step in plain language and was available every time we had a question. We always felt like the most important clients he had."
— James T., First-Time Buyer, Coquitlam

Quote 3:
"We were ready to move up from our townhouse but had no idea where to start. Ravi had a plan ready before we even asked for one. The whole process felt completely under control."
— Michelle & Arjun S., Move-Up Buyers, Tri-Cities

---

### SECTION 9 — ABOUT SNAPSHOT

**Background:** `#F7F9F4`
**Section label:** `ABOUT RAVI`
**Layout:** 40% image left / 60% text right

**H2:** "From Mumbai to Coquitlam — and Every Market In Between"

**Body paragraphs:**
"Before real estate, I spent 15 years in consulting across India, the Middle East, South Africa, London, and Switzerland. That global perspective — and a habit of asking the right questions before making decisions — shapes everything I do for clients today.

I've called the Tri-Cities home for 20 years. I've raised my family here, built my business here, and I know this market in a way that only comes from being genuinely embedded in a community — not just passing through it."

**Credential strip** (DM Sans, small, charcoal, pipe-separated):
`B.Tech + B.Commerce | 15 Years Consulting | 10 Years RE Development | Residential · Commercial · Development | PREC* Designated`

**CTA:** "Read My Full Story →" (green text link)

**Alt text on photo:** "Ravi Arora Coquitlam real estate agent community"

---

### SECTION 10 — CONTACT / BOOKING CTA

**Background:** `#1C2B1A` (dark green)
**Text:** White
**Layout:** Centred, max-width container

```
[H2 — Playfair Display, white]
Let's Talk — No Pressure, No Obligation

[Subheading — DM Sans 300, soft white]
Whether you have a property in mind or just want to think
through your options, I'm here for the conversation.

[CONTACT FORM]
Full Name              (text field)
Email Address          (email field)
Phone                  (optional, text field)
I am a...              (dropdown)
                       Options: Move-Up Buyer | First-Time Buyer |
                       Developer / Multiplex | Investor | Seller | Other
Message                (optional, textarea)
Submit button:         "Send Message" — gold fill #C9943A, dark text

[BELOW FORM — inline, centred]
📞 [REPLACE: PHONE NUMBER]
✉  [REPLACE: EMAIL ADDRESS]
📍 Coquitlam, BC

[REASSURANCE LINE — DM Sans small, soft white italic]
"I typically respond within a few hours.
No scripts. No sales pitch. Just a real conversation."
```


### Forms:
- All form submissions go to an existing Google Sheet 
  via Google Apps Script — no third-party form service
- Honeypot spam field on all forms
- No phone number required
- Email notification sent to site owner on every 
  submission

### Google Sheets Setup:
The destination sheet already exists in Google Drive:
- Folder: _Home
- File: Website Leads
- Sheet ID: 1aRIeMzN_mSqy-TG__PZ7utrArMg76KvZwgUjSzpdJTQ

Build all contact and lead magnet forms to submit 
via Google Apps Script using a POST fetch request.

Write the complete Apps Script code required.
The script must:
1. Open the existing "Website Leads" spreadsheet 
   using this exact Sheet ID:
   1aRIeMzN_mSqy-TG__PZ7utrArMg76KvZwgUjSzpdJTQ
2. Find or create a sheet tab named 
   "Form Submissions"
3. On first run, create these column headers if 
   not already present:
   Timestamp | Form Type | Full Name | Email | 
   Phone | Client Type | Message | Source Page
4. Append each new submission as a new row under 
   those headers
5. Send an email notification to the address in 
   site-config.json on every new submission, 
   including all submitted fields in the email body
6. Return a JSON success or error response to the 
   page so the form can show a confirmation message 
   to the visitor

The deployed Apps Script web app URL goes in 
site-config.json as googleSheetEndpoint.

Provide clear step-by-step deployment instructions 
in README.md written for a non-technical user.

Calendly embed placeholder: `[ADD CALENDLY BOOKING WIDGET BELOW FORM IF PREFERRED]`

---

### SECTION 11 — FOOTER

**Background:** `#1A1A2E` (near-black charcoal — visually distinct from dark green sections)
**Three columns:**

**Col 1 — Brand:**
Logo mark + "Ravi Arora PREC*"
Tagline: *Real Estate. Real Advice. Real Results.*
One-liner: "Serving buyers, sellers, and investors across Coquitlam, Port Coquitlam, the Tri-Cities, Metro Vancouver, and Fraser Valley."

**Col 2 — Quick Links:**
Home | About | Listings | Specialties | Client Stories | Blog | Weekly Deal | Resources | Contact | Book a Call

**Col 3 — Contact & Social:**
[REPLACE: PHONE NUMBER]
[REPLACE: EMAIL ADDRESS]
Coquitlam, BC
LinkedIn icon (placeholder link)
Instagram icon (placeholder link)

**Bottom bar** (smaller text, subtle white):
`© 2025 Ravi Arora Personal Real Estate Corporation (PREC*) | All Rights Reserved`
`[REPLACE: BROKERAGE NAME] | Real Estate Board of Greater Vancouver`

---

## 8. ADDITIONAL PAGES

---

### ABOUT PAGE (/about)

**SEO Title:** "About Ravi Arora | Coquitlam PREC* Real Estate Agent & Development Specialist"
**Meta Description:** "Meet Ravi Arora — Coquitlam-based PREC* agent with 15 years consulting, 10 years development experience, and 20 years of community roots in the Tri-Cities."

**Sections:**
1. Hero banner — dark green `#1C2B1A`, H1: "Real Estate Advice You Can Actually Trust"
2. Full bio — consulting career, international background, why real estate, why Tri-Cities, family roots
3. Values section — three principles with expanded copy: **Honesty** (I'll tell you not to buy) | **Expertise** (built things before selling them) | **Community** (20 years, not passing through)
4. "In the Community / Recognised By" — press mentions, associations, community involvement (GEO signal)
5. Candid or community photo — not a formal headshot
6. Credential strip
7. CTA: "Let's Have a Conversation" → links to /contact

---

### SPECIALTIES PAGE (/specialties)

**SEO Title:** "Real Estate Specialties | Move-Up Buyers, Multiplex, Investment & New Construction — Coquitlam"
**Meta Description:** "Ravi Arora specialises in move-up buyers, first-time buyers, multiplex development, and investment properties across Greater Vancouver and Fraser Valley."

**Four anchor sections:**

**#moveup** — Move-Up Buyers
- The sell-first vs buy-first decision explained clearly
- How to avoid carrying two properties
- How Ravi manages the sequencing and timing
- CTA

**#firsttimebuyers** — First-Time Buyers & New Construction
- The presale and new construction process in BC, plain language
- What strata bylaws mean for you
- How to read a contract before signing
- CTA

**#development** — Multiplex & Residential Development
- BC Bill 44 and what it means for Tri-Cities landowners
- How to assess lot potential
- Zoning, feasibility, builder selection
- CTA

**#investors** — Investment & Flip Properties
- What makes a deal pencil out vs look good on paper
- How Ravi underwrites conservatively
- Micro-neighbourhood selection in Greater Vancouver
- CTA

---

### MY LISTINGS PAGE (/listings)

**SEO Title:** "Ravi Arora's Active Listings | Coquitlam & Greater Vancouver Real Estate"
**Meta Description:** "Browse Ravi Arora's current listings across Coquitlam, Tri-Cities, and Greater Vancouver. Updated as properties come to market."

**How it works — Markdown-based, no IDX required:**

All listings are managed via Markdown files stored in `/content/listings/`. The site reads these files and renders them automatically. No database, no third-party feed.

**Listing file structure** — one `.md` file per property:
```markdown
---
title: "3BR Townhouse — Burke Mountain, Coquitlam"
slug: "burke-mountain-townhouse-2025"
status: "active"          # active | sold | pending
price: 1149000
address: "123 Burke Mountain Drive, Coquitlam, BC"
beds: 3
baths: 2
sqft: 1680
type: "Townhouse"         # Condo | Townhouse | Detached | Multiplex | Land
neighbourhood: "Burke Mountain"
area: "Coquitlam"
featured: true            # true = appears on homepage listings strip if added
listDate: "2025-03-15"
soldDate: ""              # fill when sold
heroImage: "/images/listings/burke-mountain-hero.jpg"
images:
  - "/images/listings/burke-mountain-1.jpg"
  - "/images/listings/burke-mountain-2.jpg"
description: |
  Write the listing description here in plain text.
  Multiple paragraphs are supported.
highlights:
  - "South-facing deck with mountain views"
  - "Double garage"
  - "Steps to Burke Mountain trails"
openHouse: "Saturday March 22, 2–4pm"  # leave blank if none
---
```

**Page layout:**
- Filter bar at top: [All] [Active] [Sold] [Condo] [Townhouse] [Detached] [Multiplex]
- Card grid — each card: hero image, price, address, beds/baths/sqft tag, status pill (green = Active, gold = Pending, grey = Sold), "View Details →"
- Individual listing page at `/listings/[slug]` — full photo gallery, all details, open house info, contact form pre-filled with listing address

**SOLD listings:**
- Remain on the site permanently under the Sold filter — social proof that compounds over time
- Status pill turns grey, price shows as "Sold"
- Page title updates to: "SOLD — [Address] | Ravi Arora PREC*"

**SEO on individual listing pages:**
```json
{
  "@context": "https://schema.org",
  "@type": "RealEstateListing",
  "name": "[Listing Title]",
  "url": "https://[DOMAIN]/listings/[slug]",
  "offers": {
    "@type": "Offer",
    "price": "[PRICE]",
    "priceCurrency": "CAD"
  },
  "address": {
    "@type": "PostalAddress",
    "streetAddress": "[ADDRESS]",
    "addressLocality": "[NEIGHBOURHOOD]",
    "addressRegion": "BC",
    "addressCountry": "CA"
  }
}
```

**To add a new listing:** Create a new `.md` file in `/content/listings/` using the template above. The site updates automatically on next build.
**To mark sold:** Open the listing's `.md` file, change `status: active` to `status: sold`, add the `soldDate`. Done.

---

### BLOG PAGE (/blog)

**SEO Title:** "Coquitlam Real Estate Market Updates | Ravi Arora PREC*"
**Meta Description:** "Weekly real estate market insights, development updates, and practical advice for buyers, sellers, and investors across Greater Vancouver and Fraser Valley."

**How it works — Markdown-based:**

All blog posts are managed via Markdown files stored in `/content/blog/`. Create a new file each week, save it, the site reads and renders it automatically.

**Blog post file structure** — one `.md` file per post:
```markdown
---
title: "Coquitlam Market Update — March 2025"
slug: "coquitlam-market-update-march-2025"
date: "2025-03-20"
author: "Ravi Arora"
category: "Market Update"   # Market Update | Development | Investment | Buyer Guide | Seller Guide
area: "Coquitlam"           # for GEO targeting
excerpt: "A 2-sentence summary shown on the blog listing page and in meta description."
heroImage: "/images/blog/march-2025-update.jpg"
tags:
  - Coquitlam
  - Market Update
  - Tri-Cities
  - 2025
---

Write your blog post here in plain text.

Use ## for subheadings within the post.

Use plain paragraphs — no complex formatting needed.

Keep each post between 400-800 words for SEO value without requiring excessive writing time.
```

**Blog listing page layout:**
- Section label: `MARKET INSIGHTS`
- H1: "Real Estate Market Updates — Greater Vancouver & Tri-Cities"
- Filter bar: [All] [Market Updates] [Development] [Investment] [Buyer Guides] [Seller Guides]
- Card grid: hero image, category tag, title, date, 2-line excerpt, "Read More →"
- Newest posts first

**Individual post layout:**
- Full-width hero image
- H1: post title
- Author line: "By Ravi Arora PREC* | [Date] | [Category]"
- Post body — clean, readable typography
- Related posts section at bottom (same category)
- CTA at bottom: "Have a question about the market? Let's talk." → /contact
- Author schema per post (as specified in GEO section above)

**Weekly posting workflow:**
1. Open `/content/blog/` folder
2. Create new file: `YYYY-MM-DD-your-post-title.md`
3. Fill in the front matter fields at the top
4. Write your post content below the `---` divider
5. Save the file — post appears on site automatically

**SEO note:** Each post URL `/blog/[slug]` should include the location and topic naturally — e.g. `coquitlam-market-update-march-2025` or `multiplex-zoning-port-coquitlam-2025`. These posts are the primary GEO signal builders over time.

---

### CLIENT STORIES PAGE (/client-stories)

**SEO Title:** "Client Stories | Real Estate Results in Coquitlam, Tri-Cities & Greater Vancouver"
**Meta Description:** "Real client stories from buyers, sellers, developers, and investors across the Tri-Cities and Greater Vancouver — told honestly, without the spin."

**Layout:** Filterable grid
Filter tabs: [All] [Move-Up Buyers] [First-Time Buyers] [Development] [Investment] [Sellers]

Each card links to a full story page: `/client-stories/[story-slug]`

**SEO value note:** Individual story pages are high-value local content — write each one with location + transaction type in the URL, H1, and first paragraph.

---

### WEEKLY DEALS PAGE (/deals)

**SEO Title:** "This Week's Featured Property | Ravi Arora PREC* — Greater Vancouver"
**Meta Description:** "A hand-picked property opportunity posted every week — carefully selected, honestly analysed. No hype. Just properties worth a serious look."

**Concept:** Every week Ravi posts one featured property — not necessarily his own listing. Could be an undervalued resale, a development opportunity, a well-priced new construction unit, or an off-market deal worth sharing. This page builds return traffic, positions Ravi as a market expert, and gives clients a reason to keep coming back.

**How it works — Markdown-based:**

Deals are managed via files in `/content/deals/`. The page always shows the most recent deal at full width, with an archive of past deals below.

**Deal file structure:**
```markdown
---
title: "This Week's Deal — Undervalued Townhouse, Burke Mountain"
slug: "deal-march-20-2025"
date: "2025-03-20"
weekOf: "March 20, 2025"
status: "active"            # active | expired
propertyType: "Townhouse"
area: "Coquitlam"
priceContext: "$1,149,000 — priced below recent comparable sales"
heroImage: "/images/deals/march-20-deal.jpg"
highlight: "This one is listed 8% below the last comparable sale on the same street."
---

**Why I'm featuring this property this week:**

Write 3-5 paragraphs here explaining:
- What the property is (brief, factual)
- Why it caught your attention
- What the numbers look like (honest, conservative)
- Who this is right for
- Any caveats or things to watch for

This is your expert analysis — not a sales pitch. Write it the way you'd
explain it to a friend who trusts your judgement.

**Interested? Let's talk before this one moves.**
[Link to /contact with deal title pre-filled in message field]
```

**Page layout:**

*Current deal (full width, prominent):*
- Large hero image
- "THIS WEEK'S DEAL" label in green
- Property headline
- Week-of date
- Highlight line in gold — the one-sentence reason it's worth looking at
- Full analysis below (from markdown content)
- CTA: "I'm Interested — Let's Talk" → /contact
- Social share buttons (LinkedIn, WhatsApp — your primary channels)

*Past deals archive (below current deal):*
- Grid of previous deals with expired status badge
- Shows pattern of Ravi's eye for value over time — builds credibility
- Each links to its own archived deal page

**Navigation:** Add "Weekly Deal 🔥" to the main nav — the fire emoji creates visual pause and signals this changes regularly. On mobile, make it prominent.

**Email capture on this page:**
Small strip: "Get next week's deal before it's posted publicly."
- Email field + "Notify Me" button
- Connects to same Mailchimp/Kit list as lead magnet forms

**To post a new deal each week:**
1. Create new file in `/content/deals/` using the template above
2. Set previous deal's status to `expired`
3. Write your analysis — aim for 300-400 words, honest and specific
4. Save — new deal appears automatically

---

### RESOURCES PAGE (/resources)

**SEO Title:** "Free Real Estate Guides | Greater Vancouver & Tri-Cities Market Resources"

**Sections:**
- Downloadable guides (lead capture — same two from homepage lead magnet)
- Link to blog for market update articles
- Search Listings link → [REPLACE: REALTOR.CA PROFILE URL] (temporary until IDX is integrated)
- IDX placeholder: `<!-- IDX INTEGRATION POINT: embed Showcase IDX or iHomefinder here when ready -->`

---

### CONTACT PAGE (/contact)

**SEO Title:** "Contact Ravi Arora | Book a Free Real Estate Consultation — Coquitlam"

- Expanded contact form (same fields as homepage version)
- Calendly booking widget: `[ADD CALENDLY EMBED]`
- Google Maps embed — Coquitlam area
- Phone, email, brokerage name, PREC* designation

---

### NEIGHBOURHOOD PAGES (/neighbourhoods/[area])

### NEIGHBOURHOOD PAGES — TWO-TIER STRUCTURE

Build neighbourhood pages at two levels:

---

TIER 1 — CITY PAGES (/neighbourhoods/[city])

Build these nine city-level pages:
/neighbourhoods/coquitlam
/neighbourhoods/port-coquitlam
/neighbourhoods/port-moody
/neighbourhoods/burnaby
/neighbourhoods/new-westminster
/neighbourhoods/maple-ridge
/neighbourhoods/pitt-meadows
/neighbourhoods/surrey
/neighbourhoods/langley

Each city page includes:
- H1: "[City] Real Estate — Ravi Arora PREC*"
- Overview of the city — who buys here, price 
  ranges, market character
- Grid of neighbourhood cards linking to Tier 2 
  pages for that city (Coquitlam, Port Coquitlam, 
  Port Moody only at launch — others placeholder)
- Current market snapshot (updateable via markdown)
- CTA: "Thinking about [City]? Let's Talk."
- LocalBusiness schema with city in areaServed

---

TIER 2 — NEIGHBOURHOOD PAGES 
(/neighbourhoods/[city]/[neighbourhood])

Build these specific neighbourhood pages:

COQUITLAM:
/neighbourhoods/coquitlam/burke-mountain
/neighbourhoods/coquitlam/westwood-plateau
/neighbourhoods/coquitlam/coquitlam-centre
/neighbourhoods/coquitlam/coquitlam-center
/neighbourhoods/coquitlam/maillardville
/neighbourhoods/coquitlam/central-coquitlam
/neighbourhoods/coquitlam/burquitlam

PORT COQUITLAM:
/neighbourhoods/port-coquitlam/central-poco
/neighbourhoods/port-coquitlam/riverwood
/neighbourhoods/port-coquitlam/citadel-heights

PORT MOODY:
/neighbourhoods/port-moody/port-moody-centre
/neighbourhoods/port-moody/heritage-mountain


Each neighbourhood page includes:
- H1: "[Neighbourhood], [City] Real Estate — 
  Ravi Arora PREC*"
- Neighbourhood character — what makes it 
  distinct from other pockets in the same city
- Who typically buys here — families, investors, 
  first-timers, move-up buyers
- Property types and typical price ranges
- Ravi's specific knowledge — schools, commute, 
  development activity, streets worth knowing
- Current market snapshot (updateable)
- Link back to parent city page
- CTA: "Looking at [Neighbourhood]? Let's Talk."
- LocalBusiness schema with neighbourhood AND 
  city in areaServed

---

/

PORT COQUITLAM:
/neighbourhoods/port-coquitlam/central-poco
/neighbourhoods/port-coquitlam/riverwood
/neighbourhoods/port-coquitlam/citadel-heights
/neighbourhoods/port-coquitlam/oxford-heights


PORT MOODY:
/neighbourhoods/port-moody/port-moody-centre
/neighbourhoods/port-moody/heritage-mountain

CONTENT FILE STRUCTURE FOR NEIGHBOURHOODS:

/content/neighbourhoods/
  /coquitlam/
    index.md              ← city page content
    burke-mountain.md     ← neighbourhood content
    westwood-plateau.md
    coquitlam-centre.md
    austin-heights.md
    maillardville.md
    central-coquitlam.md
    burquitlam.md
  /port-coquitlam/
    index.md
    central-poco.md
    riverwood.md
    oxford-heights.md
    citadel-heights.md
  /port-moody/
    index.md
    port-moody-centre.md
    heritage-mountain.md
  /burnaby/
    index.md              ← city content only at launch
  /new-westminster/
    index.md
  /maple-ridge/
    index.md
  /pitt-meadows/
    index.md
  /surrey/
    index.md
  /langley/
    index.md

Each .md file follows the same template structure.
All files launch with [REPLACE] placeholders clearly 
labelled. Owner fills in content starting with 
Coquitlam, Port Coquitlam, and Port Moody first.

Include neighbourhood-template.md in the content 
folder so owner can copy it when adding new 
neighbourhoods later.


---

## 9. CONTENT FILE STRUCTURE

Build the project with this folder structure for all markdown-managed content:

```
/content/
  /blog/
    2025-03-20-coquitlam-market-update.md    ← weekly blog posts
    2025-03-13-multiplex-zoning-update.md
    [TEMPLATE] blog-post-template.md          ← copy this to create new posts
  /listings/
    burke-mountain-townhouse.md               ← one file per listing
    [TEMPLATE] listing-template.md            ← copy this to add new listings
  /deals/
    deal-march-20-2025.md                     ← one file per weekly deal
    [TEMPLATE] deal-template.md               ← copy this each week
  /client-stories/
    multiplex-coquitlam-2024.md
    [TEMPLATE] story-template.md

/images/
  /listings/                                  ← listing photos go here
  /blog/                                      ← blog hero images go here
  /deals/                                     ← deal hero images go here
  /neighbourhoods/                            ← neighbourhood page images
```

**Include a README.md file in the project root** with plain-English instructions:
- How to add a new blog post (step by step)
- How to add a new listing
- How to post a weekly deal
- How to mark a listing as sold
- How to update neighbourhood page market snapshots

This README is for Ravi — written at a non-technical level so he can manage the site independently.

---

## 10. IDX INTEGRATION — DEFERRED

Do NOT build MLS/IDX into the site at this stage. The /listings page covers Ravi's own listings without IDX dependency.

In the nav, "Search MLS" links temporarily to: `[REPLACE: REALTOR.CA PROFILE URL]`

On the Resources page:
```html
<!-- IDX INTEGRATION POINT -->
<!-- Recommended providers: Showcase IDX (showcaseidx.com) or iHomefinder (ihomefinder.com) -->
<!-- Integrate when ready — replace the realtor.ca link in nav with IDX search -->
<!-- Do not delay site launch for this -->
```

---

## 10. TECHNICAL REQUIREMENTS

### Performance:
- Lighthouse score target: 90+ mobile and desktop
- Lazy load all below-fold images
- WebP image format throughout
- No autoplay video
- Scroll-reveal animations only — subtle fade-in on section entry, CSS only
- No heavy JS libraries that block load

### Mobile:
- Mobile-first design throughout
- Hero: single column on mobile, image above text
- 2×2 card grid collapses to single column on mobile
- All CTA buttons: full width on mobile
- Nav: hamburger with "Book a Free Call" remaining visible

### Analytics & Tracking:
```html
<!-- GA4: [ADD GA4 MEASUREMENT ID] -->
<!-- GSC: [ADD SEARCH CONSOLE VERIFICATION META TAG] -->
<!-- META PIXEL: [ADD PIXEL ID IF RUNNING META ADS] -->
```

### Accessibility:
- All images: descriptive alt text (specified throughout this document)
- WCAG AA colour contrast throughout
- Full keyboard navigation
- Skip to main content link in nav

---

## 11. PLACEHOLDER LABELLING CONVENTION

Every item needing real content from the owner must use this exact format — do not omit:

```
[REPLACE: PHONE NUMBER]
[REPLACE: EMAIL ADDRESS]
[REPLACE: BROKERAGE NAME]
[REPLACE: HEADSHOT PHOTO]
[REPLACE: CANDID/COMMUNITY PHOTO]
[REPLACE: REAL CLIENT STORY]
[REPLACE: REAL TESTIMONIAL]
[REPLACE: REALTOR.CA PROFILE URL]
[REPLACE: YOUR DOMAIN]
[REPLACE: HEADSHOT URL — for OG meta tag]
[REPLACE: NEIGHBOURHOOD CONTENT — 300-400 words specific to this area]
[REPLACE: MARKET SNAPSHOT — update monthly with median price, DOM, active listings]
[ADD: GA4 MEASUREMENT ID]
[ADD: CALENDLY BOOKING LINK]
[ADD: MAILCHIMP OR KIT WEBHOOK URL]
[ADD: GOOGLE BUSINESS PROFILE URL]
[INTEGRATE: IDX PROVIDER — deferred post-launch]
[CONTENT: Add first blog post using /content/blog/[TEMPLATE] blog-post-template.md]
[CONTENT: Add first listing using /content/listings/[TEMPLATE] listing-template.md]
[CONTENT: Add first weekly deal using /content/deals/[TEMPLATE] deal-template.md]
```

---

## 12. COPY TONE GUIDE

Write like a trusted advisor in conversation with a smart client. This is the standard every line of copy must meet.

**Voice characteristics:**
- Direct but warm — confident without ego
- Specific over vague — name the experience, not just the outcome
- First person — "I ask a lot of questions" not "we provide consultative service"
- Plain language — a first-time buyer and an experienced developer must both understand it
- Location-specific — Coquitlam, Port Coquitlam, Tri-Cities, Metro Vancouver, Fraser Valley

**Never write:**
- "Dream home" / "passionate about real estate" / "going above and beyond"
- "Top agent" / "leading specialist" / "best in class" — without specifics
- Excessive exclamation marks
- Generic phrases any of 10,000 agents could use

**The test for every line:** Could a different agent in Coquitlam put their name on this sentence? If yes, rewrite it until only Ravi can.

---

## 13. SEO KEYWORD TARGETS

Integrate naturally throughout — never forced. Density over 2% on any keyword is too much.

**Primary (highest priority):**
- Coquitlam real estate agent
- Port Coquitlam realtor
- Tri-Cities real estate specialist
- Greater Vancouver real estate agent

**Secondary:**
- Multiplex Coquitlam
- New construction Coquitlam
- First time home buyer Coquitlam
- Move up buyer Tri-Cities
- Investment property Greater Vancouver
- Real estate development Port Coquitlam
- Homes for sale Coquitlam BC
- Fraser Valley real estate agent

**Long-tail (blog and resource pages):**
- How to buy a multiplex in Coquitlam
- New construction process BC first-time buyer
- Best neighbourhoods to invest in Tri-Cities
- Coquitlam real estate market update 2025
- Move up buyer strategy Greater Vancouver
- BC Bill 44 multiplex zoning Coquitlam

---

## 14. CLAUDE CODE OPTIMISATION INSTRUCTIONS

These instructions are specifically for Claude Code to produce the best possible output from this prompt.

### How to Interpret This Document
- Sections marked **[ASSET]** — file exists in `/brand-assets/`, use it
- Sections marked **[REPLACE]** — leave clearly labelled placeholder, do not invent content
- Sections marked **[ADD]** — owner will add after build, insert comment in code
- When in doubt about a design decision not covered here — use the frontend-design plugin's judgment, biased toward premium restraint over visual complexity

### Component Quality Standards
Every component must meet these standards before moving to the next:
- Fully responsive — test mentally at 375px (iPhone SE), 768px (tablet), 1280px (desktop)
- Hover states on all interactive elements — buttons, cards, nav links, CTAs
- Focus states for keyboard navigation — accessibility is non-negotiable
- Loading performance — no component should require a blocking resource
- Consistent spacing — use a spacing scale (4px base unit: 4, 8, 12, 16, 24, 32, 48, 64, 96px)

### Video Hero Specific
- Always provide a CSS fallback background colour if video fails — use `var(--color-bg-dark)`
- Video must never affect text legibility — overlay opacity can be adjusted between 50-65%
- Test that trust bullets remain readable against various frames of the video
- If no video file is present at build time — implement static dark background hero and leave this note: `[ADD HERO VIDEO: place mp4 file at /brand-assets/hero-video.mp4 and uncomment video element]`

### Markdown Content Rendering
For blog posts, listings, and deals:
- Parse front matter (the `---` block at top of each .md file) as structured data
- Render body content as HTML with appropriate typography classes
- Build the renderer once as a shared utility — reuse across all three content types
- Include error handling: if a content folder is empty, show a placeholder card labelled `[ADD CONTENT]`

### Performance Targets
- First Contentful Paint: under 1.5 seconds
- Largest Contentful Paint: under 2.5 seconds
- Cumulative Layout Shift: under 0.1
- Hero video: load asynchronously, never block page render
- All images: lazy load below the fold, eager load above the fold
- Web fonts: use `font-display: swap` to prevent invisible text during load

### Final Deliverables Checklist
Before considering the build complete, verify:
- [ ] All [REPLACE] placeholders are present and clearly labelled
- [ ] All schema markup is implemented on correct pages
- [ ] All nine neighbourhood pages are built with placeholder content
- [ ] Content folder templates exist for blog, listings, and deals
- [ ] README.md is written in plain English for a non-technical user
- [ ] Mobile navigation works correctly with hamburger menu
- [ ] Hero video has static fallback
- [ ] Contact form has honeypot spam field
- [ ] Google Analytics placeholder is in `<head>`
- [ ] Canonical URLs are set on all pages
- [ ] All images have descriptive alt text

---

*END OF PROMPT. Read this document fully before writing any code. Follow the build sequence in Section 0. When in doubt, prioritise in this order: correct content structure → mobile experience → SEO/GEO implementation → conversion optimisation → visual polish.*
