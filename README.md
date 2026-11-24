# Nitrosend agent skills: email marketing for AI agents

[Nitrosend](https://nitrosend.com) is an email marketing platform built for AI agents. These 21 agent skills teach any agent (OpenClaw, Hermes Agent, Antigravity, Gemini CLI, Claude Code, Codex, Cursor) to write and send newsletters and email campaigns, build email automation (welcome series, abandoned cart, post-purchase, win-back), send transactional emails, import contacts and manage mailing lists, move off Mailchimp or Klaviyo, check deliverability and read analytics.

The skills drive the Nitrosend remote MCP server at `https://api.nitrosend.com/mcp`. Sign-in is browser OAuth, no API key, and there's a free plan.

## Install

**skills.sh (Claude Code, Codex, Cursor, OpenCode and 40+ agents)**

```bash
npx skills add nitrosend/skills
```

**Hermes Agent**

```bash
hermes skills tap add nitrosend/skills
```

Then add the MCP server to `~/.hermes/config.yaml` and sign in:

```yaml
mcp_servers:
  nitrosend:
    url: "https://api.nitrosend.com/mcp"
    auth: oauth
```

```bash
hermes mcp login nitrosend
```

**OpenClaw**

```bash
openclaw mcp add nitrosend --url https://api.nitrosend.com/mcp --transport streamable-http
openclaw mcp login nitrosend
```

**Antigravity**

```bash
agy plugin install https://github.com/nitrosend/skills
```

**Gemini CLI**

```bash
gemini extensions install https://github.com/nitrosend/skills
```

The Antigravity plugin and Gemini CLI extension bundle the MCP server; the first tool call opens the sign-in. For ChatGPT, Claude, Cursor, VS Code and other clients, see the [setup guides](https://docs.nitrosend.com/integrations/overview) or the [MCP server repo](https://github.com/nitrosend/mcp).

## Skills

| Skill | What it does |
| --- | --- |
| [`abandoned-cart-emails`](skills/abandoned-cart-emails/SKILL.md) | Build abandoned cart, abandoned checkout and browse abandonment reminder emails for an online store, plus post-purchase and win-back emails, using Shopify store activity or events an online store sends through the Events API. Use for ecommerce email marketing and cart recovery. |
| [`agency-client-email`](skills/agency-client-email/SKILL.md) | Run email marketing for agency clients: switch between the client accounts and brands this connection can reach, create a new brand with its own Brand Kit, build each brand's flows and newsletters, and keep each one's sender and contacts separate. Use for marketing agencies and freelancers managing several brands. |
| [`build-flow`](skills/build-flow/SKILL.md) | Build email automation flows with triggers, steps, waits, splits and webhooks: marketing automation and email automation for welcome series, onboarding emails, abandoned cart and browse abandonment, post-purchase, review requests, win-back, re-engagement, drip and nurture sequences, and custom event-driven flows. |
| [`compose-email`](skills/compose-email/SKILL.md) | Create or edit email templates with Nitrosend's section-based email designer: responsive, on-brand email design from the Brand Kit, email copywriting, subject lines and preview text, with preview and test sends. |
| [`contacts-and-segments`](skills/contacts-and-segments/SKILL.md) | Manage contacts, email lists, segments, tags and subscribers: import contacts by CSV, sync HubSpot or Attio, search a contact's history, build segments from data and engagement, and verify email addresses to clean the list. Use for audience management and email list hygiene. |
| [`email-brand-kit`](skills/email-brand-kit/SKILL.md) | Build an email brand kit from a website: logo, brand colours, fonts and tone of voice, so newsletters, campaigns and automated emails match the brand. Use for email branding, a brand kit, on-brand email design, brand guidelines or brand voice. |
| [`email-deliverability-check`](skills/email-deliverability-check/SKILL.md) | Check and fix email deliverability: sending domain setup, SPF, DKIM and DMARC records, sending readiness, bounces and spam complaints, so emails reach the inbox instead of spam in Gmail and Outlook. Use for deliverability, DNS records or why emails go to spam. |
| [`email-integrations`](skills/email-integrations/SKILL.md) | Connect the tools that trigger emails and update contacts: Shopify, HubSpot, Attio, Mailchimp and ActiveCampaign connect natively in the Nitrosend app, and any other app or backend, including Zapier and Make, can send contacts and events through the REST API or Events API. Use for email integrations and automations between tools. |
| [`email-marketing-bible`](skills/email-marketing-bible/SKILL.md) | Apply durable email-marketing principles without treating static benchmarks, laws, vendor features, or prices as current facts. Use for strategy, flows, deliverability, copy, segmentation, measurement, and platform evaluation. |
| [`email-platform-migration`](skills/email-platform-migration/SKILL.md) | Switch email platforms: connect ActiveCampaign, or import contacts, lists, tags and custom fields exported as CSV from MailerLite, Brevo (Sendinblue), Kit (ConvertKit), beehiiv, Substack, Constant Contact, Omnisend or any other platform, keeping unsubscribes and suppressions, then rebuild the emails you need. Use for any email migration. |
| [`import-contacts`](skills/import-contacts/SKILL.md) | Import contacts into Nitrosend from inline records or CSV, including lists exported from Klaviyo, MailerLite, Brevo, Kit (ConvertKit), beehiiv or Substack. Handles email opt-in, consent, list assignment and tagging for your mailing list and subscribers. |
| [`klaviyo-migration`](skills/klaviyo-migration/SKILL.md) | Migrate from Klaviyo to Nitrosend: import profiles and lists exported from Klaviyo as CSV, keep unsubscribes and suppressions, then rebuild flows such as welcome series, abandoned cart and post-purchase as Nitrosend drafts and connect Shopify for store events. |
| [`mailchimp-migration`](skills/mailchimp-migration/SKILL.md) | Migrate from Mailchimp to Nitrosend: connect Mailchimp to bring audiences, members and merge fields with subscribed, unsubscribed and cleaned status preserved, then rebuild the campaigns and customer journeys you still need as Nitrosend emails and flows. |
| [`nitrosend-analytics`](skills/nitrosend-analytics/SKILL.md) | Inspect Nitrosend email marketing analytics for the account, a campaign, a newsletter, a flow or a message: opens, clicks, bounces, unsubscribes, trends and benchmarks, turned into bounded recommendations on what to fix first. |
| [`nitrosend-setup`](skills/nitrosend-setup/SKILL.md) | Guided Nitrosend email marketing setup. Walks through remote MCP connection, the Brand Kit from the website, brand-subdomain preparation or customer sending-domain verification (SPF, DKIM, DMARC), and sender defaults. Also offers to configure proactive analytics (daily, weekly or monthly reports). |
| [`send-campaign`](skills/send-campaign/SKILL.md) | End-to-end email campaign and newsletter workflow: create, design, target a list or segment, preview, test, approve, and send or schedule an email campaign. Covers newsletters, promotional emails, product announcements, launches, sales and Black Friday email blasts. |
| [`send-transactional`](skills/send-transactional/SKILL.md) | Send transactional emails for app-triggered communications: receipts, password resets, magic links, OTPs, order confirmations, shipping notifications and system alerts, by REST API, SDK or Events API. Single recipient, immediate delivery, no campaign or approval needed. |
| [`shared-email-inbox`](skills/shared-email-inbox/SKILL.md) | Read and reply to email from a shared inbox: inbox conversations, replies, reply-all, Cc, Bcc and attachments, and flows that sort replies with AI and send the next email. Use for customer emails, support replies and follow-ups. |
| [`shopify-email-marketing`](skills/shopify-email-marketing/SKILL.md) | Run Shopify email marketing: connect a Shopify store, import customers with their marketing consent, and use orders, refunds and store activity in segments, newsletters and automated emails. Use for Shopify email, ecommerce email marketing and online store emails. |
| [`signup-form-builder`](skills/signup-form-builder/SKILL.md) | Create a website signup form for a mailing list and get the embed snippet for Webflow, Squarespace, WordPress, Wix, Shopify or any website. New subscribers join the list and can get a welcome email automatically. Use for signup forms, subscribe forms, newsletter signups, lead capture and growing an email list. |
| [`welcome-email-series`](skills/welcome-email-series/SKILL.md) | Build a welcome email or welcome series for new subscribers or customers: a first welcome email, then follow-up emails over the first days, triggered by a signup form or a new list member. Use for welcome emails, onboarding emails and new subscriber journeys. |

## What you can ask

- "Set up Nitrosend and build my email Brand Kit from my website."
- "Write this week's newsletter from our latest blog posts and send it to my subscribers on Thursday."
- "Build a welcome series and an abandoned cart flow for my Shopify store."
- "Move my list and unsubscribes over from Mailchimp."
- "Send a password reset email with our transactional template."
- "How did last month's email campaigns do?"

Every send needs your explicit approval.

## License

MIT
