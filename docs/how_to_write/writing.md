---
cover:
description: Here are concrete steps for producing a postmortem document. You will learn the most important information to include in the postmortem, how to collect and present that information, and how to conduct an effective analysis that results in system improvements.
---
![Step by Step](../assets/img/headers/Postmortems-StepByStep.png)

Below are the steps involved in performing a postmortem at a high level. Below are the details of how to perform each step.

1. Create a new postmortem for the incident.
1. Populate the incident timeline with important changes in status/impact and key actions taken by responders.
1. Schedule a postmortem meeting within the required timeframe for all required and optional attendees.
     - For each item in the timeline, include a metric or some third-party page where the data came from.
1. Analyze the incident.
    - Identify superficial and root causes.
    - Consider technology and process.
1. Open any immediate follow-up action tickets.
    - These, as well as additional ones, will be discussed in the postmortem meeting.
1. Ask for review.
1. Attend the postmortem meeting.
1. Share the postmortem.

## Owner Responsibilities
At the end of a major incident call, the incident response team decides on one responder to own the postmortem. Writing the postmortem will ultimately be a collaborative effort, but selecting a single owner will help ensure it gets done.

The owner of a postmortem is responsible for the following:

- Scheduling the postmortem meeting and inviting the relevant people (this should be scheduled within a week from the incident).
- Investigating the incident, pulling in whoever is needed from other teams to assist in the investigation.
- Ensuring the page is updated with all of the necessary content. See our [Template](https://riskified.atlassian.net/wiki/spaces/DEV/pages/3306618888/Template+YYYY-MM-DD+Incident+Title) for what should be included.
- Reviewing the postmortem content with appropriate parties before the meeting, and running through the topics at the postmortem meeting.
- Communicating the results of the postmortem internally.

The owner of a postmortem creates the postmortem document and updates it with all relevant information.


## Administration
![Administration](../assets/img/thumbnails/1Administration.png)

1. Create the document.
2. Add all responders to it.
3. Schedule the meeting.

The postmortem owner's first step is to create a new, empty postmortem for the Incident. Go through the history in Slack to identify the responders and add them to the page so they can help populate the postmortem.

Next, schedule the postmortem meeting for 30 minutes to an hour, depending on complexity of the incident. Scheduling the meeting at the beginning of the process helps ensure the postmortem is completed within the SLA. **The meeting should be scheduled within a week from the incident.** Don't worry about finding the best time for all attendees. The priority is to schedule within this timeframe and attendees should adjust their schedules accordingly.

Invite the following people to the postmortem meeting:

- Always
    - [Service owners](https://response.pagerduty.com/training/subject_matter_expert/) involved in the incident.
    - Key engineer(s)/responders involved in the incident.
    - Engineering manager for impacted systems.
    - Product manager for impacted systems.
- Optional
    - The company Incident Manager (for major incidents).
    
## Create a Timeline
![Timeline](../assets/img/thumbnails/2CreateATimeline.png)
Begin by focusing on the timeline. Document the facts of what happened during the incident. Avoid evaluating what should or should not have been done and coming to conclusions about what caused the incident. Presenting only the facts here will help avoid blame and supports a deeper analysis. Note the incident may have started before responders became aware of it and began the response effort. The timeline includes important changes in status/impact and key actions taken by responders. To avoid hindsight bias, start your timeline at a point before the incident and work your way forward instead of backwards from resolution.

Review the incident log in Slack to find key decisions made and actions taken during the response effort. Also include information the team didn't know during the incident that, in hindsight, you wish you would have. Find this additional information by looking at monitoring, logs, and deployments related to the affected services. You'll take a deeper look at monitoring during the analysis step, but start here by adding key events related to the incident, and include changes to incident status and the impact to the timeline.

For each item in the timeline, identify a metric or some third-party page where the data came from. This helps illustrate each point clearly and ensures you remain rooted in fact rather than opinions. This could be a link to a monitoring graph, a log search, a tweet, etc.—anything that shows the data point you're trying to illustrate in the timeline.

!!! info "Key Takeaways"
    * Stick to the facts.
    * Include changes to incident status and impact.
    * Include key decisions and actions taken by responders.
    * Illustrate each point with a metric.

## Document Impact
![Impact](../assets/img/thumbnails/3DocumentImpact.png)
Impact should be described from a few perspectives:

- How long was the impact visible? In other words, what was the length of time users/customers were affected?
    - Note the length of impact may differ from the length of the response effort. Impact may have started some time before it was detected and incident response began.
- How many customers were affected?
    - Support may need a list of all affected customers so they can reach out individually.
- How many customers wrote or called support about the incident?
- What functionality was affected and how severely?
    - Quantify impact with a business metric specific to your product. For PagerDuty this includes event submission, delayed processing, slow notification delivery, etc.

## Analyze the Incident
![Analyze](../assets/img/thumbnails/4AnalyzeTheIncident.png)
Now that you have an understanding of what happened during the incident, look further back in time to find the contributing factors that led to the incident. Technology is a complex system with a network of relationships (organizational, human, technical) that is continuously changing.

In his paper, "[How Complex Systems Fail](http://web.mit.edu/2.75/resources/random/How%20Complex%20Systems%20Fail.pdf)," Dr. Richard Cook says that because complex systems are heavily defended against failure, it is a unique combination of apparently innocuous failures that join to create catastrophic failure. Furthermore, because overt failure requires multiple faults, attributing a "root cause" is fundamentally wrong. **There is no single root cause of major failure in complex systems, but a combination of contributing factors that together lead to failure.** The postmortem owner's goal in analyzing the incident is not to identify the root cause, but to understand the multiple factors that created an environment where this failure became possible.

Cook also says the effort to find the "root cause" does not reflect an understanding of the system, but rather the cultural need to blame specific, localized forces for events. Blamelessness is essential for an effective postmortem. **An individual's action should never be considered a root cause.** Effective analysis goes deeper than human action. In the cases where someone's mistake did contribute to a failure, it is worth anonymizing this in your analysis to avoid attaching blame to any individual. Assume any team member could have made the same mistake. According to Cook, "all practitioner actions are actually gambles, that is, acts that take place in the face of uncertain outcomes."

The postmortem owner should start their analysis by looking at the monitoring for the affected services. Search for irregularities like sudden spikes or flatlining when the incident began and leading up to the incident. Include any commands or queries used to look up data, graph images, or links from monitoring tooling alongside this analysis so others can see how the data was gathered. If there is not monitoring for this service or behavior, make building monitoring an action item for this postmortem. More on [writing action items](#followup) below.

!!! warning "Importance of Monitoring"
    Puppet's 2018 State of DevOps Report highlights making monitoring configurable by the team operating the service as a foundational practice for successful DevOps. Empowering teams to define, manage, and share their own measurement of performance contributes to a culture of continuous improvement.

Another helpful strategy for targeting what caused an incident is reproducing it in a non-production environment. Experiment by modifying variables to isolate the phenomenon. If you modify or remove some input does the incident still occur?

This level of analysis will uncover the superficial causes of the incident. Next, ask why the system was designed in a way to make this possible. Why did those design decisions seem to be the best decisions at the time? Answering these questions will help you uncover root causes.

Here are some questions to help the postmortem owner identify the class of a particular problem:

- Is it an isolated incident or part of a trend?
- Was this a specific bug, a failure in a class of problem we anticipated, or did it uncover a class of issue we did not architecturally anticipate?
- Was there work the team chose not to do in the past that contributed to this incident?
- Research if there were any similar or related incidents in the past. Does this incident demonstrate a larger trend in your system?
- Will this class of issue get worse/more likely as you continue to grow and scale the use of the service?

Though it may not be a root cause, consider the process in your analysis. Did the way that people collaborate, communicate, and/or review work contribute to the incident? This is also an opportunity to evaluate and improve the incident response process. Consider what worked well and didn't work well within the incident response process during the incident.

Write a summary of the findings in the postmortem. The team may find further learnings and identify additional causes through discussion in the meeting, but the owner should do as much pre-work and documentation as possible to ensure a productive discussion.

### Questions to Ask
Below is a non-exhaustive list to help stimulate deep analysis. Ask "how" and "what" questions rather than "who" or "why" to discourage blame and encourage learning.

<table>
    <tr>
        <td>Cues</td>
        <td>
            <ul>
                <li>What were you focusing on?</li>
                <li>What was not noticed?</li>
                <li>What differed from what was expected?</li>
            </ul>
        </td>
    </tr>
    <tr>
        <td>Previous Knowledge/Experience</td>
        <td>
            <ul>
                <li>Was this an anticipated class of problem or did it uncover a class of issue that was not architecturally anticipated?</li>
                <li>What expectations did participants have about how things were going to develop?</li>
                <li>Were there similar incidents in the past?</li>
            </ul>
        </td>
    </tr>
    <tr>
        <td>Goals</td>
        <td>
            <ul>
                <li>What goals governed your actions at the time?</li>
                <li>How did time pressure or other limitations influence choices?</li>
                <li>Was there work the team chose not to do in the past that could have prevented or mitigated this incident?</li>
            </ul>
        </td>
    </tr>
    <tr>
        <td>Assessment</td>
        <td>
            <ul>
                <li>What mistakes (for example, in interpretation) were likely?</li>
                <li>How did you view the health of the services involved prior to the incident?</li>
                <li>Did this incident teach you something that should change views about this service's health?</li>
            </ul>
        </td>
    </tr>
    <tr>
        <td>Taking Action</td>
        <td>
            <ul>
                <li>How did you judge you could influence the course of events?</li>
                <li>What options were taken to influence the course of events? How did you determine that these were the best options at the time?</li>
                <li>How did other influences (operational or organizational) help determine how you interpreted the situation and how you acted?</li>
            </ul>
        </td>
    </tr>
    <tr>
        <td>Help</td>
        <td>
            <ul>
                <li>Did you ask anyone for help?</li>
                <li>What signal brought you to ask for support?</li>
                <li>Were you able to contact the people you needed to contact?</li>
            </ul>
        </td>
    </tr>
    <tr>
        <td>Process</td>
        <td>
            <ul>
                <li>Did the way that people collaborate, communicate, and/or review work contribute to the incident?</li>
                <li>What worked well in your incident response process and what did not work well?</li>
            </ul>
        </td>
    </tr>
</table>

!!! info "Key Takeaways"
    * Find contributing factors, not the root cause.
    * Focus on the system, not the humans.
    * Look for anomalies in monitoring.
    * Reproduce and experiment in a non-production environment.
    * Don't forget to review your processes.

## Follow-Up Actions<a name="followup"></a>
![Followup](../assets/img/thumbnails/5FollowUpActions.png)
After identifying what caused the incident, ask what needs to be done to prevent this from happening again. Based on your analysis, you may also have proposals to reduce the occurrence of this class of problem, rather than this specific incident from recurring.

It may not be possible (or worth the effort) to completely eliminate the possibility of this same incident or a similar incident from happening again, so also consider how you can improve detection and mitigation of future incidents. Does the team need better monitoring and alerting around this class of problem so they can respond faster in the future? If this class of incident does happen again, how can the team decrease the severity or duration? Remember to identify any actions that can make the incident response process better, too. Go through the incident history in Slack to find any to-do items raised during the incident and make sure these are documented as tickets as well. (At this phase, you are only opening tickets. There is no expectation that tasks will be completed before the postmortem meeting.)

Create tickets for all proposed follow-up actions in your task management tool. Label all tickets with the `postmortem-action-item` label. Provide as much context and proposed direction on the tickets as you can so the team's product owner will have enough information to prioritize the task against other work and the eventual assignee will have enough information to complete the task.

In the _;login:_ magazine article, "[Postmortem Action Items: Plan the Work and Work the Plan](https://www.usenix.org/system/files/login/articles/login_spring17_09_lunney.pdf)," John Lunney, Sue Lueder, and Betsy Beyer write about how Google writes postmortem action items to ensure they are completed quickly and easily. They advise all action items to be written as actionable, specific, and bounded.

- **Actionable:** Phrase each action item as a sentence starting with a verb. The action should result in a useful outcome.
- **Specific:** Define each action item's scope as narrowly as possible, making clear what is in and out of scope.
- **Bounded:** Word each action item to indicate how to tell when it is finished, as opposed to open-ended or ongoing tasks.

| Poorly Worded | Better |
|-|-|
| Investigate monitoring for this scenario. | **Actionable:** Add alerting for all cases where this service returns >1% errors. |
| Fix the issue that caused the outage. | **Specific:** Handle invalid postal code in user address form input safely. |
| Make sure engineer checks that database schema can be parsed before updating. | **Bounded:** Add automated presubmit check for schema changes. |

<small>Source: _;login:_  Spring 2017 Vol. 42, No. 1.</small>

If there are any proposed follow-up actions that need discussion before tickets can be created, make a note to add these items to the postmortem meeting agenda. These may be proposals that need team validation or clarification. Discussing these items in the meeting will help decide how best to proceed.

Be careful with creating too many tickets. Only create tickets that are P0/P1s; i.e., tasks that absolutely should be dealt with. There will be some trade-offs here, and that's fine. Sometimes the ROI isn't worth the effort that would go into performing an action that may reduce the recurrence of the incident. When that is the case, it is worth documenting that decision in the postmortem. Understanding why the team is choosing not to perform an action helps avoid learned helplessness.

Note the person who creates the ticket is not responsible for completing it. Tickets are opened under the projects for the teams that own the affected service. At least one representative for all teams that will be responsible for a follow-up action are invited to the postmortem meeting.


!!! info "Key Takeaways"
    * What needs to be done to reduce the likelihood of this, or a similar, incident from happening again?
    * How can you detect this type of incident sooner?
    * How can you decrease the severity or duration of this type of incident?
    * Write actionable, specific, and bounded tasks.

<!-- TODO: Consider starting a postmortem review process: -->
<!--
## Postmortem Review
![Review](../assets/img/thumbnails/7PostmortemReview.png)
At PagerDuty, we have a community of experienced postmortem writers available to review postmortems for style and content. This avoids wasted time during the meeting. We post a link to the postmortem into Slack to receive feedback at least 24 hours before the meeting is scheduled.

Here are some of the things we look for:

- Does it provide enough detail?
- Rather than just pointing out what went wrong, does it drill down to the underlying causes of the issue?
- Does it separate "What happened?" from "How to fix it"?
- Do the proposed action items make sense? Are they well-scoped enough?
- Is the postmortem well-written and understandable?
- Does the external message resonate well with customers or is it likely to cause outrage?

Reviewing a postmortem isn't about nitpicking typos (but do make sure the external message isn't littered with spelling and grammatical errors). It's about providing constructive feedback on valuable changes to a postmortem to get the most benefit from them.
-->
