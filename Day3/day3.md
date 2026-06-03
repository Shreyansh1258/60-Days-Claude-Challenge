# Day 3 – Role-Based Prompting

## What is Role-Based Prompting?
Role-Based Prompting is a technique where you tell an AI what role or profession it should act as before answering your question.
Instead of asking:
"How do I improve my app?"
You ask:
"You are a senior product manager. How do I improve my app?"
The AI then responds from the perspective of that role, using knowledge, priorities, and terminology that an expert in that field would typically use.

## Prompt Without Role

### Prompt
How can I improve user retention in my mobile app?

### Output
Here are the most effective strategies for improving user retention in a mobile app:
Onboarding Experience Get users to their "aha moment" as fast as possible. Reduce friction, skip unnecessary sign-up fields, and show value before asking for commitments. A good first session is the strongest predictor of long-term retention.
Push Notifications (done right) Timely, personalized, and actionable notifications bring users back — but over-messaging kills retention. Segment your audience and trigger notifications based on behavior, not just schedules.
In-App Engagement Loops Design habit-forming loops: trigger → action → variable reward → investment. Think streaks (Duolingo), progress bars, or social feedback. The goal is to make returning feel rewarding.
Personalization Tailor content, recommendations, or UI to each user's behavior. Even simple personalization (like remembering preferences) significantly reduces churn.

## Prompt With Founder Role

### Prompt
You are a startup founder.
How can I improve user retention in my mobile app?

### Output
Great question — retention was honestly the thing that kept me up at night more than anything else in the early days. Here's what actually moved the needle for us:
Nail the first 3 minutes
Everything else is secondary. If someone doesn't "get it" in their first session, they're gone. We cut our onboarding from 7 steps to 3 and Day 1 retention jumped 18 points almost overnight. Be ruthless about removing anything that isn't directly showing value.
Talk to churned users — personally
Not a survey. An actual call or voice message. I used to personally reach out to users who dropped off after Day 3. The patterns you find are gold and you simply cannot get them from analytics alone. Do this every week until you have 50+ conversations under your belt.
Find your activation metric, not a vanity one
For us it wasn't "completed sign-up" — it was a specific action inside the app that correlated with 90-day retention. Took us a while to find it, but once we did, we optimized everything toward getting users there in session one.
Don't over-invest in push notifications early
Every founder does this. You set up a drip campaign and feel productive. But if the core product loop isn't sticky, notifications just remind people why they left. Fix the product first.

## Prompt With Developer Role

### Prompt
You are a senior software developer.
How can I improve user retention in my mobile app?

### Output
How can I improve user retention in my mobile app?
Good question. From an engineering perspective, retention is heavily influenced by things we often treat as "nice to haves" — performance, reliability, and smart systems. Here's where I'd focus:
Performance is retention Users don't consciously think "this app is 200ms slower than it should be" — they just feel friction and eventually stop opening it. Profile ruthlessly. Reduce cold start time, eliminate janky animations, and lazy-load anything not needed on first render. Every 100ms improvement in load time has measurable retention impact.
Instrument everything before optimizing anything Set up proper analytics with event tracking on every meaningful user action. You can't improve what you can't measure. Tools like Mixpanel or Amplitude let you build retention cohorts and pinpoint exactly where users drop off in your funnel. That's your roadmap.
Build a robust offline-first experience Nothing kills retention like an app that's useless without a perfect connection. Cache aggressively, queue actions when offline, sync gracefully when reconnected. Libraries like WatermelonDB (React Native) or Room (Android) make this tractable.
Push notifications via a proper event-driven pipeline Don't trigger notifications from a cron job. Build behavior-based triggers — user hasn't opened in N days, left something mid-flow, reached a milestone. Firebase + a simple event queue gets you there without much overhead.
Crash rate is a retention metric A 1% crash rate sounds small but it's catastrophic at scale. Integrate Sentry or Crashlytics on day one, triage crashes by affected user count (not frequency), and treat a crashing session as a churned user.

## Comparison

- Generic prompt gives general answers.
- Founder prompt focuses on business growth.
- Developer prompt focuses on technical improvements.

## Learnings

1. Role-based prompting improves context.
2. Responses become more targeted.
3. Different roles produce different insights.

