# E-commerce Platforms & Technology Architectures (2025–2026), incl. AI and Agentic Commerce

Research note (as of 2026-11-06). Method caveat: in this session WebFetch could not reach most primary hosts (openai.com, developers.google.com, forrester.com, storeleads.app, gravitykit.com all failed DNS in the sandbox). Most findings therefore come from search-result syntheses of the cited pages. Primary sources (Stripe blog, SEC 10-K, Adobe blog) are marked where available. Treat aggregator numbers as directional.

## 1. What are the market shares of major e-commerce platforms (global and Vietnam)?

### Takeaway
Rankings depend on what is measured. **By number of stores, WooCommerce leads** worldwide and in Vietnam. **By merchant sales (GMV) and among the top/high-traffic sites, Shopify leads** worldwide: about 14% of US e-commerce in 2025 and $378B GMV. In Vietnam, WooCommerce dominates store counts, the local SaaS platforms **Sapo and Haravan** come next, and Shopify is small.

### Cited Findings
**Global: store counts and web coverage**
- HTTP Archive (May 2026, mobile sample): WooCommerce is detected on 6.64% of all measurable web origins and Shopify on 4.76%. Shopify already leads among the top 1M sites. — [GravityKit, ecommerce platform market share 2026](https://www.gravitykit.com/ecommerce-platform-market-share-2026/)
- Store Leads (an active-store tracker; date likely pre-2026): WooCommerce has about 33.4% (4.53M stores) and Shopify about 19.6% (2.66M stores). — [Purethemes WooCommerce statistics](https://purethemes.net/woocommerce-statistics/) / [Colorwhistle](https://colorwhistle.com/woocommerce-vs-shopify-statistics/). Mark: the dataset vintage is uncertain.
- BuiltWith (2026 via Barn2): WooCommerce is on about 8% of the top-1M sites that use e-commerce technology, and Shopify could overtake it. — [Barn2 WooCommerce stats](https://barn2.com/woocommerce-stats/)
- Outlier: one tracker puts Shopify at 45.99% of the "ecommerce-platform market" (2.6× WooCommerce). Its methodology differs and this is not comparable. — [TechnologyChecker](https://www.technologychecker.io/blog/shopify-analytics-trends-insights)
- Method guidance: use Store Leads for active-store counts and BuiltWith for broader detected usage. — [Purethemes](https://purethemes.net/woocommerce-statistics/)

**Global: sales and GMV (the most reliable figures, from primary filings)**
- Shopify FY2025 GMV was about $378.4B (+29% YoY), and Q4 2025 GMV was about $124B (+31%). — [Shopify Form 10-K FY2025 (SEC)](https://www.sec.gov/Archives/edgar/data/1594805/000159480526000007/shop-20251231.htm); [Quartr Q4 2025 summary](https://quartr.com/events/shopify-inc-shop-q4-2025_3eyaGK8a)
- Shopify claims more than 14% of US e-commerce in 2025, up from 12% in 2024. The figure is based on Census data plus internal estimates and excludes POS. — [Marketplace Pulse](https://marketplacepulse.com/articles/amazon-and-shopify-are-now-half-of-us-e-commerce)
- Amazon had about $440B in US sales, which is 35.7% of a $1.2T US e-commerce market in 2025. "Amazon and Shopify are now half of US e-commerce." — [Marketplace Pulse](https://marketplacepulse.com/articles/amazon-and-shopify-are-now-half-of-us-e-commerce)
- Shopify Plus: about 55% of Plus merchants are US-based (about 26,000 stores). Low confidence: the source is a marketing blog. — [Charle Agency](https://www.charleagency.com/articles/shopify-statistics/)

**Vietnam**
- AfterShip (2025) store counts in Vietnam: WooCommerce about 61.2K stores (58.9% of the total), Sapo about 12.3K, Haravan about 11.0K, Shopify about 3.8K. — [AfterShip eCommerce Statistics Vietnam 2025](https://www.aftership.com/ecommerce/statistics/regions/vn)
- AfterShip platform sales share, Vietnam: WooCommerce is first by sales. Custom-built carts are second (US$4.65B, 34.17% of platform sales), Haravan about 7.9%, and Shopify about 0.7%. — [AfterShip VN](https://www.aftership.com/ecommerce/statistics/regions/vn)
- Similarweb (Dec 2025): about 29,649 Haravan-powered websites, most heavily concentrated in Vietnam. — [Similarweb Haravan](https://www.similarweb.com/technology/haravan/)
- WMTips: WooCommerce has a 74.2% share of Vietnamese e-commerce sites in 2026. Its sample looks small, since it shows only 767 Haravan sites. — [WMTips Vietnam](https://www.wmtips.com/technologies/e-commerce/country/vn/)
- BuiltWith Sapo: 9,343 sites ever detected, but very few currently live. BuiltWith likely under-detects Sapo. — [BuiltWith trends Sapo](https://trends.builtwith.com/analytics/Sapo)
- Sapo self-reports "+230,000 merchants" across its omnichannel sales-management/POS product, which is far larger than its website count. A Sapo survey of 15,000 sellers found 77% sell on at least one online channel. Both figures are vendor-reported. — [Sapo blog "Bức tranh kinh doanh 2025"](https://www.sapo.vn/blog/buc-tranh-kinh-doanh-2025)
- Haravan (founded 2014) positions itself on omnichannel: website, social, marketplace sync (Shopee, TikTok Shop, Lazada, Tiki) and offline stores, on a subscription model. — [Hoàng Hà Mobile – Haravan là gì](https://hoanghamobile.com/tin-tuc/haravan-la-gi/)
- An independent comparison finds Sapo's website builder works well but has fewer themes than Haravan. — [StoreStarter Haravan vs Sapo](https://storestarter.pages.dev/vn-en/ecommerce-platform-southeast-asia/haravan-vs-sapo/)

### Inferences
- "Market share" should always be quoted with its metric. WooCommerce wins on store count because it is free and suits long-tail and small sites. Shopify wins on GMV and among serious or high-traffic merchants.
- In Vietnam, Sapo's and Haravan's real footprint is mostly in POS, omnichannel and order management, not in standalone websites. Website trackers undercount them. Much Vietnamese e-commerce GMV runs through marketplaces (Shopee, TikTok Shop, Lazada), which sit outside "platform" share entirely, so a merchant's own website is usually a secondary channel.

### Gaps
- No independent, current (2026) Vietnam share data by GMV covering Sapo vs Haravan. Store Leads and BuiltWith country pages could not be fetched.
- No BigCommerce, Wix or Adobe Commerce share figures were verified this session. Their general order, from widely cited trackers, is Wix and Squarespace in the mid single digits by store count and BigCommerce and Adobe Commerce at about 1% each, but this is not verified here.
- Not verified: the BigCommerce corporate rename (reported as "Commerce", 2025) and the details of Adobe Commerce as a Cloud Service.

## 2. When does headless/composable make sense vs. monolithic SaaS; what's the 2025–2026 sentiment?

### Takeaway
In 2025–2026, sentiment shifted from "MACH everywhere" to pragmatic "composable where it pays." VTEX publicly quit the MACH Alliance (Mar 2025), calling it "dogmatic," amid talk of "composable regret." Defenders blame organisational readiness, not the architecture. Meanwhile SaaS suites (Shopify Plus or Hydrogen, BigCommerce) absorbed headless options, and the "hybrid / MACH monolith" became the mainstream compromise.

### Cited Findings
- March 2025: VTEX CEO Mariano Gomide de Faria called the MACH Alliance "dogmatic" and VTEX withdrew its support. Others voiced "composable commerce regret," and the MACH Alliance president asked for an open conversation. — [Retail Tech Innovation Hub](https://retailtechinnovationhub.com/home/2025/3/26/vtex-ceo-mariano-gomide-de-faria-slams-dogmatic-mach-alliance-as-his-company-pulls-support)
- Counterpoint (May 2025): "Composable architectures and MACH aren't failing companies; what's often missing is organisational readiness." — [Retail Tech Innovation Hub](https://retailtechinnovationhub.com/home/2025/5/26/composable-architectures-and-mach-arent-failing-companies-rather-whats-often-missing-is-organisational-readiness)
- The "MACH monolith" critique: teams bundle many MACH vendors into a new, tightly coupled stack, an in-between of suite and composable. This brings developer pain and periodic replatforms. — [Uniform blog](https://uniform.dev/blogs/the-mach-monolith)
- Costs: commercetools pricing is custom and not public. One aggregator estimates $250K–$2M+/yr in licence. This is unverified. — [Saas-alternatives](https://saas-alternatives.pages.dev/alternatives/commercetools); [PricingSaaS](https://pricingsaas.com/companies/commercetools)
- Open-source headless engines: the Medusa (MIT) core is free with paid Cloud/Enterprise tiers. The Saleor core is free with Saleor Cloud plans, whose quoted entry prices conflict ($159/mo vs $795/mo). Real TCO is dominated by hosting, development and maintenance. Partner implementation rates are not published. — [Swell on Medusa pricing (competitor source)](https://www.swell.is/content/medusa-pricing); [rfp.wiki Medusa vs Saleor](https://www.rfp.wiki/retail-ecommerce/digital-commerce-platforms/medusa/saleor); [Netguru Saleor vs Medusa](https://www.netguru.com/blog/saleor-vs-medusa)
- Vendor (commercetools) framing: headless is "now mainstream." Treat as marketing. — [commercetools blog](https://commercetools.com:443/blog/time-to-switch-modern-headless-commerce-is-now-mainstream)

### Inferences (guidance by business size; synthesis, not a single source)
- **Micro/small (up to ~US$1M GMV; most Vietnamese SMEs):** use monolithic SaaS. Shopify, Wix or BigCommerce globally; Sapo or Haravan in Vietnam, where they bundle POS, marketplace sync and local payments and carriers. WooCommerce fits if the business already runs WordPress or content-led SEO and has low budget, but it carries plugin, security and hosting maintenance. Headless is almost never justified here.
- **Mid-market (~$1M–$50M):** SaaS-plus-apps (Shopify Plus, BigCommerce) covers most needs. Selective headless (e.g., Shopify Hydrogen or a Next.js front end) fits only when content or experience differentiation is a proven revenue driver and an in-house dev team exists.
- **Enterprise / complex B2B, multi-brand, multi-country:** composable (commercetools, or Adobe Commerce, SAP or Salesforce with headless front ends; Medusa or Saleor for engineering-led firms) makes sense when catalog, pricing or B2B logic and integrations outgrow SaaS. That is a seven-figure annual budget including SI and team. Readiness (product org, platform team) is the deciding factor.
- Trend: agentic commerce (section 3) favours platforms that expose clean, structured catalog, inventory and checkout APIs. Big SaaS platforms (Shopify) ship protocol support natively to all merchants, which weakens one argument for going composable.

### Gaps
- No independent quantitative data (Gartner or similar) was retrieved on how many firms reverted from composable to suites, or on actual TCO ratios. The Gartner Magic Quadrant for Digital Commerce 2025 was not accessed.

## 3. What concrete agentic commerce protocols and launches exist as of late 2026, and what adoption data exists?

### Takeaway
Two competing open protocol stacks emerged: **OpenAI + Stripe's Agentic Commerce Protocol (ACP, Sept 2025)** and **Google's AP2 (Sept 2025, payments) plus UCP (Jan 2026, with Shopify; discovery→cart→checkout)**. Card networks (Visa Intelligent Commerce, Mastercard Agent Pay) supply tokenized agent credentials. Consumer uptake of in-chat checkout was weak. **OpenAI shut down Instant Checkout in March 2026** and pivoted to discovery plus retailer apps inside ChatGPT. The protocols themselves keep spreading through platforms such as Shopify Agentic Storefronts and the Stripe Agentic Commerce Suite. Amazon's agent features (Rufus, Buy for Me) carry the only large-scale usage numbers, which are self-reported.

### Cited Findings
**OpenAI / Stripe: ACP and Instant Checkout**
- ACP is an open standard co-developed by Stripe and OpenAI to power Instant Checkout in ChatGPT. It is "open source, Apache 2.0 licensed." At launch, US ChatGPT users could buy from US Etsy sellers, with "over a million Shopify merchants" coming soon. — [Stripe blog (primary)](https://stripe.com/se/blog/developing-an-open-standard-for-agentic-commerce). Launch date: 29 Sept 2025 (per OpenAI's "Buy it in ChatGPT" post; [MetaRouter](https://www.metarouter.io/post/what-is-the-openai-stripe-partnership) misdates it to Oct 2024).
- ACP covers three specs: Agentic Checkout, Delegated Payment and Product Feed. Purchases were single-item at launch. — [VN Studios](https://vnstudios.com/blogs/vns-for-agencies-blog/agentic-commerce-protocol-what-is-it-and-why-it-matters-for-shopify-agencies); [YourStory](https://yourstory.com/ai-story/openai-instant-checkout-agentic-commerce-protocol-ai)
- ACP adopters: Salesforce (Agentforce Commerce, Oct 2025), PayPal, and Microsoft Copilot Checkout, which is built on ACP. — [The Paypers, PayPal adopts ACP](https://thepaypers.com/payments/news/paypal-adopts-acp-to-broaden-payments-and-commerce-in-chatgpt); [Inchoo, State of Agentic Commerce](https://inchoo.net/ecommerce/agentic-commerce/)
- **March 2026: OpenAI discontinued Instant Checkout.** Shoppers now discover products in ChatGPT and buy on the merchant site or in retailer ChatGPT apps. OpenAI said it is prioritising search and product discovery. — [EcomCrew](https://www.ecomcrew.com/openai-pulls-back-on-chatgpt-instant-checkout/); [Shopifreaks](https://www.shopifreaks.com/openai-pivots-from-instant-checkout-to-an-app-based-shopping-model-inside-chatgpt/); [Retail Week](https://www.retail-week.com/technology/charts-of-the-week-openai-drops-instant-checkout-what-does-that-mean/7050782.article); [Storyboard18](https://storyboard18.com/digital/openai-reduces-chatgpt-shopping-focus-shifts-to-product-discovery-93192.html)
- Reported reasons:
  - Low conversion.
  - Brands did not want to become "anonymous fulfillment centers."
  - Stale inventory and price data.
  - OpenAI never built sales-tax collection, which shows volume never scaled.
  - Sources: [Crowdfund Insider](https://www.crowdfundinsider.com/2026/03/267174-instant-checkout-in-chatgpt-reflects-enormous-challenge/); [Naturaily](https://naturaily.com/blog/agentic-commerce-shopify-guide); [marketing4ecommerce](https://marketing4ecommerce.net/en/openai-abandon-instant-checkout/)
- Adoption data (weak, conflicting): Forrester says US consumer adoption of Instant Checkout "remained low and stagnant" from debut to discontinuation. Live Shopify merchants are reported as "fewer than thirty" in one source and "about twelve" in another. A 4% merchant fee was reported (single source). — [Forrester blog (via search)](https://www.forrester.com/blogs/agentic-payments-in-b2c-commerce-where-we-are-now); [Naturaily](https://naturaily.com/blog/agentic-commerce-shopify-guide); [Paz.ai glossary](https://www.paz.ai/glossary/instant-checkout-chatgpt)
- Discrepancy: the date of OpenAI's removal is given as both March 4 and March 24, 2026 by different secondary sources.

**Google: AP2, UCP, Universal Cart**
- AP2 (Agent Payments Protocol), Sept 2025, is payment-agnostic and launched with 60+ partners including Mastercard, PayPal and Coinbase. It works alongside A2A and MCP. — [Forkast UCP glossary](https://forkast.news/glossary/universal-commerce-protocol-ucp/); [Stellagent (JP)](https://stellagent.ai/ja/insights/google-ucp-open-rails-agentic-commerce)
- UCP (Universal Commerce Protocol) was announced at NRF on 11 Jan 2026. It is open source and co-developed with Shopify, with Etsy, Wayfair, Target and Walmart involved. The first implementation is checkout inside AI Mode in Search and the Gemini app. UCP covers discovery→cart→checkout, and AP2 handles payment authorization. — [American Banker](https://www.americanbanker.com/payments/news/google-shopify-unveil-new-agentic-protocol-for-retailers); [Technobezz](https://www.technobezz.com/news/google-launches-universal-commerce-protocol-for-ai-shopping-2026-01-11-jkpd); [Shopifreaks](https://www.shopifreaks.com/google-and-shopify-launch-universal-commerce-protocol/); [Google UCP docs](https://developers.google.com/merchant/ucp)
- Shopify lists UCP supporters: Amazon, Meta, Microsoft, Salesforce, Stripe, Etsy, Target and Wayfair. — [eCommerce Fastlane](https://ecommercefastlane.com/universal-commerce-protocol-explained/)
- Google "Brand Agent" went live with Lowe's, Poshmark and Reebok. A "Universal Cart" spans Search, YouTube and Gmail. — [AI News](https://www.ainews.com/p/google-unveils-universal-commerce-protocol-to-power-agentic-shopping-across-search-gemini-and-retail); [AI Weekly](https://aiweekly.co/alerts/google-universal-cart-unifies-shopping-across-search-youtube-gmail)

**Shopify / Stripe platform rollouts**
- Shopify "Agentic Storefronts" is being activated across stores in 2026 (Spring '26 Edition). It abstracts both UCP and ACP, so merchants don't integrate the protocols directly. Sources conflict on whether merchants are auto-enrolled with opt-out. — [Weaverse](https://weaverse.io/blogs/shopify-spring-26-agentic-storefront-era); [Ask Phill](https://askphill.com/blogs/blog/agentic-commerce-for-shopify-protocols-platforms-and-what-to-prioritize-in-2026)
- The Stripe Agentic Commerce Suite launched 11 Dec 2025. At Stripe Sessions 2026 it was expanded to UCP (Google AI Mode and Gemini), alongside OpenAI, Microsoft and Meta, and extended to Wix, BigCommerce, WooCommerce and Squarespace merchants. — [eCommerce Fastlane, Stripe Sessions 2026](https://ecommercefastlane.com/stripe-agentic-commerce-playbook/)

**Payments networks and other agents**
- Visa Intelligent Commerce (Apr 2025) provides tokenized credentials for AI agents. Partners include Anthropic, Microsoft, Mistral, OpenAI and Perplexity. Mastercard Agent Pay (Apr 2025) integrates with Microsoft Azure OpenAI and Copilot Studio. — [Outlook Business](https://www.outlookbusiness.com/artificial-intelligence/perplexity-partners-with-paypal-for-direct-chat-payments-as-ai-commerce-race-heats-up); [WebFX](https://www.webfx.com/blog/ai/perplexity-in-chat-shopping/)
- Perplexity added in-chat buying with PayPal and Venmo (US), reported as "Instant Buy" before Black Friday 2025. PayPal handles payment, shipping tracking and invoicing. Reported merchants include Abercrombie & Fitch, Ashley, Fabletics, Adorama and Newegg (secondary). — [CNBC via NBC San Diego](https://www.nbcsandiego.com/news/business/money-report/perplexity-partners-with-paypal-for-in-chat-shopping-as-ai-race-heats-up/3825403/); [Stellagent](https://stellagent.ai/insights/perplexity-paypal-in-chat-shopping)
- Amazon:
  - Rufus drove "nearly $12B incremental annualized sales" in 2025 with 300M+ customers. This is Amazon's internal "downstream impact" estimate, not audited revenue. — [PPC Land](https://ppc.land/amazons-ai-shopping-assistant-drove-12-billion-in-sales-for-2025/); [Fortune (Nov 2025, ~$10B figure then)](https://www.fortune.com/2025/11/02/amazon-rufus-ai-shopping-assistant-chatbot-10-billion-sales-monetization)
  - Q1 2026 call: Rufus MAU +115% YoY and engagement +400%. — [PPC Land](https://ppc.land/amazons-ai-shopping-assistant-drove-12-billion-in-sales-for-2025/)
  - "Buy for Me" (the agent buys on third-party brand sites) grew its catalog from 65,000 items at launch to more than 500,000 by Nov 2025. — [PPC Land](https://ppc.land/amazons-ai-shopping-assistant-drove-12-billion-in-sales-for-2025/)
  - Rufus was reportedly folded into "Alexa for Shopping" in May 2026 (single source). — [Presenc.ai](https://presenc.ai/research/alexa-for-shopping-statistics-2026)

### Inferences
- Through late 2026, "agentic commerce" works mainly as **AI-driven discovery and referral** rather than autonomous purchase. Completed agent checkouts remain a niche. Merchants resist losing the customer relationship, and operational gaps (tax, returns, inventory freshness) are unsolved.
- Protocol competition (ACP vs UCP/AP2) is being neutralised by platforms. Shopify and Stripe abstract both, so for SMEs "agent-readiness" means clean product feeds, structured data and accurate inventory, not protocol engineering.
- No Vietnam-specific agentic checkout launches were found. Local relevance is mainly AI search visibility and marketplace AI features.

### Gaps
- No independent volume data (GMV or orders) for agent-completed purchases via ACP, UCP or Perplexity.
- The exact OpenAI shutdown date (Mar 4 vs Mar 24, 2026) and the primary OpenAI wording could not be verified because openai.com was unreachable from this sandbox.
- The Amazon Buy for Me launch date (beta, US, spring 2025) is not verified against Amazon's primary post this session.

## 4. How is generative AI being used in e-commerce operations, with measured impact?

### Takeaway
The best-measured impacts are on **traffic and conversion from AI assistants** (Adobe) and **AI shopping assistants inside large retailers** (Amazon Rufus, self-reported). Claims for gen-AI content such as product descriptions are mostly vendor case studies with weak methodology.

### Cited Findings
- Adobe Analytics, 2025 US holiday season (>1 trillion visits):
  - AI-referred traffic to retail sites rose 693% YoY (Nov +769%, Dec +673%).
  - AI referrals converted 31% better than other traffic, with 32% higher revenue per visit.
  - AI-referred visitors spent 45% more time on site and viewed 13% more pages.
  - In 2024, AI traffic had converted 9% worse than other traffic, so the gap reversed.
  - Sources: [Adobe blog](https://business.adobe.com/blog/ai-driven-traffic-surges-across-industries); [Digital Commerce 360](https://www.digitalcommerce360.com/2026/01/13/generative-ai-online-holiday-shopping-traffic-2025/); [Marketing Dive](https://www.marketingdive.com/news/ai-has-changed-holiday-shopping-heres-what-the-numbers-say/810265/)
- Earlier baseline: GenAI traffic to US retail sites rose 1,200% (Feb 2025 vs Jul 2024). — [Adobe blog, Mar 2025](https://blog.adobe.com/en/publish/2025/03/17/adobe-analytics-traffic-to-us-retail-websites-from-generative-ai-sources-jumps-1200-percent)
- Amazon Rufus: about $12B incremental annualized sales in 2025, plus Rufus engagement figures (see section 3). This is self-reported. — [PPC Land](https://ppc.land/amazons-ai-shopping-assistant-drove-12-billion-in-sales-for-2025/)
- An unverified claim says Rufus users convert 60% more. No methodology was given. — [Ecommerce Nation (FR)](https://www.ecommerce-nation.fr/?p=126529)
- AI product descriptions: the most-cited +23.7% conversion uplift comes from a Swiss retailer experiment, attributed to Migros or Linearloop by different sources. The original methodology is unverified. Other "+40%" claims are vendor marketing. — [Xictron](https://www.xictron.com/en/blog/ai-generated-product-descriptions-e-commerce/); [Infocepts](https://www.infocepts.com/blog/boosting-e-commerce-conversions-with-generative-ai-powered-product-descriptions)
- Academic: an LLM vs human product-ad benchmark exists (arXiv 2412.19610, Dec 2024). — [arXiv](https://arxiv.org/html/2412.19610v1)
- McKinsey (second-hand): agentic AI can speed content creation by 10–15×. The primary report was not retrieved. — [Raftlabs](https://www.raftlabs.com/blog/generative-ai-in-ecommerce)

### Inferences
- Operational uses are now standard features inside SaaS platforms: product copy, image generation and editing, semantic search and recommendations, support chatbots, and merchandising/ops assistants (e.g., Shopify Magic and Sidekick, built-in assistants on Sapo and Haravan). SMEs get gen-AI mostly through these features rather than by building their own, which is another reason SaaS suits small businesses.
- The largest measurable commercial shift is in **acquisition**: shoppers increasingly arrive via ChatGPT, Gemini or Perplexity. "Generative engine optimisation" (structured catalog data and feeds) is becoming as important as classic SEO.

### Gaps
- No rigorous, independent A/B evidence was found for gen-AI content or customer-service agents in e-commerce. Shopify's own Sidekick/Magic usage metrics and McKinsey/BCG primary reports were not retrieved.
- No Vietnam-specific measurements of AI impact in e-commerce were found.
