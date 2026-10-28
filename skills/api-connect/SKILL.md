---
name: api-connect
description: Connect an app to a third-party API such as WhatsApp Cloud API, Razorpay, Google Sheets, Google Forms or webhooks, with setup steps and working code. Use when asked to integrate an API, payment gateway, or automation.
---
# API Connect

## Ask first (only if missing)
- Which service and what should happen (send message, take payment, save lead...)
- Your stack (Next.js, Node, Apps Script, n8n, Zapier)
- Test or live mode

## Steps
1. **Account setup** - what to create in the service dashboard, and which keys you need.
2. **Env variables** - names and where to store them.
3. **Code** - the request or SDK call, with error handling.
4. **Webhook** (if the service sends events) - endpoint code + signature verification.
5. **Test** - how to test in sandbox/test mode.

## Common ones
- **WhatsApp Cloud API** - template messages need approval; 24-hour window for free-form replies.
- **Razorpay** - create order on server, open checkout on client, verify signature on server.
- **Google Sheets** - service account or Apps Script web app.
- **Google Forms** - Apps Script `onFormSubmit` trigger to push data elsewhere.

## Rules
- Keys only in server env, never in frontend code or Git.
- Always verify webhook signatures.
- Use test mode first. Say clearly when something will charge real money or message real customers.
