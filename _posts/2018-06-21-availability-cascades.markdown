---
layout: post
title:  "Availability Cascades"
date:   2018-06-21 14:50:04 -0700
categories:
---

An "availability cascade" is the concept that as a topic gains traction in the media, people perceive it to be more plausible, creating a self-reinforcing loop where the topic continues to rise in the public discourse through further momentum in the media.

A "reputational cascade" is the concept that a person who wants to earn social approval, or avoid censure, will choose to (publicly) subscribe to dominant beliefs (even if they privately disagree).

## Distortions that arise from heuristics
Heuristics are mental shortcuts used to make decisions more economically (exert less time/energy to come to conclusion). Heuristics save time but can come at the cost of distorting reality.

**Framing effect**

The framing effect describes how results can be manipulated to change an intended behavior.
For example, people are more likely to undergo treatment if told "90% of people have survived" than "10% of people have died".

**Availability bias**

Availability bias results from estimating the probability of an event based on how easily instances can be recalled. This produces substantial distortions because the frequency of an event does not need to be related to how accessible instances are in memory.

Consider the risk perception of the average person toward a shark compared to a mosquito. Most people would fear a shark more, yet only 10 people died in 2016 due to interaction with a shark, compared to 780,000 deaths due to interaction with a mosquito.

<img src="/images/posts/mosquito.png" height="auto" width="100%">

Consider the risk perception of terrorism in the US compared to the risk perception of gun violence. Availability is influenced by the volume of news we see about a topic which modulates our risk perception.

+ **Terrorism deaths = 21** (2013)
+ NYT articles on terrorism = 2,903


+ **Gun deaths = 33,636** (2013)
+ NYT articles on gun violence = 799


<img src="/images/posts/guns.png" height="auto" width="100%">

Availability bias leads to systematic errors in assessing the number of deaths due to particular risks. Overestimates are given to dangers the media persistently covers, and underestimates are given to dangers that are not publicized widely (deaths due to hospital acquired infections, medical errors, asthma).

From a machine learning perspective, availability bias reminds me of the issues that arise when distributions of data between train and test do not match. The media is exacerbating class imbalance by augmenting the number of examples in the "train" distribution (our minds model of the world), so that it is very divorced from the test data (true reality).  


## Policy

How should we allocate resources and fashion laws given the distortions that arise from cognitive heuristics?

Technocractic vs. Democratic

The technocratic response views availability cascades as the irrational consequence of groupthink, inevitable to result in gross misallocation of resources toward minor risks the mob has mongered fear over. In response, technocrats advocate for prioritizing risk mitigation based on objective measures (number of lives affected, severity of impact).

The democratic response views availability cascades as revealing risk preferences among a group of people. Even though car accidents may kill more people than shark attacks, if the consensus is that death by shark attack is worse than death by a car crash, more resources should be committed to mitigating shark attacks.

<!-- ## Distorting Policy

Framing effects can be used to distort policy evaluations.

"Loss aversion" is the observation that people are harmed more by losing $100, than they benefit from winning $100. Loss aversion can be triggered by choosing a reference point.

Monopolies like Google frame themselves as small fish in a large, heavily competitive environment (as a small player in global advertising) to avoid regulation.

Facebook, Youtube, Twitter, frame themselves as "utilities" in order to avoid regulation around verifying/policing claims spread via their platforms. -->


## Credit

[Availability cascades and risk regulation](/papers/availability-cascades.pdf) (2007)

[Availability: A Heuristic for Judging Frequency and Probability](/papers/TverskyKahneman.pdf) (1973)
