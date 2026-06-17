# Retention Strategy by Segment
## D2C Personal Care Brand — Snapshot: 2025-09-30

---

## Overview

Eight segments were derived from RFM scoring (R/F/M each 1–5, combined score 3–15) enriched with four
additional behavioural signals: average discount %, return rate, support ticket count, and 30-day web sessions.
This document assigns a specific retention action to each segment and closes with a budget prioritisation rationale.

---

## Segment 1 — Champions (n=401, churn rate=10%)

**Who they are:**  
R_score ≥ 4, F_score ≥ 4, M_score ≥ 4. These are the customers who bought within the past 25 days on average,
ordered 4+ times in 180 days, and spent ₹2,800+ in the same window. Web sessions average ~10/month.
They are the core revenue engine — Champions account for roughly 32% of total 180-day revenue despite being 17% of customers.

**Why some still churn:**  
41 Champions are predicted to churn (10%). Among them, 3 customers (e.g. CUST00036, CUST00110, CUST00184)
had R_score ≥ 4 but zero or near-zero web sessions in the past 30 days, and one had 2 support tickets.
The trigger is not RFM decay but product or experience disappointment — they stopped browsing entirely.

**Retention action:**  
- Do **not** send generic discounts. Champions currently receive avg 28% discount already; more discounts train
  them to wait for deals.
- Priority action: early access to new product launches, referral rewards, and a loyalty milestone notification
  (e.g. "You've spent ₹X with us this year — thank you").
- For the ~41 churning Champions: proactive personal outreach (WhatsApp/email from customer success, not bulk),
  asking if they had any product issues.

**Expected value:** Retaining even 20 churning Champions at avg ₹2,800 spend/6 months = ₹56,000 revenue protected.

---

## Segment 2 — Loyal Customers (n=499, churn rate=22%)

**Who they are:**  
R_score ≥ 3, F_score ≥ 3, combined RFM ≥ 10. Recency averages 38 days, frequency 3.2 orders/180d, spend ₹1,870.
They are consistent buyers across categories (avg 2.1 categories in 180d) but haven't reached Champion status.

**What drives their 22% churn:**  
The churning Loyals tend to have R_score exactly 3 (last order ~60–85 days ago) and sessions dropping from
prior highs. They haven't left yet but are drifting. Support ticket rate is low (avg 0.19), so dissatisfaction
isn't the driver — it's disengagement.

**Retention action:**  
- "Back to basics" email cadence: personalised "You haven't tried [category they haven't bought recently]"
  with a modest 10–15% discount to re-spark cross-category exploration.
- Loyalty tier nudge: customers near the Gold threshold should receive a progress notification
  ("2 more orders away from Gold status").
- Timing: activate within 30 days of snapshot to catch them before recency further degrades.

**Expected value:** 22% of 499 = ~110 customers at risk. Recovering half at avg ₹1,870 spend = ₹103k revenue.

---

## Segment 3 — High-Value but Unhappy (n=47, churn rate=70%)

**Who they are:**  
M_score ≥ 4 (avg spend ₹2,350/180d) but with either a return rate >20% OR a negative support ticket.
Only 47 customers, but they represent disproportionate revenue — and a disproportionate warning signal.
Customer CUST00208 spent ₹3,282 but has 1 negative ticket and a 0% return rate (product-level issue, not logistics).
CUST00180 returned 50% of orders worth ₹1,571 — likely a sizing or product mismatch issue.

**Why standard retention campaigns fail here:**  
A discount to CUST00208 won't fix a product quality complaint. Sending a promo to someone who returned half
their orders signals the brand doesn't know them. These customers need to feel *heard*.

**Retention action:**  
- Immediate priority: manual reach-out from the customer success team (not automated) within 7 days.
  Reference their specific ticket or return reason in the communication.
- For high-return customers: offer a free product swap or guided recommendation from a skincare expert
  (if brand has chat-based skin consultation).
- For ticket-driven unhappy customers: acknowledge the issue and offer resolution credit (not a discount coupon —
  something that solves the complaint).

**Expected value:** 70% churn on 47 customers = ~33 at risk. At ₹2,350 avg, that is ₹77,550 revenue at stake.
Even retaining 15 would protect ₹35k revenue. ROI on 47 personalised outreach calls is extremely high.

---

## Segment 4 — At-Risk (n=462, churn rate=74%)

**Who they are:**  
R_score ≤ 2 (last purchase typically 100–200 days ago) but F_score ≥ 3 or M_score ≥ 3 — meaning they *were*
good customers. Recency avg = 130 days. Sessions avg = 3.1/month vs 9.8 for Champions.
462 customers, 74% churn rate → ~342 likely to leave.

**What happened to them:**  
The drop in recency (R ≤ 2) happened despite decent prior history. Three sub-profiles within At-Risk:
1. *Faded quietly* — no tickets, no returns, just stopped coming. Disengagement.
2. *Active online but not buying* — sessions ≥ 5, cart abandonment. Price sensitivity or indecision.
3. *Returned items and went quiet* — return rate > 0 and now dormant.

**Retention action:**  
- Sub-profile 2 (online but not buying): trigger an abandoned-cart or wishlist reminder with a time-limited
  offer (e.g. "Your wishlist items are running low in stock").
- Sub-profile 1 (silently fading): reactivation email referencing their most purchased category.
  Subject line personalised: "We miss you — and your [Skin Care/Hair Care] routine."
- Sub-profile 3 (return then gone): similar to High-Value Unhappy playbook — resolve the underlying issue first.
- **Do not** spray a blanket discount to all 462. That is the fastest way to train them to expect it.

**Expected value:** With 74% churn, At-Risk is the largest revenue-at-risk pool. Even a 15% recovery rate
on 342 churning customers at avg ₹950 spend = ₹48,800 revenue protected at low campaign cost.

---

## Segment 5 — Discount-Sensitive (n=202, churn rate=55%)

**Who they are:**  
Avg discount 44%, RFM ≤ 9, frequency avg 1.1 orders/180d. They activate on deals and go quiet otherwise.
Customers like CUST00009 and CUST00010 have R_score 4–5 (recently active) but extremely low frequency — they
bought once, at a heavy discount, and haven't returned without one.

**The risk of retaining this segment:**  
Offering discounts to Discount-Sensitive customers is profitable only if they have lifetime value beyond the
promo window. At 1.1 orders/180d and avg discount already at 44%, the margin on each order is thin.

**Retention action:**  
- Test a *value-first, discount-second* approach: product education content (skincare routine guides, ingredient
  explainers) to build category engagement before the next offer.
- For customers with sessions ≥ 5 (actively browsing): small offer (10–15%) with a "curated for you" framing —
  not a clearance-style sale.
- For customers with sessions ≤ 2: minimal investment. If they only come back for >35% discounts, retaining them
  at margin-positive economics is not viable at scale.
- Suppress this segment from high-value discount campaigns that train deal-dependency further.

**Expected value:** Mixed. Focus resources only on the ~80 Discount-Sensitive customers with ≥ 3 sessions.

---

## Segment 6 — Dormant (n=203, churn rate=91%)

**Who they are:**  
R_score = 1, sessions ≤ 2. Last purchase avg 292 days ago. Near-zero discount usage — they did not respond
to the brand's existing campaigns. Churn rate 91% = 185 customers are effectively already gone.

**Realistic expectation:**  
Win-back campaigns on Dormant customers have industry reactivation rates of 3–8%. Spending significant budget
here has poor expected ROI.

**Retention action:**  
- Low-cost, low-frequency "reactivation experiment": a single re-engagement email with a strong reason to return
  (seasonal product launch, significant reformulation). No follow-up if no open/click.
- Suppress from regular campaign cadence to avoid burning sender reputation or wasting SMS credits.
- Track: if any Dormant customer clicks but doesn't purchase → move to a 2-email low-discount drip.
- Write off the rest. Redirect that budget to At-Risk and High-Value Unhappy.

---

## Segment 7 — New Customers (n=96, churn rate=17%)

**Who they are:**  
Signed up ≤ 90 days ago, made 1–2 purchases (R_score ≥ 4, F_score ≤ 2). Recency is good, frequency
hasn't had time to build. CUST00070 (49 days old, 1 session) and CUST00085 (41 days old, 8 sessions but
still 1 order) illustrate two sub-types: low-engagement and high-engagement-but-not-repeat-buying.

**Retention action:**  
- Onboarding sequence: within 15 days of first purchase, send a personalised "complete your routine" email
  cross-recommending products complementary to what they bought.
- For customers with 0 repeat orders after 30 days: trigger a second-purchase incentive (free shipping,
  not a percentage discount — protects margin).
- CUST00085 (8 sessions, no second order) is the highest-priority case: they are actively exploring but
  haven't converted again. A direct nudge with a curated recommendation has high expected conversion.

---

## Segment 8 — Occasional Buyers (n=490, churn rate=59%)

**Who they are:**  
The catch-all mid-tier: moderate across all signals. Avg recency 97 days, frequency 1.3, spend ₹750.
No dominant negative signal (not high return rate, not high discount dependency) but no strong engagement either.

**Retention action:**  
- Category-specific newsletters: since preferred_category is known, send relevant content (skin care tips,
  hair care trends) that pulls them back organically.
- Seasonal triggers: festival promotions with moderate discounts (15–20%) for customers who haven't bought
  in 60+ days.
- Keep CAC expectations low — this segment is broad and heterogeneous.

---

## Budget Prioritisation

**Total customers at risk:** ~900 (churn ≥ 50%)

Assuming a budget of ₹2,50,000 for the next 60-day retention sprint:

| Priority | Segment | Rationale | Suggested Budget |
|---|---|---|---|
| 1 | High-Value but Unhappy (47) | Highest revenue/customer at risk. 1:1 outreach has very high ROI. | ₹35,000 (₹750/customer) |
| 2 | At-Risk (462) | Largest revenue pool. Personalised win-back at ₹200–300/customer. | ₹90,000 |
| 3 | Champions (churn-predicted 41) | Personalised outreach. Cannot afford to lose them. | ₹25,000 |
| 4 | Loyal Customers (churn-predicted ~110) | Category re-engagement, loyalty nudge. | ₹40,000 |
| 5 | Discount-Sensitive (active subset ~80) | Value-first emails, light offer. | ₹20,000 |
| 6 | New Customers (96) | Low-cost onboarding email. | ₹15,000 |
| 7 | Occasional Buyers (490) | Seasonal newsletter, minimal per-user spend. | ₹20,000 |
| 8 | Dormant (203) | One reactivation attempt only. | ₹5,000 |

**Total: ₹2,50,000**

**What NOT to do:** Do not split budget equally across all segments. Dormant customers have a 91% churn rate
and have already ignored the brand's campaigns. At-Risk and High-Value Unhappy will generate 4–6x more
recovered revenue per rupee spent.

---

*Generated from rfm_modeling_snapshot.csv, snapshot date 2025-09-30. Segment assignments in segments.csv.*
