---
cover:
description: A successful postmortem process is based on a culture of honesty, learning, and accountability. Culture change requires management buy-in, but you can lead culture change no matter your role. This guide describes common challenges faced in building a culture of continuous learning through postmortems and strategies for overcoming these challenges.
---
![Accountability](../assets/img/headers/Postmortems-Accountability.png)

Information sharing and transparency also support an environment that cultivates accountability. A common challenge to effective postmortems is that, after analyzing the incident and creating action items to prevent recurrence, information sharing to increase transparency is never done.

<!-- TODO: Set a policy for when postmortem action items should be completed: -->
<!-- Start by setting a policy for when postmortem action items should be completed. At PagerDuty, high-priority action items needed to prevent a Sev-1 incident from recurring should be completed within 15 days after an incident. Action items from a Sev-2 incident should be addressed within 30 days. Communicate this expectation to all of engineering and make sure it is documented for future reference. -->

For action items to get done, they must have clear owners. Because we are an Agile and DevOps shop, the cross-functional teams responsible for the affected service are also responsible for implementing improvements expected to reduce the likelihood of failure. Engineering leadership helps clarify what parts of the system each team owns and sets expectations for which teams own new development and operational improvements. Ownership designations are communicated across the organization so all teams understand who owns what and ownership gaps can be identified. Any uncertainty about ownership of an incident's action items are discussed in the postmortem meeting with representatives for all teams that may own the action item.

We have also seen improved accountability for completing action items by involving the leaders responsible (product managers and engineering managers) for prioritizing a team's work in the postmortem meeting. Product managers are responsible for defining a good customer experience. Incidents cause a poor customer experience. Engage product managers in postmortem discussions by explaining that it will provide a wider picture of threats to customer experience and ideas on how to improve that experience. Doing so gives engineering a chance to explain the importance of these action items so that product managers will prioritize the work accordingly. Similarly, getting engineering leadership more involved in postmortem discussions gives them a better understanding of system weaknesses to inform how and where they should invest technical resources. Sharing this context with the leaders that prioritize work allows them to support the team's effort to quickly complete high-priority action items from incident analysis.

Finally, ensure postmortem action items are discoverable and regularly viewed. Document postmortem action items as you would any other task. The list of action items from an incident analysis should not only live in your postmortem document. Open tickets in your task management tool, within the project of the team that will own the action item, so it can be viewed alongside all other planned work.

<!-- TODO: Set a policy for when postmortem action items should be completed: -->
<!--    - Set a policy for postmortem action items: e.g. 15 days for Sev-1 action items, 30 days for Sev-2 action items. -->
!!! info "Key Takeaways"
    - Clarify ownership of postmortem action items.
    - Involve the leaders that prioritize work.
    - Open tickets for postmortem action items in your work management ticketing system.
