# RESTAURANT TWELVE — FULL PROJECT BRIEF
> Paste this entire document into your Claude Project Instructions. This gives Claude Code full context to build the website without re-explaining anything.

---

## 1. WHO I AM

- **Name:** Jerry Tan
- **Restaurant:** Restaurant Twelve
- **Location:** 12 Lorong 28 Geylang, Singapore 398417, Level 2 (residential landed terrace)
- **Concept:** Private dining, French fusion, 6-course tasting menu
- **Capacity:** 1–12 pax (the name comes from the unit number 12 and max 12 guests)
- **Sessions:** Friday & Saturday only (for now)
- **Price:** $130/pax (no GST, no service charge)
- **Training:** Le Cordon Bleu Paris — cuisine and pastry
- **WhatsApp:** +65 80291230
- **Instagram:** @restaurant.twelve
- **Signature:** Everything handmade — bread, pasta, sauces, all from scratch
- **Special detail:** My grandma grows the herbs used in the restaurant 🌿

---

## 2. TECH STACK

- **Framework:** Next.js
- **Hosting:** Vercel (free tier)
- **Database:** Supabase (form submissions)
- **No payment gateway** — I follow up manually via WhatsApp after form submission
- **No booking system** — interest/waitlist form only

---

## 3. BRAND & DESIGN

### Colour Palette
| Role | Colour | Hex |
|---|---|---|
| Base / background | Deep Navy | `#0B1F3B` |
| Accents, headings, lines | Muted Gold | `#C8A24A` |
| CTA button ONLY ("Request a Table") | Burnt Sienna | `#C4622D` |
| Body text on dark, light sections | Warm Off-White | `#F7F5F0` |

> **Important:** Burnt Sienna is ONLY used on the "Request a Table" button. Nowhere else.

### Typography
- **Headings:** Cormorant Garamond (serif, elegant)
- **Body:** Montserrat (sans-serif, clean)

### Logo
- **Logo A (horizontal wordmark):** "tWΞLVΣ" in a line — use in navbar, fixed top left every page, links back to Home
- **Logo B (radial):** Letters arranged in circular/star formation — use as hero centrepiece, favicon
- Logo designed by **Fable** (credit in footer)
- Files: `Logo_1_White_transparent.png` (white text, transparent bg) and `Logo_1_Black_transparent.png` (black text, transparent bg)
- Use white logo on dark/navy backgrounds, black logo on light/off-white backgrounds

### Scroll Style
- **Atomix-style:** Fixed background photo, content scrolls over it
- Background image stays locked/frozen fullscreen
- Text panels slide up over the image as user scrolls
- Smooth, cinematic, luxury feel
- Dark overlay (~40% opacity) on background photos so text is readable

### General Design Direction
- Dark navy base throughout most pages
- Off-white sections to break up the navy (not everything dark)
- Lots of breathing room — generous spacing, nothing cluttered
- Subtle gold lines and dividers
- No flashy animations — smooth elegant fades only
- Very minimal text — let photos do the talking
- Mobile-first (most guests will view on phone)

---

## 4. SITE STRUCTURE

### Pages to build now: 1, 2, 4
### Pages on hold: 3, 5, 6

---

### PAGE 1 — HOME

**Section 1: Hero**
- Full screen background: `IMG_4986.jpeg` (Jerry plating gnocchi, dark moody)
- Centre: Logo B (radial) as hero centrepiece
- Tagline: **"Where every detail is made by hand"**
- Supporting line (small): *"From the bread to the sauces"*
- CTA button (Burnt Sienna): **"Request a Table"** → links to Page 4
- Fixed background, text fades in on load

**Section 2: Menu Teaser**
- Off-white background section
- Heading: *"A glimpse into the menu. The rest — you'll discover at the table."*
- Show 3 dishes with short descriptions:

**Canapé**
Photo: `IMG_8369.jpeg`
*"A collection of handcrafted bites to begin. Small in size. Considered in every detail."*

**Spaghetti Vongolé**
Photo: `IMG_7852.jpeg`
*"Handmade pasta, clams, white wine, parsley. Every strand pulled by hand. Every clam chosen that morning."*

**Pork, Layered Potato, Red Wine Jus**
Photo: `IMG_7848.jpeg`
*"Seared pork, mille-feuille potato, zucchini, red wine reduction. Three days of preparation. One perfect plate."*

**Section 3: Gallery**
- Dark navy background
- Grid of food photos
- Photos to use: `IMG_7848.jpeg`, `IMG_7852.jpeg`, `IMG_8369.jpeg`, `IMG_0402.jpeg`, `IMG_1033.jpeg`

---

### PAGE 2 — OUR STORY

**Section 1: About Chef Jerry**
- Fixed background: `IMG_7845.jpeg` (Jerry plating 12 plates, copper lamps)
- Dark overlay on photo
- Scroll panels over the image:

**Copy:**
> Chef Jerry Tan
>
> Born and raised in Singapore, Jerry's obsession with food led him to Le Cordon Bleu Paris — where he spent a year immersed in French cuisine and pastry at one of the world's most prestigious culinary schools.
>
> Inspired by the precision and artistry of fine dining, he brought that philosophy home — but made it his own. At Restaurant Twelve, everything that reaches your table is made by hand. The bread. The pasta. The sauces. Every element crafted from scratch, because that's the only way Jerry knows how to cook.
>
> Twelve seats. One chef. Nothing outsourced.

**Section 2: Experience & Philosophy**
- Dark navy section
- What guests can expect:
  - 6-course French fusion tasting menu
  - Intimate private dining, 1–12 guests only
  - Friday & Saturday sessions
  - Everything handmade from scratch
  - Occasionally: Pizza Week (fun seasonal concept)

**Section 3: Ingredients Story**
- Two scroll panels with fixed backgrounds:

**Panel A — Tomatoes**
Background: `IMG_0402.jpeg` (heirloom tomatoes in bowl, colourful)
Gold text over dark overlay:
*"Seasonal ingredients, sourced with intention."*

**Panel B — Herbs**
Background: `IMG_1033.jpeg` (fresh basil and rosemary on marble)
Gold text over dark overlay:
*"The herbs on your plate were grown by hand — by the person who taught me that food is love."*
> (This refers to Jerry's grandma who grows the herbs — don't over-explain, just the one line)

---

### PAGE 4 — RESERVATION

- **Background colour:** Off-white `#F7F5F0` (completely different feel from other pages)
- **Text colour:** Navy `#0B1F3B`
- **Accents:** Gold `#C8A24A`
- **Submit button:** Burnt Sienna `#C4622D`

**Top half — Menu Overview**
Display clearly:
- 6-course tasting menu
- $130/pax (no GST & service charge)
- Timing: 5:30pm – 8:30pm
- Location: 12 Lor 28 Geylang, Level 2
- Courses: Canapé · Soup & Bread · Starter · Main · Pasta · Dessert

**Bottom half — Interest Form**
Form fields (submissions go to Supabase):
1. Contact Name
2. WhatsApp Number
3. Email
4. Desired reservation time (6:30pm / 7:00pm)
5. Number of guests (1–12)
6. Dietary preferences / restrictions
7. Occasion (Birthday, Anniversary, Celebration, Others)
8. Special requests
9. Checkbox: "I have read and agree to the Terms & Conditions"
10. Submit button → saves to Supabase, Jerry follows up on WhatsApp

**T&Cs section (collapsible or below form):**
- 50% deposit required to secure reservation
- Cancellations 3+ days ahead: full refund
- Cancellations within 3 days: refund only if slot is filled
- No-shows or 15+ mins late may forfeit deposit (unless prior arrangement)
- Children under 12 not catered to; under 7 not permitted
- Alcohol not served on-site
- Arrive 10 minutes early
- Outside food not permitted
- Smart casual dress code required
- Dietary constraints must be communicated during booking — no last-minute changes
- Pets not allowed
- Right to refuse service to disruptive guests
- In rare overbooking cases: will contact and offer alternatives

---

### PAGE 3 — CONNECT (on hold)
Will have: Reserve / Events / Collabs buttons at top, credits at bottom

### PAGE 5 — EVENTS (on hold)
Private events enquiry form

### PAGE 6 — COLLABS (on hold)
Brand collaboration enquiry form

---

## 5. NAVIGATION

- **Logo A (horizontal, white)** fixed top left every page — clicks back to Home (Page 1)
- Nav links: Home · Our Story · Reserve
- On mobile: hamburger menu
- Nav background: transparent over hero, solid navy when scrolled

---

## 6. FOOTER

Every page footer includes:
- WhatsApp: +65 80291230
- Instagram: @restaurant.twelve
- Logo by [Fable](https://fable.design) ← confirm exact URL
- Supported by [Unicorn.sg](https://unicorn.sg) (Jerry's father's company)
- © Restaurant Twelve

---

## 7. PHOTO FILES

All photos go in `/public/images/` folder in the Next.js project:

| Filename | Used in |
|---|---|
| `IMG_4986.jpeg` | Hero background (Page 1) |
| `IMG_7845.jpeg` | About section background (Page 2) |
| `IMG_8369.jpeg` | Canapé menu teaser + Gallery |
| `IMG_7852.jpeg` | Vongolé menu teaser + Gallery |
| `IMG_7848.jpeg` | Pork menu teaser + Gallery |
| `IMG_0402.jpeg` | Tomatoes ingredients panel (Page 2) |
| `IMG_1033.jpeg` | Herbs ingredients panel (Page 2) |
| `Logo_1_White_transparent.png` | Navbar (on dark bg), hero |
| `Logo_1_Black_transparent.png` | Light sections, Page 4 |

---

## 8. SUPABASE SETUP

Create a table called `reservations` with these columns:
- `id` (uuid, primary key)
- `created_at` (timestamp)
- `contact_name` (text)
- `whatsapp` (text)
- `email` (text)
- `reservation_time` (text)
- `num_guests` (int)
- `dietary` (text)
- `occasion` (text)
- `special_requests` (text)
- `agreed_to_tnc` (boolean)

---

## 9. KEY COPY LINES (do not change these)

- **Hero tagline:** "Where every detail is made by hand"
- **Hero subline:** "From the bread to the sauces"
- **Menu teaser intro:** "A glimpse into the menu. The rest — you'll discover at the table."
- **Grandma herb line:** "The herbs on your plate were grown by hand — by the person who taught me that food is love."
- **About closing line:** "Twelve seats. One chef. Nothing outsourced."
- **Tomatoes line:** "Seasonal ingredients, sourced with intention."

---

## 10. WHAT NOT TO DO

- Do NOT use Burnt Sienna anywhere except the "Request a Table" button
- Do NOT show full menu or prices anywhere except Page 4
- Do NOT use too many words — less is more, luxury = space
- Do NOT use bright/garish animations — subtle fades only
- Do NOT rotate or crop photos differently from how they were taken
- Do NOT add stock photos — only the 7 photos provided
- Do NOT change the copy lines listed in Section 9

---

*Built by Jerry Tan. Logo by Fable. Supported by Unicorn.sg.*
