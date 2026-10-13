# dmit promo code: which codes still validate at checkout, what each one covers, and the full LAX/HKG/TYO price list

Paste a DMIT promo code from a listicle into the cart, click "Validate Code", and there is a decent chance nothing happens. Not because the list lied when it was written, but because DMIT runs a WHMCS storefront where codes are pinned to a specific product line, a specific billing cycle, and sometimes a specific platform generation. Those things get renamed and retired constantly. A code written for "Lite" plans may match nothing on the shelf today, and a code written for a Los Angeles machine on the AN4 platform does nothing for the AN5 machine that replaced it.

So rather than dumping every string that has ever circulated, here is what is actually worth pasting, which line each code targets, and the current price ladders for Los Angeles, Hong Kong and Tokyo, so you can work out whether the discount is even worth chasing.

## What DMIT actually discounts

There is no permanent sitewide coupon. Multiple trackers that maintain DMIT coupon pages say the same thing in slightly different words: no long-running public code exists, and the savings come from billing-cycle discounts and from codes tied to particular campaigns or newly launched product lines.

That leaves three real levers:

1. **Billing cycle.** Longer prepay terms carry built-in discounts, and some entry plans get a launch discount with no code required at all.
2. **Line-specific recurring codes.** These apply to one network profile (Pro, Eyeball, or Tier 1) in one region, and "recurring" means the discount follows you into renewals rather than dying after the first invoice.
3. **Campaign codes.** Short windows, sometimes structured as a discount plus account credit rather than a straight price cut.

Everything else is noise.

## Why so many DMIT codes are dead on arrival

Three pieces of churn explain most of the failures, and knowing them saves you from testing codes that were never going to work.

**"Lite" got renamed to "Standard."** DMIT dropped the Lite label for its high-bandwidth, internationally-routed family and now calls it Standard. Any code carrying `Lite` in the name belongs to that older naming era. Some still validate because the underlying products did not change, but plenty of blog posts from that period list plans and prices that no longer exist.

**The hardware platforms rotated.** Los Angeles has been through AS3 (EPYC 7003), AN4 (EPYC 9004) and AN5 (EPYC 9005). The AN4 machines were retired around mid-April 2026, which took the cheapest LAX Pro and EB machines out of the catalogue with them. If you are comparing a $9.99/month Los Angeles Pro quote against what the cart shows you today, you are looking at two different generations.

**The campaigns put their own dates in the code.** `2025-XMAS-...` and `202510_...` are not decorative prefixes. They tell you which campaign the code belongs to, and DMIT sets the end of each campaign itself.

That is not a reason to skip the campaign codes. It is a reason to test them before you commit, which costs you about thirty seconds.

## Codes worth testing before you pay

Treat this as a test list, not a guarantee. Line eligibility is reported inconsistently between trackers, which is expected for a scheme that gets re-scoped as product lines change.

| Code | What it targets | Discount | Notes |
| --- | --- | --- | --- |
| `Lite-Annually-Recur-30OFF` | Standard / Tier 1 network, annual prepay | 30% recurring | Reported as long-running by several trackers; whether the floor is TINY or STARTER is disputed |
| `Lite-Semi-Annually-Recur-20OFF` | Standard / Tier 1 network, semi-annual prepay | 20% recurring | Same family, shorter term |
| `202510_HKG_TYO_T1_30OFF_RECURRING` | HKG T1 / TYO T1, quarterly or longer, excluding WEE | 30% recurring | Region-specific Tier 1 |
| `202510_HKG_TYO_PRO_20OFF_RECURRING` | HKG Pro / TYO Pro, quarterly or longer | 20% recurring | The CN2 GIA lines |
| `2025-TYO-T1-HI-GSL-NON-MONTHLY-30OFF` | TYO T1, TINY and above, quarterly or longer | 30% | Monthly billing not eligible |
| `2025-TYO-T1-HI-GSL-MONTHLY-10OFF` | TYO T1, TINY and above, monthly | 10% | The monthly version of the above |
| `LAX-EB-LAUNCH-NON-MONTHLY-RECURRING-20OFF` | LAX Eyeball, any non-monthly cycle | 20% recurring | Launch code that outlived the launch |
| `2025-EXISTING-CUSTOMER-10OFF` | Existing customers | 10% | Reported as gated on roughly $3.33 of monthly spend |
| `2025-XMAS-LAX-PRO-EB-ANNUALLY-STARTER-AND-HIGHER-15OFF-RECURRING` | LAX Pro / EB, annual, STARTER and up | 15% recurring + 10% account credit | Christmas campaign code |
| `2025-XMAS-LAX-PRO-EB-10-OFF-RECURRING` | LAX Pro / EB, any regular cycle | 10% recurring + 5% credit | Christmas campaign code |
| `2025-XMAS-LAX-T1-ANNUALLY-EXCL-WEE-TINY-20OFF-RECURRING` | LAX T1, annual, excluding WEE and TINY | 20% recurring + 10% credit | Christmas campaign code |
| `2025-XMAS-LAX-T1-10-OFF-RECURRING` | LAX T1, any cycle, excluding WEE | 10% + 5% credit | Christmas campaign code |

> The Christmas block is a campaign, not a standing offer. When it was announced the start was set at 22 December 2025 and the end was left open, described only as running until DMIT closes the campaign. Some of those strings may still validate and some may not. There is no cost to testing them, and no way to know without testing.

## How to test a code in half a minute

The order matters more than people expect, because most of these codes are gated on the billing cycle and you cannot change the discount retroactively.

1. Pick the region and line first. Pro, EB and T1 each have their own code pool, and a Tier 1 code will never apply to a Premium plan.
2. Set the billing cycle second. Nearly every recurring code requires quarterly, semi-annual or annual prepay. If you leave it on monthly, half the list above is ineligible by definition.
3. Add the plan to the cart and open the checkout page.
4. Paste the code into the Promotional Code field and click **Validate Code**. The price either updates or it does not, and that is your answer.
5. Check the total, not just the line item. Some codes also create an account credit that lands separately from the invoice discount.

Once the invoice is paid, the code is locked. There is no support ticket that retroactively applies a discount you forgot to enter.

## Discount plus credit is not the same as a bigger discount

The Christmas codes are structured as two separate things, and it is worth understanding the difference before you compare them against a plain 20% or 30% code.

Take the `2025-XMAS-LAX-PRO-EB-ANNUALLY-STARTER-AND-HIGHER-15OFF-RECURRING` structure: 15% off the invoice, plus 10% returned as account credit, paid out over twelve months. On a $1,000 annual invoice you pay $850 at checkout. The credit then returns $85 to your DMIT balance over the year. If you spend that balance on a future renewal, your effective cost lands at about $765, or a hair under 23.5% off list, which is the number some trackers quote for it.

That arithmetic only holds if the credit gets used. It is denominated in DMIT account balance, not in your bank account, so it is only worth face value if you intend to renew or add a second machine. If you are buying one box to evaluate and might never come back, treat the real discount as the 15% and ignore the rest. The same logic applies to the 10% plus 5% credit tier, which is worth roughly 14.5% if the credit gets spent.

That is the honest comparison against a straight 20% recurring code with no credit attached. Twenty percent you keep, versus 23.5% you have to spend again at the same shop.

## Pick the network before the code

The single most expensive mistake with DMIT is buying the wrong network profile, because the price gap between them for identical CPU and RAM is often larger than any coupon will ever close.

| Line | Routing profile | Who it fits | Entry price |
| --- | --- | --- | --- |
| Tier 1 (Standard) | International BGP, no China-specific optimisation | International traffic, backups, CI runners, relay nodes, cost-sensitive deployments | $36.90/year for WEE, $6.90/month for TINY |
| Eyeball (EB) | CMIN2 / CMI "best effort" China optimisation | Budget-first buyers who still want mainland visitors to do better than a plain route | Around $9.99/month on the older LAX ladder |
| Premium (Pro) | CN2 GIA on the China-facing paths | Anyone who genuinely needs stable mainland latency at peak hours | Around $14.90/month on the current LAX AN5 ladder |
| Premium Secure (sPro) | CN2 GIA plus Cloudflare Magic Transit scrubbing | Sites that attract DDoS traffic | Priced above Pro |

If your audience is not in mainland China, Tier 1 is the rational purchase and you should stop reading the Pro code list entirely. Paying CN2 GIA money for traffic that never touches China is the most common way people waste a discount.

Ready to see what the cart says with your cycle selected? 👉 [Check current DMIT pricing and live stock](https://www.dmit.io/aff.php?aff=12046)

## The full Tier 1 / Standard ladder

These are the most consistently reported prices across every tracker and review site that covers DMIT, and they apply across Los Angeles, Hong Kong and Tokyo unless noted. Traffic is metered one-way, and when you burn through it the machine is throttled rather than suspended.

| Plan | vCPU | RAM | SSD | Traffic / port | After the cap | Price | Buy |
| --- | --- | --- | --- | --- | --- | --- | --- |
| WEE | 1 | 1 GB | 20 GB | 1 TB @ 4 Gbps | 50–100 Mbps unmetered | $36.90/year | [ Order WEE](https://www.dmit.io/aff.php?aff=12046) |
| TINY | 1 | 1 GB | 20 GB | 2 TB @ 4 Gbps | 100 Mbps unmetered | $6.90/month | [ Order TINY](https://www.dmit.io/aff.php?aff=12046) |
| STARTER | 1 | 2 GB | 40 GB | 4 TB @ 10 Gbps | 100 Mbps unmetered | $12.90/month | [ Order STARTER](https://www.dmit.io/aff.php?aff=12046) |
| MINI | 2 | 2 GB | 60 GB | 8 TB @ 10 Gbps | 100 Mbps unmetered | $21.90/month | [ Order MINI](https://www.dmit.io/aff.php?aff=12046) |
| MICRO | 4 | 4 GB | 80 GB | 16 TB @ 10 Gbps | 200 Mbps unmetered | $32.90/month | [ Order MICRO](https://www.dmit.io/aff.php?aff=12046) |
| MEDIUM | 4 | 8 GB | 160 GB | 32 TB @ 10 Gbps | 200 Mbps unmetered | $49.90/month | [ Order MEDIUM](https://www.dmit.io/aff.php?aff=12046) |
| LARGE | 8 | 16 GB | 320 GB | 64 TB @ 10 Gbps | 500 Mbps unmetered | $99.90/month | [ Order LARGE](https://www.dmit.io/aff.php?aff=12046) |
| GIANT | 8 | 24 GB | 640 GB | 128 TB @ 10 Gbps | 1 Gbps unmetered | $199.90/month | [ Order GIANT](https://www.dmit.io/aff.php?aff=12046) |

Two regional variations are worth knowing. Hong Kong's Standard line dropped its cheapest $6.90/month configuration at some point, so the Hong Kong ladder now starts higher than the Los Angeles and Tokyo ones. And annual pricing is not simply twelve times the monthly figure: the documented Hong Kong annual list is $76.90 for TINY, $154.80 for STARTER, $262.80 for MINI, and so on. Multiply those by 0.7 and you land exactly on $53.83, $108.36 and $183.96, which is how the 30% annual recurring code shows up in the wild. That is a useful sanity check: if a "discounted" price you see quoted is not exactly 70% of the annual list, it is coming from a different code or a different cycle.

## Premium (Pro) and Eyeball (EB) ladders

Same warning as before: these lines rotate platforms and sell out. Los Angeles moved from AN4 to AN5 in 2026, and the entry price climbed with it.

**Premium (CN2 GIA)**

| Region | TINY | Pocket | STARTER | MINI | MICRO | MEDIUM | LARGE | GIANT |
| --- | --- | --- | --- | --- | --- | --- | --- | --- |
| Los Angeles (AN5) | $14.90/mo | $21.90/mo | $43.90/mo | $79.90/mo | $110.90/mo | $289.90/mo | $499.90/mo | $1,009.90/mo |
| Hong Kong | $39.90/mo | — | $79.90/mo | $119.90/mo | $159.90/mo | $179.90/mo | $239.90/mo | $499.90/mo |
| Tokyo | $21.90/mo | — | $39.90/mo | $79.90/mo | $159.90/mo | $259.90/mo | $429.90/mo | $799.90/mo |

**Eyeball (CMIN2 / CMI)**

| Region | TINY | Pocket | STARTER | MINI | MICRO | MEDIUM | LARGE | GIANT |
| --- | --- | --- | --- | --- | --- | --- | --- | --- |
| Los Angeles | $9.99/mo | $14.90/mo | $29.90/mo | $58.88/mo | $74.99/mo | $168.88/mo | $338.88/mo | $619.99/mo |
| Hong Kong | $29.90/mo | — | $59.90/mo | $89.90/mo | $129.90/mo | $199.90/mo | $389.90/mo | $789.90/mo |
| Tokyo | $25.90/mo | — | $55.90/mo | $85.90/mo | $119.90/mo | $179.90/mo | $369.90/mo | $749.90/mo |

Los Angeles prices above reflect the ladder that was current before the AN4 retirement, so treat the LAX Pro row as the AN4 reference point and expect the AN5 equivalents to sit higher, as the entry figures show. Tokyo Eyeball stock is intermittent and the older AS3 generation of that line was discontinued, so do not assume it is orderable on any given day.

👉 [See which DMIT plans are in stock right now](https://www.dmit.io/aff.php?aff=12046)

## The small charges that quietly eat your discount

A 20% code on a $12.90/month plan saves you about $31 a year. Three line items can hand that back, and none of them appear on the promo page.

**IP replacement.** Every 15 days you get a free IP swap. Outside that window it is $5 per change. This matters more than it sounds, because DMIT does not guarantee that a monthly plan's assigned IP is reachable from every region, and IP blocks are the most common reason people ask for a swap.

**IP Guarantee+.** For about $1 per month on monthly plans, you get a guaranteed globally reachable IP, with free reassignment by ticket if the one you receive is blocked. On the cheap plans this is a meaningful percentage of the base price and it is not covered by any code.

**Maintenance windows.** One recurring complaint in user write-ups is that DMIT does not always email ahead of host-node maintenance, so a machine can go briefly unavailable without warning. If you need documented notice and a written SLA, this is the thing to weigh, not the coupon.

On the other side of the ledger, throttling instead of suspension is a genuine saving. When you exceed your traffic allowance the port drops to somewhere between 50 Mbps and 1 Gbps depending on plan, and the machine keeps serving. A burst does not take your site down.

## Quick answers

**Can I stack two codes?** No. One promotional code per order.

**Do the discounts apply to renewals?** If the code name contains `Recurring`, yes, and that is most of the valuable ones. The `-50OFF` style one-time codes apply to the first invoice only.

**Can I apply a code after paying?** No. Validate before you check out.

**Is there a code for the cheapest plans?** Sometimes the cheapest machines carry a launch or annual discount with no code at all, and the cart applies it automatically. Test the codes anyway, but check whether the price already moved.

**Are the campaign codes still alive?** Unknown, and anyone telling you otherwise with confidence is guessing. Paste them and let the validator answer.

## What to do with all this

If you are buying Tier 1 for non-China traffic, the decision is easy: pick the region, set annual billing, try `Lite-Annually-Recur-30OFF` first because 30% recurring is the deepest thing on the list and it beats any credit-plus-discount structure you have to spend twice. If your visitors are in mainland China, decide between Pro and EB on the price ladder, not on the coupon, then apply the corresponding regional code and accept 20% as a good outcome.

Either way, verify the number in the cart. DMIT renames lines, retires platforms and closes campaigns, and the invoice total is the only price that is actually true.

👉 [Start at DMIT, pick your plan, and validate your code at checkout](https://www.dmit.io/aff.php?aff=12046)
