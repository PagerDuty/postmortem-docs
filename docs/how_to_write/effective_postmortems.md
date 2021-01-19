---
cover:
description: Here are concrete steps for producing a postmortem document. You will learn the most important information to include in the postmortem, how to collect and present that information, and how to conduct an effective analysis that results in system improvements.
---
![Effective Postmortems](../assets/img/headers/Postmortems-Tips.png)

Writing detailed and accurate postmortems allows you to learn quickly from mistakes and improve systems and processes for everyone. This guide lists some of the things we do to make sure our postmortems are effective.

## Do
- Make sure the timeline is an accurate representation of events.
- Define any technical lingo/acronyms you use that newcomers may not understand.
- [Separate what happened from how to fix it](https://www.youtube.com/watch?v=TqaFT-0cY7U).
- Write follow-up tasks that are actionable, specific, and bounded in scope.
- [Discuss how the incident fits into our understanding of the health and resiliency of the services affected](https://www.pagerduty.com/blog/postmortem-understand-service-reliability/).

## Do Not
- Use the word "outage" unless it really was an outage. Accurately reflect the impact of an incident. Outage is usually too broad a term to use. It can lead customers to think the product was fully unavailable when that likely was nowhere near the case.
- Change details or events to make things "look better." Be honest in postmortems, otherwise they lose their effectiveness.
- Name and shame someone. Keep postmortems blameless. If someone deployed a change that broke things, it's not their fault. Everyone is collectively responsible for building a system that allowed them to deploy a breaking change.
- Blame "human error." Very rarely is the mistake "rooted" in a human performing an action. There are often several contributing factors (the script the human ran didn't have rate limiting, the documentation was out of date, etc.) that can and should be addressed.
- Only point out what went wrong. Drill down to the underlying causes of the issue.