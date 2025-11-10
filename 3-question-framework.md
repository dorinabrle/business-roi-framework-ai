# The 3-Question Framework

## The Context

Maybe you built something because it was technically interesting. Maybe you wanted to see if you could solve a problem. Maybe you just liked the challenge.

That's completely valid. Not everything needs a business case.

But sometimes the questions come: from a manager, a peer, a potential user, or your own curiosity. "Could this be a product?" "What's the value?" "How do we justify using this?"

When those questions come, here's how to answer them.

## The Problem

You: "We use speculative cascading to optimize token generation with fallback routing!"

Buyer: "...cool. What does that mean for my AWS bill?"

Buyer could be a CTO, a project manager, a team lead, a product owner, or anyone else making the call on whether to use your solution. This gap is where promising tech goes to die. Not because the tech isn't good, but because the translation is missing.

## The Solution

Three questions that translate any technical feature into business value. Answer these when you need to, and you can talk to anyone from a developer to a CFO without losing either of them.

## The 3 Questions

### 1. What Pain Does This Solve?

Not what your tech does. What *problem* it fixes.

**Bad answer:** "We implement advanced caching mechanisms"

**Good answer:** "Your AI chatbot costs $8K/month because you're re-processing the same questions. We cache common responses."

**The translation:** Your tech → Their headache going away

**Real examples:**
- "You're spending $50K/year on OpenAI because every user query hits GPT-4. We route simple queries to cheaper models." (LLM optimization)
- "Your team wastes 10 hours/week debugging API failures in production. We catch them in development." (Testing tool)
- "You're paying for 20 CI/CD pipeline runs when only 3 matter. We run smart diffs." (Build optimization)

**[Cascadeflow](https://github.com/lemony-ai/cascadeflow) example:**
"You're spending $200K/year on LLM APIs like OpenAI. 40-85% of that spend is on queries that could use cheaper models with zero quality loss. We use token-level speculative cascading to automatically route requests to the most cost-effective model that meets your quality threshold. The core is MIT licensed and free. For enterprise features like advanced analytics, SSO, and dedicated support, hypothetical pricing would be around $20-30K/year - but even without those, the core tool delivers the cost savings."

**Important:** If you can't name a specific painful number (usually this is cost, time, risk, or convenience-though convenience is softer), you might not have a business yet. You might have a really cool technical achievement-and that might be exactly what you want. But if someone's asking you for the business case, this is where you need to start.

### 2. How Much Does It Cost Them Now?

Put a number on the pain. Vague pain doesn't open wallets. This is where you calculate the ROI (return on investment) - how much money they'll save or make compared to what they'll spend.

**Framework:**
```
Current Cost = [What they're spending/losing now]
Your Solution Cost = [What they'll spend with you]
Net Savings = [The difference]
Payback Period = [How long until they break even]
```

**What "payback period" actually means:** This is how long it takes for the money they paid you to pay itself back through savings. Once they hit this point, they're actually gaining more money (through time saved or costs reduced) than they spent. Break-even is when savings = what they paid you. After that, it's pure gain.

**Example 1: LLM Cost Optimization Tool**
```
Current: $200K/year on OpenAI API
Tool reduces their API costs to: $80K/year (60% reduction)
Tool/service cost: $25K/year
Total new cost: $105K/year ($25K + $80K)
Net savings: $95K/year ($200K - $105K)
Payback period: 3.2 months

How we calculated 3.2 months:
- First year cost of the tool: $25K
- They save $95K/year, which is $7,917/month ($95K ÷ 12)
- $25K ÷ $7,917/month = 3.16 months (rounded to 3.2)
- After 3.2 months, they've saved enough to cover your $25K cost
- From month 4 onward, they're saving $7,917/month in pure profit
```

**Example 2: Developer Productivity Tool**
```
Current: 5 developers × 8 hours/week wasted × $80/hour = $166K/year in wasted time
Your solution: $12K/year subscription
Net savings: $154K/year
Payback period: Less than 1 month

How we calculated "less than 1 month":
- Your solution costs $12K/year = $1,000/month
- They save $154K/year = $12,833/month
- $12K ÷ $12,833/month = 0.93 months (about 28 days)
- They break even in less than a month
```

**Example 3: Infrastructure Optimization**
```
Current: $25K/month cloud costs
Your solution reduces cloud costs to: $17K/month
Your tool costs: $2K/month
Total new cost: $19K/month ($2K + $17K)
Net savings: $72K/year ($6K/month × 12)
Payback period: 4 months

How we calculated 4 months:
- Current: $25K/month = $300K/year
- New cost: ($2K + $17K) = $19K/month = $228K/year
- Savings: $300K - $228K = $72K/year = $6K/month
- Your tool costs $2K/month
- First year: They pay $24K for your tool ($2K × 12 months)
- They save $6K/month
- $24K ÷ $6K/month = 4 months to payback
```

**Reality check:** If your payback period is longer than 6 months, you're going to have a harder time selling. If it's longer than 12 months, you're basically asking for an act of faith.

### 3. Why Can't They Just Build It Themselves?

This is the question developers always think but rarely ask out loud. You need a good answer.

**Weak answers:**
- "It's really complex" (They have engineers. Complex is their job. Often they even like the challenge. You don't want to encourage them to try it first before realizing it might actually be too much work for them.)
- "We have special IP" (Unless you have actual trade secrets they can't reverse-engineer, this is just wishful thinking.)
- "We're faster" (Maybe for the first version. Then what?)

**Strong answers:**
- "You *could* build it, but it'll take 2-3 engineers 4-6 months. That's $120K+ in salary for something we charge $15K/year for. Plus you'd need to maintain it."
- "We process 50M requests/day across 200 customers. Your dataset won't catch the edge cases we've seen."
- "This requires deep domain expertise in [specific area]. You could hire that expertise for $200K/year or pay us $30K/year."
- "The first version is easy. The next 50 features your users will demand? That's where this gets expensive."

**The nuclear option (use carefully):**
"Your engineers *should* build your core differentiators. They *shouldn't* build commodity infrastructure. That's why you use AWS instead of building your own data centers."

**[Cascadeflow](https://github.com/lemony-ai/cascadeflow) example:**
"You could build LLM cost optimization yourself. The basic routing logic takes maybe 2-3 weeks. But token-level speculative cascading with sub-10ms latency overhead, handling all the edge cases across different LLM providers, maintaining compatibility as APIs change, optimizing for your specific use case: that's 6+ months of specialized work. We've already done that, tested it at scale, and open sourced it under MIT license. You can use it free and modify it however you want. Your call on whether your engineers should spend 6 months on infrastructure or on your actual product."

## Putting It All Together

Let's use [cascadeflow](https://github.com/lemony-ai/cascadeflow) as a real example (we're building this at Lemony):

**Question 1: What pain?**
"You're spending $200K/year on LLM APIs. 40-85% of those costs are unnecessary because simpler queries could use cheaper models with zero quality loss. But routing is complex and you don't have visibility into optimization opportunities."

**Question 2: How much does it cost them now?**
```
Current: $200K/year on OpenAI
With cascadeflow (free MIT core): Costs drop to $80-120K/year (40-60% reduction)  
Enterprise features (hypothetical): $25K/year for advanced analytics, SSO, support
Total with enterprise: $105-145K/year
Net savings: $55-95K/year
Payback period: 3-5 months (if using enterprise tier)

Note: Core is completely free (MIT), so actual savings could be $80-120K/year with zero tool cost.
```

**Question 3: Why not build it?**
"You could build this. It'd take 2-3 engineers about 6 months ($150K+ in salary) to get to production-ready with token-level cascading, proper fallback routing, and sub-10ms latency overhead. Then you need to maintain it as LLM providers change their APIs every quarter. Or you could deploy cascadeflow (MIT licensed, free) in an afternoon."

## The Formula

```
[Pain with specific numbers] + [Your solution with ROI] + [Why buying beats building] = Business case
```

## Common Mistakes

### Mistake #1: Using percentages instead of dollars
"We reduce costs by 40%" sounds impressive until someone asks "40% of what?"

Better: "We reduce costs by 40%. For a company spending $100K/year, that's $40K saved."

### Mistake #2: Comparing to the wrong baseline
Don't compare your $50K/year solution to a $30K/year competitor. Compare it to the $200K/year pain of not solving the problem at all.

### Mistake #3: Forgetting the "do nothing" option
Your competition isn't just other vendors. It's also "we'll just live with this problem" or "we'll build it ourselves."

**From my experience, this is one of the most crucial mistakes to avoid.** Changing habits is one of the biggest hurdles in bringing something to market, even if your solution is objectively and fundamentally better. Opening your mind to something new, changing your day-to-day workflow, educating yourself on a new tool, convincing your team to adopt it... these are massive barriers. Change is hard.

This is one of the main reasons why even brilliant technology fails. The pain of change often feels bigger than the pain of the current problem, even when the math says otherwise.

**The fix:** Make adoption as painless as possible. Show them it takes 10 minutes to set up, not 2 weeks. Prove you won't disrupt their workflow. Give them a trial that requires zero commitment. The easier you make change, the more likely they'll actually do it.

### Mistake #4: Optimizing for the wrong buyer
Your competition isn't just other vendors. It's also getting everyone aligned on the decision.

If the users love it but their manager hates the cost model, you have a hobby. If management loves it but the team refuses to adopt it, you have shelfware. If the project manager sees value but can't get budget approval, you're stuck.

You need to make your case work for everyone involved in the decision: the people using it, the people approving it, and the people paying for it.

## Practical Exercise

Take your project and answer these three questions right now. If you can't answer them with specific numbers in 10 minutes, you have more work to do before you're ready to sell anything.

**Your turn:**

1. What pain? (Be specific. Use numbers.)
   
   _________________________________________________

2. How much does it cost them now? (Show the math.)
   
   Current: _______________________________________
   
   Your solution: _________________________________
   
   Net savings: ___________________________________
   
   Payback: _______________________________________

3. Why can't they just build it?
   
   _________________________________________________

If you can fill this out convincingly, you're ready to have business conversations. If you can't, keep working on it. No shame in that-most projects start here.

## Next Steps

- Use the [Cost Model Template](./cost-model-template.md) to build detailed ROI calculations
- Check the [Red Flags Checklist](./red-flags-checklist.md) to make sure your answers hold up
- Review the [Vendor Evaluation Rubric](./vendor-evaluation-rubric.md) to see how buyers will actually evaluate you

---

*Remember: Your code might be beautiful, and that might be reason enough to build it. But when someone asks about business value, technical beauty doesn't answer the question. Use this framework when you need it.*
