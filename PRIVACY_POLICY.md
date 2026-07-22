Privacy Policy for Momentum
Last Updated: July 22, 2026

1. Introduction
Momentum ("the App") is an accountability and habit-coaching app. This Privacy Policy explains what information Momentum collects, how it's used, where it's stored, and the choices you have — written to match what the App actually does, not a generic template.

If you do not agree with this policy, please do not use the App.

2. Information We Collect
2.1 Account Information
When you sign in (email/password or Google Sign-In), we collect your email address and display name via Firebase Authentication. We do not receive or store your password — that's handled entirely by Firebase/Google's authentication infrastructure.

2.2 Information You Provide
Profile information: your stated identity goal, top goals, struggle areas (e.g. motivation, forgetfulness, procrastination), and structure preference
Tasks, habits, and events: titles, categories, scheduled dates/times, priority, duration, completion status, and notes
Daily logs: fulfillment scores and reflections you record
Coach conversations: every message you send to the AI Coach, and its replies
Alarm and check-in settings: your chosen wake-up time, check-in times, and which days they're active
2.3 Information Collected Automatically
Push notification token: an identifier issued by Firebase Cloud Messaging, used only to deliver this app's own notifications to your device
Lifetime stats: counters such as tasks completed, current/longest streak — derived from your own task activity
Crash and error reports: if the app crashes or hits an unexpected error, technical details (device model, OS version, app version, and a stack trace) are sent to Firebase Crashlytics so we can fix the problem. These reports do not intentionally include your task content or coach conversations.
Gemini usage counters: a daily count of AI Coach requests and an approximate token count, used only to enforce a fair-use daily limit and are not linked to conversation content beyond that count
2.4 What We Do Not Collect
Momentum has no advertising SDK, no third-party analytics SDK, and does not track you across other apps or websites. There is no in-app purchase or payment data collection at this time.

3. How Your Information Is Stored
All of the information in Section 2.2 and 2.3 (profile, tasks, daily logs, coach conversations, alarm/check-in settings, push token, lifetime stats) is stored in Firestore, Google's cloud database, under Google Cloud/Firebase infrastructure — not only on your device. This lets your data sync correctly if you reinstall the app or sign in again, and is what makes account deletion (Section 6) meaningfully complete.

Two things are genuinely device-local and never leave your phone:

Scheduled local notifications (task reminders, the wake-up alarm's day-to-day scheduling, check-in nudges) are scheduled directly with Android's notification system on your device.
Your chosen notification sound is a setting on your device's own notification channel, handled by Android, not by Momentum.
4. The AI Coach and Google Gemini
When you use the AI Coach — sending a chat message, requesting a daily greeting, or generating an insight — the relevant context (your goals, struggles, recent task activity, and the conversation itself) is sent server-side to Google's Gemini API to generate a response. This happens through Momentum's own backend (a Firebase Cloud Function), using Momentum's own API credentials — you are never asked for your own API key.

This transmission is necessary to generate any AI Coach response; there is no way to use the AI Coach without it.
Google's handling of this data is governed by Google's Privacy Policy and their API terms of service.
You can use every other part of Momentum (tasks, habits, calendar, alarms, check-ins) without ever opening the Coach, and none of your data reaches Gemini unless you do.
Not every Coach interaction calls Gemini — some daily greetings are generated from a template using your own stats when nothing meaningful has changed, at no data-transmission cost beyond what's already stored in Firestore.
5. How We Use Your Information
Core functionality: creating, scheduling, and tracking your tasks, habits, and events
Reminders and alarms: scheduling and delivering local notifications and, as a reliability backstop for time-critical alerts (task-start reminders, the wake-up alarm), a server-triggered push notification via Firebase Cloud Messaging
AI coaching: generating personalized responses and proactive check-ins via Google Gemini (Section 4)
Crash diagnostics: identifying and fixing bugs (Section 2.3)
Abuse and cost protection: per-account daily limits on AI requests and notification-scheduling operations, so a bug or bad actor can't run up unbounded usage
6. Your Rights and Choices
6.1 Delete Your Account
You can permanently delete your account from Profile → Delete account inside the App. This immediately and permanently deletes your profile, tasks, daily logs, coach conversations, alarm/check-in settings, and your Firebase Authentication account itself. This action cannot be undone and does not require contacting us.

6.2 Notification Controls
You can enable or disable notification permissions, the exact-alarm permission, and battery-optimization exemption at any time through your device's own system settings — the App surfaces links to these directly from Profile → Notifications & alarms.

6.3 Avoiding the AI Coach
Since there's no separate opt-out toggle, the simplest way to avoid any data reaching Google Gemini is to not open the Coach section of the app — every other feature works independently of it.

7. Data Sharing
We share information only with the service providers necessary to run the App:

Google Firebase (Authentication, Firestore, Cloud Functions, Cloud Messaging, Crashlytics) — the infrastructure the App runs on
Google Gemini API — only for AI Coach requests you initiate (Section 4)
We do not sell, rent, or trade your personal information. We may disclose information if legally required to do so (e.g. a valid court order).

8. Data Retention
Your data is retained for as long as your account exists. Deleting your account (Section 6.1) permanently removes it from our systems immediately. Independent of your account, Google may retain its own infrastructure-level logs (e.g. Cloud Function invocation logs, Gemini API request logs) according to Google's own retention policies — these are operational logs, not a substitute copy of your data.

9. Children's Privacy
Momentum is not directed at children under 13, and we do not knowingly collect information from children under 13. If you believe a child has provided us information, contact us (Section 11) and we will delete it.

10. International Data Transfer
Momentum runs on Google Cloud/Firebase infrastructure, which may process and store data in countries other than your own, including the United States. By using the App, you consent to this transfer.

11. Contact
Questions about this policy or your data: [insert real support email before publishing]

12. Changes to This Policy
We'll update the "Last Updated" date above whenever this policy changes. Continued use of the App after an update means you accept the revised policy.
