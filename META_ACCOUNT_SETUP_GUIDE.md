# Sniperform USA — Meta Account Setup Guide
**Step-by-step for Madigix or in-house team**

---

## PART 1: PREREQUISITES & VERIFICATION

### Before You Start
You need access to:
- [ ] **Shopify admin** (to set up Meta Pixel and CAPI)
- [ ] **Meta Business Manager** account (facebook.com/business/manager)
- [ ] **Meta Ads Manager** (ads.facebook.com)
- [ ] **Google Analytics 4** (to verify conversions)

### Accounts to Confirm
- [ ] **Shopify store:** sniperform.com (US store, not AU)
- [ ] **Meta Business Account:** Sniperform USA
- [ ] **Pixel ID:** (you should already have one, verify it exists)
- [ ] **Conversion window settings:** Should be 7-day click (or 7d view+click)

---

## PART 2: ENABLE CONVERSIONS API (CAPI) — CRITICAL

**Why:** CAPI sends server-side purchase data to Meta, fixing iOS/privacy tracking gaps. Without this, Meta sees only 30–50% of actual conversions.

**Time:** 15 minutes

### Step 1: Log in to Shopify Admin

```
Go to: sniperform.com/admin
Log in with your credentials
```

### Step 2: Navigate to Apps & Integrations

```
Left sidebar → Settings (bottom)
Click → Apps and integrations
```

### Step 3: Search for Meta Pixel

```
Search bar: "Meta Pixel"
Click the official app (by Meta Platforms Inc.)
Click: "Add app"
```

### Step 4: Authorize Meta Pixel

```
You'll see a popup asking for permissions
Click: "Allow" or "Authorize"
Shopify will connect to your Meta account automatically
```

### Step 5: Enable Conversions API

Once inside the Meta Pixel app:
```
Look for: "Conversions API" toggle or "Enable server-side tracking"
Toggle it: ON
Click: Save
```

✅ **CAPI is now enabled.** Shopify will automatically send purchase data to Meta.

### Step 6: Verify It's Working (Do This!)

**This is critical — don't skip this step.**

1. **Go to your Shopify store** (incognito mode, different device if possible)
   ```
   Visit: sniperform.com
   ```

2. **Buy a test product**
   - Go through full checkout
   - Use test card: `4242 4242 4242 4242`
   - Any future expiration date
   - Any CVC (e.g., 123)
   - Complete purchase

3. **Wait 30 seconds**

4. **Go to Meta Events Manager**
   ```
   business.facebook.com → Events Manager
   Select your pixel
   Look for: "Test Events" tab
   ```

5. **Verify the purchase event appears**
   - You should see your test purchase within 1–2 minutes
   - Event type: "Purchase"
   - Value: $59.95 (or however much the test product cost)
   - Status: "Verified" ✅

**If you see the event:** CAPI is working. ✅ Continue.

**If you DON'T see the event:** CAPI setup failed. Troubleshoot:
- Verify Meta Pixel app is installed in Shopify
- Check that Conversions API toggle is ON
- Try purchasing again
- Wait 5 minutes and refresh
- If still not working, contact Meta support or Madigix

---

## PART 3: FIX CAMPAIGN STRUCTURE

### Step 1: Audit Current Campaigns

**Go to:** Meta Ads Manager → Campaigns

**For EACH campaign, check:**
1. **Campaign name** — Is it clear what this campaign does?
2. **Campaign objective** — Should be "Conversions" (not "Awareness" or "Traffic")
3. **Destination URL** — Where does traffic go?
4. **Budget** — Daily or lifetime? How much?
5. **Status** — Active or paused?

### Step 2: Identify & Pause Homepage Campaigns

**Red flag:** Any campaign sending traffic to `sniperform.com` (homepage) instead of landing page

**Action:**
1. Find campaigns with homepage destination
2. Click campaign → Edit
3. Change destination URL to: `sniperform.com/[landing-page-url]`
   - (Ask Oliver for the exact landing page URL)
4. Click Save

**Or, if homepage campaigns are underperforming (ROAS < 0.25x):**
1. Click campaign
2. Click "Pause campaign"
3. Reallocate budget to landing page campaigns

### Step 3: Set Conversion Window to 7-Day

**This is important for accurate ROAS tracking.**

**For EACH active campaign:**
1. Click campaign name
2. Click "Edit"
3. Scroll to: "Attribution Window" or "Conversion Window"
4. Change from "1-day click" to "7-day click" (or "7d view + click" if available)
5. Click "Save"

**Why:** Many sales happen 3–7 days after the initial ad click. 1-day window undercounts conversions.

---

## PART 4: CREATE CORE CAMPAIGNS

### Campaign Structure Template

You should have these **5 campaigns** running in parallel:

#### **Campaign A: AWARENESS**
- **Objective:** Video Views (or Reach)
- **Audience:** Broad + 1% Lookalike (purchasers)
- **Daily budget:** $30–40
- **Destination:** Landing page (awareness → clicks, not conversions)
- **Creative:** Attention-grabbing videos (spirit level in action, big lift, hook text)

**Setup steps:**
1. Create new campaign
2. Choose objective: "Video Views" (not Conversions)
3. Name it: "AWARENESS — Video Hooks"
4. Set daily budget: $35
5. Create ad set (see "Audience Setup" section below)

---

#### **Campaign B: CONVERSION (CORE)**
- **Objective:** Conversions
- **Audience:** 3x audience stacks (see below)
- **Daily budget:** $100–150 (main spend here)
- **Destination:** Landing page (optimized for conversions)
- **Creative:** 3x hero hook tests (Control + 2 variants)

**Setup steps:**
1. Create new campaign
2. Choose objective: "Conversions"
3. Name it: "CONVERSION — Hero Hooks Test"
4. Set daily budget: $125
5. Create 3 ad sets (one per audience stack)

---

#### **Campaign C: RETARGETING — WARM**
- **Objective:** Conversions
- **Audience:** Website visitors (30 days)
- **Daily budget:** $40–60
- **Destination:** Landing page
- **Creative:** Social proof, guarantee messaging

**Setup steps:**
1. Create new campaign
2. Choose objective: "Conversions"
3. Name it: "RETARGETING — Warm (Visitors)"
4. Set daily budget: $50
5. Create audience (website visitors, last 30 days)

---

#### **Campaign D: RETARGETING — HOT**
- **Objective:** Conversions
- **Audience:** Add-to-Cart + Initiate Checkout (7 days)
- **Daily budget:** $20–30
- **Destination:** Landing page
- **Creative:** Scarcity, countdown, urgency

**Setup steps:**
1. Create new campaign
2. Choose objective: "Conversions"
3. Name it: "RETARGETING — Hot (ATC + Init Checkout)"
4. Set daily budget: $25
5. Create 2 audiences:
   - Audience 1: Add-to-Cart (last 7 days)
   - Audience 2: Initiate Checkout (last 7 days)

---

#### **Campaign E: LOYALTY (Optional, Phase 2)**
- **Objective:** Conversions
- **Audience:** Purchasers (90 days)
- **Daily budget:** $20–30
- **Destination:** Landing page (bundle upsell section)
- **Creative:** "Upgrade to double pack + free shaker"

**Setup steps:**
1. Create new campaign (after initial campaigns are running well)
2. Choose objective: "Conversions"
3. Name it: "LOYALTY — Bundle Upsell"
4. Set daily budget: $25
5. Create audience: Purchasers (last 90 days)

---

## PART 5: AUDIENCE SETUP

### Audience 1: Fitness Enthusiast (Primary)

**Go to:** Meta Ads Manager → Audiences → Create Audience

**Settings:**
```
Location: United States (all states)
Age: 25–64
Gender: All
Languages: English

Interests:
✓ Gym
✓ Fitness
✓ Strength Training
✓ Bodybuilding
✓ CrossFit
✓ Personal Training
✓ Fitness Equipment
✓ Fitness Brands

Behaviors:
✓ Fitness & Wellness

Devices: All (desktop, mobile, tablet)

Detailed Targeting Expansion: OFF
```

**Name:** "Fitness Enthusiast 25-64"

**Save this audience** (you'll use it in Campaign B, ad set 1)

---

### Audience 2: Strength Sport Athlete

**Go to:** Meta Ads Manager → Audiences → Create Audience

**Settings:**
```
Location: United States (all states)
Age: 25–54
Gender: All
Languages: English

Interests:
✓ Powerlifting
✓ Weightlifting
✓ CrossFit
✓ Strength & Conditioning
✓ Fitness Coaching

Behaviors:
✓ Fitness Equipment purchases (last 90 days) [if available]

Devices: Mobile + Desktop

Detailed Targeting Expansion: OFF
```

**Name:** "Strength Sport Athlete 25-54"

**Save this audience**

---

### Audience 3: Lookalike (1% Based on Purchasers)

**Go to:** Meta Ads Manager → Audiences → Create Audience → Lookalike

**Settings:**
```
Source audience: All purchasers (custom audience based on Shopify purchases)
Countries: United States
Lookalike size: 1% (highest similarity)
```

**Name:** "Lookalike 1% — Purchasers"

**Save this audience**

---

### Audience 4: Website Visitors (for Retargeting)

**Go to:** Meta Ads Manager → Audiences → Create Audience → Custom Audience

**Settings:**
```
Source: Website
Data source: Your Pixel
Event: All website visitors
Time window: Last 30 days
Exclude: People who already purchased
```

**Name:** "Website Visitors 30d (Non-Purchaser)"

**Save this audience**

---

### Audience 5: Add-to-Cart (for Hot Retargeting)

**Go to:** Meta Ads Manager → Audiences → Create Audience → Custom Audience

**Settings:**
```
Source: Website
Data source: Your Pixel
Event: Add to cart
Time window: Last 7 days
Exclude: People who already purchased
```

**Name:** "Add-to-Cart 7d"

**Save this audience**

---

### Audience 6: Initiate Checkout (for Hot Retargeting)

**Go to:** Meta Ads Manager → Audiences → Create Audience → Custom Audience

**Settings:**
```
Source: Website
Data source: Your Pixel
Event: Initiate checkout
Time window: Last 7 days
Exclude: People who already purchased
```

**Name:** "Initiate Checkout 7d"

**Save this audience**

---

## PART 6: CREATIVE SETUP

### Creative Test Matrix (Campaign B: Core Conversion)

**You need 3 ad creatives:**

#### Creative 1: CONTROL — "Thicker Grips = Bigger Arms"
- **Format:** Vertical video (9:16 aspect ratio)
- **Length:** 15–30 seconds
- **Hook (0–3s):** "Thicker grips = bigger arms" (text + voiceover)
- **Proof (3–15s):** Show spirit level vial on bar, person lifting heavy, stable grip
- **Results (15–30s):** Before/after muscle activation, person flexing arm
- **CTA (last 2s):** "Learn how" (soft CTA, not aggressive)
- **Sound:** Music + voiceover OR silent with captions

#### Creative 2: VARIANT A — "Your Left Arm is Weaker"
- **Format:** Vertical video (9:16)
- **Length:** 15–30 seconds
- **Hook (0–3s):** "Your left arm is weaker. You don't even know it."
- **Proof (3–15s):** Split-screen showing uneven pull, spirit level reveals imbalance
- **Results (15–30s):** Same person corrects imbalance, even bar path
- **CTA:** "Discover the imbalance" (curiosity-based)

#### Creative 3: VARIANT B — "Grip is Holding You Back"
- **Format:** Vertical video (9:16)
- **Length:** 15–30 seconds
- **Hook (0–3s):** "Grip is holding you back. Here's the fix."
- **Proof (3–15s):** Person struggles to hold weight (grip fails), frustrated
- **Results (15–30s):** Same person with thick grip, lifts easily, controlled, powerful
- **CTA:** "Unlock more strength"

### Upload Creatives to Meta

**Go to:** Meta Ads Manager → Ad Creative Library

**For each video:**
1. Click "Create"
2. Upload video file (MP4, MOV, etc.)
3. Add text overlay/captions
4. Add headline + ad copy
5. Save as "Ad Creative"

**Then assign to ad sets** (see Campaign Setup below)

---

## PART 7: PIXEL EVENTS & CONVERSION TRACKING

### Standard Events to Track

Meta should auto-track these on your Shopify store:

| Event | When fired | Use |
|-------|-----------|-----|
| **PageView** | Every page load | Audience building |
| **ViewContent** | Product page viewed | Warm audience |
| **AddToCart** | Add to cart clicked | Hot audience |
| **InitiateCheckout** | Checkout started | Hot audience (retarget) |
| **AddPaymentInfo** | Payment info added | Very hot audience |
| **Purchase** | Order completed | Conversion + loyalty audience |

**Verify these are firing:**
1. Go to Meta Events Manager
2. Click your Pixel
3. Go to "Test Events"
4. Visit your website and take the actions above
5. You should see events populate in real-time

**If events aren't firing:**
- Verify CAPI is enabled (see Part 2)
- Check Shopify Meta Pixel app is active
- Clear browser cache and try again
- Wait 5 minutes and refresh

---

## PART 8: CAMPAIGN SETUP WALKTHROUGH

### Creating Campaign B (Core Conversion) — Step by Step

**Navigate to:** Meta Ads Manager → Create Campaign

#### Step 1: Campaign Settings
```
Campaign objective: Conversions
Campaign name: CONVERSION — Hero Hooks Test
Special ads categories: [Leave blank unless applicable]
```

#### Step 2: Campaign Budget & Scheduling
```
Budget type: Daily budget
Daily budget: $125
Start date: [Today or tomorrow]
End date: [Leave blank for ongoing]
Bid strategy: Automatic bids (Meta chooses lowest cost per conversion)
```

#### Step 3: Create Ad Set 1 (Audience 1: Fitness Enthusiast)
```
Ad set name: AUDIENCE 1 — Fitness Enthusiast
Conversion event: Purchase
Audience: Select "Fitness Enthusiast 25-64" (created above)
Placements: Automatic (Meta shows your ads where they perform best)
Placement options: Instagram Feed, Instagram Stories, Facebook Feed, Facebook Stories, Audience Network, In-Stream Videos
Languages: English
```

**Budget allocation:**
- Total daily budget: $125
- Split across 3 ad sets: ~$42/day each
- (Or allocate 50% to Audience 1, 25% to Audience 2, 25% to Audience 3)

#### Step 4: Create Ad (Assign Creative)
```
Format: Single Image or Video
Creative: Select "Creative 1 — Thicker Grips (Control)" [uploaded earlier]
Headline: "Thicker grips = bigger arms"
Ad copy: "Join 5,000+ lifters who are getting bigger arms. See how the pros do it."
Display link: sniperform.com
Call to action button: "Learn More"
Landing page: [Landing page URL]
```

#### Step 5: Review & Launch
```
Review all settings
Click: "Create Campaign"
Wait for approval (usually 1 hour)
Monitor performance
```

**Repeat steps 3–5 for:**
- Ad Set 2: Audience 2 (Strength Sport Athlete) + Creative 2 (Variant A)
- Ad Set 3: Audience 3 (Lookalike 1%) + Creative 3 (Variant B)

---

## PART 9: DAILY MANAGEMENT & OPTIMIZATION

### Weekly Checklist

**Monday (Report Day):**
- [ ] Check ROAS, CVR, CPC, CPM for each campaign (last 7 days)
- [ ] Identify underperformers (ROAS < 0.25x)
- [ ] Note top-performing creatives/audiences

**Wednesday (Optimization):**
- [ ] Pause campaigns with ROAS < 0.25x
- [ ] Increase budget for campaigns with ROAS > 0.50x (+10–15%)
- [ ] Implement any feedback from previous week

**Friday (Testing):**
- [ ] Launch new creative tests (if fresh content ready)
- [ ] Monitor new campaigns for initial performance
- [ ] Audit landing page (any issues?)

### Key Metrics to Monitor

| Metric | What it means | Action |
|--------|---------------|--------|
| **ROAS < 0.25x** | Campaign losing money | Pause or audit creative |
| **ROAS 0.25–0.50x** | Underperforming, but salvageable | Test new creative, audience |
| **ROAS 0.50–0.75x** | On track, but room to improve | Keep running, optimize bids |
| **ROAS 0.75–1.0x** | Healthy performance | Scale budget +10–15% |
| **ROAS > 1.0x** | Winning campaign | Scale aggressively +15–25% |

---

## PART 10: TROUBLESHOOTING

### Issue: CAPI Not Working

**Symptoms:** Events not showing in Events Manager

**Solutions:**
1. Verify Meta Pixel app is installed (Shopify Admin > Apps)
2. Verify Conversions API toggle is ON
3. Check that your pixel ID matches in Shopify
4. Make a test purchase, wait 2–3 minutes
5. Clear cache and refresh Events Manager
6. Contact Meta support if still broken

---

### Issue: Campaigns Not Approving

**Symptoms:** Campaign stuck in "Pending Review"

**Solutions:**
1. Check for policy violations (landing page content)
2. Verify ad copy is clear and honest
3. Check that CTA button is present
4. Wait 24 hours (Meta has review queue)
5. Contact Meta support if >24h

---

### Issue: Very High CPC ($2+), Low CTR

**Symptoms:** Ads expensive, nobody clicking

**Solutions:**
1. **Audience too broad:** Narrow targeting (use Audience 1 or 2, not broad)
2. **Creative weak:** Test new hook copy or video
3. **Placement issues:** Check if Instagram Reels performing worse than Feed
4. **Frequency too high:** People are seeing ad too many times, ignore it
   - Solution: Create new creative variations
5. **Landing page broken:** Audit on mobile, check loading time

---

### Issue: Low Conversion Rate (< 0.3%)

**Symptoms:** Traffic coming, but not converting

**Solutions:**
1. **Landing page issues:**
   - Test on mobile/tablet (check tablet rendering bug)
   - Verify form is simple (not asking too many questions)
   - Verify CTA button is visible above the fold
2. **Audience mismatch:** Are you showing the right offer to the right people?
3. **Trust signals missing:** Add testimonials, guarantee, social proof to landing page
4. **Price objection:** Maybe $60 is too high for this audience
   - Test lower-price bundle or payment plan

---

## PART 11: QUARTERLY OPTIMIZATION

### Month 1 Goals
- ✅ CAPI working
- ✅ All campaigns live
- ✅ 3x creative tests running
- ✅ ROAS 0.35–0.50x

### Month 2 Goals
- ✅ Campaigns optimized (underperformers paused)
- ✅ Budget rebalanced by age bracket
- ✅ Retargeting campaigns live (Campaigns C + D)
- ✅ ROAS 0.50–0.75x
- ✅ CAPI validated + data quality confirmed

### Month 3 Goals
- ✅ Budget increased (revenue supports it)
- ✅ Secondary channels tested (TikTok, YouTube)
- ✅ Email sequences running (supporting paid)
- ✅ ROAS 0.75–1.0x+

---

## FINAL CHECKLIST (Before Launching)

- [ ] **CAPI enabled and tested** (saw test purchase in Events Manager)
- [ ] **Landing page URL verified** (all campaigns point to correct URL)
- [ ] **5 campaigns created** (or at least Campaigns A + B to start)
- [ ] **6 audience stacks created** (3 for core campaign, 3 for retargeting)
- [ ] **3 creative assets uploaded** (hook variations)
- [ ] **Conversion event set to Purchase** (not "Leads" or other)
- [ ] **Conversion window set to 7-day click** (or 7d view+click)
- [ ] **Budget allocated correctly** (total ~$150–200/day Month 1)
- [ ] **Landing page mobile tested** (loads fast, checkout works)
- [ ] **Testimonials on landing page** (at least 5, with photos)

**Once all boxes are checked, launch and monitor daily for first week.**

---

## SUPPORT & QUESTIONS

If Madigix has questions or blockers:
1. Reference this guide for setup steps
2. Check Meta's official documentation (business.facebook.com/help)
3. Contact Meta support (blue "?" icon in Ads Manager)
4. Reach out to Oliver for landing page questions or creative briefs

---

**Setup time estimate: 3–4 hours for someone new to Meta.**  
**Ongoing management: 2–3 hours per week.**

**Let's make this work.** 🚀

