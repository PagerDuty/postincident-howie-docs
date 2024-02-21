![Interview Header](assets/images/headers/Howie-Interview.png)

## Interview incident participants
So far you have consolidated the existing data from tools used in everyday software engineering work to make it quick and easy for you to understand who was involved and what responders did during the incident. However, that data only tells part of the story. A lot of incident response happens offline: in direct messages, in face-to-face conversations, and, importantly, within the heads of those involved as they reason about what is happening and why!

Interviewing the participants involved can help elicit more details about what was confusing and why, the event, the response efforts, and surface important knowledge about the system (which includes the technical architecture but also teams, company culture, and communication patterns). Talking to different people involved one-on-one will expose the differences between what they believe happened and why. Often these deltas are used to run the most productive incident review.

This section is built on methods from critical incident technique<sup>[8](https://www.jeli.io/howie/authors-acknowledgements)</sup> and critical decision method<sup>[9](https://www.jeli.io/howie/authors-acknowledgements)</sup> for investigating incidents. It covers deciding who to interview, conducting the interviews, and working with the data collected after the interview.

## Deciding who to interview
We are rarely given unlimited time to conduct an investigation, as many organizations seek to complete their investigations within a given time window or require the findings from the investigation to inform immediate work. Therefore, you’ll need to decide how to use your time to provide the optimal insights for your investigation.

Who you will interview and how many people you will interview depends on several factors like interviewees’ availability, the time you have to complete the investigation, and the amount of relevant new information you get from each interview.

Your initial analysis will help you identify high-value interview subjects. As you work through chat or audio transcripts, you’ll notice key players. This often includes people who are leading the response (formally as incident commander or informally), who bring key insights (like relevant hypotheses about the problem), add important context (to validate/invalidate a hypothesis or to bring a broader perspective to the problem), or manages stakeholder relations that could impact response efforts (such as providing updates to leadership or customers to keep them in the loop). Don’t worry about compiling the most comprehensive list of participants right away. As you conduct the first batch of interviews, you will learn about additional participants that you’ll find are important to interview. Some suggestions for who could be interviewed are:

- Key players in the event – did they have a leading role or were they heavily involved in the detection, diagnosis, or resolution of the incident?
- People that might feel blamed – interviewing these participants can help alleviate fear and make sure their perspectives are accurately represented in the investigation.
- People that weren’t expected to be involved (people that weren’t on-call) – these participants can be critical sources of expertise and their involvement evidence of resilience within the system.
- People that were “lone wolves” (taking action independent of the group efforts) or exist on “islands of knowledge” (they were the only one who knew what was needed to resolve the incident).
- Owners (or former owners) of the impacted system.
- People who hold subject-matter expertise on the systems or components involved in the incident.
- Person that wrote the work ticket that prompted the person to write changes related to the incident.
- Person that wrote said change.
- People that are new to the organization – these participants can help surface hidden assumptions or contradictions.

You will find that interviews reveal interesting details about the system of work in general. You’ll gain context into organizational change efforts that may have contributed to the event, team dynamics that help or hinder coordination, or external forces that force tradeoff decisions in the moment. As an investigator, you will face important decisions about how to integrate these findings into your analysis. It’s necessary to include some of these details to place the decisions and actions into the broader context of how work happens in your organization. Manage your time constraints by stopping your interviewing when the amount of relevant new information drops off noticeably.

## Sequencing
Knowing who to interview can help you as an investigator in managing your time. It is also important to consider how to schedule your interviews. Start with the “high-value interview” participants—the ones you think will give you the greatest context or the highest signal-to-noise ratio. That way if you run short of time you’ve targeted the key players.

Investigators often struggle with trying to schedule participants for follow-up conversations, so it’s likely that availability of participants may drive your interview schedule, so be flexible and ready to ask your questions when a participant has time!

Some additional tips for sequencing interviews:

- **If two interviewees are related in some way (for example, an engineer recruited a customer service agent into the event) start with the person who had the higher involvement or will have the most knowledge about the event.**
- **It’s common to have to loop back to follow up with a participant after your interview if new information comes up in other interviews or during other parts of your data collection. You may wish to do this via direct message or email instead of a second interview to save time.**

## Length
How long you spend talking to a participant can vary depending on the interviewee’s role in the event. We recommend a minimum of twenty minutes, but don’t spend more than sixty minutes in a single session. In any case, you should respect your interviewee’s other commitments, and plan the duration accordingly—it’s better to finish early than run long.

## Approaching interviewees
Incidents can be emotionally charged events in an organization—especially if there was substantial impact or the event was very public. Be conscious of the fear of being blamed when reaching out to participants for follow-up. Some people may be defensive or avoidant.

We recommend sending an informal email or direct message first to introduce yourself and the purpose of your outreach and to let them know you’ll be sending an invite. Give them an opportunity to ask questions and, if you sense hesitation, reassure them the discussion will be confidential.

Send a calendar invite for a discussion or chat. Calling it an interview can be intimidating to some interviewees (it can come across as an interrogation or investigation). Include the details about the incident you are investigating and some information about how you are conducting the investigation (we’ve offered some guidance for what to say in the Appendix). Always give the option to opt out.

If the incident was contentious or difficult and you are not familiar with the interviewee, it can be useful to have someone who knows them (a colleague or manager) send an introductory message to help you build trust and rapport.

## Preparing for the interview
Your preparation begins with analyzing the full scope of all the communication channels used to conduct the incident response (these may include chat transcripts, call recordings, etc.).

Review the participant’s contributions in the channels, look at their team and tenure information, see who else from their team participated, and perhaps follow up on how they had participated in similar, previous incidents.

There are many different ways to conduct an interview. It may be informed by the nature of the event itself, personal preference, and the desired outcomes. As you develop more skills in interviewing, you will adjust your style. To start, consider the following:

- If you are new to interviewing, it helps to conduct interviews in pairs until you get more experience. It is cognitively demanding to be asking questions, listening for answers, capturing answers, and thinking of your follow-up questions simultaneously. Recording the interviews can help you revisit the answers, but shorthand notes will help you be more efficient in your analysis.
- Review your corporate policies about collecting and storing video and audio recordings of your colleagues.
- Pair with someone to scribe, who has also conducted interviews, to record the participants’ answers. Having access to scribe notes can help you as an interviewer review earlier discussion points as the interview progresses.
- Encourage the scribe to aid the lead investigator with follow-up questions (over chat) or to jump in directly with questions.
- If conducting a virtual interview, have the scribe turn their camera off and mute their microphone so it’s not distracting that they are taking notes. Conversely, the scribe can take notes by hand.
- If you do not have a scribe but are able to record the interview; make use of online transcription services to quickly and easily get a written record of the interview.
- Be mindful of time and your objectives with the interview. While open-ended questions give us broad context, they can run down your time, so if you have specific questions to ask make sure to leave enough time for them.
- Keep in mind that having a broad selection of threads to pull gives lots of places for insight during the learning review.

## Kick off the interview right
As you start off your interview, you will want to make sure you are ready and bring any materials you have analyzed, including notes and charts.

Here’s the pattern we always follow to get the conversation started smoothly:

1. When you start the discussion, introduce yourself and your scribe (if you have someone helping you take notes).
1. Explain what you are doing with the interview, that multiple perspectives help form a more coherent picture of what happened.
1. Say that you would like to record the interview so you can faithfully represent what they share with you.
1. Ask for the interviewee’s consent to be recorded, but make it clear who will be reviewing the recording and how long you plan on retaining it.
1. Let them know if they want something off-the-record, you can stop the recording. In this case, none of the materials should be attributed to the interviewee but may be used as a jumping-off point for further investigation.
1. Explain to them the broader process of the investigation so they know how they fit into the bigger picture (that this interview will be part of the broader analysis that will get developed and distributed for feedback as well as shared with a larger audience).
1. Ask them if they remember the incident. The interviewee may not recall it well if it was a long time ago or they’ve been in multiple incidents since then. Ask if they need a refresh on the incident (you can either give a brief synopsis or have them review the channel).
1. Highlight the qualities of the incident that made it an attractive target for investigation.
1. Explain this is not about corrective actions
1. Ask if they have any questions before you begin.

!!! tip
    Note: Productive interviews usually have a talking ratio of 5:1 (interviewee to interviewer). Your job as the interviewer is not to show knowledge of a situation (even if you do know about it), it is to extract what the responder knew about it.

To help interviewees feel comfortable with you and reorient themselves to the event, it is useful to start with general questions like:

- How did you first get brought into the event?
- What was your understanding of the situation as you were pulled in?
- From your perspective, can you explain what happened in the incident?

These questions can help get your interviewee talking in a natural way, allow you to find natural openings to ask about specific parts of the event, and can even provide you with a summarized point of view that is different from the one you arrived at during your initial analysis.

## Getting more specific
Use details of the incident that you noted in your review of the transcripts to drive your questions. These are often things like:

- How did you get notified of this incident?
- What did you mean by $X?
- Tell me about the ordering of events?
- At one point you said: “$X”— what did you mean by this?
- At what point did you discover $POTENTIAL_MITIGATOR OR $POTENTIAL_ TRIGGER?
- What dashboards were you looking at? What were you searching for in $logs $dashboards? Can you show us?
- What was your comfortability with assessing the situation? How long have you been here? How have you seen things done?
- Are you frequently on-call or responding to things like $X? Is anyone on-call for $X? How did you feel it went?
- What surprised you in this incident?
- How did the shape of the incident response take place?
- Have some specific questions ready (the ones you tagged as “participant follow- up”) but also allow the conversation to flow naturally.
- Ask for clarification as needed—better to have them over-explain something you know than to make an assumption.
- Ask for further clarification when interviewees share their opinions or counterfactuals.

## After the interview
Go back through the interview notes and tidy up any sentence fragments, add context, and clean up typos. Spend a few minutes reflecting on the themes that emerged for you. You may want to identify ones that seem strong and ones that were weaker or would need further follow up. This should include any questions that remain unanswered or aspects of the event that are still unclear to you. This will help narrow your follow-ups. Identify anyone you’d want to interview next or if there are further questions to a previous interview. Begin your outreach immediately to keep the investigation moving forward. Link any supporting materials (including video recordings or transcripts) to your interview notes or documents you’ve begun compiling. Distribute the interview notes to co-investigators (as appropriate; you will want to be careful to not violate the privacy of your interviewee). Touch base with the interviewee later the same day or shortly after with a casual note like: “Thanks, I appreciate your insight, it is clear you have a lot of expertise in $X. If any additional thoughts come up, please send them my way.” Continually provide updates to keep them in the loop and engaged in the process.


