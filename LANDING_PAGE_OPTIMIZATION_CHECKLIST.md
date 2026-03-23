# Sniperform USA — Landing Page Optimization Checklist
**Complete conversion optimization roadmap**

---

## PART 1: CRITICAL FIXES (Week 1)

### 🚨 TABLET RENDERING BUG
**Issue:** 2,100 sessions with zero conversions (likely tablet checkout broken)

**Testing:**
- [ ] Test checkout on iPad (iOS)
- [ ] Test checkout on Android tablet
- [ ] Check form field widths (should be 100% of viewport)
- [ ] Check CTA button sizing (min 44px height, easy to tap)
- [ ] Verify payment processor loads correctly
- [ ] Test form submission (no errors)

**Fixes if broken:**
1. **Form fields:** Ensure inputs stack vertically on mobile
   ```css
   input, select, textarea {
     width: 100%;
     font-size: 16px; /* Prevents zoom on iOS */
   }
   ```

2. **CTA button:** Make it prominent and large
   ```css
   .cta-button {
     width: 100%;
     padding: 16px;
     font-size: 18px;
     min-height: 44px;
   }
   ```

3. **Checkout page:** Load testing (should load < 3 seconds on 3G)
   - Optimize images (compress, use WebP)
   - Minimize JavaScript
   - Use CDN for static assets

**Deadline:** April 3 (critical for Week 1 campaign launch)

---

### 📸 REPLACE PLACEHOLDER TESTIMONIALS

**Current state:** Landing page has placeholder testimonial section  
**Goal:** Replace with real customer names, credentials, photos

**What you need:**
- [ ] 8–10 real customer testimonials
- [ ] Format: Name, title/credential, photo, quote (1–2 sentences), specific result

**Example format:**
```
[Photo] Mike Johnson
Strength Coach, Austin TX

"I've been coaching for 15 years. This is the first grip product 
that actually makes a difference. My clients added 2 inches per arm 
in 60 days. Game changer."

⭐⭐⭐⭐⭐
```

**How to collect:**
1. Email past customers (see template below)
2. Offer small incentive ($20 discount on next order)
3. Request: Photo + short quote + permission to use
4. Collect video testimonials if possible (15–30s)

**Collection email template:**
```
Subject: Help us celebrate your wins! (and get $20 off)

Hi [Customer Name],

You've been using Sniperform grips for [X weeks/months], and we'd love 
to hear about your experience!

Would you be willing to share a quick testimonial? It takes 2 minutes:

1. What's your name + what you do? (e.g., "John, strength coach")
2. What was the biggest change you noticed?
3. Any specific results? (e.g., arm size, strength gains)
4. Can we use a photo of you in our marketing?

As a thank you, we'll send you a $20 discount code for your next order.

Reply to this email and let us know!

—Sniperform
```

**Deadline:** April 14 (needed for Week 3–4 retargeting campaigns)

---

### 🎥 ADD VIDEO TESTIMONIALS (2–3)

**Why:** Video testimonials convert 3–5x better than text

**What you need:**
- 15–30 second videos
- Real customer or trainer using the product
- Speaking directly to camera
- Specific result mentioned

**Recording specs:**
- Phone camera (iPhone 12+ quality fine)
- Good lighting (natural window light best)
- Quiet room (no gym noise)
- Stable (use tripod or prop phone)

**Video testimonial script template:**
```
[Person on camera, holding the grips]

"Hi, I'm [Name], [credential]. I've been using Sniperform for [X weeks].

The biggest change? My arms grew [X inches] in [X weeks/months]. 
But more importantly, my form is way better. The spirit level shows 
me exactly when I'm pulling uneven.

If you're serious about arm growth, you need these."

[End with product in hand or on bar]
```

**Where to feature on landing page:**
- Hero section (1 testimonial, auto-playing, muted)
- Testimonial carousel (2–3 testimonials rotating)
- Above final CTA (1 testimonial as social proof)

**Deadline:** April 14

---

### 📊 ADD TRUST SIGNALS

**Current elements:**
- [ ] Guarantee (90-day, money back)
- [ ] Return policy (free return shipping)
- [ ] Testimonials (5+ displayed)
- [ ] Review/rating badges (if any 3rd party reviews exist)
- [ ] Customer count ("Join 5,000+ lifters")
- [ ] Product specs/certifications
- [ ] Brand/media mentions (if applicable)

**Where to place them:**
1. **Hero section:** "⭐⭐⭐⭐⭐ Trusted by 5,000+ serious lifters"
2. **Above CTA buttons:** "90-day guarantee. 100% risk-free."
3. **FAQ section:** Address common objections
4. **Testimonial section:** Display customer photos + quotes
5. **Product cards:** Show specs, material, warranty

**Deadline:** April 7

---

## PART 2: CONVERSION OPTIMIZATION (Weeks 2–4)

### A/B TEST HERO COPY

**Current hero:** [Ask Oliver for exact copy]

**Test variations:**
1. **Control:** [Current copy]
2. **Variant A:** "The first grip with a built-in spirit level"
3. **Variant B:** "Thicker grips = bigger arms + balanced strength"
4. **Variant A2:** "Join 5,000+ lifters who added 10–15 lbs per arm"

**How to test:**
- Split traffic 25% to each variant
- Run for 2 weeks minimum
- Measure: CVR, time on page, bounce rate
- Winner gets scaled budget

**Deadline:** April 14 (implement by Week 3)

---

### REDUCE FRICTION IN CHECKOUT

**Current state:** Check if checkout is optimized

**Audit checklist:**
- [ ] Minimal required fields (email, address, payment — that's it)
- [ ] Guest checkout option (don't force login)
- [ ] Progress indicator ("Step 1 of 3")
- [ ] Estimated delivery date shown
- [ ] Payment options clear (Visa, Mastercard, PayPal, Apple Pay)
- [ ] Error messages helpful (not vague)
- [ ] Mobile keyboard optimized (number pad for zip code, etc.)

**Optimizations to test:**
1. **Pre-fill state/country** (if targeting USA, default to USA)
2. **Progressive disclosure** (show only necessary fields first)
3. **Auto-focus next field** (after filling one field, cursor moves to next)
4. **Disable "Continue" button until form valid** (prevent errors)
5. **Show security badges** (SSL certificate, payment processor logos)

**Deadline:** April 14

---

### OPTIMIZE ABOVE-THE-FOLD

**"Above the fold"** = What users see before scrolling

**Checklist:**
- [ ] **Headline is clear** (answers "why should I care?")
- [ ] **Hero image/video is compelling** (product in action, not just on white background)
- [ ] **Subheadline supports main headline** (gives reason to believe)
- [ ] **Primary CTA is visible** (button should stand out, use brand color)
- [ ] **Value prop is obvious** (in 5 seconds, user knows what this is)

**Optimizations:**
1. **Hero video:** Show spirit level vial in action on heavy barbell
2. **Headline size:** Make it large and readable on mobile
3. **CTA button:** Use brand teal color, high contrast
4. **Remove friction:** Don't ask for email before they click CTA
5. **Social proof placement:** Show "5,000+ customers" or "⭐⭐⭐⭐⭐" near headline

**Deadline:** April 7

---

### ADD MICRO-CONVERSIONS & ENGAGEMENT

**Goal:** Track user behavior + keep them engaged

**Micro-conversions to add:**
1. **Email capture:** "Get our free grip training guide" (before checkout, capture email)
2. **Quiz:** "What's your grip type?" (educational, personalizes page)
3. **Video engagement:** Track which sections users watch
4. **Time on page:** Measure attention by scroll depth

**Implementation:**
1. **Email popup:** Appears after 45 seconds or on exit-intent
   - Offer: Free PDF guide
   - Collect: Email only (not name)
   - Frequency: Once per user per month

2. **Quiz module:** Appears on landing page
   - 3 questions (5 seconds to complete)
   - Results show personalized product recommendation
   - Tracks completion as micro-conversion

3. **Video analytics:** Use Wistia or Mux
   - Track play %, drop-off points
   - Identify which testimonials keep viewers longest

**Deadline:** April 21

---

## PART 3: ADVANCED OPTIMIZATION (Weeks 5–12)

### PERSONALIZATION BY TRAFFIC SOURCE

**Goal:** Show different messaging based on where visitor came from

**Variants by source:**

| Traffic Source | Headline | Focus | CTA |
|---|---|---|---|
| **Instagram** | "Your left arm is weaker" | Bilateral balance angle | "See the imbalance" |
| **YouTube** | "Thicker grips = bigger arms" | Size/strength angle | "Learn the science" |
| **Google Search** | "Best thick grip for arm training" | Comparison/review angle | "Compare prices" |
| **Email** | "Your guarantee expires tomorrow" | Urgency/scarcity | "Get yours" |

**How to implement:**
- Use UTM parameters to identify source (e.g., `?utm_source=instagram`)
- Use JavaScript to show/hide page elements based on UTM
- Track which variant converts best

**Deadline:** May 1 (after initial campaigns running)

---

### SCARCITY & URGENCY MECHANICS

**Goal:** Increase conversion rate with limited-time/limited-supply signals

**Mechanics to test:**

1. **Stock countdown:** "Only 18 left in stock"
   - Use actual inventory count
   - Update real-time
   - Use Omega Countdown or similar plugin

2. **Time-limited offer:** "This price expires at [time]"
   - Use countdown timer
   - Reset daily (or weekly if running continuous offer)
   - Show urgency clearly

3. **Email exclusivity:** "Exclusive for email subscribers"
   - Offer early access or discount
   - Drive email signups

4. **Flash sale announcements:** "⚡ Today only: 20% off"
   - Use announcement bar at top of page
   - Rotate daily

**Deadline:** April 21 (start with stock countdown)

---

### BUNDLE UPSELL MECHANICS

**Current state:** Single pack vs double pack with free shaker

**Optimizations to test:**

1. **Default to bundle:** Pre-check "double pack + free shaker" instead of single
   - Increases AOV (average order value) by 15–25%
   - Easy to uncheck if user prefers single

2. **Progressive disclosure:** Show upsell AFTER quantity selected
   - Reduces initial friction
   - Shows relevant offer at right moment

3. **Savings messaging:** "Save $20 with double pack + free shaker"
   - Show dollar savings, not just value
   - Use bold color for savings amount

4. **Comparison table:**
   ```
   Single Pack       |  Double Pack + Free Shaker
   $59.95           |  $99.95 (Save $20!)
   1x grip          |  2x grips
   Standard ship    |  Free expedited shipping
   60-day guarantee |  90-day guarantee
   ```

**Deadline:** April 21

---

### GUARANTEE AMPLIFICATION

**Current guarantee:** 90-day money-back

**Amplify with:**
- [ ] Risk-reversal language ("100% risk-free")
- [ ] Easy return process ("Free return shipping both ways")
- [ ] Clear conditions ("No questions asked")
- [ ] Deadline ("30/60/90 days")
- [ ] Visual badge (use brand colors)

**Guarantee placement:**
- Hero section (near CTA)
- Each CTA button
- FAQ section
- Testimonials (customer quote about guarantee ease)

**Example badge:**
```
┌─────────────────────────┐
│  ✓ 90-Day Guarantee     │
│  ✓ Free Returns         │
│  ✓ Full Refund          │
│  ✓ No Questions Asked   │
└─────────────────────────┘
```

**Deadline:** April 7

---

## PART 4: ANALYTICS & MEASUREMENT

### CONVERSION FUNNEL TRACKING

**Install on landing page:**

```
Metric | Target (Month 1) | Target (Month 3)
---|---|---
Page views | 1,000+ | 2,000+
Unique visitors | 800+ | 1,500+
Email signups | 200+ | 500+
Video plays | 400+ | 1,000+
Add-to-cart | 50+ | 150+
Checkout initiated | 35+ | 100+
Purchase | 5–8 | 20–30
CVR | 0.6–1.0% | 1.2–1.8%
```

**How to track:**
- GA4: Enable ecommerce events + enhanced ecommerce
- Shopify: Built-in analytics
- Meta pixel: Verify all events firing

---

### IDENTIFY BOTTLENECKS

**Measure drop-off at each step:**

```
Step | Drop-off %
---|---
Visitor → Email signup | 75%
Visitor → ATC | 93%
ATC → Checkout initiated | 30%
Checkout → Purchase | 15%
```

**Biggest opportunities (if this is your funnel):**
1. **Email signup:** Only 25% capturing email → test better offer/placement
2. **ATC rate:** Very high drop-off → messaging issue or price objection
3. **Checkout drop-off:** 30% not completing checkout → friction in form
4. **Purchase drop-off:** Only 85% buying after checkout → security concerns or technical issues

---

## PART 5: TESTING ROADMAP

### Month 1: Foundation
- [ ] Fix tablet rendering bug
- [ ] Add real testimonials (8–10 text + 2–3 video)
- [ ] A/B test hero copy (run for 2 weeks)
- [ ] Add trust signals (guarantee badge, customer count, etc.)
- [ ] Implement stock countdown
- [ ] Measure: CVR baseline, bounce rate, ATC rate

### Month 2: Optimization
- [ ] Winner from hero copy test → scale
- [ ] Test bundle upsell mechanics (default to bundle)
- [ ] Test scarcity messaging (urgency + social proof)
- [ ] Email capture popup + lead magnet
- [ ] Reduce checkout friction
- [ ] Measure: CVR improvement %, AOV change, email subscribers

### Month 3: Advanced
- [ ] Personalization by traffic source
- [ ] Dynamic testimonials (rotate daily)
- [ ] Video testimonial on hero
- [ ] Quiz for personalization
- [ ] Advanced retargeting (personalized landing page by audience)
- [ ] Measure: CVR target 1.2–1.8%, sustained ROAS 1.0x+

---

## QUICK WINS (Implement Immediately)

**These take <1 hour each, high impact:**

1. **Add customer count:** "Join 5,000+ lifters" (if true) → +3–5% CVR
2. **Add guarantee badge:** "90-day guarantee, free returns" → +5–8% CVR
3. **Add video testimonial to hero:** Auto-play, muted → +10–15% watch rate
4. **Pre-check bundle:** Default to double pack + free shaker → +15–25% AOV
5. **Implement stock countdown:** "Only X left" → +3–7% urgency
6. **Simplify checkout:** Remove non-essential fields → +2–5% CVR

**Expected lift from all 6:** +50–75% improvement in funnel metrics

---

## FINAL CHECKLIST

- [ ] Tablet rendering tested and fixed (critical)
- [ ] 8–10 real testimonials with photos added
- [ ] 2–3 video testimonials embedded
- [ ] Hero copy A/B test live
- [ ] Trust signals displayed prominently
- [ ] Stock countdown implemented
- [ ] Bundle upsell optimized (default to bundle)
- [ ] Checkout friction reduced (minimal fields)
- [ ] Guarantee amplified (badge + messaging)
- [ ] Email capture popup added
- [ ] Analytics tracking verified (GA4 + Shopify + Meta)
- [ ] Conversion funnel mapped + drop-off points identified

**Once all complete, you're ready for paid ads to scale.** ✅

