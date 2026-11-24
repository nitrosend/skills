# Nitrosend

Nitrosend is an email marketing platform built for AI agents. The `nitrosend` MCP server in this extension connects to `https://api.nitrosend.com/mcp`; the first tool call opens a browser OAuth sign-in.

- Start with `nitro_get_status` when the account, brand or sending readiness is unknown.
- For any new email copy or design, call the compose tool with `composition_mode: "intent"` and follow its `next_call`.
- Never send without the user's explicit approval: review with `nitro_review_delivery`, send a test with `nitro_send_test_message`, then approve and send with `nitro_control_delivery`.
- The skills in `skills/` cover setup, campaigns and newsletters, flows, transactional email, contacts, migration from Mailchimp or Klaviyo, deliverability and analytics.
