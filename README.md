# TAMI for Claude

![TAMI](assets/tami-icon.png)

TAMI is a B2B data assistant for sales, marketing and research teams. This plugin connects Claude to TAMI's MCP server, so you can find and research companies and contacts by describing them in plain language, without dashboards or exports.

## What you can do

- **Search companies** in plain English by country, sector, size, turnover and technology.
- **Find and enrich contacts:** decision makers by job title, seniority and department, with verified work email and phone where available.
- **Match from a website or company name:** get a full company profile, or companies similar to it.
- **Detect what a business uses:** shipping providers, payment processors and e-commerce platforms.
- **Read company news:** recent company and sector news, with headline, date and link.
- **Professional network:** look up professional profiles and company pages, and get summaries of their recent activity and posts.
- **Draft outreach:** a personalised message for a prospect from the information gathered.
- **Check your usage:** see how much of your allowance is left.

## What you need

A TAMI account with available credits. There is no separate subscription for using TAMI in Claude: it uses the same credit wallet as the TAMI API and Lead Enrichment, and lookups that return nothing use no credits. Prices are at https://tami.ai/pricing/.

The first time Claude uses a TAMI tool, your browser opens TAMI's sign-in page. Sign in with your TAMI account and approve the requested permissions. Claude never sees your password. The plugin only reads data and drafts text: it never writes to your other systems or sends messages on your behalf.

## What this plugin contains and where your data goes

- The plugin contains no code. It only tells Claude the address of TAMI's MCP server: `https://mcp.tami.ai/mcp`.
- When Claude calls a TAMI tool, the request it builds (search criteria, company websites or names, the contact details you ask about) is sent to `https://mcp.tami.ai/mcp`, and TAMI's answer comes back to Claude.
- Sign-in uses OAuth through `https://mcp.tami.ai` and TAMI's sign-in service at `https://auth.tami.ai`.
- The plugin sends nothing anywhere else. On TAMI's side, results come mainly from TAMI's own B2B database; news and professional-network data are retrieved through licensed providers.
- The data you request becomes part of your Claude conversation and is processed by Anthropic under Anthropic's terms. TAMI's privacy policy has a section on the TAMI AI connector for AI assistants.

## Example prompts

- "Find SaaS companies in Berlin with 50 to 200 employees."
- "Fintechs in Germany using Stripe."
- "Who ships with DPD and turns over more than £10M?"
- "Find companies similar to iwoca.co.uk and profile the top three."

## More information and support

- About TAMI in AI assistants: https://tami.ai/mcp/
- Privacy policy: https://tami.ai/privacy-policy/ (privacy and data requests: dataprivacy@tami.ai)
- Terms of service: https://tami.ai/terms-of-service/
- Support: support@tami.ai or https://tami.ai/contact-us/
