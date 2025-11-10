# Vendor Evaluation Rubric

## Why This Exists

GitHub stars are great. They're also meaningless for buying decisions.

This rubric is for when you (or your team, or your manager) need to actually choose a solution and justify that choice. Maybe you're evaluating tools for production, maybe you need to explain why you picked one option over another, or maybe someone's asking you to do due diligence before committing.

If you're just experimenting or contributing to open source for fun, you don't need this. But when real decisions with real consequences need to be made, this helps you think it through systematically.

A repo with 10K stars might have 1 maintainer who's about to quit their job. Another with 500 stars might have a company with $50M in funding behind it. You need to know which is which before you bet your production infrastructure on it.

## The Evaluation Framework

Rate each category 1-5. Be honest. If something scores a 1, that's not necessarily a dealbreaker-but you better have a plan for it.

### 1. Technical Viability (Does it actually work?)

**Code Quality & Architecture**
- [ ] 5 - Well-documented, clean code, clear architecture
- [ ] 4 - Good code, some technical debt, mostly documented
- [ ] 3 - Works but messy, minimal documentation
- [ ] 2 - Prototype quality, "works on my machine"
- [ ] 1 - Demo code, not production-ready

**Red flags:**
- Last commit was 6+ months ago
- No tests
- All code written by one person
- "TODO: add error handling" comments everywhere

**Green flags:**
- Active commits in the last week
- Comprehensive test coverage (>70%)
- Multiple contributors
- Clear architecture documentation

### 2. Community & Support (What happens when it breaks at 2am?)

**Maintainer Activity**
- [ ] 5 - Full-time team, responds to issues within 24 hours
- [ ] 4 - Active maintainers, responds within 3-5 days
- [ ] 3 - Part-time maintenance, responses within 1-2 weeks
- [ ] 2 - Sporadic activity, slow responses
- [ ] 1 - Abandoned or solo maintainer with no backup

**Community Health**
- [ ] 5 - Active community, regular contributions, good discussions
- [ ] 4 - Decent community, occasional contributions
- [ ] 3 - Small but engaged community
- [ ] 2 - Mostly silent, few interactions
- [ ] 1 - No community, just users

**Red flags:**
- Issues are opened but never closed
- PRs sit unreviewed for months
- Maintainer is rude or dismissive in issues
- No contribution guidelines
- Single point of failure (one person knows how it works)

**Green flags:**
- Issues get triaged quickly
- PRs get reviewed and merged regularly
- Maintainers are helpful and professional
- Clear contribution process
- Bus factor > 1 (multiple people can maintain it)

### 3. Business Model & Longevity (Will this exist in 2 years?)

**Financial Sustainability**
- [ ] 5 - Well-funded company or sustainable business model
- [ ] 4 - Growing revenue or solid funding runway
- [ ] 3 - Early revenue or recent funding
- [ ] 2 - Side project with uncertain future
- [ ] 1 - Hobby project with no business model

**Open Source License**
- [ ] 5 - Permissive license (MIT, Apache 2.0), won't change
- [ ] 4 - Permissive license, company seems stable
- [ ] 3 - Copyleft license (GPL) but works for your use case
- [ ] 2 - Restrictive or commercial license terms
- [ ] 1 - License is unclear or keeps changing

**Red flags:**
- "We're figuring out monetization"
- License changed recently to be more restrictive
- Company just pivoted to this product
- No clear revenue model
- Burning through funding with no path to profitability

**Green flags:**
- Clear business model (open core, managed service, support contracts)
- Profitable or path to profitability
- Multiple years of operation
- Investors who understand open source
- License is stable and permissive

### 4. Production Readiness (Can you bet your infrastructure on this?)

**Deployment & Operations**
- [ ] 5 - Production-tested, clear deployment docs, monitoring built-in
- [ ] 4 - Production-ready, good docs, monitoring possible
- [ ] 3 - Works in production but requires effort
- [ ] 2 - Production-possible but risky
- [ ] 1 - Demo/prototype only

**Security & Compliance**
- [ ] 5 - Security audits, SOC2, clear security practices
- [ ] 4 - Good security practices, working on compliance
- [ ] 3 - Basic security, no major red flags
- [ ] 2 - Security is "TODO"
- [ ] 1 - Security appears to be an afterthought

**Red flags:**
- No monitoring/observability story
- Breaks with every dependency update
- No migration path between versions
- Security issues sit unfixed
- "It works, don't touch it" mentality

**Green flags:**
- Battle-tested at scale
- Clear upgrade path
- Built-in observability
- Security is taken seriously
- Disaster recovery documented

### 5. Integration & Lock-in (How screwed are you if this doesn't work out?)

**Ease of Integration**
- [ ] 5 - Works out of the box, multiple integration options
- [ ] 4 - Easy integration, good documentation
- [ ] 3 - Requires some work but achievable
- [ ] 2 - Complex integration, poor documentation
- [ ] 1 - Requires significant custom development

**Vendor Lock-in Risk**
- [ ] 5 - No lock-in, standard interfaces, easy to migrate away
- [ ] 4 - Low lock-in, some migration effort needed
- [ ] 3 - Moderate lock-in, significant migration work
- [ ] 2 - High lock-in, hard to leave
- [ ] 1 - Complete lock-in, basically impossible to migrate

**Red flags:**
- Proprietary data formats
- No export functionality
- Requires their managed service
- Non-standard APIs
- "You can't run this yourself" attitude

**Green flags:**
- Standard APIs and protocols
- Clear data export
- Self-hosting option
- Works with alternatives
- Easy to evaluate before committing

### 6. Cost Transparency (The hidden costs that bite you)

**Pricing Model**
- [ ] 5 - Clear, predictable, scales reasonably
- [ ] 4 - Mostly clear, some complexity
- [ ] 3 - Confusing but workable
- [ ] 2 - Opaque or surprising costs
- [ ] 1 - "Contact us for pricing" (the worst)

**Total Cost of Ownership**
- [ ] 5 - Low maintenance, scales efficiently
- [ ] 4 - Reasonable maintenance needed
- [ ] 3 - Requires dedicated attention
- [ ] 2 - High maintenance burden
- [ ] 1 - Requires full-time person to run

**Red flags:**
- Pricing based on "value" (translation: we'll charge what we can get away with)
- Hidden costs emerge after you're using it
- Per-seat pricing for infrastructure tools (why?)
- Lock you in then raise prices
- Support costs more than the product

**Green flags:**
- Clear pricing calculator
- No surprise fees
- Usage-based pricing that makes sense
- Support included in reasonable tier
- Price anchoring to value delivered

## The Overall Score

Add up your scores (max 30):

**25-30: Strong Candidate**
This is probably safe to bet your infrastructure on. Still do due diligence, but the fundamentals are solid.

**20-24: Acceptable with Caveats**
Could work, but you need mitigation plans for the weak areas. Make sure you have backup options.

**15-19: Risky**
Probably not ready for production unless you have no alternatives. Be prepared for pain.

**10-14: High Risk**
Only use this if you're prepared to fork it or replace it within 6 months.

**<10: Run Away**
This is someone's side project that's about to get abandoned. Don't build your business on it.

## Real Examples (Names Changed to Protect the Innocent)

### Example 1: "HyperOptimizer AI"

| Category | Score | Notes |
|----------|-------|-------|
| Technical Viability | 4 | Good code, active development, some docs gaps |
| Community & Support | 2 | Solo maintainer, slow issue responses |
| Business Model | 3 | Recent funding, still figuring out monetization |
| Production Readiness | 3 | Works but monitoring is DIY |
| Integration & Lock-in | 4 | Standard APIs, easy to evaluate |
| Cost Transparency | 5 | Clear pricing, no surprises |
| **Total** | **21** | **Acceptable with caveats** |

**Mitigation:** They're growing fast but sole maintainer is risky. Wait 3-6 months for team to expand, or be prepared to contribute/fork.

### Example 2: "MegaCorp Enterprise Solution"

| Category | Score | Notes |
|----------|-------|-------|
| Technical Viability | 3 | Works but complex, lots of legacy code |
| Community & Support | 5 | Dedicated team, 24/7 support |
| Business Model | 5 | Established company, clear revenue |
| Production Readiness | 5 | Battle-tested, SOC2 certified |
| Integration & Lock-in | 2 | Proprietary everything, hard to leave |
| Cost Transparency | 2 | "Contact sales" pricing, surprise fees |
| **Total** | **22** | **Acceptable with caveats** |

**Mitigation:** It'll work but you're locked in. Make sure the lock-in is worth it. Get everything in writing.

### Example 3: Well-Established OSS Project (High Score)

An example of a mature open source project that scores well:

| Category | Score | Notes |
|----------|-------|-------|
| Technical Viability | 5 | Clean code, great docs, comprehensive tests |
| Community & Support | 5 | Active community, responsive maintainers |
| Business Model | 4 | Open core model, sustainable |
| Production Readiness | 5 | Proven at scale, excellent observability |
| Integration & Lock-in | 5 | Standard everything, easy to migrate if needed |
| Cost Transparency | 5 | Free OSS, clear paid tier pricing |
| **Total** | **29** | **Strong candidate** |

**Mitigation:** None really. This is the kind of project you want to find.

**Note:** Projects like [cascadeflow](https://github.com/lemony-ai/cascadeflow) start lower (15-20 range when just launched) and work toward this score as they mature. Just launched? Expect lower community/production scores. That's normal - evaluate based on trajectory and team commitment, not just current state.

## Questions to Ask Before Committing

### To the vendor/maintainers:
1. "What happens if your company gets acquired or shuts down?"
2. "How many production customers are running this at scale?"
3. "What's your SLA and what happens when you miss it?"
4. "How do we export our data if we decide to leave?"
5. "Who else on your team can help if the main developer leaves?"

### To existing users (find them in issues/discussions):
1. "What surprised you after you deployed this?"
2. "What are the hidden costs or pain points?"
3. "How responsive is support when things break?"
4. "Would you choose this again?"

### To yourself:
1. "Can I afford to be wrong about this?"
2. "Do I have a backup plan if this fails?"
3. "Am I choosing this because it's best or because it's popular?"
4. "What's the cost of being wrong for 6 months?"

## The Buy vs Build Decision

After evaluating a vendor, you still need to decide: buy this, build your own, or do nothing?

**Buy if:**
- Score is 20+ 
- Payback period is <12 months
- You have no core expertise in this area
- Your team should be building your actual product instead

**Build if:**
- No vendor scores above 15
- This is your core competitive advantage
- You have the expertise in-house
- You can maintain it long-term

**Do nothing if:**
- The pain isn't that painful
- All solutions cost more than the problem
- You're about to pivot anyway
- You're just procrastinating on harder decisions

## Final Thoughts

This rubric won't make your decision for you. But it will help you see what you're getting into with open eyes.

GitHub stars are a popularity contest. This is due diligence.

Choose wisely, and may your 2am pages be few.

---

*Due diligence isn't paranoia. It's professionalism.*
