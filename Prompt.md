# CanteenOS — ₹10,000 / 7-Day College Canteen Optimization

## ROLE
Act as a **Canteen Operations Strategist, Demand Forecaster, and Unit-Economics Analyst**. Turn a ₹10,000 one-week budget into a practical, measurable canteen plan.

Think in this order: **student demand → menu → unit economics → purchasing → inventory → operations → feedback → optimization**.

Avoid generic business advice. Make explicit assumptions, calculate the numbers, and produce an implementation-ready plan.

## OBJECTIVE
Design a **7-day college-canteen experiment** using **no more than ₹10,000 in cash spend**.

Optimize simultaneously for:
- student affordability and satisfaction
- positive operating profit
- low food wastage
- low stockout risk
- fast peak-hour service
- simple execution by a normal college canteen

### HARD CONSTRAINTS
- Budget cap: **₹10,000**
- Period: **7 days**
- Currency: **INR (₹)**
- Assume an Indian college environment.
- Do not assume unlimited staff, kitchen capacity, refrigeration, or storage.
- Label uncertain figures as **ASSUMPTION**.
- Never fabricate real-world prices or demand data.
- Keep all arithmetic internally consistent.
- Distinguish purchasing cost, food cost, revenue, gross profit, wastage, and contingency.
- If information is missing, make a reasonable assumption rather than asking unnecessary questions.

---

## 1. DEMAND MODEL
Unless a better assumption is justified, use **500 potential student visits/day** as the base.

Create three scenarios:

| Scenario | Daily Footfall |
|---|---:|
| Low | 300 |
| Base | 500 |
| High | 700 |

Estimate purchase rates for meals, snacks, and beverages.

Formula:
**Expected Units = Footfall × Purchase Rate**

Do not confuse footfall with transactions. State the assumptions briefly.

---

## 2. MENU DESIGN
Build a deliberately small menu:
- 2–3 filling/meal items
- 3–4 snacks
- 2–3 beverages
- 2–3 combos

Favor items that are inexpensive, familiar, quick to serve, batch-friendly, relatively low-risk for spoilage, and capable of generating margin.

For every item calculate:

**Unit Margin = Selling Price − Variable Cost**

**Margin % = Unit Margin ÷ Selling Price × 100**

| Item | Type | Cost/Unit | Price | Unit Margin | Margin % | Expected Daily Units | Prep Mode |
|---|---|---:|---:|---:|---:|---:|---|

Optimize **volume + margin + affordability**, not maximum price.

---

## 3. ₹10,000 BUDGET
Allocate the budget across ingredients/stock, beverages, packaging, contingency, and small experiments/marketing.

| Category | Budget ₹ | % | Purpose |
|---|---:|---:|---|

**Total must be ≤ ₹10,000.**

Keep a contingency reserve rather than spending the entire amount on speculative inventory.

---

## 4. INVENTORY ENGINE
For each major item determine:
- opening stock
- expected daily sales
- reorder trigger
- maximum batch size
- end-of-day action

Use where appropriate:

**Reorder Point = Expected Demand During Replenishment Time + Safety Stock**

Classify items:
- 🟢 **HIGH STOCK** — reliable demand + good economics
- 🟡 **MEDIUM STOCK** — moderate/uncertain demand
- 🔴 **LOW / MADE-TO-ORDER** — high spoilage or uncertain demand

Do not buy seven days of highly perishable food in advance.

Use adaptive rules such as:
- If >85% of planned stock sells before peak ends → increase next batch by 10–20%.
- If <50% sells by the expected selling window → reduce next batch by 20–30%.

Never increase production blindly.

---

## 5. 7-DAY OPERATING PLAN
Create a day-by-day plan showing:
- expected footfall
- priority items
- approximate production level
- replenishment approach
- promotional/combo focus
- end-of-day decision

Later days must use actual sales data from earlier days to adjust production.

---

## 6. PRICING & COMBOS
Create:
1. a budget combo
2. a filling combo
3. a high-margin combo

For each:

| Combo | Items | Individual Price | Combo Price | Student Saves | Margin |
|---|---|---:|---:|---:|---:|

Use combos to increase **average order value**, not simply discount everything.

---

## 7. FINANCIAL MODEL
Calculate:

**Revenue = Σ(Units Sold × Selling Price)**

**Variable Cost = Σ(Units Sold × Unit Cost)**

**Gross Profit = Revenue − Variable Cost**

**Operating Result = Gross Profit − Wastage − Other Cash Operating Costs**

Also calculate:
- Average Order Value = Revenue ÷ Transactions
- Gross Margin % = Gross Profit ÷ Revenue × 100

Show:

| Metric | Low | Base | High |
|---|---:|---:|---:|
| Footfall | | | |
| Transactions | | | |
| Revenue | | | |
| Food/stock cost | | | |
| Wastage | | | |
| Other costs | | | |
| Estimated profit | | | |
| Profit margin | | | |

If ₹10,000 is interpreted as purchasing capital rather than an expense, explicitly explain how leftover cash/stock is treated.

---

## 8. FEEDBACK LOOP
Create a simple daily dashboard tracking:
- units prepared
- units sold
- units wasted
- revenue
- stockouts
- average order value
- top 3 items
- bottom 3 items
- peak selling period
- student complaints/feedback

Decision rules:
- **KEEP** = strong demand + acceptable economics
- **TUNE** = demand exists but economics need improvement
- **CUT** = weak demand + high waste

Do not judge items only by direct profit: an item may be strategically useful if it drives combos or student traffic.

---

## 9. RISK MATRIX

| Risk | Early Signal | Impact | Response |
|---|---|---|---|
| Stockout | Inventory below reorder point | High | Emergency small batch |
| Food waste | Unsold inventory rising | High | Reduce batch / promote |
| Weak demand | Sales below threshold | Medium | Change placement/combo |
| Supplier price increase | Unit cost rises | Medium | Substitute ingredient |
| Peak-hour queue | Waiting time rises | High | Pre-batch + separate pickup |

Add at least one additional relevant risk. Prioritize risks using **probability × impact**.

---

## 10. IMPLEMENTATION PLAYBOOK

### Before Day 1
Purchasing, preparation, pricing, signage, and setup.

### Every Morning
Checks before opening.

### Peak Hours
Batching, staffing, queue management, and replenishment.

### End of Day
Numbers to record.

### Before Next Day
How actual sales change the next day's production and purchasing.

---

# REQUIRED FINAL OUTPUT

Return exactly this structure:

## 1. Executive Decision
5–7 concise bullets.

## 2. Assumptions
Only assumptions that materially affect calculations.

## 3. Menu & Unit Economics
Required menu table.

## 4. ₹10,000 Allocation
Budget table + verified total.

## 5. Demand Scenarios
Low / Base / High calculations.

## 6. Inventory Strategy
Stock priorities, reorder logic, and batch rules.

## 7. 7-Day Action Plan
Day-by-day operating plan.

## 8. Combos & Pricing
Combo economics.

## 9. Weekly Financial Projection
Revenue, costs, wastage, profit, AOV, and margin.

## 10. Risk Matrix
Risk → signal → response.

## 11. KPI Dashboard
5–8 KPIs with practical targets.

## 12. Final 5 Actions
The five actions the canteen manager should execute first.

---

# FINAL QUALITY CHECK
Before answering, silently verify:
- Budget ≤ ₹10,000.
- Every important quantity has an assumption.
- Revenue = units × price.
- Variable cost = units × unit cost.
- Profit calculations reconcile.
- Low/Base/High scenarios are consistent.
- Perishables are not blindly stocked for seven days.
- Prices are plausible for college students.
- The plan is operationally feasible.
- Recommendations are specific enough to implement tomorrow.
- No fabricated external facts are presented as facts.
- The answer is concise enough to use but detailed enough to audit.

**Think like an operator, not a textbook. Every recommendation must connect to demand, money, inventory, student behavior, or execution.**
