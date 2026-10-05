# Business Questions & Findings

## Q1. How is the e-commerce business performing overall?
**Analyzed:** orders, customers, sales, delivery rate, delivery time, reviews, monthly sales.  
**Result:** 99,441 orders; 96,096 customers; R$13.59M product sales; 96,478 delivered; 97.02% delivery rate; 12.50 days average delivery; 4.09/5 average review. November 2017 was the highest monthly sales period observed.  
**Finding:** Strong transaction volume and delivery completion with generally positive customer reviews.  
**Recommendation:** Investigate what drove the November 2017 sales peak.  
**Caveat:** Final observed period is incomplete/sparse.

## Q2. Which product categories generate the most sales?
**Result:** Top by items sold included Bed Bath Table, Health Beauty, Sports Leisure. Top by sales included Health Beauty, Watches Gifts, Bed Bath Table.  
**Finding:** Volume and sales rankings do not perfectly match; item value matters.  
**Recommendation:** Evaluate categories using both volume and value.

## Q3. Is sales performance concentrated among a small number of sellers?
**Result:** Top sellers shown were approximately R$200K–R$229K each; top 10 appeared to represent roughly 13% of total product sales from the dashboard visualization.  
**Finding:** Seller sales appear relatively diversified.  
**Recommendation:** Benchmark high-performing sellers.  
**Caveat:** 13% is an approximate visual estimate, not a dedicated concentration metric.

## Q4. Are high-volume categories also generating high sales value?
**Result:** Health Beauty and Bed Bath Table performed strongly across volume and sales. Computers had approximately R$1,098 average item price among categories displayed.  
**Finding:** Sales performance is not determined by volume alone.  
**Recommendation:** Use volume, total sales, and average item price together.

## Q5. Is the customer base primarily one-time or repeat?
**Result:** 96,096 customers; 2,997 repeat; 93,099 one-time; 3.12% repeat purchase rate.  
**Finding:** The customer base is overwhelmingly one-time.  
**Implication:** Retention and reactivation are major opportunities.  
**Recommendation:** Investigate post-purchase engagement, loyalty, reactivation, and category-level repeat behavior.

## Q6. Does repeat purchasing vary across customer states?
**Result:** Among the top 10 states analyzed: RJ 3.40%, GO 3.28%, SP 3.22%.  
**Finding:** Differences exist but are relatively small.  
**Recommendation:** Use higher-performing states as benchmarks.  
**Caveat:** Limited to the top 10 customer states shown.

## Q7. How frequently are customers purchasing?
**Result:** Orders per customer across the top 10 customer states were approximately 1.03–1.04.  
**Finding:** Purchase frequency remains close to one order per customer.  
**Recommendation:** Focus on retention and reactivation.

## Q8. How effectively are orders being delivered?
**Result:** 96,478 delivered; 97.02% delivery rate; 12.50 average days; 88,644 on-time; 7,826 late; 91.89% on-time rate.  
**Finding:** Delivery completion is high, but late deliveries remain an operational investigation area.  
**Recommendation:** Investigate markets and operational conditions associated with late deliveries.

## Q9. Where are late deliveries more concentrated?
**Result:** Among states shown: BA 14.0%, RJ 13.5%, ES 12.2%.  
**Finding:** Late-delivery rates vary across markets.  
**Recommendation:** Investigate carrier, seller location, order volume, and delivery distance.  
**Caveat:** The dashboard shows where rates are higher, not why; no causation is claimed.

## Q10. Is delivery performance associated with customer satisfaction?
**Status:** **Not analyzed in the current model.**  
A dedicated delivery-timing classification linked to reviews was not added. A future version could compare review scores for on-time versus late deliveries. No causal conclusion is made.

## Q11. How satisfied are customers overall?
**Result:** 4.09/5 average review; 77.07% positive (4–5); 14,575 low-rated (1–2); approximately 14.69% low-rated.  
**Finding:** Overall sentiment is positive, but a meaningful minority are low-rated.  
**Recommendation:** Analyze low-rated experiences alongside delivery, products, and customer segments.  
**Note:** Score 3 is neither positive nor low-rated under these definitions.

## Q12. Does customer experience vary across major customer markets?
**Result:** Observed state averages approximately 3.9–4.2/5; PR 4.2, SP 4.2, MG 4.1; lowest observed value 3.9.  
**Finding:** Satisfaction is positive but not uniform.  
**Recommendation:** Compare satisfaction with order volume, product mix, and delivery performance.  
**Caveat:** State associated with the lowest 3.9 score was not separately recorded.

# Overall Takeaways
1. Strong transaction and delivery performance.
2. Customer retention is the clearest opportunity.
3. Category analysis should consider both volume and value.
4. Delivery is generally strong but not uniform across markets.
5. Customer satisfaction is generally positive.
6. The dashboard identifies where to investigate; deeper operational data is required to determine causes.
