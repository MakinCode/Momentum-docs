# Momentum Privacy Policy

**Last updated:** 31 July 2026

This policy explains what personal data the Momentum app ("Momentum", "we", "us") collects, why, and what rights you have over it. It's written to describe what the app actually does — not aspirational or boilerplate language — so it should be kept in sync with the app whenever data handling changes.

## Who controls your data

Momentum is developed and operated by **Paul Elliott**, a sole developer based in the United Kingdom. For any question about this policy or your data, contact **p.elliott92@live.co.uk**.

## What we collect

**Account & profile**
- Email address and authentication credentials (via Firebase Authentication, or your Google account if you sign in with Google)
- Onboarding responses: your goals, biggest struggles, life areas you want to improve, description of a successful day, and how much structure you prefer
- App preferences: reminder times, notification settings, alarm schedule, theme, check-in days/times

**Tasks, habits, and events**
- Titles, notes, schedule, recurrence rules, reminders, category, and priority for everything you create in the app

**AI coach**
- Your conversation history with the coach
- Daily activity logs used to generate coaching context
- **Pro tier only:** a longer-term memory of goals, patterns, obstacles, and wins the coach has picked up from conversation, and short notes about people you've mentioned (e.g. "Sarah — running buddy") — kept deliberately minimal, just enough for the coach to reference them naturally

**Device & usage**
- A push-notification token tied to your device, so reminders can reach you
- Your device's timezone offset, used to correctly reset daily limits and reminders at your local midnight, not UTC
- Usage counters (e.g. how many AI messages or items you've created that day), used only to enforce plan limits
- Crash and diagnostic data if the app crashes (via Firebase Crashlytics)

We do not collect payment card details directly — if you subscribe to Pro, payment is handled entirely by Google Play, and we only receive confirmation of your subscription status.

## Why we collect it, and who else sees it

| Data | Purpose | Shared with |
|---|---|---|
| Account/profile/tasks | Running the app's core features | Stored in our Firebase/Google Cloud database. Not shared with anyone else. |
| Coach conversations, goals, struggles | Generating your coach's replies | Sent to **DeepSeek**, the third-party AI provider that powers the coach. Also stored in our own database so the coach has continuity across sessions. |
| Push token | Delivering reminders and alarms | Google's Firebase Cloud Messaging (the delivery mechanism for Android notifications) |
| Crash reports | Fixing bugs | Firebase Crashlytics (Google) |
| Subscription status | Unlocking Pro features | Google Play Billing |

**We never sell your data.** We don't share it with advertisers, data brokers, or anyone outside the processors listed above.

**International transfers:** DeepSeek processes and stores data in China, per their own privacy policy. This means using the AI coach transmits your messages — including goals and struggles you've shared — to servers there. China does not have a UK "adequacy" decision, and DeepSeek doesn't name a specific transfer safeguard (no Standard Contractual Clauses, no International Data Transfer Agreement) — so instead of relying on a safeguard we can't confirm exists, we ask for your **explicit, informed consent** to this specific transfer before your account is created (UK GDPR Article 49(1)(a)). Before you consent, we tell you: who receives your data (DeepSeek), where it's processed (China), that China hasn't been assessed as offering the same standard of protection as the UK, and what that risks in practice — no independent supervisory authority to appeal to, and your usual rights over the data may not apply the same way once it's there. You can't complete sign-up without agreeing to this, since the AI coach is core to what Momentum does — the choice is presented on its own, separately from any other agreement, during onboarding. You can withdraw this consent any time in Settings → AI coach, without deleting your account — this turns the coach off (DeepSeek stops receiving anything new) while everything else keeps working; turning it back on shows you the same disclosure again before it's re-enabled, since consent has to be freshly informed each time it's given. This is enforced server-side, not just hidden in the app: the Cloud Function that talks to DeepSeek checks this setting itself before every call. *[Legal basis and wording checked directly against the EDPB's Guidelines 2/2018 on Article 49 derogations (section 2.1, esp. 2.1.3) on 2026-07-30, not just the bare statute text — but a solicitor still hasn't reviewed it, and should before this goes live. One thing the guidelines themselves flag still worth acting on: they describe consent as a "high threshold" that "might prove not to be a feasible long term solution" — treat this as a stopgap and keep pursuing a named safeguard (SCCs/IDTA) from DeepSeek, or an alternative provider, rather than relying on this indefinitely.]*

**Model training:** DeepSeek uses data sent to it to improve its own models. *[The opt-out DeepSeek describes is a setting on the API account, not something an individual Momentum user can control directly — Momentum has one API account behind all users, so whatever is set there applies to everyone. Check platform.deepseek.com's account/API settings for a data-usage or "improve the model" toggle; if none exists, ask their support directly whether it can be disabled for an API/business account (their consumer-app opt-out may not extend to API accounts by default). Once confirmed, replace this bracket with a plain statement of fact — e.g. "We've opted out of this on your behalf" or "DeepSeek may use conversation content to improve their models; we're seeking an opt-out" — don't leave a bracket in a published policy.]*

## How long we keep it

Your data is kept for as long as your account exists. AI memory (Pro tier) is periodically condensed to keep it manageable as it grows, but nothing is automatically deleted on a timer — it persists until you delete it yourself or delete your account. You can clear your coach conversation history or AI memory independently, without deleting your account, from the 3-dot menu in the Coach screen.

**Deleting your account is permanent and immediate.** It erases your tasks, habits, events, coach conversation history, AI memory, and usage records, and removes your login credentials entirely. This isn't a deactivation — the data is gone.

## Your rights

If you're in the UK or EU, you have the right to:
- **Access** the personal data we hold about you
- **Correct** it if it's inaccurate — most of this you can already do directly in the app
- **Delete** it — available directly in-app via Settings, or by contacting us
- **Export** a copy of your data
- **Object to or restrict** certain processing

To exercise any of these, contact **p.elliott92@live.co.uk**. If you're in the UK and unhappy with our response, you can complain to the Information Commissioner's Office (ico.org.uk). If you're in the EU, you can contact your local data protection authority.

## Children

Momentum is not directed at, and we do not knowingly collect data from, children under 13.

## Security

Data is encrypted in transit (TLS) and at rest, using Google Cloud/Firebase's platform-level encryption. Access to your data is scoped to your account only — enforced both in how the app is built and by server-side rules on our database that we've specifically audited for this.

## Changes to this policy

If we make a material change to what we collect or how we use it, we'll update this page and the "Last updated" date above. Continuing to use Momentum after a change means you accept the update.

---

<!--
INTERNAL NOTE — not part of the published policy, strip before publishing:

Generated 2026-07-30 against the actual current codebase (audited via file-level
tracing, not assumptions) so this reflects real behavior rather than generic
privacy-policy boilerplate. Before publishing:

1. Fill in [DATE OF PUBLICATION]. Developer name and contact email are set.
2. China-hosting is confirmed directly against DeepSeek's own privacy policy
   (cdn.deepseek.com/policies/en-US/deepseek-privacy-policy.html, fetched
   2026-07-30) — it applies to API traffic, not just their consumer app.
   Since DeepSeek doesn't name a transfer safeguard, the legal basis is now
   explicit consent (UK GDPR Article 49(1)(a)), gated in onboarding — see
   Onboarding.jsx's "privacy" step and UserProfile.ai_processing_consent_at.
   Get a solicitor to review the actual consent wording before shipping;
   Article 49(1)(a) has specific informed-consent requirements this hasn't
   been checked against.
   Still open: whether Momentum's API account has opted out of DeepSeek using
   sent data for model training, and reflecting that choice in the "Model
   training" line above.
3. Re-check this document whenever data handling changes (new AI provider,
   new third-party SDK, retention policy changes, etc.) — it will drift out of
   sync with the app otherwise, which is the exact problem this document was
   written to fix in the first place (see the in-app onboarding copy fix in
   the same batch of work, commit c0d47bc).
4. Also update the app's Play Console "Data safety" section to match this
   document once published — that's a separate Play Console form, not
   something in this repo.
-->
