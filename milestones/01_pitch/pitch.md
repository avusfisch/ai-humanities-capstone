# Milestone 1 — Pitch
**Due: 30.10.2026**

---

## Working title: Discourse on Lucid Dream Induction Techniques in online communities

## The theme and question
A lucid dream is a dream in which the dreamer is aware that they are dreaming.
They can occur spontaneously; nevertheless, frequent lucid dreamers are rare
in the general population
<sup>[1](https://doi.org/10.2466/09.pms.112.1.104-108)</sup>.
An individual's lucid dreaming frequency may however be increased through the usage
of specific lucid dream induction techniques 
<sup>[2](https://doi.org/10.1016/j.concog.2012.07.003)</sup>.

The goal of the project is to analyse the mentions of popular lucid dream induction techniques
in dedicated online communities (e.g. r/LucidDreaming), particularly how often which technique 
is mentioned and how mentions changed over time. Additionally, I plan to analyze the number 
of usage reports of techniques (being posts that mention that one has used the technique),
and to explore the amount of success and failure reports (being usage posts that mention 
that one has successfully/unsuccessfully used a technique).

## The material
The analyzed data stems from the r/LucidDreaming and r/Dreams subreddits, as
well as the lucid dreaming forums DreamViews and LD4all. Combined, this results
in a dataset of ~5.3 million posts, posted between May 2002 and July 2026. 

## Why AI?
Given the large scope of the data, manual coding would not be feasible. 
While a simple (e.g. regex-based) count of mentions based purely on name matches 
would be doable, this would result in many false positives since some technique
names (e.g. MILD, WILD, Reality Checks) are ambiguous and can also occur in
other contexts. 
This, in addition to the even more complex identification of successful/unsuccessful
usage reports, makes LLMs/AI a good fit for the project.

## Implementation Plan
1. Given the large number of posts, my plan is to first create an
extensive list of lucid dream induction techniques, based on previous
research, discussion with active members of the analyzed online communities and
LLM search results, and then build a regex filter to identify candidate posts. 
2. Depending on the number of remaining posts, my plan is then to either use a cheap LLM, 
a decision model (e.g. Jev), or a fine-tuned
encoder (e.g. BERT trained on LLM-labeled data), to filter out false positives for
techniques with ambiguous names.
3. For the identification of usage posts a similar procedure will be applied, again utilizing either 
a cheap LLM, a decision model, or a fine-tuned encoder.
4. The classification of successful/unsuccessful usage posts is presumably most complex,
since a usage post could mention several techniques, so the model has to be very context 
sensitive to correctly attribute success/failure mentions. 
I assume an LLM would be the best fit here, but depending on the number of posts an
alternative approach might be necessary.

## Motivation
Research on lucid dream induction techniques in the past was mostly focused on 
usage in the research setting; thus the project contributes to the exploration of 
lucid dream induction usage outside the research setting.
I'm also analyzing similar questions in my Master's thesis using survey data, so
a comparison between the results would be interesting. 

## Concerns
The most prominent potential issues result from the large number of posts in
the dataset, which makes resource efficiency particularly important.
Another potential issue is that at each step of the project, differences in the
classification accuracy across posts from different time points could produce
false positive trends; checking this is again made difficult by the large time span
covered by the posts.
