---
cover:
description: The basics of Postmortems. Why postmortems are important, when they should be done, and who is responsible for the postmortem.
---
![What is a Postmortem?](assets/img/headers/Postmortems-WhatIs.png)

> What went wrong and how do we learn from it?

A postmortem (or post-mortem) is a process intended to help you learn from past incidents. It typically involves a blame-free analysis and discussion soon after an event has taken place. An artifact is produced that includes a detailed description of exactly what went wrong in order to cause the incident, along with a list of steps to take in order to prevent a similar incident from occurring again in the future. An analysis of how effective your incident response process itself was during the incident should also be included in the discussion. The value of postmortems comes from helping institutionalize a culture of continuous improvement.

## Why Do Postmortems
During incident response, the team is 100% focused on restoring service. They cannot (and should not) be wasting time and mental energy thinking about how to do something optimally or performing a deep dive on what caused the incident. That's why postmortems are essential—they provide an opportunity to reflect once the issue is no longer impacting users. **The postmortem process drives focus, instills a culture of learning, and identifies opportunities for improvement that otherwise would be lost.**

Without a postmortem, you fail to recognize what you're doing right, where you could improve, and, most importantly, how to avoid making the same mistakes in the future. Conducting an effective postmortem allows you to learn quickly from your mistakes and improve your systems and processes. A well-designed, blameless postmortem allows teams to continuously learn, serving as a way to iteratively improve your infrastructure and incident response process. Be sure to write detailed and accurate postmortems in order to get the most benefit out of them.

## When to Do a Postmortem
**Do a postmortem for every major incident**. This includes **any time incident response is triggered**—even if it is later discovered that severity was actually lower, it was a false alarm, or it quickly recovered without intervention. A postmortem should not be neglected in these cases because it is still an opportunity to review what did and did not work well in the incident response process. If the incident should not have triggered incident response, it is worthwhile understanding why it did so monitoring can be tuned to avoid unnecessarily triggering incident response in the future. Doing this analysis and follow-up action will help prevent alert fatigue going forward.
<!-- TODO: The above seems a bit too strict. We might want to define guidelines that better fit our current practices -->
Postmortems are done shortly after the incident is resolved, while the context is still fresh for all responders. Just as resolving a major incident becomes top priority when it occurs, completing the postmortem is prioritized over planned work. Completing the postmortem is the final step of your incident response process. Delaying the postmortem delays key learning that will prevent the incident from recurring.

**Hold a postmortem meeting within a week after the incident.** Because scheduling a time when everyone is available can be difficult, the expectation is people will adjust their calendars to attend the postmortem meeting within this timeframe.

## Who Is Responsible for the Postmortem
At the end of a major incident, the incident response team will decide on one responder to own the postmortem. Note that the postmortem owner is not solely responsible for completing the postmortem themselves. **Writing a postmortem is a collaborative effort** and should include everyone involved in the incident response. While engineering will lead the analysis, the postmortem process might involve the company Incident Manager, customer support, account management and product management teams. The postmortem owner coordinates with everyone who needs to be involved to ensure it is completed in a timely manner.

It is important to designate a single owner to avoid the bystander effect. If you ask all responders or a team to do the postmortem, you risk everyone assuming someone else is doing it, and therefore, no one does. When selecting an owner you may choose a single individual who meets any of the following criteria:

- Was initially assigned to the alert and took a leadership role investigating during the incident
- Was the primary on-call responder for the most heavily affected service
- Manually triggered the incident to initiate incident response

Doing the postmortem is not a punishment, and the owner is not the person that "caused" the incident. Effective postmortems are blameless. In complex systems there is never a single cause, but a combination of factors that lead to failure. The owner is simply an accountable individual who performs select administrative tasks, follows up for information, and drives the postmortem to completion. Writing the postmortem will ultimately be a collaborative effort, but selecting a single owner to orchestrate this collaboration helps ensure it is done.
