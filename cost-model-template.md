# Cost Model Template

## What This Is

A spreadsheet you won't hate. Plug in your numbers, get your ROI (return on investment). Send it to finance people and watch them actually read it.

**Important context:** This is for when someone's asking you for numbers, or when you're trying to figure out if pursuing something commercially makes sense. If you're just building to see if you can, or experimenting with an idea, you can skip this entirely. Come back when/if you need it.

## The Basic Formula

```
ROI = (Money Saved - Money Spent) / Money Spent × 100%

Payback Period = Money Spent / (Money Saved per Year)
```

That's it. Everything else is just details.

## The Template

### Part 1: Current State (Baseline)

What does it cost them to keep doing what they're doing?

| Category | Cost | Frequency | Annual Cost |
|----------|------|-----------|-------------|
| **Direct Costs** |
| Cloud/API spending | | /month | |
| Software licenses | | /year | |
| Infrastructure | | /month | |
| **Indirect Costs** |
| Developer time wasted | | hours/week | |
| Support tickets | | tickets/month | |
| Downtime/incidents | | incidents/year | |
| **Total Current Annual Cost** | | | **$________** |

### Part 2: Your Solution Costs

What does it cost them to use your solution?

| Category | Cost | Frequency | Annual Cost |
|----------|------|-----------|-------------|
| Implementation | | one-time | |
| Your product/service | | /month | |
| Ongoing maintenance | | /month | |
| Training | | one-time | |
| Migration costs | | one-time | |
| **Total Solution Cost (Year 1)** | | | **$________** |
| **Total Solution Cost (Year 2+)** | | | **$________** |

### Part 3: New State (With Your Solution)

What do their costs look like after implementing your solution?

| Category | Old Cost | New Cost | Annual Savings |
|----------|----------|----------|----------------|
| Cloud/API spending | | | |
| Developer time | | | |
| Support tickets | | | |
| Other | | | |
| **Total Annual Savings** | | | **$________** |

### Part 4: The Business Case

```
Year 1:
  Annual Savings: $________
  Solution Cost: $________
  Net Benefit: $________
  ROI: ________%
  Payback Period: ________ months

Year 2+:
  Annual Savings: $________
  Solution Cost: $________
  Net Benefit: $________
  ROI: ________%
```

## Real Example: LLM Cost Optimization Tool

Let's use an LLM cost optimization tool as an example. Here's how a customer's math might look:

### Current State
| Category | Cost | Frequency | Annual Cost |
|----------|------|-----------|-------------|
| OpenAI API calls | $18,000 | /month | $216,000 |
| Engineer time debugging API issues | 15 hours/month × $100/hour | /month | $18,000 |
| **Total Current Annual Cost** | | | **$234,000** |

### Solution Costs
| Category | Cost | Frequency | Annual Cost |
|----------|------|-----------|-------------|
| Implementation | $3,000 | one-time | $3,000 (Year 1 only) |
| Tool/service cost | $2,083 | /month | $25,000 |
| Training | $1,000 | one-time | $1,000 (Year 1 only) |
| **Total Solution Cost** | | | **$29,000 (Year 1)** |
| | | | **$25,000 (Year 2+)** |

### New State
| Category | Old Cost | New Cost | Annual Savings |
|----------|----------|----------|----------------|
| LLM API calls (60% reduction) | $216,000 | $86,400 | $129,600 |
| Engineer debugging time (70% reduction) | $18,000 | $5,400 | $12,600 |
| **Total Annual Savings** | **$234,000** | **$91,800** | **$142,200** |

### The Business Case
```
Year 1:
  Annual Savings: $142,200
  Solution Cost: $29,000
  Net Benefit: $113,200
  ROI: 390%
  Payback Period: 2.4 months

Year 2+ (no implementation costs):
  Annual Savings: $142,200
  Solution Cost: $25,000
  Net Benefit: $117,200
  ROI: 469%
  (Already paid back, so ongoing benefit is immediate)
```

**Note:** Tools like [cascadeflow](https://github.com/lemony-ai/cascadeflow) are MIT licensed and free to use, which makes the business case even simpler - pure cost savings with no tool cost. The example above assumes a paid service for illustrative purposes.

## Real Example: Developer Productivity Tool

You built a tool that catches bugs before production.

### Current State
| Category | Cost | Frequency | Annual Cost |
|----------|------|-----------|-------------|
| Developer time on bug fixes | 10 devs × 6 hours/week × $90/hour | /week | $281,000 |
| Production incidents | 8 incidents/year × $15,000 each | /year | $120,000 |
| Customer churn from bugs | 2 customers/year × $50,000 ARR | /year | $100,000 |
| **Total Current Annual Cost** | | | **$501,000** |

### Solution Costs
| Category | Cost | Frequency | Annual Cost |
|----------|------|-----------|-------------|
| Implementation | $8,000 | one-time | $8,000 (Year 1 only) |
| Your service | $1,500 | /month | $18,000 |
| **Total Solution Cost** | | | **$26,000 (Year 1)** |
| | | | **$18,000 (Year 2+)** |

### New State (Conservative: 60% reduction in bugs)
| Category | Old Cost | New Cost | Annual Savings |
|----------|----------|----------|----------------|
| Developer bug fixing time | $281,000 | $112,000 | $169,000 |
| Production incidents | $120,000 | $48,000 | $72,000 |
| Customer churn | $100,000 | $60,000 | $40,000 |
| **Total Annual Savings** | **$501,000** | **$220,000** | **$281,000** |

### The Business Case
```
Year 1:
  Annual Savings: $281,000
  Solution Cost: $26,000
  Net Benefit: $255,000
  ROI: 981%
  Payback Period: 1.1 months

Year 2+ (no implementation costs):
  Annual Savings: $281,000
  Solution Cost: $18,000
  Net Benefit: $263,000
  ROI: 1,461%
  (Already paid back, so ongoing benefit is immediate)
```

## Common Objections (And How to Address Them)

### "I can always find numbers that will make this work somehow"

**The concern:** You can tune any model to show positive ROI. Just adjust assumptions until it looks good.

**The reality:** Yes, you can. And decision-makers know this. That's why:
- **Use conservative numbers:** Under-promise so you over-deliver
- **Show your assumptions explicitly:** "Assuming 50% reduction based on X, Y, Z"
- **Offer multiple scenarios:** Conservative, expected, optimistic
- **Back it up with references:** "Similar company saw 45-60% reduction" (with source)

If you have to twist the numbers too hard to make them work, that's telling you something.

### "If they don't get the value, it's just not for them"

**The concern:** Why bother with all this math? Either they see the value or they don't.

**The reality:** This works for small purchases ($50/month). It fails for anything serious because:
- Decision-makers need to justify purchases to others
- Multiple stakeholders need alignment (users, managers, finance)
- "Trust me, it's valuable" doesn't get budget approval
- Your competitors ARE doing the math

You might understand the value intuitively. The person approving the $50K purchase doesn't. Help them help you.

### "My technology will see organic growth because it's simply so good"

**The concern:** Great products sell themselves. If I build something amazing, people will naturally adopt it.

**The reality:** The graveyard of startups is full of technically superior products that nobody bought. Why?
- Distribution beats product quality
- Better doesn't always mean different enough to justify switching
- Change management is harder than you think
- "Good enough" incumbent beats "technically better" challenger most of the time

Even [cascadeflow](https://github.com/lemony-ai/cascadeflow) - which can provably save companies $100K+/year - requires business cases to justify adoption. And it's free and open source.

If your product is so good that no one needs convincing, you're either:
1. The rare exception (possible but unlikely)
2. Not talking to real decision-makers yet (more common)

## Tips for Building Your Model

### 1. Be Conservative
Better to under-promise and over-deliver. If you think you can save 80%, pitch 50% and make them heroes when it's 80%.

### 2. Use Their Numbers, Not Yours
Don't say "our average customer saves $100K." Say "based on your $200K current spend, you'd save approximately $80K."

### 3. Show Year 1 vs Year 2+
Implementation costs are real. Show them the payback period, then show them what Year 2 looks like when those costs disappear.

### 4. Include "Soft" Costs (But Don't Go Crazy)
Developer time has value. Downtime has cost. Customer churn is real money. But if you start adding "improved morale" and "strategic alignment," you've lost them.

### 5. Give Them Three Scenarios
| Scenario | Savings | Likelihood |
|----------|---------|------------|
| Conservative | $50K/year | 90% confident |
| Expected | $80K/year | 70% confident |
| Optimistic | $120K/year | 40% confident |

Let them pick which one they're comfortable with.

## Common Mistakes

### Mistake #1: Forgetting Implementation Costs
Your product is $10K/year but takes $50K to implement? That's a 6-year payback period. Good luck.

### Mistake #2: Only Showing the Best Case
If everything needs to go perfectly for your ROI to work, it won't work.

### Mistake #3: Using Percentages Without Context
"90% cost reduction!" sounds amazing until you realize they're only spending $5K/year to begin with.

### Mistake #4: Ignoring Opportunity Cost
"We'll save you $50K/year" vs "You could spend 6 engineer-months building this instead of building actual features."

### Mistake #5: Making It Complicated
If your ROI calculator needs a PhD to understand, you've already lost. Keep it simple.

## Download This Template

Copy the tables above into:
- **Google Sheets** (easiest to share)
- **Excel** (if they're that kind of company)
- **CSV** (if they're engineers)

Or just use it as markdown in your README. We're not precious about formats here.

## What Good Looks Like

A good cost model:
- Takes 10 minutes to fill out
- Uses their actual numbers
- Shows payback in months, not years
- Includes conservative assumptions
- Survives a CFO asking "but what if...?"

A bad cost model:
- Requires certified accountant
- Uses only your "average customer" data
- Shows 1000% ROI (nobody believes this)
- Assumes everything goes perfectly
- Falls apart when someone asks a basic question

## Next Steps

- Fill out this template with your actual numbers
- Run it by someone in finance (they'll catch the mistakes)
- Use it in sales conversations
- Update it as you get real data

And remember: if your ROI case requires a vision quest and two acts of faith, you might need to rethink your pricing.

---

*Numbers don't lie. But they do need context.*
