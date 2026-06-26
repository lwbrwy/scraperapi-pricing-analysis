# ScraperAPI Pricing Explained: How Much Does It Actually Cost? What Do Hobby, Startup, and Business Plans Include? Is There a Free Trial or Discount Code? (Full Credit Cost Breakdown Inside)

So you typed "ScraperAPI pricing" into Google because you want a straight answer, not a glossy sales page. Fair enough. The pricing page itself is simple at first glance — a few plans, a few dollar amounts — but the moment you start scraping real websites, the actual cost depends on something the landing page barely mentions: credit multipliers. A request to a basic blog costs 1 credit. The same kind of request to Amazon costs 5. Hit Google or Bing and it jumps to 25. Add JavaScript rendering or a Cloudflare bypass and the number climbs again.

This is the part most people miss until they're three weeks into a project, staring at a dashboard wondering why their "100,000 credits" disappeared after 7,000 requests. Let's walk through what you're actually paying for.

## What Is ScraperAPI, in One Paragraph

ScraperAPI is a web scraping API that handles the unglamorous infrastructure work — proxy rotation, headless browser rendering, CAPTCHA solving, retries — so you can send one API call and get back a clean HTML or JSON response instead of building and babysitting your own scraping stack. It routes requests through a pool of more than 40 million IPs spread across 50+ countries, and it's used by a sizable list of companies doing e-commerce monitoring, SEO tracking, market research, and AI training data collection.

That's the pitch. The pricing question is where things get more interesting.

## How the Credit System Actually Works

Every plan gives you a monthly bucket of **API credits**. Every request you send burns some number of those credits, but — and this is the detail that matters — not every request costs the same.

> A standard, unprotected page costs **1 credit**. Scraping Amazon costs **5 credits**. Google and Bing (and their subdomains) cost **25 credits**. LinkedIn costs **30 credits**. Sites guarded by Cloudflare, Datadome, or PerimeterX add another **10 credits** on top when ScraperAPI has to bypass that protection.

On top of the domain-based pricing, optional parameters add their own multipliers:

| Parameter | Extra Credit Cost |
|---|---|
| `premium=true` | +10 credits/request |
| `render=true` (JS rendering) | +10 credits/request |
| `screenshot=true` | +10 credits/request |
| `ultra_premium=true` | +30 credits/request |
| `premium=true` + `render=true` | 25 credits/request total |
| `ultra_premium=true` + `render=true` | 75 credits/request total |

One genuinely fair detail: **you're only billed for successful requests.** Failed scrapes (anything outside a 200 or 404 response) don't burn your credits, so you're not paying for the service's own failures — only for data it actually delivered.

This is also why a lot of independent reviews flag the "100,000 credits" number on the entry-level plan as misleading if read at face value. If your target is Amazon with rendering turned on, that's 15 credits per request — meaning your 100,000-credit allowance gets you roughly 6,600 successful scrapes, not 100,000. Before committing to a plan, it's worth running a few test requests through the [Domain Cost Estimator](https://api.scraperapi.com/account/urlcost) in the dashboard so you know your real per-request cost ahead of time.

## ScraperAPI Plans and Pricing — Full Comparison Table

Here's the complete current lineup, pulled straight from the official pricing page. All plans include JS rendering, premium proxies, JSON auto-parsing, rotating proxy pools, custom headers, CAPTCHA/anti-bot bypass, custom sessions, automatic retries, unlimited bandwidth, and a 99.9% uptime guarantee — the difference between tiers is volume, concurrency, and geotargeting scope.

| Plan | Monthly Price | Annual Price (10% off) | API Credits/Month | Concurrent Threads | Geotargeting | Buy Link |
|---|---|---|---|---|---|---|
| **Free Trial** | $0 (7 days) | — | 5,000 (one-time trial) | 5 | — | [ Start free trial, no card needed](https://www.scraperapi.com/?fp_ref=coupons) |
| **Hobby** | $49/mo | $44.10/mo | 100,000 | 20 | US & EU only | [ Get the Hobby plan](https://www.scraperapi.com/?fp_ref=coupons) |
| **Startup** | $149/mo | $134.10/mo | 1,000,000 | 50 | US & EU only | [ Get the Startup plan](https://www.scraperapi.com/?fp_ref=coupons) |
| **Business** | $299/mo | $269.10/mo | 3,000,000 | 100 | Global | [ Get the Business plan](https://www.scraperapi.com/?fp_ref=coupons) |
| **Scaling** (Most Popular) | $475/mo | $427.50/mo | 5,000,000 | 200 | Global | [ Get the Scaling plan](https://www.scraperapi.com/?fp_ref=coupons) |
| **Professional** | $975/mo | $877.50/mo | 10,500,000 | 300 | Global | [ Get the Professional plan](https://www.scraperapi.com/?fp_ref=coupons) |
| **Advanced** | $1,975/mo | $1,777.50/mo | 21,500,000 | 500 | Global | [ Get the Advanced plan](https://www.scraperapi.com/?fp_ref=coupons) |
| **Enterprise** | Custom quote | Custom quote | 22,000,000+ | 500+ | Global | [ Contact sales for Enterprise pricing](https://www.scraperapi.com/?fp_ref=coupons) |

A few things worth noting from this table that aren't obvious at a glance:

- **Geotargeting is gated by tier.** Hobby and Startup are limited to US & EU proxies only. If your project needs country-level targeting anywhere else in the world, you need at least the Business plan.
- **Pay-as-you-go is only available from Scaling upward.** On Hobby, Startup, and Business, running out of credits mid-cycle means either upgrading to the next tier or talking to support — there's no PAYG overflow option.
- **Credits don't roll over.** Whatever you don't use resets at renewal, so it's worth sizing your plan to your actual monthly volume rather than overbuying "just in case."
- **Unlimited analytics history** kicks in starting at the Business plan; Hobby and Startup are capped at 30 days of dashboard history.

## Is There a Free Plan or Free Trial?

Yes, and it's not a watered-down demo. New accounts get **1,000 free API credits** with up to 5 concurrent connections just for signing up — no credit card required. On top of that, the **7-day trial** bumps you up to **5,000 credits**, which is enough to actually test the service against your real scraping targets (not a toy example) before you decide whether to pay for anything.

This matters more than it sounds like, because the entire pricing question hinges on your specific use case. A 5,000-credit trial against a normal blog gets you 5,000 test requests. The same trial against Amazon with rendering enabled gets you a few hundred. Running your own numbers during the trial period is the only way to know which plan actually fits before you commit.

## Is There a ScraperAPI Discount Code?

There's an automatic 10% discount baked into every plan if you choose annual billing instead of monthly — no code needed, it's applied at checkout. For new users on monthly billing who want to test the waters at a reduced cost on their first invoice, signing up through a current promotional link before subscribing is generally the easiest way to lock in whatever introductory offer is active at the time.

👉 [Check the current sign-up offer and start your free trial here](https://www.scraperapi.com/?fp_ref=coupons)

## Hobby vs. Startup vs. Business: Which Plan Should You Actually Pick?

This is the question that actually matters more than the raw price tag, since the "right" plan depends entirely on what you're scraping and how often.

**Pick Hobby ($49/mo) if:**
You're running a personal project, a small side hustle, or testing an idea — checking competitor prices on a handful of products, monitoring a few dozen pages, or building a prototype. 100,000 credits sounds like a lot until you remember Amazon costs 5x and Google costs 25x; for plain unprotected pages, though, this genuinely covers a lot of ground.

**Pick Startup ($149/mo) if:**
You've outgrown casual scraping and need consistent volume — say, a small SaaS product or an agency running scraping jobs for a handful of clients. 1,000,000 credits with 50 concurrent threads is a meaningful step up, though you're still capped at US/EU geotargeting.

**Pick Business ($299/mo) if:**
You need global geotargeting (not just US/EU), unlimited analytics history, or you're running production-grade infrastructure that other parts of your business depend on. This is also the first tier where the jump in concurrent threads (100) starts to matter for larger parallel jobs.

**Pick Scaling and above if:**
You're past the "which plan" question and into "how do we keep this predictable at high volume" territory — these tiers add pay-as-you-go overflow billing so you're never hard-capped mid-month, plus priority support starting at Professional.

## What People Actually Say About ScraperAPI

Independent review aggregation paints a fairly consistent picture: ScraperAPI sits around **4.5/5 on Trustpilot** and **4.4/5 on G2**, with the majority of reviews landing in five-star territory. The recurring praise points are the same across most platforms — clean documentation, a genuinely simple integration (drop it into existing code as a proxy replacement), and responsive support. One long-time reviewer specifically called out that upgrading or downgrading plans was painless, which tracks with how the credit system is structured.

On the critical side, the most common complaint isn't about reliability — it's about the credit math being less intuitive than the headline number suggests, especially once you start mixing in rendering and premium-proxy parameters on harder targets. Independent benchmarking from third-party testers has also noted that performance varies a lot by target: ScraperAPI tends to perform very well on mainstream sites like Amazon, GitHub, and standard e-commerce pages, but less consistently on sites with aggressive, frequently-changing anti-bot systems.

## How ScraperAPI Compares to Other Scraping APIs

If you're weighing this against alternatives, here's roughly how the positioning shakes out based on current market comparisons:

- **vs. Bright Data** — Bright Data is the more powerful, more expensive enterprise option, generally starting around $499/mo, aimed at teams that need the highest possible success rates regardless of cost.
- **vs. Scrape.do** — Scrape.do undercuts ScraperAPI on raw entry price (around $29/mo), which appeals to budget-conscious solo developers running simple, unprotected scrapes.
- **vs. ScrapingBee** — Similar developer experience and a comparable $49/mo entry point, generally without the same credit multiplier system, which makes its costs more predictable for some workloads.
- **vs. Oxylabs / ScrapingDog** — Strong alternatives if structured, platform-specific JSON output is your priority over raw HTML.

None of these are universally "better" — it depends on whether your priority is price predictability, raw success rate on hard targets, or ease of integration. For most developers running moderate-volume scrapes against mainstream sites, ScraperAPI's balance of price and simplicity is exactly why it remains one of the most recommended starting points in this category.

## Frequently Asked Questions

**Does one API request always cost one credit?**
No. The base rate is 1 credit for a standard page, but the actual domain (Amazon, Google, LinkedIn, etc.) and any parameters you add (rendering, premium proxies) multiply that cost. Use the dashboard's cost estimator to check before scraping at scale.

**What happens if I run out of credits mid-month?**
On Hobby, Startup, or Business, you can upgrade to the next tier (which usually comes with a better price-per-credit) or contact support about a custom arrangement. Scaling, Professional, Advanced, and Enterprise customers can keep scraping via pay-as-you-go at a fixed rate instead.

**Can I cancel anytime?**
Yes — cancellation is available anytime from the dashboard or by contacting support, and you won't be charged again after cancelling.

**Is there a refund policy?**
ScraperAPI offers a 7-day, no-questions-asked refund if you're not satisfied with the service.

**Do unused credits roll over?**
No. Your credit balance resets at each renewal, so it's worth matching your plan size to your actual monthly usage rather than stockpiling unused credits.

## Bottom Line

If your scraping target is mostly plain pages without heavy anti-bot protection, the Hobby plan's $49/month genuinely covers a lot of ground for personal projects or early-stage products. The moment Amazon, Google, LinkedIn, or Cloudflare-protected sites enter the picture, run your numbers through the credit table above first — the sticker price and the real cost per successful scrape are two different things.

The cleanest way to find out which plan fits your actual workload is to just test it: sign up for the free trial, point it at your real targets, and watch your credit consumption in the dashboard before deciding anything.

👉 [Start your free ScraperAPI trial — 5,000 credits, no credit card required](https://www.scraperapi.com/?fp_ref=coupons)
