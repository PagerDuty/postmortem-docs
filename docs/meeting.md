---
cover:
description: After you have completed the written postmortem, follow up with a meeting to discuss the incident. The purpose of this meeting is to deepen the postmortem analysis through direct communication and to get buy-in for action items.
---
![The Postmortem Meeting](assets/img/headers/Postmortems-Meeting.png)

## Purpose
After you have completed the written postmortem, follow up with a meeting to discuss the incident. **The purpose of this meeting is to deepen the postmortem analysis through direct communication and to get buy-in for action items.** The asynchronous production of the written postmortem helps the team start learning from the incident, but having a conversation leads to deeper learning. Furthermore, having a meeting scheduled to discuss the written postmortem creates [accountability](culture/accountability.md) for the postmortem to be completed in a timely manner. Using this time to discuss action items also helps ensure that those tasks will be completed.

An anti-pattern for the postmortem meeting is to be overly focused on the immediate concerns documented in the written postmortem. Avoid filling the meeting time by simply reading through each section of the document. The best use of this time is to take a step back from the detailed analysis to better understand the systemic factors that led to the incident.

Some teams make use of the [Retrospective Prime Directive](http://retrospectivewiki.org/index.php?title=The_Prime_Directive) to set the tone for the meeting and serve as a regular reminder of the goals. It can be a helpful tool to anchor the discussion and provide a clean slate to start a retrospective, postmortem, or post-incident review.

>
  "Regardless of what we discover, we understand and truly believe that everyone did the best job they could, given what they knew at the time, their skills and abilities, the resources available, and the situation at hand."
  --Norm Kerth, Project Retrospectives: A Handbook for Team Review


**The most important outcome of the postmortem meeting is buy-in for the action plan.** This is an opportunity to discuss proposed [action items](how_to_write/writing.md), brainstorm other options, and gain consensus among team leadership. Sometimes the ROI of proposed action items is not great enough to justify the work or postmortem action items must be delayed for other priorities. The postmortem meeting is a time to discuss these difficult decisions and make clear what work will and will not be done, as well as the expected implications of those choices.

Whereas the written postmortem is intended to be shared widely in the organization, the primary audience for the postmortem meeting is the teams directly involved with the incident. This meeting gives the team a chance to align on what happened, what to do about it, and how they will communicate about the incident to internal and external stakeholders.

!!! tip
    Send a link to the postmortem document to meeting attendees 24 hours before the meeting. Though the postmortem does not need to be complete when it is sent to the attendees, it should be finished before the postmortem meeting. It is still worth sending an incomplete postmortem to meeting attendees in advance so they can start reading through the document.

    This will help you avoid wasting time in the meeting simply reading through the document. Remember the purpose of the meeting is to have an in-depth conversation about what caused the incident and how to prevent it in the future, not to review the document. The postmortem meeting is also an opportunity to clarify any questions about what happened and what the team plans to do to prevent it from happening again. Encourage attendees to ask any and all questions to help everyone get on the same page
    and help the team consider new perspectives for their analysis.

## Agenda
Here is a sample agenda for the meeting:

1. **Postmortem owner** summarizes incident causes and timeline, and leads discussion:
    - What were the larger cultural and structural factors that lead to the incident? **How did we get here?**
1. **Postmortem owner** summarizes proposed follow-up action items, and leads discussion:
    - Is the team **confident** this plan will reduce the likelihood of this incident recurring?
    - **What more or different work might be needed?**
    - Will team leadership (Engineering Manager, Product Manager, Tech Lead, etc.) **commit** to prioritizing these action items?
1. **Postmortem owner** (or company **Incident Manager**, if present) summarizes customer impact.
    - Provide any new context about customer reaction to the incident.

## Who Participates
The postmortem owner invites the following people to the postmortem meeting. Below is more detail about the role each plays in the discussion.

- Always
    - [Service owners](https://response.pagerduty.com/training/subject_matter_expert/) and other key engineers involved in the incident.
        - On-call service owners and other engineers that responded to the incident are the experts of the affected services. During the postmortem meeting they can provide historical context about how the systems were built, cultural context about what was happening with the team leading up the incident, and proposals for what work would reduce the likelihood of this incident recurring.
        - Productive postmortem discussions will include engineers with in-depth knowledge of the part of the system that their team owns. If the engineer(s) that responded to the incident are newer to the team, it will be helpful to include more experienced engineers from their team in the postmortem meeting.
    - Engineering manager for impacted systems.
        - The manager responsible for the teams that responded to the incident attends the postmortem meeting to inform their staffing and technical investment decisions
    - Product manager for impacted systems.
        - Product managers attend postmortem meetings to understand the effect incidents have on their customers' experience. For postmortem action items to be prioritized and completed, it is critical to engage product managers in this discussion of the importance and scope of proposed follow-up tasks.
- Optional (Only major incidents)
    - Company Incident Manager.
        - The incident manager can speak to customers' reactions to the incident. They need to understand the team's decision on action items so they can finalize and send external messaging, if needed.

<!-- TODO: Consider adding a section about facilitation (or rather, communication in a postmortem meeting) -->
<!--
## Facilitation
### What Is Facilitation
The facilitator's role in the postmortem meeting is different from the other participants. The facilitator does not voice their own ideas in the meeting; instead, they encourage the group to speak up and keep the discussion on track. The postmortem owner, the incident commander, or any other meeting attendee that played an active role during the incident are the ones who need to contribute to the discussion and should not also be responsible for facilitating.

The facilitator:

- Encourages people to speak up and makes sure that everyone is heard.
- Clarifies insights and challenges the team with questions.
- Helps the team see different perspectives and different options.
- Keeps everyone on time and on track. Cuts off tangents and stops people from dominating the entire meeting.
- Speaks as little as possible. Remember to guide the discussion, but do not take over the meeting.

The facilitator does not:

- Make decisions.
- Take sides. If the facilitator takes sides, team members might feel attacked and might stop contributing to the meeting.
    - Comment on what people say, even if they are trying to give positive feedback. It may make the speaker feel validated, but it might also make the others feel worse about what they have to say or discourage them from contributing something.

### Who Should Facilitate
Good facilitators tend to have a high level of emotional intelligence and can easily read non-verbal cues to understand how people are feeling. They use this sense to cultivate an environment where everyone is comfortable speaking. Agile coaches and project managers are often skilled facilitators. At PagerDuty, we have a guild of confident facilitators who coach individuals interested in learning how to facilitate. When searching for individuals in your organization to help facilitate postmortem meetings, look for people with these core competencies:

- Can read non-verbal cues to assess how people are feeling in the room and spot who might have something to say.
- Can paraphrases what is said to clarify for self and others.
- Can ask open questions to stimulate deeper thinking.
- Is comfortable interrupting when discussion gets off track or when someone dominates the discussion.
- Can redirect conversation to focus on goals.
- Can keep track of time and give time reminders.
- Can drive discussion to decision-making and action items.

Postmortem meeting facilitators do not need to be experts in the affected systems. Facilitators do not need to be well-versed in the content of the discussion. Remember, the facilitator does not contribute their own opinions to the discussion, but works to get others to speak. The meeting attendees that were involved with the incident response are the experts on the incident, and the facilitator will ask the right questions to encourage those experts to share information with the group.

Your facilitator should, however, be familiar with the postmortem process and the goals of the postmortem meeting so they can guide the group discussion to achieve those goals. Postmortem meeting facilitators must have a strong understanding of [blamelessness](culture/blameless.md) so they can help the group avoid blaming speech in the meeting.

## Facilitation Tips
The postmortem meeting facilitator helps the team dig deeper into their analysis, [avoid blame](culture/blameless.md), and get buy-in for their action items. Common challenges for the postmortem meeting are being overly focused on the written postmortem and succumbing to the tendency to blame individuals for system failure. Below are tips on how to run effective postmortem meetings and how to handle awkward situations when they arise.

**Housekeeping**

- Set ground rules at the beginning of the meeting.
    - Set the expectation that everyone should speak but no-one should hog the conversation.
    - Remind the group that we practice blameless postmortems.
- Establish a safe word for when the conversation gets off track.
    - If a team member notices the conversation is getting off-topic they can say the safe word and have the team re-evaluate the usefulness of the discussion. At PagerDuty, some teams use the acronym ELMO which stands for "Enough, let's move on." This takes pressure off the facilitator alone to interrupt when discussion gets off-topic.
- Share the agenda so the team is clear on what is on- and off-topic.
- Use a timer to timebox.
    - You can timebox each agenda item. Presenting a timer makes everyone aware of the time limit and reduces the need for the facilitator to interrupt for time.
- Present the postmortem document from your laptop onto the TV so everyone can see.

[**How to avoid blame:**](culture/blameless.md)

- Remind the team at the start of the meeting and/or when blame occurs during the meeting that we have agreed to practice blameless postmortems and call each other out when blame occurs.
- Look out for and avoid "who" or "why" questions, which limit analysis and imply blame. Instead ask "what" and "how" questions, such as:
    - "What did you think was happening?"
    - "What did you do next?"
    - "How did that action make sense at the time?"
- When inquiring about a human action, abstract to an non-specific responder. Remind the team anyone could have made the same mistake.
    - "What could have led any responder to take that action?"

**What to do when the conversation is getting off-topic:**

- The facilitator's job is to keep the team on track and will need to interrupt to remind the team of the meeting goals by asking if it is valuable to continue with a topic or if it can be taken offline.
    - "Sorry to interrupt, but this topic seems unrelated to the goals of this meeting, do we want to go back to the original topic or continue with this discussion?"
- Timebox agenda items. Once the time is done they can vote if they want to keep talking for another few minutes.

**What to do when one person is dominating the meeting:**

- Say upfront that participation from everyone is important. Explain the facilitator's responsibilities so they won't be offended if they are asked to stop talking or speak up. Pay attention to how much people are talking throughout the meeting.
- "I wasn't able to hear what the first person was saying."
- Act as a mediator and call out when people are getting interrupted: "Hold that thought – I want to make sure Shari has a chance to finish"

**If a team member has not said anything, how do you get them to contribute:**

- "Let's go around the room and hear from everyone"
- "What's stood out for you so far?"
- "What else might we need to consider?"

**How to stimulate analysis:**

- Ask open questions, no questions that can be answered with "yes" or "no."
- Reference our [analysis questions](resources/analysis.md). The team may have asked themselves these questions as they were preparing the written postmortem. Asking some of these in the meeting will encourage new, collaborative thinking.
-->
