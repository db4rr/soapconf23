![](assets/title.svg)

Note:
New slides start after three empty lines.
Notes are only visible in speaker mode, press "s" to access it. 




<img src="assets/kitty.png" alt="Cute kitten on the Fez Medina" style="max-height: 60vh">

Note:
DANIEL - it's important for us to set the right tone for this presentation 




<img src="assets/cat-terminal.png" alt="Cat looking at code" style="max-height: 60vh">

Note:
DANIEL - because we are going to be talking about technical stuff




<img src="assets/cat-plate-spinning.png" alt="Cat looking at multiple spinning plates" style="max-height: 60vh">

Note:
DANIEL - running the technical part of content operations at Dolby is keeping multiple spinning plates from falling




<img src="assets/DBCU.png" alt="Frontpage of Dolby Customer" style="max-height: 60vh">

Note:
DANIEL - we enable content operations allowing teams to publish content in our Dolby Customer portal




<img src="assets/customers.png" alt="Dolby customers" style="max-height: 60vh">

Note:
DANIEL - our customers are partners who license our technologies to integrate them into their products, or customers who use our software tools (like Atmos Renderer). Both technologies and products need documentation.




<img src="assets/outputs.png" alt="Dolby documentation outputs" style="max-height: 60vh">

Note:
DANIEL - we provide online and offline outputs: Dolby Customer pages, offline static HTML pages, and PDF




### DITA-OT publishing in GitLab

<pre class="mermaid">
%%{init: {'theme': 'neutral' } }%%
graph LR
    oxygen(Writer: Oxygen XML editor) --> XML & MD
    vscode(Engineer: VS Code editor) --> MD

    subgraph GitLab
        XML("DITA XML files") --> DITA("DITA-OT docker")
        MD("Markdown files") --> DITA
    end
    DITA --> PDF & HTML & DBCU[Dolby Customer]
</pre>

Note:
MARTA - we moved from closed CMS to corporate GitLab to allow better collaboration with Engineering teams




### Slingshots + Publishing-as-a-Service

<pre class="mermaid">
%%{init: {'theme': 'neutral' } }%%
graph LR
    oxygen(Writer: Oxygen XML editor) --> XML & MD
    vscode(Engineer: VS Code editor) --> MD & PaaS

    subgraph GitLab
        XML("DITA XML files") --> DITA("DITA-OT docker")
        MD("Markdown files") --> DITA
        PaaS("PaaS - Markdown files") --> DITA

    end
    DITA --> PDF & HTML & DBCU[Dolby Customer]
    DITA --> slingshot(Slingshot - JFrog or GitLab)
</pre>

Note:
MARTA - moving to GitLab allowed us to add more collaboration methods: PaaS repos and various Slingshots




### The promise of Markdown + DITA

* Collaborarion: expectations vs. reality
* Markdown, the lesser evil (*mind the flavours*)
* Testing all new goodies for both source formats
* Decisions for compatibility - examples: 
    * Equations: MathML as external files
    * Diagrams: Mermaid (*ask Daniel on a coffee break*)

Note:
MARTA - Tech Comms collaborate with Eng, but how do we know if our customers and partners are happy with the outcome...?
THIS SHOULD BE THE PPT HALF POINT




<img src="assets/business-data.png" alt="Business making data-based decisions" style="max-height: 60vh">

Note:
DANIEL - We need data to understand what customers do, and use that insights to prioritize and make decisions




<img src="assets/hotjar-heatmap.png" alt="Example hotjar heatmap" style="max-height: 60vh">

Note:
DANIEL - We use Google Analytics/Tag Manager, Hotjar and custom reports from our CMS




### Data Analytics infrastructure

<pre class="mermaid">
%%{init: {'theme': 'neutral' } }%%
flowchart LR
    subgraph Data Collection
        IGX("Ingeniux CMS") -->|Nightly Build| AWS("MySQL database")
        SF("SalesForce") -->|Nightly Build| AWS
        GA("Google Analytics")
    end
    subgraph Data Visualisation
        AWS --> PBID("Power BI Desktop") --> PBIS("Power BI Service")
        GA --> PBID
    end
</pre>

Note:
JAKUB




### Pipeline

Note:
JAKUB




### So why all that effort?

Note:
JAKUB




<img src="assets/raw_data.png" alt="Google Analytics raw output" style="max-height: 60vh">

Note:
JAKUB - 




<img src="assets/report_screenshot.png" alt="The final product of our efforts" style="max-height: 60vh">

Note:
JAKUB -




### What sort of questions do we actually answer?

* How are people accessing my documentation?
* Which pages are visited the most frequently?
* What's more popular between online docs and downloading a deliverable?

Note:
JAKUB - From our Tech Writers we get the most interest around navigation flows and documentation pages popularity.




<img src="assets/cat-hats.png" alt="PubEng wears many hats" style="max-height: 60vh">

Note:
DANIEL - Summary: we wear many hats, we learn and experiment a lot




<img src="assets/data.png" alt="Page views and download data" style="max-height: 60vh">

Note:
DANIEL - capturing this data allows us to check our assumptions re: how customers use our materials




<img src="assets/customer-pain.png" alt="Customer pain" style="max-height: 60vh">

Note:
DANIEL




## Data guides ContentOps <!-- .element: class="fragment" -->

### Start from questions, not data sources <!-- .element: class="fragment" -->

Note:
DANIEL -- We'll be happy to take your questions, and feel free to come to us during breaks