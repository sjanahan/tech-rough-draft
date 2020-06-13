# How to keep a complex, multi-team project moving forward?

## Background 
Hi y'all, I'm Janahan Sivaraman and I'm a Staff Software Engineer
@ Walmart Labs - Health and Wellness. Prior to Walmart Labs, I was a Staff
Software Engineer working on AdTech systems for Jet.com that enabled Jet to
publish its catalog all over the internet, allowed affiliates to monetize their
presence, and even for Jet itself to monetize its digital real estate.

At Jet we were the Growth Engineering Team, responsible for the systems that
allowed Jet to grow to 1 million users even faster than Instagram. 

When Jet's Engineering teams were reallocated towards Walmart Labs in June 2019,
we were lucky enough to keep >90% of the squad together and Walmart Lab's Health
and Wellness organization was gracious enough to have us.

## Situation
The first thing the business folks in Health and Wellness approached us to solve
was a system to help drive adherence of therapy for chronically ill patients. 

Understanding the different subsystems, I proposed an architecture that
necessitated that some of the compute and storage be in the Cloud. The next
question I had was how do y'all deploy to the Cloud?

I talked to four existing teams within Health and Wellness and got four
different answers - none of which came with a resounding "and you should follow
our lead". The existing deployment solutions were either brittle, non-compliant
for HIPAA, or highly manual to operate.

Understanding that minimizing iteration loops is a major key to delivering software
solutions quickly, a group of us proposed an entire HIPAA Cloud, a set of cloud-native
infrastructure where as much HIPAA compliance was pushed down into the
infrastructure so that application developers could focus on owning business
logic. 

We pitched the HIPAA Cloud to our stakeholders in November 2019, got their
buy-in from a time and financial perspective, and started working towards this
vision.

While the technical details are interesting, I'll be focusing today on what I
learned from folks not in Engineering - as they taught me specific, actionable
techniques to ensuring this project - which involved more than 10 teams across
Engineering, Software Foundations, Compliance, and the Security Operations
Center, to be completed in just 5 months (of which 2 months were during the
COVID-19 pandemic)!

## Action
#### Come to the meeting prepared with architecture diagram
  * It's significantly easier to come to a meeting with a visual representation
  of what you're speaking about. Otherwise you'll spend a non-trivial amount of
  time getting folks to build mental models solely based on your words. Level
  setting the technical discussion focuses the conversation on what yet hasn't
  been solved instead of what your vision is
#### Establish your stakeholders early and send Executive Summaries weekly
  * By identifying your stakeholders early, you ensure that you have the support
  of folks who control how humans and money are allocated. For that support,
  it's critical for the sake of transparency that you update them on a cadence
  that gives them the confidence that they need not initiate correspondece
  relating to status updates. Cesar Ramirez, our Software Foundations Customer
  Relationship Manager, suggested this early on in the HIPAA Cloud journey and
  allowed us to own the narrative about the progress we were making all along 
  the way. 
#### Use JIRA tickets not only for documenting asks, but also escalation 
  * History is written by the winners. Some folks - either acting in bad faith
  or due to opportunity cost, may agree to an ask from you that they won't
  honor. By documenting exactly what you're asking for in a JIRA ticket, you
  ensure there is a paper trail of what you asked for and why it's important.
  Additionally, now that you have a receipt for your ask, it's a perfect place
  to escalate to their management when promises are broken. 
#### Keep a positive attitude (especially externally) 
  * Folks gravitate to and follow optimistic people. If the future isn't better
  than the now, what's really the point of being part of it? 
  * The bigger the project, the more important this positive attitude is. You'll
  need the buy-in of so many folks that it's critical you give them the
  confidence to move forward with you.
#### Take meticulous meeting notes
  * Our Software Foundations Program Manager, Chad Rivoli,
  taught me this. Again, history is written by the winners. By owning the
  narrative of who attended, what happened, and what action items came out of a
  meeting, you can hold folks accountable to their word and defend against folks
  who misremember their commitments.
  * He kept this in chronological order in a JIRA notebook and replied-all to
  every single meeting with a link to that specific page in the JIRA notebook,
  no imatter how insignificant that meeting seemed.
#### All statements must be captured in writing (especially from Compliance)
  * There will be times when folks say one thing one day and a few weeks later
  some other folks challenge the first group's word - especially if it's
  relating to compliance. If you don't get decisions in writing, you'll waste
  time setting up additional meetings so that the second group can hear the
  first group's statement from their mouths. Additionally, it's demoralizing for
  the folks driving to rehash things they considered settled. Another big
  shoutout to Cesar Ramirez for teaching me this technique!

## Result
By applying these specific, actionable techniques we were able to deliver an
entire HIPAA Cloud, which includes Kubernetes, Kafka, CosmosDB, ElasticSearch,
Spark, and Splunk in just **five months**. We have even established a well-worn
playbook for how additional building blocks - like relational databases,
low-latency out-of-process caches, blob storage, etc. can be added to the
HIPAA Cloud.

Working quickly is an effective way to ensure that your project gets finished before
management can reprioritize and that your colleagues stay engaged. 

There is no way we could have seen the COVID-19 pandemic reaching the USA in
November 2019, but because we moved so quickly, the first application that went
to all 5500 stores was deployed on this HIPAA Cloud in the first week of May
2020. It enabled Walmart to capture associates symptoms and let them know
whether it was safe for them to come in or not, and if not, when they should
return to work.

I'm so proud to have been a driving force in supporting Walmart's response to
COVID-19 and to keep our in-store associates safe from the ravages of this
pandemic.

I want to give a huge shoutout to Cesar Ramirez and Chad Rivoli for teaching me
techniques that I would have otherwise floundered around for years to figure out
myself. By working with folks with different skill sets, we can be exposed to
blind spots in our view of the world and better equip ourselves for navigating
complex scenarios and driving for the change you want to see.
