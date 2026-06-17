# Manual Review Cases — Ambiguous Retention Decisions
## D2C Personal Care Brand — Snapshot: 2025-09-30

These 10 customers were selected because the segment-level rule gives a default answer, but individual signals suggest the decision deserves closer scrutiny. All data below comes from `rfm_modeling_snapshot.csv`.

---

## Case 1 — CUST00036 | Champion, but churning

| Signal | Value |
|---|---|
| Segment | Champions |
| R/F/M scores | 4 / 5 / 4 (RFM = 13) |
| Recency | 27 days |
| Frequency | 4 orders / 180d |
| Spend | ₹1,737 / 180d |
| Return rate | 25% |
| Avg discount | 36.5% |
| Tickets (90d) | 1 |
| Sessions (30d) | 0 |
| Last campaign | bundle_discount |
| Churn label | **YES** |

**Why it's ambiguous:**  
CUST00036 is a Champion by RFM — recent enough, frequent, decent spend. But they had *zero* web sessions in the past 30 days despite being only 27 days since their last order. They also raised a support ticket (sentiment not negative, but a ticket exists) and have a 25% return rate. They received a bundle_discount campaign but still churned.

**Decision:**  
Do NOT re-offer a discount (their avg is already 36.5% — more discounting will deepen margin loss without securing loyalty). This customer needs to be contacted directly about their return. The return on 1 of 4 orders could indicate a product quality issue in their preferred category (Makeup). Escalate to product team.  
**Action:** Personal email from customer success + request to understand the return reason. If a product defect is involved, replace proactively. Do not assign to bulk campaign.

---

## Case 2 — CUST00110 | Champion, 4 sessions, 2 tickets, still churning

| Signal | Value |
|---|---|
| Segment | Champions |
| R/F/M scores | 4 / 5 / 5 (RFM = 14) |
| Recency | 35 days |
| Spend | ₹2,425 / 180d |
| Tickets (90d) | 2 (50% negative) |
| Sessions | 4 |
| Last campaign | new_launch |
| Churn label | **YES** |

**Why it's ambiguous:**  
CUST00110 has one of the highest RFM scores possible (14/15) and is still predicted to churn. Their 2 tickets with a 50% negative rate is the signal. They spent ₹2,425, received a new_launch campaign, and are in the 35–44 age group (typically more considered buyers). The sessions (4) suggest they haven't mentally disengaged yet.

**Decision:**  
This is likely a complaint-driven exit, not disengagement. The tickets are the smoking gun. Immediate 1:1 outreach acknowledging the service experience is the only viable intervention. Offering a discount here would feel dismissive of their complaint.  
**Action:** Customer success call within 48 hours. Offer a resolution-specific remedy (free replacement, expedited refund, or direct escalation to brand team). Do not send generic promotional email.

---

## Case 3 — CUST00130 | Labelled At-Risk, but not churning — high sessions

| Signal | Value |
|---|---|
| Segment | At-Risk |
| R/F/M scores | 2 / 1 / 4 (RFM = 7) |
| Recency | 88 days |
| Spend | ₹1,272 / 180d |
| Loyalty tier | Gold |
| Avg discount | 48% |
| Sessions | 9 |
| Last campaign | new_launch |
| Churn label | **NO** |

**Why it's ambiguous:**  
At-Risk segment has a 74% churn rate, but CUST00130 did *not* churn. Their recency is 88 days (not great) but they are still browsing 9 sessions/month. Gold loyalty tier and ₹1,272 spend suggest they have real category investment. The 48% discount is a concern — they may return only for heavy deals.

**Decision:**  
This customer is worth careful handling. They are actively browsing (9 sessions) but not converting despite being 88 days since last purchase. The barrier is either price (discount dependency) or product assortment. Since they did not churn, a targeted product suggestion based on what they viewed is more likely to convert than another discount.  
**Action:** Send a personalised "complete your routine" recommendation (based on preferred_category: Skin Care) with a modest 10% loyalty-tier offer framed as Gold-member exclusive. Monitor sessions — if they drop below 3 in the next 14 days, escalate.

---

## Case 4 — CUST00099 | At-Risk, 144 days recency, NOT churning

| Signal | Value |
|---|---|
| Segment | At-Risk |
| R/F/M scores | 2 / 3 / 4 (RFM = 9) |
| Recency | 144 days |
| Spend | ₹1,472 / 180d |
| Age group | 45+ |
| Sessions | 4 |
| Campaign clicks | 2 |
| Last campaign | welcome_offer |
| Churn label | **NO** |

**Why it's ambiguous:**  
144 days since last order, recency score 2, and classified At-Risk — but did not churn. This customer is in the 45+ age group (category: Fragrance) and actually clicked 2 campaign links. The engagement hasn't converted to a purchase yet, but the intent signal is there.

**Decision:**  
The 2 campaign clicks suggest they're responsive to outreach — they just haven't bought. The most likely barrier is that the campaigns haven't matched their preference (Fragrance). Generic Skin Care or Hair Care campaigns would be irrelevant.  
**Action:** Segment this customer into a fragrance-specific campaign flow. A limited-time seasonal fragrance set (with free shipping, not a discount) could convert the browsing intent. Flag for 30-day follow-up.

---

## Case 5 — CUST00027 | High-Value but Unhappy, 100% return rate, NOT churning

| Signal | Value |
|---|---|
| Segment | High-Value but Unhappy |
| R/F/M scores | 3 / 1 / 5 (RFM = 9) |
| Spend | ₹2,128 / 180d |
| Return rate | **100%** |
| Sessions | 11 |
| Campaign clicks | 2 |
| Preferred category | Baby Care |
| Age group | 45+ |
| Churn label | **NO** |

**Why it's ambiguous:**  
This is the strangest case in the dataset. CUST00027 returned 100% of their orders (1 order, 1 return) yet spent ₹2,128 on paper, is still browsing 11 sessions/month, and has not churned. They are classified as High-Value but Unhappy — correct by rule, but their continued active browsing suggests they haven't given up on the brand.

**Decision:**  
A 100% return rate from a single order in Baby Care for a 45+ customer suggests product fit mismatch — possibly bought for a child/grandchild and the item was wrong (size, formulation). They are still engaged (11 sessions, 2 campaign clicks). This is a customer who wants to buy but had a bad first experience with a specific SKU.  
**Action:** Proactive outreach (not a promotion) asking if they need help finding the right product. If a customer service rep can identify the specific return reason, a guided recommendation to an alternative SKU in Baby Care could convert a return into a loyal repeat buyer. Do not write off this customer.

---

## Case 6 — CUST00009 | Discount-Sensitive, NOT churning, 11 sessions

| Signal | Value |
|---|---|
| Segment | Discount-Sensitive |
| R/F/M scores | 4 / 1 / 2 (RFM = 7) |
| Recency | 31 days |
| Avg discount | 49% |
| Sessions | 11 |
| Campaign clicks | 0 |
| Preferred category | Skin Care |
| Churn label | **NO** |

**Why it's ambiguous:**  
CUST00009 has a 49% average discount — the highest in the Discount-Sensitive group — but only bought once (F=1) and is recent (31 days). They did not churn. The 11 sessions and 0 campaign clicks is an unusual combination: they browse heavily on their own but don't respond to email/push campaigns.

**Decision:**  
This is a self-directed browser who responds to content, not campaigns. Standard retargeting campaigns will continue to fail (0 campaign clicks). Their discount at 49% suggests they found the product via a deal — possibly first order.  
**Action:** Experiment with in-app or on-site personalisation rather than email campaigns. If they're browsing 11 sessions/month, show them recommendations during browse sessions. The next offer should be site-level (flash sale notification, cart nudge) not email-based.

---

## Case 7 — CUST00067 | Loyal Customer with return and ticket, churning

| Signal | Value |
|---|---|
| Segment | Loyal Customers |
| R/F/M scores | 3 / 3 / 4 (RFM = 10) |
| Recency | 63 days |
| Spend | ₹1,246 / 180d |
| Return rate | 50% |
| Tickets (90d) | 1 |
| Sessions | 1 |
| Campaign clicks | 2 |
| Preferred category | Baby Care |
| Age group | 18-24 |
| Churn label | **YES** |

**Why it's ambiguous:**  
Loyal Customer by RFM (score 10) but is churning. The signals are clear in hindsight: 50% return rate, a ticket filed, and sessions dropped to 1. Campaign clicks (2) suggest they are still nominally reachable, but their intent is to leave. At 18–24 and in Baby Care, this may be a new parent who had a product experience problem.

**Decision:**  
Standard loyalty retention playbook will not work here. The 50% return rate in Baby Care for an 18–24 customer is a strong quality signal — wrong product formulation, or a product that didn't meet safety expectations for a newborn. A discount offer would feel tone-deaf.  
**Action:** Proactive outreach specifically about the return and ticket. Lead with empathy and safety reassurance (if Baby Care item is involved, this is reputationally important for the brand). Offer an alternative product with guided safety information. If they don't respond within 14 days, accept churn.

---

## Case 8 — CUST00085 | New Customer, 8 sessions, ₹1,258 first order, churning

| Signal | Value |
|---|---|
| Segment | New Customers |
| R/F/M scores | 5 / 1 / 4 (RFM = 10) |
| Days since signup | 41 |
| Recency | 14 days |
| Spend | ₹1,258 (1 order) |
| Sessions | 8 |
| Campaign clicks | 0 |
| Avg discount | 20% |
| Churn label | **YES** |

**Why it's ambiguous:**  
CUST00085 signed up 41 days ago, placed a ₹1,258 first order (solid for a new customer), is still only 14 days since last order, and has 8 sessions. Yet the churn model predicts them as churning. No tickets, no returns, 0 campaign clicks.

**Decision:**  
This customer is actively engaged (8 sessions, recent order) but hasn't made a second purchase. The churn signal may be based on the 41-day signup window without repeat ordering, not actual disengagement intent. However, without a second purchase, their loyalty hasn't been tested.  
**Action:** This is the highest-priority New Customer for second-purchase conversion. Since 0 campaign clicks suggests email isn't landing, try an in-app notification or WhatsApp message (if consent given) with "Complete your Skin Care routine" cross-sell. A small first-repeat incentive (free sample with next order) could seal the loyalty before the 60-day window closes.

---

## Case 9 — CUST00016 | Dormant with a campaign click

| Signal | Value |
|---|---|
| Segment | Dormant |
| R/F/M scores | 1 / 1 / 1 (RFM = 3) |
| Recency | 215 days |
| Sessions | 2 |
| Campaign clicks | 1 |
| Last campaign | welcome_offer |
| Churn label | **YES** |

**Why it's ambiguous:**  
215 days since last order, classified Dormant — yet this customer clicked 1 campaign link in the last 30 days. Dormant customers are usually suppressed from further campaigns, but a click is a real intent signal.

**Decision:**  
One click on a welcome_offer campaign from a 215-day dormant customer is a weak but non-zero signal. The Dormant default is to write off — but this customer is worth a single follow-up.  
**Action:** Send exactly one targeted re-engagement email within 48 hours of this analysis (while the click is fresh). Make the offer compelling (free shipping + a specific product in their preferred category: Skin Care for 18-24 customer). If no response within 7 days, suppress permanently from campaign cadence.  
**Do not** invest more than 1 follow-up communication. The churn prediction is likely correct — but the click at least warrants one attempt.

---

## Case 10 — CUST00253 | Platinum loyalty tier, Occasional Buyers, churning

| Signal | Value |
|---|---|
| Segment | Occasional Buyers |
| R/F/M scores | 1 / 1 / 1 (RFM = 3) |
| Recency | 191 days |
| Sessions | 3 |
| Campaign clicks | 1 |
| Last campaign | new_launch |
| Loyalty tier | **Platinum** |
| Preferred category | Skin Care |
| Age group | 18-24 |
| Churn label | **YES** |

**Why it's ambiguous:**  
CUST00253 is a Platinum loyalty tier member — the highest tier. Yet their current 180-day RFM is 3/15 (minimum possible), with 191 days since last order and no spend in 180 days. This means their Platinum status was earned in a previous period and has since gone dormant. One campaign click in the past 30 days is the only active signal.

**Decision:**  
This is a lapsed Platinum customer — one of the most counterintuitive cases. Bulk campaign treatment (Occasional Buyers) significantly underinvests in a customer who once had high value. But their current RFM suggests a clean break — possibly a life event, budget change, or a competitor win.  
**Action:** This customer should NOT be left in the Occasional Buyers cadence. Move to a "Platinum Reactivation" track: a personalized message acknowledging their Platinum history ("You've been one of our most valued members") with a meaningful offer — not a percent discount, but a complimentary Skin Care product with next order. Their campaign click suggests the brand isn't completely off their radar. Invest one high-quality reactivation attempt.  
**If no response:** Downgrade their loyalty tier flag in the CRM to avoid continued high-cost treatment.

---

*All customer IDs and metrics are from rfm_modeling_snapshot.csv, snapshot date 2025-09-30.*
