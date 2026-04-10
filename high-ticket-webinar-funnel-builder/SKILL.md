---
name: high-ticket-webinar-funnel-builder
description: "Complete playbook for building high-ticket info product launches. Covers webinar funnels, GHL CRM automation, sales scripting, ad campaigns, and full go-to-market infrastructure. Use when planning or building launches for courses, coaching, masterminds, certification programs, and premium training offers."
---

# High-Ticket Webinar & Funnel Builder

This skill enables any bot to plan, build, and optimize a complete high-ticket info product launch, from webinar funnel to CRM automation to ad campaigns. Based on InfoPros' methodology for clients selling digital courses, coaching programs, and premium training.

---

## Who This Is For

Businesses selling high-ticket info products ($500-$10k+):
- Online courses and digital training programs
- Coaching and consulting packages
- Masterminds and group programs
- Certification programs
- Done-with-you / done-for-you services

---

## Phase 1: Offer Architecture

Before building anything, nail the offer.

### Offer Definition Checklist
- **Product:** What exactly is being sold? (course, coaching, hybrid)
- **Price point:** What's the ticket price? ($997, $2,997, $5,000+)
- **Delivery model:** Self-paced, live cohort, 1-on-1, group, hybrid
- **Timeline:** How long is the program? (6 weeks, 90 days, 12 months)
- **Guarantee:** What's the risk reversal? (30-day, results-based, conditional)
- **Ideal client:** Who gets the BEST results from this program?
- **Transformation:** What's the before/after? What specific outcome?

### Pricing Psychology for High-Ticket
- Under $1,000: Can sell directly from a webinar or VSL
- $1,000-$3,000: Webinar to application to sales call
- $3,000-$10,000: Webinar/VSL to application to sales call (mandatory)
- $10,000+: Multi-touch (webinar + nurture + call + possibly second call)

### Offer Stack Framework
Build the offer stack for the webinar pitch:
1. **Core program** (the main deliverable)
2. **Bonus 1:** Fast-start / quick win (removes "where do I start?" objection)
3. **Bonus 2:** Templates / swipe files (removes "I don't know how" objection)
4. **Bonus 3:** Community access (removes "I'll be alone" objection)
5. **Bonus 4:** Live support / Q&A (removes "what if I get stuck" objection)
6. **Price anchor:** Total value = 5-10x the actual price
7. **Urgency layer:** Deadline, limited spots, bonus expiration, price increase

---

## Phase 2: Webinar Funnel Architecture

### Funnel Pages (build in GHL)

**Page 1: Registration Page**
- Headline: Problem-aware hook (what they want + implied method)
- Subheadline: Specific outcome + timeframe
- Bullet points: 3-5 things they'll learn (curiosity-driven, not answers)
- Registration form: Name, email, phone (phone optional but recommended for SMS follow-up)
- Social proof: testimonials, logos, "X people registered"
- Urgency: "Live on [date]" or "Limited replay available for 48 hours"

**Page 2: Thank You / Confirmation Page**
- Confirm registration
- Add-to-calendar links (Google Cal, iCal, Outlook)
- "What to expect" section
- Optional: Self-liquidating offer (SLO) - low-ticket ($27-$97 tripwire to offset ad costs)
- Share buttons (refer a friend)

**Page 3: Webinar Room / Replay Page**
- Live: Embed webinar platform (WebinarJam, EverWebinar, Zoom, StreamYard)
- Replay: Embedded video with CTA below
- Chat/Q&A sidebar (live only)
- CTA button below video: "Apply Now" or "Book Your Call"
- Countdown timer for replay expiration

**Page 4: Application Page**
- 5-10 qualifying questions:
  1. What's your current situation? (where they are now)
  2. What's your goal? (where they want to be)
  3. What have you tried before? (establishes pain + eliminates tire kickers)
  4. What's your timeline? (urgency filter)
  5. What's your investment capacity? (budget qualifier)
  6. Are you the decision maker? (closes spouse objection early)
  7. Phone number + best time to reach
- Submit button: "Apply for [Program Name]"

**Page 5: Booking Page**
- Calendar embed (GHL calendar or Calendly)
- "You've been accepted" messaging
- Photo of the coach/team
- What to expect on the call
- Testimonials from people who booked calls

**Page 6: Sales Page (for those who skip webinar)**
- Long-form VSL or sales letter
- Full offer stack
- FAQ section
- Testimonials and case studies
- Multiple CTA buttons throughout

### Funnel Flow Diagram
```
Ad Click
  -> Registration Page (opt-in)
    -> Thank You Page (confirmation + SLO)
      -> Email/SMS reminders (pre-webinar sequence)
        -> Webinar (live or replay)
          -> Application Page (qualifying questions)
            -> Booking Page (calendar)
              -> Sales Call
                -> Close / Follow-up
```

---

## Phase 3: GHL CRM Automation

### Pipeline Stages (build in GHL)

```
Pipeline: [Client Name] - Webinar Funnel
  Stage 1: Registered (just opted in)
  Stage 2: Attended (watched webinar, live or replay)
  Stage 3: Applied (submitted application)
  Stage 4: Booked (scheduled a call)
  Stage 5: Showed (attended the call)
  Stage 6: Pitched (received the offer)
  Stage 7: Closed Won (purchased)
  Stage 8: Closed Lost (declined)
  Stage 9: No Show (missed call, needs rebooking)
  Stage 10: Follow-Up (needs nurture sequence)
```

### Automation Workflows

**Workflow 1: Registration Confirmation**
- Trigger: Form submission on registration page
- Actions:
  1. Create/update contact in GHL
  2. Add to pipeline Stage 1 (Registered)
  3. Send confirmation email (subject: "You're in! Here's your webinar link")
  4. Send confirmation SMS (if phone provided)
  5. Tag: "webinar-registered"
  6. Add to pre-webinar email sequence

**Workflow 2: Pre-Webinar Nurture**
- Trigger: Tag "webinar-registered" added
- Email sequence (if live webinar):
  - Immediately: Confirmation + what to expect
  - 24 hours before: "Tomorrow's the day" reminder
  - 1 hour before: "We start in 60 minutes" + link
  - 15 minutes before: "Starting NOW" + direct link
- Email sequence (if evergreen):
  - Immediately: "Your replay is ready" + link
  - 12 hours later: "Did you catch the training?"
  - 24 hours later: "Replay expires in 24 hours" (urgency)

**Workflow 3: Post-Webinar Follow-Up**
- Trigger: Webinar attended (webhook or manual tag)
- Actions:
  1. Move to Stage 2 (Attended)
  2. Tag: "webinar-attended"
  3. Send email: "Thanks for joining. Here's the next step" + application link
  4. Send SMS: "Great seeing you on the training! Apply here: [link]"
  5. If no application in 24h: reminder email
  6. If no application in 48h: urgency email ("spots filling up")
  7. If no application in 72h: final push + direct reply CTA

**Workflow 4: Application Submitted**
- Trigger: Application form submission
- Actions:
  1. Move to Stage 3 (Applied)
  2. Tag: "application-submitted"
  3. Send email: "Application received. Book your strategy call"
  4. Send SMS with booking link
  5. Internal notification to sales team (email or Slack)
  6. If not booked in 2h: SMS follow-up
  7. If not booked in 24h: email + SMS combo
  8. If not booked in 48h: phone call task assigned to sales rep

**Workflow 5: Call Booked**
- Trigger: Calendar booking
- Actions:
  1. Move to Stage 4 (Booked)
  2. Tag: "call-booked"
  3. Send confirmation email with call details
  4. Send SMS confirmation
  5. 24h before: reminder email
  6. 1h before: SMS reminder with meeting link
  7. Assign contact to specific sales rep

**Workflow 6: No-Show Recovery**
- Trigger: Call marked as no-show (manual or automated)
- Actions:
  1. Move to Stage 9 (No Show)
  2. Tag: "no-show"
  3. Immediately: SMS "We missed you! Here's a link to rebook"
  4. 1h later: Email with rebooking link
  5. 24h later: "Last chance to grab your spot" SMS
  6. If no rebook in 72h: Move to Follow-Up stage

**Workflow 7: Post-Call Follow-Up (didn't close)**
- Trigger: Moved to Stage 8 (Closed Lost)
- Actions:
  1. Tag with objection reason (price, timing, spouse, not ready)
  2. Enter objection-specific nurture sequence
  3. Price objection: payment plan offer in 48h
  4. Timing objection: check back in 2 weeks
  5. Spouse objection: invite to watch replay together + rebook
  6. Not ready: long-term nurture (weekly value emails for 90 days)

**Workflow 8: Closed Won - Onboarding**
- Trigger: Moved to Stage 7 (Closed Won)
- Actions:
  1. Tag: "client-[program-name]"
  2. Remove from all sales sequences
  3. Send welcome email with onboarding instructions
  4. Send SMS: "Welcome to the family!"
  5. Create task for onboarding team
  6. Add to client community (Skool, Facebook Group, Discord)

---

## Phase 4: Webinar Script Framework

### The Perfect Webinar Structure (90 minutes)

**Opening (5 min)**
- Pattern interrupt: Start with a bold claim or contrarian statement
- Promise: "By the end of this training, you'll know exactly how to [specific outcome]"
- Credibility: Brief story of your results (not a full bio dump)
- Rules: "Stay to the end, take notes, be ready to take action"

**The Hook / Origin Story (10 min)**
- Where you were (relatable struggle)
- The turning point (discovery moment)
- Where you are now (proof it works)
- Key insight: "I realized [the big idea]"

**Content Section 1: The Framework (15 min)**
- Teach your proprietary framework/method
- Give it a name (e.g., "The 5-Step Ascension Model")
- Explain WHAT to do, not HOW (the how is in the program)
- Use case studies and examples
- Each step should create an "aha" moment

**Content Section 2: Proof & Case Studies (10 min)**
- 3-5 client results (diverse: different starting points, industries, timelines)
- Screenshot testimonials, video testimonials, before/after metrics
- "If [client name] can do it starting from [bad situation], you can too"

**Content Section 3: The Problem with DIY (10 min)**
- Address why they can't do this alone
- Time cost of figuring it out yourself
- Money cost of mistakes
- Opportunity cost of waiting
- "You can either spend 2 years and $50K figuring this out, or..."

**The Transition (5 min)**
- "I have something that will shortcut this entire process for you"
- Bridge from free content to the paid offer
- "Would it be okay if I shared how I can help you implement this?"

**The Pitch (20 min)**
- Reveal the program name
- Walk through the offer stack (each component with value)
- Stack the value: show total value vs. price
- Reveal the price (anchor high, then reveal actual)
- Payment plan option
- Guarantee / risk reversal
- Urgency: deadline, limited spots, bonus expiration
- Clear CTA: "Click the button below to apply"

**Q&A / Objection Handling (15 min)**
- Pre-seed common objections during the content
- Address the top 5 objections:
  1. "I don't have the money" -> Payment plan + ROI math
  2. "I don't have the time" -> Time cost of NOT doing it
  3. "I need to think about it" -> What's there to think about? + Urgency
  4. "I need to talk to my spouse" -> Watch replay together + rebook
  5. "Will this work for me?" -> Case study of someone similar
- End with final CTA and countdown

---

## Phase 5: Sales Call Script

### Discovery Call Framework (45-60 min)

**Rapport (3 min)**
- Small talk, find common ground
- "Tell me a little about yourself and your business"

**Situation (10 min)**
- "What's your current situation with [topic]?"
- "How long have you been dealing with this?"
- "What have you tried before?"
- "Why didn't those things work?"

**Pain (10 min)**
- "What's this costing you right now?" (money, time, stress, opportunity)
- "If nothing changes in the next 6-12 months, where do you end up?"
- "How does this affect [their family/health/business/confidence]?"
- Let them sit in the pain. Don't rush to fix it.

**Desire (5 min)**
- "If you could wave a magic wand, what would your [topic] look like?"
- "What would that mean for your [life/business/family]?"
- "On a scale of 1-10, how committed are you to making this happen?"

**Bridge (5 min)**
- "Based on what you've told me, I think we can help. Let me explain how."
- Walk through the program as it applies to THEIR situation
- "For you specifically, this would mean [personalized outcome]"

**Present (10 min)**
- Program details mapped to their pain points
- "Remember when you said [pain point]? This module specifically addresses that"
- Offer stack with personalized framing
- Price presentation: "The investment is [price]"
- Payment plan: "We also have a payment plan of [X]/month for [Y] months"

**Close (10 min)**
- "So, what questions do you have?"
- Handle objections using the Feel-Felt-Found method
- "Is this something you'd like to move forward with?"
- If yes: Take payment, send welcome materials
- If no: "What would need to be different for this to be a yes?"
- If maybe: "I understand. The offer is valid until [deadline]. Let me send you the details."

### Common Objection Rebuttals

**"It's too expensive"**
- "I understand. Can I ask, what were you expecting the investment to be?"
- "If this program delivered [their stated goal], would it be worth [price]?"
- "We have a payment plan that breaks it down to [$/month]. Is that more manageable?"

**"I need to think about it"**
- "Totally fair. What specifically do you want to think about?"
- "Is it the program itself, or is it the investment?"
- "I find that 'thinking about it' usually means there's a specific concern. What is it?"

**"I need to talk to my spouse"**
- "That makes sense. Would it help if I sent you a summary you could share with them?"
- "Is your spouse supportive of you investing in [their goal]?"
- "Would it help if we did a quick call together?"

**"I've been burned before"**
- "I'm sorry to hear that. What happened?"
- "What was different about that program vs. what we're offering?"
- "That's actually why we include [guarantee/support]. We're invested in your success."

**"Now isn't the right time"**
- "When would be the right time?"
- "What would need to change for it to be the right time?"
- "The people who get the best results are the ones who start before they feel ready."

---

## Phase 6: Ad Campaign Architecture

### Meta Ads Structure

**Campaign 1: Webinar Registration (Cold)**
- Objective: Conversions (registration)
- Audience: Lookalike 1-3% of past buyers/leads, interest-based targeting
- Creative: Video ad (2-3 min, teach + invite format)
- Copy: Problem agitation + "free training" + specific outcome promised
- Budget: Start at $50-100/day, scale based on CPR (cost per registration)
- Target CPR: $3-8 for warm, $8-15 for cold

**Campaign 2: Retargeting (Warm)**
- Objective: Conversions
- Audience: 
  - Registered but didn't attend
  - Attended but didn't apply
  - Applied but didn't book
  - Booked but no-showed
- Creative: Testimonial videos, urgency-based ads, "last chance" messaging
- Budget: 20-30% of total ad spend

**Campaign 3: Evergreen Nurture**
- Objective: Engagement/Traffic
- Audience: All webinar registrants (180 day window)
- Creative: Value content, case studies, behind-the-scenes
- Purpose: Stay top of mind, build trust, re-engage for future launches

### Google Ads Structure

**Campaign 1: Search - High Intent**
- Keywords: "[topic] course", "[topic] coaching program", "how to [outcome]"
- Ad copy: Specific outcome + free training offer
- Landing page: Webinar registration page
- Budget: Based on keyword CPCs, typically $20-50/day to start

**Campaign 2: YouTube - Pre-Roll**
- Targeting: Custom intent audiences, competitor channels, topic-based
- Creative: 30-60s hook video leading to registration
- CTA: "Register for the free training"

### Key Metrics to Track

| Metric | Target |
|--------|--------|
| Cost per registration | $5-15 |
| Registration to attendance rate | 30-50% |
| Attendance to application rate | 15-30% |
| Application to booking rate | 50-70% |
| Show rate | 70-85% |
| Close rate | 20-40% |
| Cost per acquisition | Varies (should be < 20% of product price) |
| Return on ad spend (ROAS) | 3-5x minimum |

---

## Phase 7: Tech Stack Checklist

### Required Tools
- [ ] **GHL Sub-Account** (CRM, pipeline, automations, forms, calendar, email, SMS)
- [ ] **Webinar Platform** (WebinarJam, EverWebinar, Zoom, or StreamYard)
- [ ] **Payment Processor** (Stripe connected to GHL)
- [ ] **Domain** (branded, SSL enabled)
- [ ] **Ad Accounts** (Meta Business Manager, Google Ads)
- [ ] **Tracking** (Google Analytics 4, Meta Pixel, Google Tag Manager)
- [ ] **Calendar** (GHL calendar or Calendly)

### Optional But Recommended
- [ ] **Community Platform** (Skool, Circle, Facebook Group, Discord)
- [ ] **Course Platform** (Kajabi, Teachable, Skool, GHL Memberships)
- [ ] **Video Hosting** (Vimeo Pro for sales pages, Wistia)
- [ ] **Heatmap/Analytics** (Hotjar, Microsoft Clarity)
- [ ] **Call Recording** (Zoom cloud recording, Fireflies.ai)

---

## Phase 8: Launch Timeline

### 4-Week Launch Sprint

**Week 1: Foundation**
- [ ] Finalize offer (price, bonuses, guarantee)
- [ ] Write webinar script
- [ ] Build registration page
- [ ] Build thank you page
- [ ] Set up GHL pipeline and tags
- [ ] Create email/SMS templates

**Week 2: Funnel Build**
- [ ] Build webinar room/replay page
- [ ] Build application page
- [ ] Build booking page
- [ ] Build sales page (backup for non-webinar path)
- [ ] Connect all pages (forms, redirects, tracking)
- [ ] Build all GHL workflows (registration, nurture, follow-up)
- [ ] Test entire funnel end-to-end

**Week 3: Content & Ads**
- [ ] Record webinar (or prep for live)
- [ ] Create ad creatives (3-5 variations)
- [ ] Write ad copy (5-10 variations)
- [ ] Set up Meta ad campaigns
- [ ] Set up Google ad campaigns (if applicable)
- [ ] Install all tracking pixels
- [ ] Test tracking (verify conversions fire correctly)

**Week 4: Launch & Optimize**
- [ ] Turn on ads (start at 50% budget)
- [ ] Monitor registration flow daily
- [ ] Host live webinar (or activate evergreen)
- [ ] Sales team briefed and ready
- [ ] Monitor pipeline daily
- [ ] Scale winning ads, kill losers
- [ ] Daily standup on metrics

---

## Quick Reference: Conversion Benchmarks

| Stage | Good | Great | Fix If Below |
|-------|------|-------|-------------|
| Ad CTR | 1.5% | 3%+ | 1% |
| Landing page opt-in | 30% | 50%+ | 20% |
| Registration to attend | 35% | 50%+ | 25% |
| Attend to apply | 20% | 35%+ | 10% |
| Apply to book | 50% | 70%+ | 40% |
| Show rate | 75% | 85%+ | 60% |
| Close rate | 25% | 40%+ | 15% |

If any metric drops below the "Fix If Below" column, that's the bottleneck. Fix that stage before scaling ad spend.
