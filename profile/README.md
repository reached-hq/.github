# ReachED

**Building data systems for better education access in the Philippines.**

We are a data engineering capstone team in the FTW Data Engineering program.

National education totals show how many learners the Philippines enrolls, but not **where** public-school enrollment puts the most pressure on classrooms and teachers. We bring together official DepEd, PSA and HDX data so that pressure can be compared for every city and municipality.

> **Business question:** How should we prioritize the provision of classrooms and teachers among cities based on their respective enrollment needs?

## Tech stack

<img src="https://img.shields.io/badge/Databricks-FF3621?style=for-the-badge&logo=databricks&logoColor=white" alt="Databricks"> <img src="https://img.shields.io/badge/Apache_Spark-E25A1C?style=for-the-badge&logo=apachespark&logoColor=white" alt="Apache Spark"> <img src="https://img.shields.io/badge/SQL-336791?style=for-the-badge" alt="SQL"> <img src="https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white" alt="Python"> <img src="https://img.shields.io/badge/pandas-150458?style=for-the-badge&logo=pandas&logoColor=white" alt="pandas"> <img src="https://img.shields.io/badge/GeoPandas-139C5A?style=for-the-badge&logo=geopandas&logoColor=white" alt="GeoPandas"> <img src="https://img.shields.io/badge/DuckDB-FFF000?style=for-the-badge&logo=duckdb&logoColor=black" alt="DuckDB"> <img src="https://img.shields.io/badge/pytest-0A9EDC?style=for-the-badge&logo=pytest&logoColor=white" alt="pytest"> <img src="https://img.shields.io/badge/GitHub_Actions-2088FF?style=for-the-badge&logo=githubactions&logoColor=white" alt="GitHub Actions"> <img src="https://img.shields.io/badge/Git-F05032?style=for-the-badge&logo=git&logoColor=white" alt="Git">

## What we built

| | |
|---|---|
| **For** | LGU Local School Boards, which decide how the Special Education Fund is spent |
| **Scope** | Public basic education, Kindergarten to Grade 12, in all 1,642 Philippine cities and municipalities |
| **Answer** | A review status for every city and municipality (Priority 1 to 3, Monitor, No current pressure identified, Data review) and the order in which to review them |
| **Decision boundary** | It says where to look first, not how many classrooms or teachers to add |

- **ReachED: Education Access Priority Dashboard.** Four views: which LGUs to review first, why an LGU has its status, which schools to verify first, and how reliable the data is. See the [planner guide](https://github.com/reached-hq/edu-access-intelligence/blob/main/dashboards/planner-guide.md).
- **A planning-priority rule** that counts two separate signals, classroom pressure and teacher pressure, and uses public-enrollment growth to decide how urgent they are. Every status can be traced back to its measures.
- **An outlier check** that shows whether an LGU's status depends on schools with extreme reported figures, so those schools are verified first.
- **Trusted Gold tables** of schools, places, enrollment, classrooms, teachers, population and poverty, all matched to the Philippine Standard Geographic Code.
- **A data-quality dashboard** showing every check the pipeline ran, by layer and source.

## How we work

- **Evidence before answers.** The business question comes from what education planners need to decide *and* what the data can validly support.
- **Inspect before trusting.** Every dataset is inventoried and profiled before we use it, and missing data is never read as "no pressure".
- **Engineered, not one-off.** Data moves through a tested pipeline on Databricks, with quality checks, version control, CI/CD and documentation at every step.

## Team

**Maria Angela Felisilda** — Group Leader · Data Analytics Audit Officer  
Built the DepEd personnel pipeline; designed and built the Gold model; set the AP1 to AP4 metrics and built the planning-priority matrix; wrote the failure-recovery runbook.  
<a href="https://www.linkedin.com/in/mafelisilda/"><img src="https://img.shields.io/badge/LinkedIn-0A66C2?style=for-the-badge" alt="LinkedIn"></a> <a href="https://github.com/mafelisilda"><img src="https://img.shields.io/badge/GitHub-181717?style=for-the-badge&logo=github&logoColor=white" alt="GitHub"></a>

**Ina Louise Magno** — Freelance Marketing Designer  
Built the DepEd enrollment and facilities pipeline, the school-to-PSGC map, the Databricks job with its alerts and CI/CD deploys, the outlier check, and the LGU planner dashboard; set up the team's GitHub workflow and documentation.  
<a href="https://www.linkedin.com/in/ina-louise-magno/"><img src="https://img.shields.io/badge/LinkedIn-0A66C2?style=for-the-badge" alt="LinkedIn"></a> <a href="https://github.com/hyenalouise"><img src="https://img.shields.io/badge/GitHub-181717?style=for-the-badge&logo=github&logoColor=white" alt="GitHub"></a>

**Catherine Joy Balane** — Inventory Management Specialist  
Built the PSA poverty pipeline, the public-school coordinates lane and school-location map, the Gold enrollment, population and poverty tables, and the data-quality dashboard; aligned AP1 to AP4 with the business question; co-led the final presentation.  
<a href="https://www.linkedin.com/in/catherine-joy-balane/"><img src="https://img.shields.io/badge/LinkedIn-0A66C2?style=for-the-badge" alt="LinkedIn"></a> <a href="https://github.com/catweyine"><img src="https://img.shields.io/badge/GitHub-181717?style=for-the-badge&logo=github&logoColor=white" alt="GitHub"></a>

**Maeve Ylain Sean Lumague** — Chemical Engineer  
Built the PSGC geography reference, the EMISD school-to-PSGC crosswalk, and the school-age population map and Gold tables; reconciled totals from source to Gold and recorded the full dev runs; closed the handoff docs; co-led the final presentation.  
<a href="https://www.linkedin.com/in/maeveylainsean/"><img src="https://img.shields.io/badge/LinkedIn-0A66C2?style=for-the-badge" alt="LinkedIn"></a> <a href="https://github.com/maeveylain"><img src="https://img.shields.io/badge/GitHub-181717?style=for-the-badge&logo=github&logoColor=white" alt="GitHub"></a>

**Sara Erika Celadiña** — Industrial Engineer  
Built the HDX boundaries and their PSGC crosswalk, the PSA school-age population pipeline, and the DepEd school-to-PSGC match rule; drew the ERD.  
<a href="https://www.linkedin.com/in/saraevcldn/"><img src="https://img.shields.io/badge/LinkedIn-0A66C2?style=for-the-badge" alt="LinkedIn"></a> <a href="https://github.com/saraevcldn"><img src="https://img.shields.io/badge/GitHub-181717?style=for-the-badge&logo=github&logoColor=white" alt="GitHub"></a>

## Repositories

| Repo | Description |
|---|---|
| [`edu-access-intelligence`](https://github.com/reached-hq/edu-access-intelligence) | Main capstone project: ingestion, pipeline, analytics, dashboards, data quality and documentation |
