# Red Flags Checklist

## What This Is

First things first: not every project needs to be a business. Building something because it's technically interesting, or to solve your own problem, or just to see if you can - that's all completely valid.

This checklist is for when you've decided (or are being pushed) to turn your project into a business. It's a collection of things I wish the 200+ startups I've coached had known before they learned them the expensive way.

Full disclosure: I've made plenty of these mistakes myself. That's how I know they're mistakes. There's no need for you to repeat them.

These aren't theoretical concerns. These are "we just spent 6 months building something nobody will pay for" and "our demo works great but enterprises won't touch it" and "we have 10,000 users and $0 in revenue" real-world pain.

If you see yourself in these and you're pursuing the business path, don't panic. Just fix it before you spend another 6 months going in the wrong direction.

If you're NOT pursuing the business path, you can safely ignore all of this and go back to building cool stuff.

## Product & Market Fit Red Flags

### 🚩 "All my developer friends love it"

**The problem:** Your coding buddies think it's cool. That's awesome if you're building for fun or to solve a shared technical problem. Stars, community, and enthusiastic users are actually a phenomenal foundation - like freemium in the app world. Many free users help ensure the product becomes really good, it gets tested at high volumes, and you get valuable feedback.

**Why it becomes dangerous (if you want a business):** The pathway from community to revenue needs to be clear from the start. GitHub stars ≠ customers. Developers who think something is "technically interesting" ≠ people who will pay. You need a plan for which target groups or features you'll monetize, not just hope that popularity converts to revenue.

**Real example:** Had a team with 5,000 GitHub stars and amazing engagement from the developer community. Zero revenue after 18 months because they built for technical excellence and community love, with no clear path to monetization. The community was great. The business plan wasn't.

**The fix (if you want to pursue this commercially):** Build community AND a business model simultaneously. Decide early: What's free forever? What might have paid tiers? Who would pay and why? Community can be your rocket fuel, but you need to know where the rocket is going. 

For [cascadeflow](https://github.com/lemony-ai/cascadeflow), we're going for a community first with a fully MIT licensed core, knowing we'll add enterprise features (open core model) later. That's a plan, not hoping it works out.

### 🚩 "We have thousands of users"

**The problem:** People love free stuff. Payment is a completely different decision.

**Why it's dangerous:** "Users" and "customers" are not the same word for a reason. You can have 50,000 users and zero revenue. I've seen it happen more times than I can count.

**Real example:** Developer tool with 30,000 developers using it. Tried to introduce a $9/month paid tier. Got 47 paying customers. That's a 0.15% conversion rate. They're still trying to figure out why.

**The fix:** Test pricing early. Even if it's just a "pay what you want" button. You'll learn very quickly whether people value your solution or just like that it's free.

### 🚩 "It works great in our demo"

**The problem:** A prototype that impresses coders is not the same as enterprise-ready software. Not even close.

**Why it's dangerous:** The gap between "works on my laptop" and "works in a bank's production environment at 3am" is roughly 10x the work you've done so far. Security, compliance, monitoring, disaster recovery, audit logs, SSO, role-based access control, data residency... the list goes on.

**Real example:** Amazing AI tool that worked beautifully. Then enterprise customers started asking questions. "Where is your SOC2 report?" (What's SOC2?) "How do you handle GDPR?" (How do we what?) "What's your SLA?" (Our what now?) Deal died.

**The fix:** Talk to enterprise buyers early. They'll tell you exactly what's missing. Don't wait until after you've built everything.

## Business Model Red Flags

### 🚩 "We'll figure out monetization later"

**The problem:** Later never comes, or comes too late.

**Why it's dangerous:** If you build for free and try to charge later, you've trained your users that your product should be free. Also, if you don't know how you'll make money, you don't know what to build.

**Real example:** Open source project with huge adoption. Tried to introduce a paid tier after 2 years. Community revolted. "You're betraying the open source spirit!" Fork created. Now two dying projects instead of one successful one.

**The fix:** Decide your business model on day one. Open core? Managed service? Support contracts? Pick one. Build for that model from the start.

**Important clarification:** "Open core" means MIT/free today, enterprise features later. That IS a day-one decision. You're not "figuring it out later" - you're executing the GitLab/Elastic playbook: build community with free core, monetize enterprise features. That's different from "we'll figure out monetization someday."

### 🚩 "Our competitor charges $X, so we'll charge less"

**The problem:** Racing to the bottom is not a business strategy.

**Why it's dangerous:** If your only value proposition is "we're cheaper," you'll lose to the next person who's cheaper. Also, low prices attract the worst customers-the ones who demand the most and pay the least.

**Real example:** Team saw a competitor at $50/month, priced at $29/month. Competitor had $10M in funding and was using pricing as a customer acquisition strategy (they were losing money on purpose). Startup couldn't compete on price or features. Dead in 8 months.

**The fix:** Price on value, not on competition. If you save someone $100K/year, charge $30K/year. If you can't explain value, you can't charge for value.

### 🚩 "We're building a platform"

**The problem:** Platforms are what you become, not what you start as. The issue here is SCOPE, not ambition.

**Why it's dangerous:** Platforms require network effects. Network effects require scale. Scale requires money and time. You probably have neither.

**Real example:** "We're building the AWS of healthcare." No you're not. AWS had Amazon's resources and still took 15 years to become "AWS." You have three developers and a dream.

**The clarification:** Saying "we're the AWS cost explorer for AI" (specific tool, specific domain) is fine. Saying "we're AWS for startups" (trying to be everything) is not. The red flag is about being too broad, not about using successful companies as reference points.

**The fix:** Build one thing that solves one problem really well. "AWS cost explorer for AI" is specific. "AWS for finance" is not. Once you have 1,000 happy customers for your one thing, then think about becoming a platform.

For cascadeflow, we're focused on one thing: LLM cost optimization through token-level cascading. Not "AI platform." Not "developer infrastructure platform." One specific, valuable problem.

## Technical Red Flags

### 🚩 "It's 90% done, we just need to..."

**The problem:** The last 10% takes 90% of the time.

**Why it's dangerous:** "Just need to add error handling, monitoring, tests, security, documentation, and make it scale" is not 10% of the work. It's the work.

**Real example:** Team spent 3 months building the core algorithm. Beautiful code. Then spent 9 months on "the rest"-making it production-ready, handling edge cases, adding proper logging, fixing the 47 ways it could break.

**The fix:** The definition of "done" is "deployed to production and handling real traffic without paging you at 2am." Adjust your estimates accordingly.

### 🚩 "We'll just scale it later"

**The problem:** Later is usually too late.

**Why it's dangerous:** "We'll just scale it" works until it doesn't. Then you're down, your customers are angry, and you're rewriting everything while also trying to keep the business alive.

**Real example:** Product went viral. Couldn't handle the load. Spent 6 weeks firefighting instead of talking to customers. By the time they fixed it, the moment had passed.

**The fix:** You don't need to build for Google scale on day one. But you do need to know what breaks at 10x your current load and have a plan for it.

### 🚩 "Anyone could build this"

**The problem:** If it's true, someone will. Probably someone with more money than you.

**Why it's dangerous:** "Simple" is not the same as "easy to replicate." But if your entire moat is "we built it first," you don't have a moat.

**Real example:** Great product, simple concept. Well-funded competitor copied it in 3 months with a bigger team and better marketing. Original startup couldn't compete.

**The fix:** Your moat isn't that you built it. It's: your data, your network effects, your brand, your deep expertise, your customer relationships, or your execution speed. Build that, not just features.

## Go-to-Market Red Flags

### 🚩 "If we build it, they will come"

**The problem:** No they won't.

**Why it's dangerous:** Distribution is harder than building. Marketing is harder than engineering. Sales is harder than product development. Nobody tells you this in computer science class.

**Real example:** Technically superior product. Better architecture. Cleaner code. Better performance. Lost to inferior competitor who had a VP of Sales and a marketing budget.

**The fix:** Build distribution into your plan from day one. How will people find you? How will they try you? How will they buy from you? These questions are as important as "how does the algorithm work?"

### 🚩 "We're targeting everyone"

**The problem:** If you're for everyone, you're for no one.

**Why it's dangerous:** "Our tool helps all developers" means you help none of them specifically. Specific pain points get budgets. Generic nice-to-haves don't.

**Real example:** "We make developers more productive!" (So does coffee.) "We help teams collaborate!" (So does Slack.) "We optimize workflows!" (What workflows?) No traction.

**The fix:** Pick the narrowest possible customer you can survive on. "DevOps engineers at Series B startups dealing with Kubernetes cost overruns." That's specific enough to build for.

### 🚩 "We don't need sales, we're product-led"

**The problem:** Product-led growth is great. It's also not enough for anything over $50K/year.

**Why it's dangerous:** Developers can approve a $500/month tool. They cannot approve a $50K/year contract. That needs procurement, legal, security review, and a VP signature. That's sales.

**Real example:** Amazing adoption, developers loved it, usage was through the roof. Couldn't close enterprise deals because they had nobody who could navigate procurement. Lost deals to worse products with better sales teams.

**The fix:** Product-led growth gets you to $1M ARR. Sales gets you to $10M. You need both.

## Team & Execution Red Flags

### 🚩 "We're all technical co-founders"

**The problem:** Who's selling? Who's talking to customers? Who's making sure you don't run out of money?

**Why it's dangerous:** A company of five engineers is a research project, not a startup. Someone needs to own the business side or you'll build impressive technology that nobody buys.

**Real example:** Four excellent engineers. Beautiful architecture. Zero revenue after 2 years. Nobody wanted to "do the business stuff." Eventually hired a CEO. Should have done it 18 months earlier.

**The fix:** If you're all technical, get a business co-founder, hire business people early, or commit to one technical founder becoming the business leader. Don't just hope the business stuff will work itself out.

### 🚩 "We're waiting for the perfect moment to launch"

**The problem:** The perfect moment is a myth.

**Why it's dangerous:** While you're polishing your product, someone else is talking to customers and iterating. Guess who wins?

**Real example:** Team spent 18 months in stealth. Launched to crickets. Competitor had launched 12 months earlier with a worse product but now had customer feedback, revenue, and momentum.

**The fix:** Launch when you have something that solves one problem well enough that someone will pay for it. Not perfect. Not complete. Good enough.

### 🚩 "We'll raise money to solve this problem"

**The problem:** Money doesn't solve problems. It just makes problems more expensive.

**Why it's dangerous:** Investors want to see traction, product-market fit, and a path to profitability. "We need money to figure out our business model" is not investable.

**Real example:** "We have 50,000 users! We'll raise a Series A and hire salespeople!" VCs asked: "What's your conversion rate?" (0.1%) "What's your CAC?" (Don't know) "What's your LTV?" (Don't know) No funding.

**The fix:** Raise money to scale what's working, not to figure out what works. Figure that out with sweat equity first.

## The Reality Check Test

Go through this checklist honestly. For each red flag:

**🚩 = Major problem, fix immediately**
**⚠️ = Concerning, needs a plan**
**✅ = You're good here**

If you have more than 3 major red flags, stop building and fix your fundamentals first.

If you have 1-2 major red flags, you can keep building but make a plan to address them within the next quarter.

If you have zero red flags, congratulations. You're either in the top 5% of startups or you're not being honest with yourself.

## What Good Looks Like

Just so you know I'm not all doom and gloom, here's what the successful startups I've coached had in common:

✅ Talked to customers before writing code
✅ Tested pricing early (even if it was just "would you pay $X?")
✅ Built for a specific, narrow use case first
✅ Had someone owning the business side
✅ Launched before they felt ready
✅ Knew their unit economics (CAC, LTV, churn)
✅ Had a clear answer to "why can't they just build this?"
✅ Focused on one thing and did it really well
✅ Could articulate their business model in one sentence
✅ Actually had customers, not just users

## Next Steps

**If you're not pursuing the business path:** You can close this document and go back to building. Seriously. Not everything needs to be monetized.

**If you found yourself in these red flags and ARE pursuing business:**

1. Don't panic. Everyone hits some of these.
2. Pick the biggest one and fix it this month.
3. Use the [3-Question Framework](./3-question-framework.md) to sharpen your value prop.
4. Use the [Cost Model Template](./cost-model-template.md) to validate your business case.
5. Talk to 10 potential customers this week. Not to pitch, to learn.

And remember: the goal isn't to avoid all mistakes. The goal is to make them quickly, learn fast, and not make the same mistake twice.

---

*The best time to fix these was before you started. The second best time is now.*
