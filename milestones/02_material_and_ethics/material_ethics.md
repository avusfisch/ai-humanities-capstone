# Milestone 2 — Material and Ethics Note
**Due: 13.11.2026**

---

(My original plan for the capstone project was to have several LLMs compete in
the social deduction game Secret Hitler. However, I have now discovered that
there already are several existing papers which explored this, so I decided to
switch to something different (see new pitch.md))

## Your collection

**What is it?**
The analyzed data stems from the r/LucidDreaming and r/Dreams subreddits, as
well as the lucid dreaming forums DreamViews and LD4all. Combined, this results
in a dataset of ~5.3 million posts, posted between May 2002 and July 2026. 

**Where does it come from?**
Reddit data stems from a large dataset containing the post history of the
40,000 largest subreddits shared by the user Watchful1 as a continuation of the
Pushshift Reddit dataset, both of which have been used in previous academic
research 
<sup>[1](https://doi.org/10.1609/icwsm.v14i1.7347)</sup>
<sup>[2](https://doi.org/10.1177/20563051211019004)</sup>
<sup>[3](https://doi.org/10.1002/aur.70066)</sup>
<sup>[4](https://doi.org/10.1145/3818677)</sup>
<sup>[5](https://doi.org/10.1145/3706598.3713161)</sup>
<sup>[6](https://doi.org/10.18653/v1/2025.acl-long.1395)</sup>.
Recently, the Watchful1 dataset has been taken down upon Reddit's request
<sup>[7](https://www.reddit.com/r/pushshift/comments/1v50ved)</sup>, 
with Reddit referring researchers to its official research programme
(r/reddit4researchers).
Data from lucid dreaming forums was scraped by myself between May and July 2026.

---

## Ethical considerations

**Copyright and licensing**
The dataset consists of public social media posts. 

**Consent**
Obtaining individual consent from each user is neither common practice in
large-scale research on public social media data, nor generally feasible, given
the large number of posts and the time span they cover.

**Risks and benefits**
Given the level of abstraction of the planned analyses (frequency of technique
mentions, usage posts, successful/unsuccessful usage posts across several
communities), I see no plausible negative consequences which could result from
the analyses themselves. Additionally, the results can be assumed to be of high
interest to the members of the analyzed communities.

Publicly sharing the dataset could, however, enable misuse of the data in ways
which negatively affect community members (e.g. tracking the activities of
specific individuals in a way that could expose personal data that they did not
intend to share). While this is by no means a unique risk which would only
arise by publication of this dataset, given that copies of the whole Reddit
dataset can still be found online, and that the forum data is scrapable
within the time frame of a few days, it still would make misuse of the data
accessible to a wider range of individuals. Hence, potential publication of the
dataset must be handled with care, and if the decision to publish the dataset is
made, additional anonymization measures might be beneficial (the effect of such
measures can be assumed to be limited though, since original user names could be
easily identified by searching for specific posts in the communities).

**Whose voices are present?**
Individuals who posted in the analyzed online communities between May 2002 and
July 2026. When interpreting the findings, it has to be taken into account that
these should not be viewed as being representative of users of lucid dreaming
techniques/individuals with an interest in lucid dreams as a whole, as the members
of those communities presumably mostly stem from Western/industrialized
countries and are relatively young.

**Limits**
The project analyses discourse about induction techniques, which does not
necessarily equal popularity of a technique or usage experiences. A technique
being mentioned more often than another could, among other reasons, also result
from a technique being more controversial, or more difficult to use. Similarly,
a higher number of usage failure posts of a technique could, for example, also
result from greater disappointment if that technique is generally viewed as
effective, while unsuccessful attempts with a technique that is already viewed
as not being effective might not prompt users to post about such an experience.
On Reddit, discourse is additionally influenced by the platform's algorithm,
which, for example, results in posts which generate more engagement being
displayed to a greater number of users. Lastly, results are also potentially
influenced by posts missing due to communities' moderation policies (e.g.
r/LucidDreaming rules limit the discussion of induction techniques viewed as
pseudoscientific) and technical errors
<sup>[8](https://doi.org/10.1371/journal.pone.0200162)</sup>.


