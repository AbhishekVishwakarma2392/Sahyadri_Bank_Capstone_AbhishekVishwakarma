# Sahyadri Bank Digital Transformation Roadmap — Team Capstone

Sahyadri Bank is a mid-sized private bank. Its board has approved a digital-transformation budget but has not decided what to do first. Nine initiatives are on the table, a payments app is gaining users against a rival, and the board wants a clear plan. Your team has been asked one question: **"Which kind of transformation are we really attempting, which domain should we transform first, and does the business case hold?"**

You will answer in four connected Parts. Part 1 classifies the initiatives by type of transformation and business model. Part 2 analyses the payments app as a platform against its rival. Part 3 chooses the first domains and designs the first one. Part 4 puts the portfolio into a Power BI board dashboard, builds and tests the business case, and presents. This is **a single connected case, not four separate exercises**: each Part's output is the next Part's fixed input.

Every technique below is one you practised in the course: the three types of digital transformation and why they fail, the product / project / solution / platform grid, platforms and network effects (including Metcalfe's law), ecosystems, domain selection by value and feasibility, the value-lever hierarchy, zero-based design, the five-step business case, agile pods, and Power BI cards, slicers, charts, a simple DAX measure and conditional formatting. **No new tool or concept is introduced.** The only things not taught in class are the slide tool and GitHub in the final task.

**Total marks:** 100 · **Team size:** 3-4 · **One deliverable:** a single public GitHub repository link (see the final task).

## Submission Guidelines (read first)

- **One submission per team:** a public GitHub repository link. Everything for Parts 1-4 is in that one repository.
- **Tools:** Microsoft Excel (formulas, pivot tables, charts) for scoring, calculations and the business case, and Power BI Desktop (or the Power BI web service if Desktop does not run on your computer) for the board dashboard. Nothing else is needed for the analysis.
- **Use only the supplied data files** and do not edit the originals; work on copies.
- **Hand-off rule:** each Part starts from the exact numbers of the previous Part. If you find a mistake, fix it in the earlier Part and carry it forward.
- **If you use a GenAI assistant** (to explain a result, for example), check every number it gives you against Excel or Power BI. An unchecked number is treated as an error.
- **Rounding:** percentages to 1 decimal, currency to the nearest unit, other values to 2 decimals. Allow ±0.01 on 2-decimal values and ±0.1 on 1-decimal values when checking the answers below. Use ₹ only. In Power BI, format rate fields (averages of 0/1 columns) as percentages. **Standard deviation always means the sample standard deviation** (`std()` in pandas, `STDEV.S` in Excel and Sheets). Medians and quartiles use the default linear-interpolation method of pandas and of Excel's `MEDIAN` and `QUARTILE`.
- **Team work:** each member must be able to explain any Part. Record who did what in the README.
- **Originality:** your analysis and presentation must be your own team's work.
- **No subscription is needed:** Slides can be made in **Google Slides** or **LibreOffice Impress** (both free) instead of PowerPoint; GitHub and Google Colab are free with a free account; any free GenAI assistant is enough. **Power BI Desktop** is a free download for **Windows 10/11 only** (it does not run on macOS). Use a Windows PC, your institution's lab, or a Windows virtual machine. The free Power BI web account needs a work or school email address, so a personal Gmail account will not work there. **Spreadsheets:** the course used Excel, whose Data Analysis ToolPak needs desktop Excel (a Microsoft 365 trial asks for a card and converts to a paid plan — do not rely on it). Every spreadsheet task can instead be done in free **Google Sheets** or **LibreOffice Calc** with ordinary functions; the *Free-tool fallbacks* section at the end of this brief gives the formulas.

## Data Pack (3 files)

| File | Contents |
|---|---|
| `initiatives.csv` | The nine candidate initiatives (9 rows): `initiative_id, initiative, description, annual_benefit_lakh, investment_lakh` (₹ lakh). |
| `domains.csv` | Five candidate domains scored 1-5 on four value and four feasibility criteria (5 rows): `domain, description, customer_experience, financial_benefit, speed_to_value, synergy, executive_sponsorship, data_tech_readiness, ease_of_adoption, scaling_capability`. |
| `platform_users.csv` | Six quarters of users on the bank's payments app and its main rival (6 rows): `quarter, bank_customers_thousand, bank_merchants_thousand, rival_customers_thousand, rival_merchants_thousand`. |

---

## Part 1 — What Kind of Transformation Is This? (Excel) (20 marks)

Start by being clear about what each initiative is. Import `initiatives.csv` into a sheet `Initiatives` in `sahyadri_analysis.xlsx`.

**Tasks**

1. **Why transformations fail** *(4 marks)*. Match each statement about the bank to the failure cause it shows — **lack of urgency, insufficient leadership, limited vision, weak execution capabilities**, or **missing middle-out leadership** — and give one fix: (a) branch managers say digital is 'nice to have' and there is no deadline; (b) the CEO talks about digital but has named no executive owner; (c) the plan is a list of 30 apps with no picture of the bank in three years; (d) the last app project slipped twice because the bank lacked cloud and data engineers; (e) the managers who run the loan process were not involved in designing the new one.
   *Concept: reasons digital transformations fail; middle-out leadership · Session 13.*
2. **Classify the nine initiatives** *(7 marks)*. Classify each initiative as **operational transformation (digitisation)**, **business-model transformation** or **strategic transformation**, with a one-line reason from its description.
   *Concept: three types of digital transformation · Session 13.*
3. **Business-model grid** *(5 marks)*. Place each offering on the **product / project / solution / platform** grid (how comprehensive the offering is × how customised): (a) a standard savings account sold over the counter; (b) a one-off customised infrastructure loan for a dam builder; (c) the SME cash-flow solution of initiative I3; (d) the merchant payments app of initiative I2. Say which two axes define the grid.
   *Concept: business-model framework: inclusiveness × customization → product, project, solution, platform · Session 13.*
4. **Money by type** *(4 marks)*. Using a pivot table or formulas on `Initiatives` (add a `type` column from task 2), compute for each type the **number of initiatives**, **total investment**, **total annual benefit** and **three-year benefit per ₹ invested** (= annual benefit × 3 ÷ investment). Which type gives the best and which the worst return? Save the nine initiatives with their `type` column as `initiatives_typed.csv`; Part 4 uses it.
   *Concept: summarising with pivot tables; comparing types of transformation · Session 1, 13.*

**Acceptance criteria**

- (a) lack of urgency; (b) insufficient leadership; (c) limited vision; (d) weak execution capabilities; (e) missing middle-out leadership; each with a fix.
- Classification: **operational** — I1, I5, I6, I8, I9; **business-model** — I2 (platform), I3 (solution), I7 (platform/marketplace); **strategic** — I4 (new domain with new competitors).
- Grid: (a) **product**; (b) **project**; (c) **solution**; (d) **platform**; axes = inclusiveness (comprehensiveness) of the transactions and customisation of the offering.
- By type (count / investment ₹ lakh / annual benefit ₹ lakh / 3-year benefit per ₹): operational **5 / 360 / 720 / 6.00**; business-model **3 / 700 / 1010 / 4.33**; strategic **1 / 600 / 500 / 2.50**. Total investment **1660**, total annual benefit **2230**. Best return: **operational**; worst: **strategic**.

---

## Part 2 — The Payments App as a Platform (Excel) (23 marks)

Initiative I2 is a platform. Analyse it against the rival using `platform_users.csv` (sheet `Platform`).

**Tasks**

1. **Pipeline or platform?** *(4 marks)*. Classify each as a **pipeline (linear) business** or a **platform**, with one reason: (a) home loans; (b) the merchant payments app; (c) the SME supplier-lender marketplace; (d) fixed deposits.
   *Concept: platform vs pipeline business · Session 14.*
2. **Sides and network effects** *(5 marks)*. Name the **sides** of the payments app. Give one **same-side** and two **cross-side** network effects. Explain why more users make the app more valuable (positive feedback).
   *Concept: two-sided markets; same-side and cross-side network effects · Session 14.*
3. **Metcalfe's law and the rival** *(7 marks)*. Using **value ∝ n²** (n = customers), compute for each quarter the network value of the bank (customers²) and the rival, and the **bank-to-rival ratio**. Compute **merchants per 1,000 customers** for both. Compute the correlation between customers and merchants across the six quarters for each firm. Say in which quarter the bank overtakes the rival, what the ratio is in Q6, and why a correlation does not by itself prove the cross-side effect. (A line chart of both firms' customers by quarter is welcome.)
   *Concept: Metcalfe's law (value ∝ n²); cross-side network effects; winner-take-all · Session 14, 16.*
4. **Ecosystem map** *(4 marks)*. List at least **five ecosystem participants** around the payments app (for example merchants, customers, device makers, other banks, regulators) and rate the bank on the five **ecosystem-driver** qualities — brand strength, customer experience, relationship ownership, value extraction, destination status — as *strong / partial / weak*.
   *Concept: business ecosystem, ecosystem driver · Session 14.*
5. **Three moves** *(3 marks)*. Propose three strategic moves for the bank that use what you found (for example grow the merchant side, add complementary services to create lock-in, protect data) and say which implication of platform economics each one uses.
   *Concept: strategic implications: switching costs, data, speed to scale, partnerships · Session 14.*

**Acceptance criteria**

- (a) pipeline; (b) platform; (c) platform; (d) pipeline, each with a reason (linear value chain vs connecting two or more sides).
- Sides: customers (users) and merchants (plus the bank as owner). Same-side: more customers make the app a common standard others copy (or share payment requests); cross-side: more merchants make the app more useful for customers, and more customers attract more merchants.
- Network value (bank / rival / ratio): Q1 **1,600 / 4,900 / 0.33**; Q2 **3,025 / 6,400 / 0.47**; Q3 **5,625 / 8,100 / 0.69**; Q4 **10,000 / 10,000 / 1.00**; Q5 **16,900 / 12,100 / 1.40**; Q6 **28,900 / 14,400 / 2.01**. The bank overtakes the rival in **Q5** (130 vs 110 thousand customers); the Q6 ratio is **2.01** (about 2 times).
- Merchants per 1,000 customers (bank / rival): Q1 **75.0 / 85.7**, Q6 **100.0 / 91.7**. Correlation customers-merchants: bank **0.999**, rival **1.000** — both very strong, but with six points and a common growth trend this shows association, not proof of cause.
- At least five participants are listed and the five driver qualities rated with reasons; three moves are each linked to a named implication.

---

## Part 3 — Choose and Design the First Domain (Excel) (19 marks)

Now decide where to start. Use `domains.csv` (sheet `Domains`).

**Tasks**

1. **Score the domains** *(7 marks)*. Compute each domain's **average value score** (first four criteria) and **average feasibility score** (last four). Treat an average of **3.5 or more as high**. Place the domains on a value × feasibility grid and choose the domain(s) to transform first (the guideline is 2-5 domains; avoid going too small, too big or too thin). Name the top domain.
   *Concept: domain prioritisation by value and feasibility; how many domains to choose · Session 15.*
2. **Define the domains** *(3 marks)*. State whether each domain is defined as a **workflow/process**, a **customer journey** or a **business function**, using its description.
   *Concept: three ways to define a domain · Session 15.*
3. **Lever, solution, use case** *(4 marks)*. For the top domain write the hierarchy **domain → value lever → solution → use case**, with at least two value levers and two use cases.
   *Concept: hierarchy of domain, value lever, solution and use case · Session 15.*
4. **Zero-based design** *(5 marks)*. The loan process today has five steps: (1) customer fills a paper form at a branch; (2) clerk re-types it into the system; (3) credit officer pulls documents and checks them by hand; (4) manager signs the sanction letter; (5) cash is disbursed after a manual call to the customer. Mark each step with one of the four principles — **understand and simplify; orchestrate and digitise; automate and integrate; reorganise and empower** — and state a target of **at least a 50% reduction** from today's average of **12 days** from application to disbursal (compute the target).
   *Concept: zero-based journey design: survival minimum, principles, 50% reduction target · Session 15.*

**Acceptance criteria**

- Averages (value / feasibility): Loan origination **4.25 / 4.00**; First-account onboarding **3.50 / 3.50**; Merchant payments **3.75 / 3.25**; Wealth advisory **3.00 / 3.50**; Collections **2.50 / 3.75**. With the 3.5 cut-off, **Loan origination and First-account onboarding** are high on both; Merchant payments is high on value but just below the feasibility cut-off (3.25); Wealth advisory (3.00) and Collections (2.50) are below the cut-off on value. The top domain is **Loan origination**.
- Loan origination — workflow/process; First-account onboarding — customer journey; Merchant payments — workflow/process; Wealth advisory — business function; Collections — workflow/process.
- The hierarchy shows the domain (Loan origination), at least two value levers (for example faster disbursal, lower processing cost, higher approval of good customers), solutions (for example a digital loan platform) and at least two use cases (for example online application, automated document check).
- Target: **12 days → 6 days or fewer**. Steps: 1 orchestrate and digitise; 2 automate and integrate (remove re-typing); 3 automate and integrate; 4 reorganise and empower (delegated e-sign) or understand and simplify; 5 orchestrate and digitise.

---

## Part 4 — Board Dashboard, Business Case and Presentation (Power BI and Excel) (38 marks)

Build the board's dashboard in Power BI from your Part 1 output and the platform data, save it as `sahyadri_dashboard.pbix` (if you must use the web service, put the shared link in the README and describe your steps), then build the business case for the top domain, using initiative **I9** (`initiatives.csv`: investment ₹180 lakh, annual benefit ₹330 lakh), and test it.

**Tasks**

1. **Load the data and the measure** *(2 marks)*. Load `initiatives_typed.csv` (your Part 1 output) and `platform_users.csv` into Power BI. Create the measure `3-Year Return per ₹ = SUM(initiatives[annual_benefit_lakh]) * 3 / SUM(initiatives[investment_lakh])`.
   *Concept: importing CSV into Power BI, a simple DAX ratio measure · Session 8, 12, 11.*
2. **Cards and slicer** *(2 marks)*. Cards: **Total Investment**, **Total Annual Benefit** (sums) and **3-Year Return per ₹**. Slicer: `type` (buttons). Test with **Operational** selected.
   *Concept: cards and slicers · Session 11, 8.*
3. **Board visuals** *(6 marks)*. (a) A **combo chart** with total investment as columns and total annual benefit as a line, by `type` (dual axis). (b) A **line chart** of bank and rival customers by quarter. (c) A **matrix** with `initiative` in rows showing investment, annual benefit and the `3-Year Return per ₹`, with **conditional formatting** that turns the return **red when below 5** (the 5× payback target) and green otherwise.
   *Concept: combo, line and matrix visuals, rules-based conditional formatting · Session 11, 15.*
4. **Five-step business case** *(9 marks)*. Write the business case in five steps: (1) problem to solve; (2) solutions and use cases; (3) data and technology requirements; (4) impact and investment; (5) implementation plan. In step 4 compute the **three-year benefit**, the **benefit-to-investment ratio** and test it against the **5× payback target**; then re-test a **worst case** in which benefits are **30% lower** and investment **30% higher**. Say what you would do if the worst case fails.
   *Concept: five-step business case; ±30% estimation; 5× payback target · Session 15.*
5. **Pod and accountability** *(4 marks)*. Define an **agile pod of 5-10 people** from the roles Product Owner, Scrum Master, Software Engineers, UX/UI Designers, Data Scientists/Engineers and Business Analysts/Subject-Matter Experts, with headcounts. Show how staffing changes across **discovery, proof of concept/MVP, production and change management**. Name an accountable owner (role) for each of the five business-case steps.
   *Concept: agile pod composition and staffing by life-cycle phase; accountability · Session 15.*
6. **Final task (mandatory): presentation and GitHub** *(15 marks)*.
   (a) **Presentation** *(10 marks)*: create a PowerPoint (or equivalent) deck of **6-8 slides**: (1) the problem; (2) the approach; (3) what kind of transformation (Part 1); (4) the platform position against the rival (Part 2); (5) the domains chosen and the first domain's design (Part 3); (6) the dashboard view, the business case, the worst case and the **recommendation** (Part 4); (7) risks, ownership and next steps. Every number on a slide must match your workbook, notebook or dashboard.
   (b) **GitHub** *(5 marks)*: create a free GitHub account if you do not have one; create a **public** repository named `sahyadri-bank-roadmap-capstone`; on the repository page choose *Add file → Upload files*, drag in the files listed under *Submission*, and *Commit changes*. Submit the repository link.
   *Concept: presenting findings and a recommendation from a case · Session 12 (storytelling with dashboards). GitHub and slide software were not taught in the course; this task is included at the course owner's request.*

**Acceptance criteria**

- Cards (all initiatives): Total Investment **1660**; Total Annual Benefit **2230**; 3-Year Return per ₹ **4.03**. With **Operational** selected: investment **360**, annual benefit **720**, return **6.00**.
- Combo chart by type (investment / annual benefit): Operational **360 / 720**, Business-model **700 / 1010**, Strategic **600 / 500**. The line chart shows the bank overtaking the rival in Q5 (130 vs 110 thousand customers) and reaching 170 vs 120 in Q6.
- Matrix 3-Year Return per ₹ by initiative: I1 **6.00**; I2 **4.80**; I3 **5.20**; I4 **2.50**; I5 **9.00**; I6 **5.25**; I7 **3.50**; I8 **6.60**; I9 **5.50**. Red (below 5): **I2, I4, I7** (the two platforms/marketplace and the strategic entry); all others green.
- Three-year benefit **₹990 lakh**; ratio **5.50×** (passes the 5× target). Worst case: three-year benefit **₹693.0 lakh** vs investment **₹234 lakh** → **2.96×** (fails). A staged proof-of-concept-first response is proposed.
- The pod has 5-10 people with all roles represented; staffing differs by phase; five owners are named.
- The recommendation: transform **Loan origination first** (value 4.25, feasibility 4.00) with **First-account onboarding** as the second domain (Merchant payments follows once its feasibility improves); treat I9 as an operational transformation (it returns 5.50 per ₹, above the 5× target, and operational initiatives as a group return the most, 6.00 per ₹), and keep the strategic I4 (lowest return, 2.50) out of the first wave.
- The deck has 6-8 slides covering problem, approach, transformation types, platform position, domain choice, business case and recommendation, and risks; sampled numbers match the workbook.
- The repository is public, opens without a login, and contains every file listed under *Submission*.

---

## Submission

Submit **one link**: your public GitHub repository. It must contain at minimum:

```
README.md                          (team members and who did what; all written answers, one section per task; a 5-sentence summary of the recommendation)
data/initiatives.csv              (supplied, unmodified)
data/domains.csv                  (supplied, unmodified)
data/platform_users.csv           (supplied, unmodified)
sahyadri_analysis.xlsx            (workings: sheets Initiatives, Platform, Domains, BusinessCase)
initiatives_typed.csv             (Part 1 output, input of the dashboard)
sahyadri_dashboard.pbix           (Part 4; or the shared-report link in the README)
SahyadriBank_Presentation.pptx    (the 6-8 slide deck)
```

## Free-tool fallbacks (Google Sheets, LibreOffice Calc or Excel for the web)

These give the same numbers as the ToolPak tasks above. They use standard functions; round as in the guidelines.

- **Pivot tables**: *Insert → Pivot table* (Excel, Google Sheets) or *Data → Pivot Table* (LibreOffice Calc). Averages, counts and sums are all available.
- **Correlation**: `CORREL(range1, range2)`.