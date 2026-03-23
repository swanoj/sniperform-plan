# SNIPERFORM USA MARKET — COMPREHENSIVE MARKETING PLAN
**Prepared for:** Sniperform USA  
**Date:** March 2026  
**Focus:** Meta Account Setup, Content Strategy, & Conversion Optimization  
**Primary Goal:** Scale paid social ROAS from 0.37x → 1.2x+ within 90 days

---

## EXECUTIVE SUMMARY

### Current State
- **Meta ROAS:** 0.37x actual (Meta reports 0.70x — pixel data is broken)
- **Conversion rate:** 0.55% (benchmark: 1.5–3%)
- **Critical gaps:** Zero retargeting, broken CAPI, age-spend mismatch (55–64 age bracket outperforms but underfunded)
- **Checkout funnel:** 92% drop-off from Add-to-Cart → Purchase (indicates UX/trust/tracking issues)

### Immediate Wins (30 days)
1. Fix tracking & CAPI configuration
2. Pause homepage spend, redirect to optimized landing page
3. Activate retargeting (3-tier audience funnel)
4. Reallocate budget to high-performing age brackets (25–44, 55–64)
5. Launch 3x hero creative tests

### 90-Day Outcome
- **Target ROAS:** 1.2x–1.5x
- **Target conversion rate:** 1.2–1.8%
- **Monthly ad spend:** $8K–$12K USD
- **Monthly revenue:** $10K–$18K USD
- **Supporting organic/email:** 20–30% incremental revenue lift

---

## PART 1: PRODUCT POSITIONING & MESSAGE STRATEGY

### The Core Promise
**"The first gym grip that tells you when you're cheating yourself."**

Sniperform sits at a unique intersection:
- **Thick grip training** (established category, owned by Fat Gripz)
- **Bilateral balance feedback** (new angle — patent-backed, competitors can't copy)
- **Modern UX & conversion mechanics** (vs Fat Gripz's dated website)

### Why This Matters for USA Market
The USA strength training market is **highly competitive but unsaturated on the balance angle**. Most lifters:
- Know thicker grips = bigger arms (commoditized)
- Have **no idea** their left/right strength is imbalanced (Sniperform's differentiator)
- Will pay $60 for a tool that reveals this imbalance + fixes it in real time

### Four Science Pillars (Use These in ALL Content)
1. **Irradiation:** Thick grip → ↑ grip activation → radiates neural drive up arm chain → bigger biceps/triceps
2. **Neural Inhibition:** Thin bars cause CNS to limit force output; thick grips bypass this protective mechanism
3. **Weak Link Theory:** Grip is often the bottleneck in arm training; removing it allows muscles to work harder
4. **Bilateral Balance (Sniperform exclusive):** Most lifters have a dominant side without realizing it; spirit level vial reveals + corrects this in real time

**Content Pillar Mapping:**
- Each pillar = 1 piece of content per week (blog, reel, carousel, email)
- Rotate across paid social, organic, email
- Use in landing page copy, ad copy, and organic content

---

## PART 2: META ACCOUNT SETUP FOR USA MARKET

### Phase 1: Account Audit & Fix (Week 1)

#### Issue #1: Tracking is Broken
**Current state:** GA4 checkout events broken, CAPI not configured, Meta pixel data incomplete

**Action plan:**
1. **Audit GA4 setup**
   - Verify purchase event is firing (check real-time reports while making a test purchase)
   - Verify ecommerce event parameters: transaction ID, value, items, currency
   - Test with Google Tag Assistant Chrome extension
   
2. **Enable CAPI (Conversions API) — Critical**
   - This is the biggest gap. CAPI sends server-side purchase data to Meta, bypassing iOS/browser tracking limitations
   - Setup steps:
     - Go to Meta Events Manager → Conversions API
     - Create new dataset for US store
     - Get API token from Shopify (Apps > Settings > API credentials)
     - Install Conversions API on Shopify (Shopify app > Meta Pixel, enable Conversions API)
     - Test: make a purchase, verify in Meta Events Manager within 30 mins
   - Impact: +30–50% more accurate ROAS reporting + better ad optimization

3. **Set purchase conversion window to 7-day click (not 1-day)**
   - Many sales happen 3–7 days after click
   - Current setup likely undercounts conversions
   - Go to Ads Manager → select campaign → go to Edit → scroll to "Attribution window" → change from 1d click to 7d click or 7d view+click

#### Issue #2: Budget Going to Wrong Landing Page
**Current:** Paid traffic sent to homepage (0.00 ROAS)  
**Fix:** Pause homepage campaigns, redirect all traffic to landing page

**Action:**
1. Pause all campaigns with homepage destination URL
2. In Ads Manager, verify all active campaigns point to `sniperform.com` landing page (not just sniperform.com home)
3. Create audience exclusion: exclude anyone who already visited the landing page from homepage campaigns
4. Redirect: Set up 301 redirect on homepage → landing page in Shopify Settings > Online Store > Domains (if possible)

#### Issue #3: Age-Spend Mismatch
**Current:** 55–64 age bracket has **highest ROAS** but only gets **14% of spend**

**Action:**
1. Go to Ads Manager → Performance by Age & Gender report
2. Identify all age brackets with ROAS > 0.50x
3. Create age-specific campaigns:
   - **Campaign A:** Ages 25–34 (core young lifter audience, high volume)
   - **Campaign B:** Ages 35–44 (established gym-goer, proven spender)
   - **Campaign C:** Ages 45–55 (serious hobbyist, high ROAS)
   - **Campaign D:** Ages 55–64 (elite/experienced, highest ROAS — should be well-funded)
4. Allocate budget proportional to ROAS:
   - 40% to Ages 25–34
   - 25% to Ages 35–44
   - 20% to Ages 45–55
   - 15% to Ages 55–64
5. Review weekly, rebalance if performance shifts

### Phase 2: Campaign Structure (Week 1–2)

#### Meta Account Structure (Recommended)
```
Account: Sniperform USA
├─ Campaign A: AWARENESS
│  ├─ Audience: Broad + lookalike (1% LLA based on purchasers)
│  ├─ Objective: Video Views
│  ├─ Daily budget: $30–40
│  └─ Creative: Attention-grabbing (spirit level in action, big lift, hook text)
│
├─ Campaign B: CONVERSION (Core)
│  ├─ Audience: Narrow targeting (detailed below)
│  ├─ Objective: Conversions
│  ├─ Daily budget: $100–150 (main spend)
│  └─ Creative: Product-focused, landing page → purchase
│
├─ Campaign C: RETARGETING — Warm Audiences
│  ├─ Audience: Website visitors (last 30 days)
│  ├─ Objective: Conversions
│  ├─ Daily budget: $40–60
│  └─ Creative: Social proof, guarantee, discount incentive
│
├─ Campaign D: RETARGETING — Hot Audiences
│  ├─ Audience: ATC + Initiate Checkout (last 7 days)
│  ├─ Objective: Conversions
│  ├─ Daily budget: $20–30
│  ├─ Creative: Scarcity (low stock), countdown, 90-day guarantee
│  └─ CTA: "Complete your order"
│
└─ Campaign E: LOYALTY (Future)
   ├─ Audience: Purchasers (last 90 days)
   ├─ Objective: Conversions (bundle upsell)
   ├─ Daily budget: $20–30
   └─ Creative: "Add the double pack" / free shaker offer
```

#### Campaign B: Core Conversion Targeting
**Daily budget:** $100–150 USD  
**Objective:** Conversions  
**Pixel event:** Purchase

**Audience Stacks (Test 3 audiences in parallel):**

**Audience 1: Fitness Enthusiast (Primary)**
- **Location:** USA (all states)
- **Age:** 25–64
- **Interests:** {Gym, Fitness, Strength Training, Bodybuilding, CrossFit, Personal Training, Fitness Equipment, Fitness Brands} (use all 8)
- **Behaviors:** Fitness & Wellness interests
- **Device:** All (desktop, mobile, tablet — but test desktop separately)
- **Language:** English
- **Lookalike:** Also create 1% Lookalike of all-time purchasers (if enough data)
- **Exclusions:** Exclude competitors (Fat Gripz audience, generic grip brands)

**Audience 2: Strength Sport Athlete (Secondary)**
- **Location:** USA
- **Age:** 25–54 (skew younger for this audience)
- **Interests:** {Powerlifting, Weightlifting, Crossfit, Strength & Conditioning, Fitness Coaching}
- **Behaviors:** Fitness Equipment purchases (in last 90 days if available)
- **Device:** Mobile + Desktop
- **Exclusions:** Recent Fat Gripz customers (if pixel data available)

**Audience 3: Lookalike + Custom Combo**
- **1% Lookalike:** Based on purchasers (highest value)
- **Exclude:** Website visitors who've already seen ads

**Note:** For each audience, set **Detailed Targeting Expansion = OFF** (Meta defaults to ON; turn it off to keep targeting tight).

---

## PART 3: CREATIVE STRATEGY & AD TESTING MATRIX

### Hero Hook (Master Control)
**"Thicker grips = bigger arms"**

This has driven 82% of historical revenue. It works. Test variations around it, not against it.

### 30-Day Creative Test Plan

**Test 1: Hook Variations (Video — Play/Placement Optimized)**

| Variation | Hook | Visual | CTA | Audience | Daily Budget | Success Metric |
|-----------|------|--------|-----|----------|--------------|-----------------|
| Control | "Thicker grips = bigger arms" | Spirit level vial on bar, big lift | "See how" | Audience 1 | $40 | ROAS > 0.50x |
| Variant A | "Your left arm is weaker. You just don't know it." | Split screen: uneven pull, spirit level reveals imbalance | "Learn why" | Audience 1 | $30 | CTR > 3% |
| Variant B | "Grip is holding you back. Here's the fix." | Close-up: person frustrated, can't grip weight, puts on grips, lifts easily | "Unlock more" | Audience 2 | $30 | CVR > 0.8% |
| Variant C | "The $60 upgrade serious coaches have been recommending for years." | B-roll of trainer recommending, lifter using, before/after muscle activation | "Join the pros" | Audience 3 | $30 | ROAS > 0.40x |

**Creative specs:**
- **Format:** Vertical video (9:16 aspect ratio)
- **Length:** 15–30 seconds
- **Audio:** Music + voiceover OR silent with captions
- **Hook timing:** First 3 seconds must stop the scroll
- **Visual payoff:** Spirit level vial must be visible/prominent
- **Product shot:** Full grip on the bar in a real gym environment
- **CTA:** Soft (not "BUY NOW!" — more "Learn how" or "See results")

---

### Test 2: Audience Age-Segment Creative (Parallel)

| Age Bracket | Hook Angle | Visual Tone | CTA Tone |
|-------------|-----------|------------|----------|
| 25–34 | "Add 20% more stimulus to every set" | High energy, gym footage, muscle pump shots | Ambitious ("Max out your gains") |
| 35–44 | "Train smarter, not just harder" | Technique focus, controlled movement, CNS education | Efficient ("Work like a pro") |
| 45–55 | "Quality over quantity — this is how elite athletes train" | Slower pace, precision, expert validation | Authority ("Coach recommended") |
| 55–64 | "Your experience demands precision. This is built for you." | Sophisticated, technical detail, bilateral balance | Expert ("Serious lifters only") |

**Run 4 separate ad sets (ages 25–34, 35–44, 45–55, 55–64) with custom messaging per age bracket.**

---

### Test 3: Static Image Ads (Control vs Video)

| Format | Creative | Audience | Budget | Notes |
|--------|----------|----------|--------|-------|
| Static + Text | Hero product shot (grip on bar) + "Thicker grips = bigger arms" | Audience 1 | $15 | Baseline |
| Carousel | 5 images: hook text, close-up of vial, lift in progress, muscle activation, guarantee | Audience 1 | $15 | High engagement test |
| Video (15s) | "Thicker grips" hook + spirit level vial in action | Audience 1 | $20 | Expected winner |

---

### Retargeting Creative (Campaigns C & D)

**For Warm Audiences (Website visitors, 30-day window):**

| Ad Type | Hook | Visual | CTA | Notes |
|---------|------|--------|-----|-------|
| Static | "90-day guarantee. Risk free." | Product on bar + guarantee badge | "Try risk-free" | Trust signal |
| Carousel | Images: vial detail, lift, muscle activation, guarantee, testimonial | Step-by-step (how it works) | "Shop now" | Education |
| Video (20s) | "See why 5,000+ lifters trust Sniperform" | Customer testimonials, footage, guarantee | "Join them" | Social proof |

**For Hot Audiences (Add-to-cart, last 7 days):**

| Ad Type | Hook | Visual | CTA | Notes |
|---------|------|--------|-----|-------|
| Urgent Static | "Only 3 left in stock" (if true, use countdown timer) | Product image + stock counter | "Complete order" | Scarcity |
| Video (15s) | "Here's what you're missing" — show spirit level + happy lifter | Testimonial, vial in action, price | "Get yours" | FOMO |
| Carousel | Images: 1) product, 2) guarantee, 3) testimonial, 4) vial detail, 5) price + CTA | Lifecycle | "Check out" | Nudge |

---

## PART 4: LANDING PAGE OPTIMIZATION

### Current State
- 10 iterations completed
- Core elements: hook, 3-step lifestyle, before/after, bundle upsell, science section, testimonials (placeholder), competitive comparison, guarantee, FAQ

### Optimization Roadmap (30–60 days)

#### Week 1–2: Critical Fixes
1. **Replace all placeholder testimonials** with real names, credentials, before/after photos
   - Target: 8–10 testimonials from real customers or coaches
   - Include: Name, title (e.g., "Strength Coach"), photo, quote, specific result (e.g., "+15 lbs on rows")
2. **Add video testimonials** (if budget allows)
   - 15–30 second customer testimonials showing spirit level in use
   - 2–3 videos embedded on page (one in hero, one in testimonial section, one above CTA)
3. **Fix tablet rendering bug** (reported: 2,100 sessions with zero conversions)
   - Test checkout flow on iPad + Android tablet
   - Verify all buttons are tap-friendly (44px minimum height)
   - Check form field widths on tablet viewport

#### Week 2–3: Conversion Optimization
1. **A/B test hero copy variations**
   - Control: Current copy
   - Variant A: Lead with "The first grip with a built-in spirit level"
   - Variant B: Lead with "Thicker grips = bigger arms + balanced strength"
   - Run 50/50 traffic split, measure conversion rate + time on page
2. **Add urgency/social proof elements**
   - Live visitor counter (Justuno or similar)
   - Stock countdown (if applicable)
   - Rotating testimonial banner above fold
3. **Reduce form friction**
   - Minimize required fields at checkout
   - Offer guest checkout option
   - Show estimated delivery date

#### Week 3–4: Advanced Optimization
1. **Test bundle upsell mechanics**
   - Current: Single pack vs double pack with free shaker
   - Test: Progressive disclosure (show upsell after customer selects quantity)
   - Test: Pre-check "free shaker" bundle as default
2. **Add micro-conversions**
   - Email capture: "Get our free grip training guide" (pre-checkout)
   - Quiz: "What's your grip type?" (identifies customer archetype, personalizes page)
   - Video play tracking (which sections viewers watch most)
3. **Scarcity/exclusivity messaging**
   - "Only X units available this month"
   - "Patented technology — nowhere else available"

---

## PART 5: CONTENT STRATEGY & ORGANIC LEVERAGE

### Weekly Content Calendar (5 Pillars, 3 weeks = 15 pieces)

**Pillar 1: Science of Thick Grip Training**

| Week | Format | Topic | Platform | Effort |
|------|--------|-------|----------|--------|
| 1 | Reel (60s) | "Why thick grips = bigger arms" (Irradiation explained) | Instagram | Medium |
| 2 | Blog post (1,200 words) | "The Complete Science Behind Thick Grip Training" | sniperform.com/blog | High |
| 3 | Email series (3 emails) | "The Science Behind Sniperform" (Irradiation → Neural Inhibition → Weak Link → Balance) | MailChimp | Medium |

**Pillar 2: Bilateral Balance (Sniperform Exclusive)**

| Week | Format | Topic | Platform | Effort |
|------|--------|-------|----------|--------|
| 1 | Reel (45s) | "Is your left arm weaker? Here's how to find out." | Instagram/TikTok | Low |
| 2 | Carousel (5 slides) | "One-sided training is slowing your gains" | Instagram | Medium |
| 3 | YouTube Short (60s) | "The imbalance costing you 10 lbs per arm" | YouTube Shorts | Medium |

**Pillar 3: Product Proof & Application**

| Week | Format | Topic | Platform | Effort |
|------|--------|-------|----------|--------|
| 1 | Reel (45s) | "Spirit level vial in action — heavy deadlift" | Instagram | Medium |
| 2 | Carousel (6 slides) | "How to use Sniperform: curls, rows, cable work" | Instagram | Medium |
| 3 | TikTok (30s) | "Why coaches are obsessed with Sniperform" | TikTok | Low |

**Pillar 4: Expert Validation**

| Week | Format | Topic | Platform | Effort |
|------|--------|-------|----------|--------|
| 1 | Blog/case study (800 words) | "Why Strength Coaches Recommend Sniperform" | sniperform.com | High |
| 2 | Reel (45s) | Customer testimonial (real coach using product) | Instagram | Medium |
| 3 | Email | "What 1,000+ serious lifters know about grip training" | MailChimp | Low |

**Pillar 5: Training Tips & Authority**

| Week | Format | Topic | Platform | Effort |
|------|--------|-------|----------|--------|
| 1 | Reel (60s) | "5 exercises that benefit most from thick grips" | Instagram | Medium |
| 2 | Blog post (1,500 words) | "The Complete Guide to Arm Training with Thick Grips" | sniperform.com | High |
| 3 | YouTube (5 mins) | "Why your arms aren't growing — and how Sniperform fixes it" | YouTube | High |

### Content Production Workflow
1. **Batching:** Record 2–3 weeks of video content in 1 session (cheaper, consistent aesthetic)
2. **Tools:** Canva (graphics), CapCut (video editing), Rev.com (transcription)
3. **Scheduling:** Use Meta Business Suite to pre-schedule posts (publish on consistent days: Tue, Thu, Sat)
4. **Repurposing:**
   - 1 long-form blog → 3 reels + 1 carousel + 1 email sequence
   - 1 YouTube video → clip 2–3 TikToks/Shorts + 1 reel

---

## PART 6: EMAIL MARKETING (Untapped Lever)

### Current State
- No email sequences in place
- Untapped customer base on website (estimated 2,000–5,000 visitors/month, ~0% capture rate)

### 30-Day Email Plan

#### Sequence 1: Lead Magnet (Website Visitors)
**Goal:** Convert 10–15% of website visitors to email subscribers

**Lead magnet:** Free PDF guide — "The Science Behind Bigger Arms: A Lifter's Guide to Thick Grip Training" (800 words, includes the 4 pillars)

**Placement:**
- Inline popup on landing page (appears after 45 seconds or on exit-intent)
- Post-purchase thank you email (offer bonus guides)

**Sequence (5 emails over 10 days):**
1. **Day 1:** Lead magnet delivered + intro email ("Here's what thicker grips actually do to your arms")
2. **Day 3:** Science email (Irradiation + Neural Inhibition detailed)
3. **Day 5:** Bilateral balance email ("Find your imbalance in 30 seconds")
4. **Day 7:** Social proof email (customer testimonials, before/after)
5. **Day 9:** Soft pitch email (20% discount code, link to landing page)

#### Sequence 2: Post-Purchase (Customers)
**Goal:** Build loyalty, drive repeat purchases + referrals

**Sequence (6 emails over 30 days):**
1. **Day 1:** Thank you + how to use guide
2. **Day 5:** "How to maximize your Sniperform grips" (3 exercises to prioritize)
3. **Day 10:** Customer testimonial/case study (build confidence in product)
4. **Day 15:** Referral incentive ("Get $20 off for each friend who buys")
5. **Day 21:** Bundle upsell ("Upgrade to double pack + free shaker")
6. **Day 30:** Feedback request (NPS + testimonial harvest)

#### Sequence 3: Abandoned Cart
**Goal:** Recover 15–25% of abandoned carts

**Trigger:** Checkout abandonment (start within 1 hour)

**Sequence (3 emails over 3 days):**
1. **Hour 1:** "Did you forget this? 90-day guarantee + free returns."
2. **Day 2:** "Only 3 left in stock — see why 5,000+ lifters chose Sniperform"
3. **Day 3:** "Last chance — 48-hour cart hold + $10 off code COMEBACK10"

---

## PART 7: 90-DAY ROADMAP & MILESTONES

### Week 1–2: Foundation (Fix Tracking, Launch Core Campaign)
- [ ] Enable CAPI on Shopify
- [ ] Fix GA4 purchase event tracking
- [ ] Pause homepage campaigns
- [ ] Create 3x audience stacks (Fitness Enthusiast, Strength Athlete, Lookalike)
- [ ] Launch Campaign B (Core Conversion) with 3x creative tests
- [ ] Launch Campaign A (Awareness) with hook variation test
- [ ] Implement tablet rendering fix
- [ ] Collect 5 real testimonials (outreach to existing customers)

**Expected metrics:** Setup complete, $1,200 spent, initial CTR/CPM data

---

### Week 3–4: Scale & Retargeting
- [ ] Replace placeholder testimonials on landing page
- [ ] Launch Campaign C (Retargeting — Warm Audiences)
- [ ] Launch Campaign D (Retargeting — Hot Audiences)
- [ ] A/B test hero copy on landing page
- [ ] Implement live visitor counter + stock countdown
- [ ] Set up email lead magnet + launch Sequence 1 (Lead Magnet)
- [ ] Publish 3x content pieces (2 reels, 1 carousel)
- [ ] Audit & optimize bundle upsell messaging

**Expected metrics:** ROAS 0.40x–0.50x, retargeting campaigns live, email subscribers +200–300

---

### Week 5–6: Content & Authority
- [ ] Publish first long-form blog post (1,500 words: "Complete Guide to Arm Training with Thick Grips")
- [ ] Launch email Sequence 2 (Post-Purchase)
- [ ] Harvest 3–5 customer testimonials (video + text)
- [ ] Create 4x age-segment specific ad variations
- [ ] Implement micro-conversions (quiz, video tracking, email capture)
- [ ] Audit creative performance, pause underperformers
- [ ] Publish 4x organic content pieces

**Expected metrics:** ROAS 0.50x–0.65x, blog traffic +500–800 visits, email subscribers +400–500

---

### Week 7–8: Optimization & Expansion
- [ ] Rebalance budget by age bracket (increase 55–64 from 14% → 25%)
- [ ] Test 2x new creative angles (audience-specific variations)
- [ ] Run landing page micro-optimization tests (form friction, urgency)
- [ ] Launch Sequence 3 (Abandoned Cart)
- [ ] Evaluate bundle upsell mechanics, test progressive disclosure
- [ ] Explore TikTok as secondary paid channel (with working UTM tracking)
- [ ] Publish 3x content pieces + 1x YouTube video

**Expected metrics:** ROAS 0.70x–0.85x, conversion rate +0.65–0.75%, email subscribers +600–800

---

### Week 9–12: Scale & Target ROAS
- [ ] Increase daily ad spend from $150 → $200–250 (if ROAS maintains 0.75x+)
- [ ] Launch lookalike campaigns (1%, 5%, 10% based on purchasers)
- [ ] Evaluate TikTok performance, allocate 10–15% of budget if ROAS > 0.50x
- [ ] Scale best-performing creative (weekly budget increases, 10–15% per week)
- [ ] Test seasonal angles (summer/fall training seasons, New Year momentum, etc.)
- [ ] Full content calendar in place (15+ pieces published, organic reach +1000–2000 followers)
- [ ] Customer testimonials (8+ collected, rotating in ads + landing page)
- [ ] Email list +2,000–3,000 subscribers

**Target outcomes:**
- **ROAS:** 1.0x–1.2x
- **Conversion rate:** 1.0–1.5%
- **Monthly ad spend:** $8K–$10K
- **Monthly revenue from paid:** $8K–$12K
- **Organic + email contribution:** +30–40% incremental revenue

---

## PART 8: SUCCESS METRICS & TRACKING

### Primary KPIs (Track Weekly)
| Metric | Current | 30-Day Target | 90-Day Target |
|--------|---------|---------------|---------------|
| **ROAS (Paid Social)** | 0.37x | 0.55x–0.65x | 1.0x–1.2x |
| **Conversion Rate** | 0.55% | 0.75–1.0% | 1.2–1.8% |
| **CPC (Cost Per Click)** | ~$1.20 | $1.00–1.10 | $0.85–0.95 |
| **CPM (Cost Per 1K Impressions)** | ~$8.50 | $7.50–8.00 | $6.50–7.50 |
| **ATC (Add-to-Cart) Rate** | 2.8% | 3.5–4.0% | 5.0–6.0% |
| **ATC → Checkout Rate** | 8% | 10–12% | 15–20% |
| **Monthly Paid Revenue** | ~$1,800 | $3,000–4,000 | $8,000–12,000 |

### Secondary KPIs (Track Monthly)
| Metric | Target | Notes |
|--------|--------|-------|
| **Cost Per Acquisition (CPA)** | <$40 | (Revenue minus COGS ÷ # of customers) |
| **Customer Lifetime Value (CLV)** | >$150 | (Target 3:1 CLV:CPA ratio) |
| **Email Subscriber Growth** | +500/month | From lead magnet + landing page |
| **Email Open Rate** | 25%+ | Industry benchmark |
| **Email Click Rate** | 3%+ | Industry benchmark |
| **Organic Social Reach** | +2,000–3,000 | Monthly followers + impressions |
| **Blog Traffic** | +200–400 visitors/month | From organic search + social |

### Dashboard Setup (Recommended Tools)
1. **Google Data Studio** (free)
   - Connect: Google Ads, Meta Ads, GA4, Shopify
   - Daily dashboard: ROAS, CVR, CPC, spend, revenue
   
2. **Meta Ads Manager** (native)
   - Campaign performance by age, placement, creative
   - Attribution window: 7-day click
   - Breakdown: Conversions, ROAS, CPC, CTR

3. **Shopify Analytics** (native)
   - Revenue by traffic source
   - Customer data (AOV, repeat rate)
   - Product performance

---

## PART 9: CREATIVE ASSET CHECKLIST

### Required Immediately (Week 1)
- [ ] 3x 15–30 second vertical video ads (hero hook variations)
- [ ] 5x high-res product images (grip on bar, vial detail, person lifting, close-ups)
- [ ] 2x testimonial static graphics (customer name, quote, result)
- [ ] 1x carousel (5 images: problem → solution → proof)

### Required by Week 2
- [ ] 3x age-segment specific ad variations (text + static)
- [ ] 2x video testimonials (customer + coach, 15–30s each)
- [ ] 1x hero landing page banner image (hook + CTA)

### Required by Week 4
- [ ] 10x customer testimonial quotes (with names, titles, photos)
- [ ] 3x before/after graphics (muscle activation, grip strength, visual improvements)
- [ ] 5x reels for organic social (science explainer, bilateral balance, product proof, tips, expert validation)

### Content Audit (Existing Assets in Dropbox)
- **Product images:** Shopify CDN (Oliver to provide URLs)
- **CAD/engineering renders:** SolidWorks files (for spec sheets, comparison visuals)
- **Brand aesthetic reference:** sniperform.com.au (dark gunmetal + teal)

---

## PART 10: BUDGET ALLOCATION (Monthly, 90-Day Build)

### Month 1: Foundation ($3,000 budget)
| Channel | Weekly Budget | Allocation | Focus |
|---------|---------------|-----------|-------|
| **Meta Awareness (Campaign A)** | $140 | 5% | Hook + creative testing |
| **Meta Conversion (Campaign B)** | $700 | 35% | Core performance, 3x creative tests |
| **Meta Retargeting (Campaigns C+D)** | $300 | 15% | Warm + hot audiences |
| **Organic + Email** | $60 | 3% | Design + copywriting |
| **Content Creation** | $100 | 5% | Video production, testimonial collection |
| **Reserve / Optimization** | $600 | 30% | Pause underperformers, scale winners, A/B testing |
| **Tools (CAPI, email, tracking)** | $50 | 2.5% | Software (Klaviyo, tracking, etc.) |

**Total:** $1,950/week = $7,800/month

---

### Month 2: Scale ($8,000 budget)
| Channel | Weekly Budget | Allocation | Focus |
|---------|---------------|-----------|-------|
| **Meta Awareness** | $200 | 5% | 2x lookalike audiences |
| **Meta Conversion (Core)** | $1,300 | 35% | Scale best performers +15% |
| **Meta Retargeting** | $500 | 15% | Warm + hot + cart abandonment |
| **TikTok (test)** | $300 | 8% | New platform test (if setup complete) |
| **Email + Organic** | $200 | 5% | Content calendar + email sequences |
| **Content Creation** | $300 | 8% | Blog posts, video testimonials, organic content |
| **Reserve / Optimization** | $700 | 18% | Rebalance, test, iterate |
| **Tools** | $100 | 2.5% | Software |

**Total:** $3,600/week = $14,400/month (but can dial down to $8K if budget constrained)

---

### Month 3: Optimize ($10,000 budget)
| Channel | Weekly Budget | Allocation | Focus |
|---------|---------------|-----------|-------|
| **Meta (all campaigns)** | $1,800 | 45% | Scale core campaigns, pause underperformers |
| **TikTok (secondary)** | $400 | 10% | Scale if ROAS > 0.50x, else shift to Meta |
| **Organic + Content** | $400 | 10% | Content calendar full-spin, blog SEO, YouTube |
| **Email Marketing** | $100 | 2.5% | Sequences live, list growth |
| **Reserve / Optimization** | $1,100 | 27.5% | Scale winners, test new angles, seasonal campaigns |
| **Tools + Tools** | $200 | 5% | Advanced tracking, attribution, analytics |

**Total:** $4,000/week = $16,000/month (scale back to $10K if needed)

**Note:** Recommended approach is to start at Month 1 budget ($7.8K), scale to Month 2 only after confirming 0.55x+ ROAS, then scale to Month 3.

---

## PART 11: COMPETITIVE ADVANTAGE & DIFFERENTIATION

### vs. Fat Gripz (Primary Competitor)

| Factor | Fat Gripz | Sniperform | Sniperform Win |
|--------|-----------|-----------|-----------------|
| **Thick Grip** | Yes | Yes | Tie |
| **Bilateral Balance Feedback** | No | Yes (patented spirit level) | ✅ Major |
| **Website Design** | ~2008 era, poor UX | Modern Shopify, high-intent | ✅ Large |
| **Guarantee** | 60-day, paid return shipping | 90-day (double pack), both-way shipping | ✅ Better |
| **Science Content** | Good (3 mechanisms) | Better (4 mechanisms, exclusive bilateral balance) | ✅ Edge |
| **Amazon presence** | 16,000+ reviews, huge | None yet | Fat Gripz lead |
| **Brand credibility** | Military + athlete endorsements | None yet (placeholder section) | Fat Gripz lead |
| **Video marketing** | None | Strong creative + landing page | ✅ Major |
| **Conversion mechanics** | None | Bundle upsell, countdown, live counter | ✅ Large |
| **Social proof** | None on site | Testimonials (being collected) | Tie (after testimonials added) |

**Key differentiator:** The **patented spirit level** is Sniperform's moat. Fat Gripz can't copy this. Use this relentlessly in messaging.

---

## PART 12: RED FLAGS & RISK MITIGATION

### Risk 1: Pixel Data Quality (High Impact)
**Issue:** CAPI not configured = Meta doesn't see conversions = budget wasted on non-converting audiences  
**Mitigation:** 
- Enable CAPI Week 1 (non-negotiable)
- Test: Make 5 test purchases, verify each appears in Meta Conversion API within 30 mins
- Monitor: Check Meta Events Manager daily Week 1–2

### Risk 2: Tracking Attribution (Medium Impact)
**Issue:** TikTok UTM templates broken = can't measure TikTok ROAS  
**Mitigation:**
- Fix UTM structure Week 1: `?utm_source=tiktok&utm_medium=paid&utm_campaign=awareness`
- Test: Post link in comments, click through, verify UTM parameters in GA4
- Delay TikTok spend until tracking confirmed

### Risk 3: Budget Rebalancing Misfire (Medium Impact)
**Issue:** Moving 14% of spend from 25–34 to 55–64 age bracket could hurt volume  
**Mitigation:**
- Gradual rebalance: Shift 1–2% per week, not all at once
- Monitor ROAS + volume daily Week 3–4
- If 55–64 ROAS drops below 0.40x, revert shift

### Risk 4: Tablet Rendering Bug (High Impact on Conversion)
**Issue:** 2,100 sessions with zero conversions likely = broken checkout on tablet  
**Mitigation:**
- Test Week 1 on iPad + Android tablet yourself
- QA checklist: form fields, CTA buttons (min 44px), checkout flow, payment processor loading
- Deploy fix before launching retargeting (which will drive more mobile traffic)

### Risk 5: Creative Fatigue (Medium Impact)
**Issue:** Over-exposure to same creative → declining CTR + ROAS  
**Mitigation:**
- Rotate creative every 2–3 weeks
- Publish 3–4 new ad variations per week
- Monitor frequency cap: If average frequency > 3, refresh creative

### Risk 6: Competitor Response (Low-Medium Impact)
**Issue:** Fat Gripz could copy Sniperform's messaging or improve their ads  
**Mitigation:**
- Move fast in Months 1–2 (establish market position + brand recognition)
- Focus on **bilateral balance messaging** (their IP moat — Fat Gripz can't compete here)
- Build customer testimonials + email list early (sticky, defensible)

---

## PART 13: SUCCESS CHECKLIST (90 Days)

### Week 1–2: Foundation ✓
- [ ] CAPI configured + tested
- [ ] GA4 purchase tracking verified
- [ ] Homepage campaigns paused
- [ ] Campaign B (Core Conversion) launched with 3x creative tests
- [ ] Campaign A (Awareness) launched
- [ ] Tablet rendering bug fixed
- [ ] 5+ customer testimonials collected

### Week 3–4: Retargeting & Landing Page ✓
- [ ] Campaigns C + D (Retargeting) live
- [ ] Landing page testimonials updated (real names, credentials, photos)
- [ ] Hero copy A/B test live
- [ ] Live visitor counter + stock countdown added
- [ ] Lead magnet (free PDF) created + email Sequence 1 launched
- [ ] Email subscribers +200–300

### Week 5–8: Content & Authority ✓
- [ ] 2x long-form blog posts published
- [ ] 10+ customer testimonials collected (mix of text + video)
- [ ] 4x age-segment specific ad variations running
- [ ] Email Sequences 2 + 3 (Post-Purchase + Cart Abandonment) live
- [ ] 15+ organic content pieces published (reels, carousels, shorts)
- [ ] ROAS 0.50x–0.65x sustained
- [ ] Email subscribers +800–1,000

### Week 9–12: Scale ✓
- [ ] ROAS 1.0x–1.2x achieved
- [ ] Daily ad spend increased to $200–250 (sustainable)
- [ ] Lookalike audiences (1%, 5%) tested + scaled if profitable
- [ ] TikTok secondary channel tested (if ROAS > 0.50x)
- [ ] Content calendar running (4–6 pieces/week organic)
- [ ] Email list 2,000+ subscribers
- [ ] Conversion rate 1.2–1.8% sustained
- [ ] Monthly revenue from paid $8,000–$12,000

---

## APPENDIX: IMPLEMENTATION PRIORITY MATRIX

**High Priority (Do in Week 1–2):**
1. Enable CAPI on Shopify ⭐⭐⭐ (biggest impact on data quality + optimization)
2. Pause homepage campaigns ⭐⭐⭐ (stop wasting budget)
3. Fix tablet rendering bug ⭐⭐⭐ (already losing 2,100 conversions)
4. Launch core conversion campaign (Campaign B) ⭐⭐⭐ (revenue generation)
5. Collect real testimonials ⭐⭐ (needed for Week 2 landing page update)

**Medium Priority (Weeks 2–4):**
1. Launch retargeting campaigns ⭐⭐ (huge untapped lever)
2. A/B test hero copy ⭐⭐ (optimize top of funnel)
3. Set up email lead magnet + sequences ⭐⭐ (build owned audience)
4. Create 4x age-segment ad variations ⭐ (micro-optimize spend)

**Lower Priority (Weeks 4+):**
1. Blog content calendar (important but scales slower)
2. Organic social growth (supports paid, not core driver Month 1)
3. TikTok as secondary channel (only if Meta performing well)

---

## CONTACT & NEXT STEPS

**Owner:** Oliver (Sniperform)  
**Primary store:** sniperform.com (US)  
**Secondary store:** sniperform.com.au (AU) — not part of this plan

### Immediate Actions (This Week)
1. Grant agency/marketer access to:
   - Meta Business Manager (Ads Manager + Events Manager)
   - Shopify + Shopify app store (for CAPI configuration)
   - Google Analytics 4
   - Hotmail/email account for testimonial outreach
2. Share Shopify product CDN URLs (for ad creative)
3. Confirm budget allocation + approval for Month 1 ($7.8K)
4. Identify 5–10 existing customers for testimonial collection

### Week 1 Kickoff
- CAPI setup + testing
- Creative production begins (3x hero videos, testimonial collection)
- Campaign structure built (audiences, pixel events, creative assignments)
- Core conversion campaign launches

---

**Plan prepared for overnight execution. Ready to scale Sniperform's USA market presence.**
