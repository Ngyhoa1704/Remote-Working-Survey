# Remote Work and Its Implications on Productivity, Morale, and Future Policy
![image](https://github.com/user-attachments/assets/8ba2ff6e-9f34-4ae1-8a13-6ec912cff222)

If you want to view detailed my thought process before handling this project, please access the Google Docs link below or the PDF file provided:
https://docs.google.com/document/d/1iCmeLSC9ItpE73MnTdm_BrgQM0LAgDMMbG2I_oFwEkk/edit?tab=t.0
## Project Summary Report
**Research Context:** Survey of 1,500 remote workers in New South Wales (NSW), Australia
**Survey Periods:** August–September 2020 and March–April 2021

## 1. Introduction
This analysis aims to evaluate how remote working during the COVID-19 pandemic affected employee productivity and morale and to derive insights to guide long-term remote work policy. The survey dataset comprises responses from 1,500 workers across two time points in 2020 and 2021, allowing comparative analysis across different stages of the pandemic.

The target audience for this report is organizational leadership or policy-makers seeking to understand the impact of remote work and make informed decisions about future work arrangements.

## 2. Research Objectives
The project was designed with the following core objectives:
- To quantify changes in productivity under remote work conditions across 2020 and 2021.
- To identify factors influencing employee morale and wellbeing during remote work.
- To evaluate employee preferences and managerial perspectives on the future of remote work.
- To generate evidence-based recommendations for sustainable post-pandemic work policies.

## 3. Methodology
### 3.1 Data Preparation
Given the volume and complexity of survey responses (73 questions in 2020, 109 in 2021), the first step involved transposing the survey questions into a structured format. Each question was reviewed and classified by its relevance to the following analytical dimensions:

- Productivity (self-assessment, managerial view, occupational variation)
- Morale and wellbeing (barriers, time use, mental health)
- Policy formulation (employee expectations, retention, and attraction)

Where appropriate, categorical responses were consolidated (e.g., Likert scales or % brackets) to enhance clarity and enable year-over-year comparison. Unpivot techniques in Power Query were used to normalize multi-variable responses and prepare the data for visualization and aggregation in Power BI.

## 4. Analytical Findings
### 4.1 Productivity
**Self-Assessment:** Both surveys included questions where employees rated their productivity working remotely compared to working in the office. Response categories were consolidated into five levels, and a year-over-year comparison indicated a moderate increase in perceived productivity in 2021.
![image](https://github.com/user-attachments/assets/ea262b58-f8ae-4204-9b0d-f9e887cead43)


**Managerial Perspective:** A parallel question in the 2021 survey provided insight into how managers assessed their teams’ productivity. The results corroborated employee self-assessments, reflecting a generally positive view of remote work productivity.
![image](https://github.com/user-attachments/assets/5a511bd0-3641-4d3b-80d7-93e4c63e87ea)

**Occupational Differences:** A cross-sectional breakdown by occupation revealed that while most roles experienced productivity gains, certain job functions were disproportionately affected by lower productivity under remote settings. This highlights the importance of occupation-specific policy design.
![image](https://github.com/user-attachments/assets/4a039a3a-d464-475a-8daf-12a0aa7a52cc)

### 4.2 Morale and Wellbeing
**Barriers to Remote Work**: The 2021 survey included several questions related to motivational, social, and health-related barriers. These were treated as proxy indicators for morale. Consolidated into three categories (“worsened,” “same,” “improved”), results showed that while issues like isolation were challenging, many employees reported feel better and more active which lead to improved overall wellbeing.
![image](https://github.com/user-attachments/assets/684133e0-4469-4d92-b6ec-76bb2d09912e)

**Time Use Patterns:** Respondents reported decreased commuting time and increased personal or family time when working remotely. This redistribution of time likely contributed to improved work-life balance, suggesting a positive effect on overall morale.
![image](https://github.com/user-attachments/assets/cef90485-df10-4716-a56f-2a69063c8d86)

### 4.3 Policy Implications
**Employee Preferences:** When asked about future work preferences, employees expressed a strong interest in continuing remote or hybrid work arrangements. Responses were recoded into simplified day-based categories to communicate the distribution of preferences more effectively.
![image](https://github.com/user-attachments/assets/ec5395a6-e202-4ef5-830c-60e5ca1a6419)

**Retention and Recruitment:** Managers were also asked whether offering remote work options would improve employee retention and talent attraction. A significant proportion responded positively, supporting the strategic importance of flexible work arrangements in future workforce planning.
![image](https://github.com/user-attachments/assets/fd790af4-6493-4cf7-a8f5-62bca92cd5a8)

## 5. Challenging Points of the Project 
The core complexity of this project stemmed not from the technical implementation of visuals or DAX measures in Power BI, but rather from the structural and semantic complexity of the raw survey data itself.

### 5.1 Dataset Composition and Challenges
The project utilized two large-scale survey datasets from 2020 and 2021, each containing approximately 1,500 respondent entries. The 2020 dataset comprised 73 survey questions, while the 2021 dataset expanded significantly to 109 questions. The data was rich in insight but difficult to analyze directly due to the following challenges:

- **Highly verbose question phrasing**, with multiple conditional and explanatory clauses embedded in single questions.
- **Lack of standardized formatting across the two survey**, making direct year-over-year comparisons non-trivial.
- **Wide-format structure** that stored all questions as columns, making initial manual inspection and tagging inefficient.

### 5.2. Preprocessing Strategy
To address these challenges, a systematic data restructuring process was conducted:
- **Transposition of survey questions**: All column headers (survey questions) were transposed into a separate reference table, allowing for clearer reading, tagging, and comparison across both years.
- **Categorization and tagging:** Each question was manually reviewed and tagged according to its relevance to the three analytical themes:
  - _Productivity_
  - _Morale and Wellbeing_
  - _Policy and Organizational Strategy_

This tagging process served as the analytical backbone for the entire dashboard. It ensured that insights drawn from each visualization were grounded in appropriately classified inputs and supported a coherent narrative structure.

**Data normalization via Power Query:** Many survey responses required transformation, particularly for Likert-scale or categorical responses. In cases where multiple variables were embedded in a single survey structure (e.g., multiple questions about barriers to morale), an **unpivot transformation** was applied to convert the data into long-form structure suitable for grouped aggregation and visual comparison.

### 5.3. 2021 Key Questions Extracted
The following are selected examples of questions from the 2021 dataset that were identified as central to the project's objectives:

**Productivity:**
  - Self-assessment of productivity while working remotely vs. in-office.
  - Manager assessments of team productivity during remote work.

**Morale and Wellbeing:**
  - Questions on whether barriers such as _motivation, isolation, poor management,_ and _health and safety_ had worsened or improved.
  - Statements measuring emotional and physical wellbeing, such as:
    - “I feel better on days I work remotely”
    - “I am more active on remote working days”
    - “I feel better when seeing colleagues in person”
  - Quantitative time-use responses on how daily hours were redistributed across activities such as commuting, sleep, work, and family time.

**Policy Preferences:**
  - Preferred number of days working remotely post-COVID.
  - Managerial agreement with statements about remote work improving team cohesion, employee retention, and talent attraction.

## 6. Conclusion
The data supports the implementation of a **hybrid remote work policy** that maximizes productivity and employee satisfaction while addressing role-specific constraints. The visual dashboard provides a consolidated, comparative overview of the pandemic’s influence on work experiences and offers a foundation for informed policy-making in the post-COVID era.




