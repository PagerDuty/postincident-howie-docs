![Analyze Header](assets/images/headers/Howie-Analyze.png)
## Analyze incident data
Incident analysis is iterative. You move from a general awareness of the incident to having deep knowledge of the event as you work your way through incident-specific data and other artifacts. As you progress in your investigation, it will inform your understanding of the technology, participants, and progression. At times it may be necessary to circle back to data or people you’ve spoken with to confirm or clarify new details as they emerge.

As you prepare for conducting the initial analysis, the first step is to get yourself familiar with the event. Sometimes, this step is easy because you were already aware of the event, so you know what happened and who was involved. Other times you may just get a verbal report from someone who was either in the event or tracked it in some way along with the request that you investigate. Other times you may be asked to investigate the incident without any context. Regardless of how you become the investigator, our recommended approach to conducting the analysis includes:

1. Orienting yourself around the initial data you have aggregated (transcripts, people data, alert logs, on-call schedules, dashboards, etc.) by tagging to organize your analysis;
1. Creating a narrative and timelines of the event;
1. Making note of the emerging themes and key questions remaining to be answered
1. Identifying any additional data you need in order to answer the questions
1. (Optional) Identifying and preparing for interviewees (if conducting interviews)
1. Compiling the data collected and themes
1. Consolidating your analysis, supporting data, and themes into a calibration document for review and/or to guide your facilitation
1. Your analysis should be refined and deepened following discussions in post-mortems or after a review from participants.

Let’s look at each of these steps in more detail.

## Tagging
A useful way to orient yourself to the event is to read over the data you’ve collected. This helps orient you to the event itself and helps you begin to make sense of different parts of the incident. For example, how did the event get detected? Who was brought in to help? How did they react to what was going on? Most investigators will immediately begin looking for information to assess the nature and severity of the incident and any key moments in time to help develop a timeline.

To begin to deepen this process, we suggest flagging events of interest and we refer to this as tagging. We suggest tagging with a defined set of words that group similar parts of the data around important aspects of the incident and how it was handled. To prepare for tagging, we see investigators cut and paste ChatOps transcript data into a text editor or print out hard copies of the data. Find a method that works best for you and that is flexible enough to let you work with the data all the way through to the report or meeting facilitation.

To start, the investigator reads through the transcript, tags key events, and begins building the narrative of the event. We recommend having a standard set of tags for your organization that everyone involved in an investigation can reference. What tags you use, their definitions, and how many you have will depend on how deep of an analysis you conduct. We’ve seen teams that just use a few tags to help them build the timeline and identify key moments in time (for example: detection, diagnosing, repair completed) and other teams that tag extensively, identifying things like when hypotheses about the contributing factors are raised and proved/disproved, when updates are provided to external stakeholders, sudden changes in system behavior, or actions that were taken to minimize impacts.

!!! tip "Tagging is often an iterative process"
    The goal is not to be comprehensive in your tagging at the start; that’s a lot of pressure to take on and may not be necessary. Instead, think of tagging as a way to organize and hone your investigation. As we’ve mentioned before, the extent of your tagging and annotating will depend on how much time you have, how many people are involved in the investigation, and how deeply you want to explore the event.
You may only have time for the first pass; if you’re able to spend more time tagging, you may be able to gather additional insights into your incident. There is no right or wrong—tagging is a process to help you see more in an incident. As you hone your skills as an investigator, you will improve your ability to draw out deeper insights from the data you collect.

Two basic tags that help support moving quickly to your next steps are marking any messages or events relating to how you’ll tell the story of what happened with “narrative” and tagging anywhere you have a question for someone who was a part of the event as “participant follow-up”

!!! question "What is the narrative?"
    A deeper analysis goes beyond simply recounting what happened in a basic chronological timeline. Instead, try to recreate the event as it happened, walking through the progression of the event and identifying what made it challenging or easy to diagnose and resolve.<sup>[6](https://howie-guide.pagerduty.com/authack/#references)</sup> Investigators who recreate the timeline by creating a narrative about what happened tell a story that allows for complexities and confusions to become apparent. This allows readers of a post-incident report (or participants in a learning review meeting) to get more actively engaged with the investigation since it tells a richer, more compelling account. Readers can imagine the situation the way it happened, not in hindsight when the outcome was known and it is easily understood what should have happened. Learning becomes clearer when you go beyond a simple timeline.
Here are some examples of things you as the investigator can ask yourself to focus your tagging and lay out the narrative to take an analysis deeper.

### Look at what was happening at the beginning of the incident by asking yourself:
1. What did the responders think was happening?
1. Who joined or was recruited to help?
1. What information is available? What’s uncertain/ambiguous? Who is asking? Who is answering?

### Examine how the group was diagnosing the problem they face by asking:
- What were the hypotheses being put forward? *During this time there will be multiple hypotheses put forward, some of which endure and some of which will be quickly discounted or ignored (these are all signals you want to pay attention to).*
- Who is proposing hypotheses about the potential sources of the outage? *Seeing who proposes a hypothesis can be useful to narrow in on formulating a potential interview question for that person.*
- Who is helping to prove or disprove these hypotheses? *Most hypotheses are supported or disproved by others who provide evidence in the form of dashboards, log files, or specialized knowledge about how a piece of software works.*
- What action was taken? By whom? *Some actions may be taken to safeguard the system from further deterioration, others can be to gather more information or try to prove or disprove a hypothesis.*
- Was there any ambiguity or confusion about what was happening? *This is very common and is often a signal about the difficulty or complexity of the failure, not about the knowledge or skills of the responders.*
  
### How was the team working together and with others during the incident?
- Where are examples of successful coordination between different parties involved? *Incidents test practices and procedures and can identify opportunities for improvement or revisions to workflows.*
- Does a team proactively anticipate who will be needed to help resolve the incident and are able to easily bring them in? *Recruiting specialized skill sets is crucial for speedy resolution, especially in hard problems. A key factor to reducing mean time to respond is smoothing out this coordination.*
- Where are communication breakdowns occurring? *Are the responders able to share information quickly and easily?*
  
## Creating timelines
Incident timelines provide a way to orient a reader or learning review participant to what happened during the incident. Going beyond a text-based timeline and creating a more visual representation of the timeline allows you to see your incident from different points of view, craft stories (based on said points of view), and enhance collaboration. We recommend developing multiple timelines when you have the time to do so. This can allow you to focus a timeline to see the false-starts, red herrings, and progression of the event that can move past the idea that the incidents display a clean, forward progression between “detect, diagnose, and repair.”<sup>[7](https://howie-guide.pagerduty.com/authack/#references)</sup> Many find that creating a timeline also gives them an initial structure for organizing the multiple data sources that can sometimes get messy. You can create timeline visualizations of events, keywords, specific participants, and different data types.

## Making notes
As you work through the initial review of the transcript, you will come up with questions. If the question is specific to a particular message, you should leave a note for yourself or co-analysts to come back to it later and note who you want to reach out to for follow-ups.

An example of this practice would be if you see a message from a responder saying, “I actually think $SOFTWARE is involved so rolling back those changes should help.” You might want to tag this as part of the narrative (since it was a proposed hypothesis about what was causing the issue, along with a suggestion about what would help), as well as a participant follow-up tag and add a note to yourself to ask that person, “How did you know it was $SOFTWARE? What did you notice that made that a likely culprit? Why did you suggest the rollback?” This way you can compile your timeline from your narrative tags and start to arrange the questions you’ll answer in your next steps.

Some other examples of questions you may have are:

- How does this piece of technology work? What is the history behind it at this organization?
- Where did this work start?
- What was the business reason behind it?
- How did we know to reach out to this subject matter expert?
- How did we find this information?
- What sorts of pressures were responders under?
- What does this (acronym, reactji, etc) mean?
- Who else knows this?

## Identifying interviewees during your initial analysis
Reviewing the available data serves as an orientation to the event and sets the investigator up for deeper analysis if time and resources allow. After orienting yourself to the event through your initial review and tagging, you will have a general sense of who might be good candidates to interview.

#### If holding individual interviews is not feasible, it is still beneficial to identify key participants you might want to call upon in a review meeting or to aid with reviewing any reports that are generated.

We’ve said it before, and we’ll say it again: analysis is iterative! As you work through reconstructing what happened and talking to participants, new sources of information will become available. As you review this new information, it may drive more questions to be answered.

A great example of this comes from an incident review one of the authors was leading. In the review meeting the investigator asked a participant how they noticed the source of the problem. It turned out this engineer had dealt with the issue so many times before that they set up a dashboard to monitor it and ping them when there was trouble!

When this was shown to other engineers, it generated a detailed discussion about the piece of software and the variability of its performance, and it identified other “explody bits” that other engineers felt were unstable and monitored more closely. In this way, as new information becomes available you may need to return to previously interviewed participants to follow up.
