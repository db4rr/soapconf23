# Keeping the plates spinning: ContentOps at Dolby
*Soap Conference 2023 presentation*

## Abstract submitted to soap!

### First draft

In the front: Dolby Customer, a massive content web portal integrated with the company sales backend, and a combination of static HTML and standalone PDFs for offline consumption. In the back: GitLab repos with DITA and Markdown, CI publishing pipelines running DITA-OT in docker, and docs-as-code collaboration with SMEs. On top of it all: Analytics to understand how our customers interact with content, and drive development and UX decisions. 

### Edited by GPT as more friendly

Dolby team presents a case study on how they implemented ContentOps (Content Operations) to improve their content management process and to enhance their customers' experience.

They showcase their front-end interface, Dolby Customer, which is a large content web portal integrated with their company's sales backend. The portal is accompanied with static HTML and standalone PDFs for offline consumption.

On the back-end, they use GitLab repositories to store and collaborate on DITA and Markdown. They also utilize GitLab CI publishing pipelines that run DITA-OT in Docker containers to automate the content publishing process. Git-based process facilitates the collaboration with subject matter experts (SMEs) and helps introduce the docs-as-code approach to this collaboration.

To measure the effectiveness of their content, they also implemented analytics to understand how customers interact with the content, and to drive development and UX decisions.

## Outline of our 40 min. talk
 
* 5min Daniel - Intro, who we are, what we do
Who is our customer, how they consume stuff
PDF, HTML Webhelp, Dolby Customer
    Screenshots
* 5min Marta - DITA-OT publishing in GitLab
DITA-based documentation
Why we moved from dedicated CCMS into GitLab: Improve collaboration with Dolby SMEs
How it went (training Tech Comms in git)
How it works: DITA-OT as Docker in GitLab, publishing as CI pipelines
Markdown input (CommonMark - one needs to choose their flavor)
* 5min Marta - What options GitLab opens
Dolby Customer integration
Doc slingshots
Publishing-as-a-Service: non-writers have own documentation or contribute to writers
* 5min Marta - Collaboration with SMEs
How we imagined Markdown-based docs-as-code and how it actually worked
The promise of Markdown + DITA 
    Decisions for compatibility: MML as external files
    Mermaid graphics inline (you can catch Daniel on a coffee break)
    Testing: everything we do must work in both source formats
* 5 min Daniel - Data Analytics Intro
Why we need to know what happens in Dolby Customer
    what do folks look at, what do folks download
How we started with Analytics ( UA > GA4, hotjar, future: GTM integrating both)
    Scn: heatmap z Hotjar
    Hotjar: all clicks on Dolby Atmos just to go further
* 10 min Jakub - DataAnalytics Infrastructure 
Infrastructure to gather
    mermaid
Infrastructure to present
    Screen from reports
* 5min Daniel - DataAnalytics: Making use of information
Customer suffering with downloads
    anonymous screen re: download pain
Future: outbound links, maybe video?
Lesson learned: better to start from questions than from data sources
Lesson learned: customers still need offline. we need to keep an ear to the ground.
    SCNs downloads monthly + page views monthly
