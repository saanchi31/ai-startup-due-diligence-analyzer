AI Startup Due Diligence Analyzer

An end-to-end multi-agent AI workflow that automates startup due diligence by analyzing multiple startup documents and generating a consolidated investor-ready report.

Overview

Startup due diligence requires reviewing multiple documents such as founder resumes, pitch decks, financial models, and cap tables. Since this information is distributed across different files, manually comparing everything is time-consuming and prone to inconsistencies.

This project automates that process using a multi-agent AI workflow built with n8n.

Each startup document is analyzed independently by a specialized AI agent. The individual analyses are then aggregated, verified for consistency, and transformed into a structured due diligence report highlighting investment insights, risks, inconsistencies, and missing information.

The final report is automatically generated and delivered to the user.

Features : 

Multi-agent AI architecture
Automated startup document analysis
Independent analysis of each uploaded document
Cross-document consistency verification
Detection of conflicting information
Identification of missing information
Automated investor-style due diligence report generation
Automatic report delivery through email
End-to-end workflow automation using n8n
Documents Supported
Founder Resume
Pitch Deck
Financial Model
Cap Table

WORKFLOW ARCHITECTURE 
<img width="317" height="392" alt="image" src="https://github.com/user-attachments/assets/c3ff8686-ca4d-4d37-9f93-d443224a644b" />


Why Multiple AI Agents?

Instead of using one large prompt for every document, this project assigns a dedicated AI agent to each document type.

Different startup documents require different types of reasoning.

For example:

Financial models require numerical reasoning.
Founder resumes require profile evaluation.
Pitch decks focus on business strategy.
Cap tables require ownership analysis.

Using specialized AI agents reduces prompt complexity, improves analysis quality, and keeps the context focused before combining everything into a final report.

AI Analysis Includes : 

Executive Summary
Startup Overview
Founder Analysis
Business Model Analysis
Market Analysis
Financial Analysis
Cap Table Analysis
Investment Risks
Red Flags
Missing Information
Cross-document Inconsistencies
Follow-up Questions for Founders
Overall Investment Recommendation


Tech Stack


Workflow Automation :

n8n

AI :

OpenRouter API

Large Language Models (LLMs)

Google Services :

Google Forms

Google Drive API

Gmail API
Report Generation : 

HTML

PDF Conversion

Engineering Challenges

Building the workflow involved significantly more than prompt engineering.

Some of the major challenges included:

Managing increasingly large prompts
Maintaining consistent AI output formats
Parsing nested JSON responses
Combining outputs from multiple AI agents
Handling conflicting information across startup documents
Designing cross-document consistency verification
Managing Google Drive upload delays
Binary data handling
HTML to PDF conversion
Reliable communication between workflow nodes

One important realization during development was that the AI models were rarely the main issue.

Most debugging time was spent handling integrations, data flow, and workflow reliability.

Key Learnings :

Multi-agent workflow design

Prompt modularization

AI output standardization

Cross-document consistency verification

Workflow orchestration using n8n

Building reliable automation pipelines

Managing API limitations

Handling document processing workflows

Current Limitations

Supports PDF documents only

Depends on document quality

No OCR support

No live market verification

No startup database integration

LLM responses may vary depending on the selected model

Future Improvements

Add support for additional startup documents

Build a web dashboard for investors

Integrate live market and competitor research

Implement startup scoring and ranking

Store reports in a searchable database

Add human review and approval workflow

Introduce retry and fallback mechanisms

Move critical workflow logic into code where appropriate

Add schema validation before report generation


Demo
A complete walkthrough of the workflow is available below.

https://github.com/user-attachments/assets/7068bf78-a4ae-4feb-934c-7824d240f140



Screenshots
n8n Workflow

<img width="925" height="395" alt="Screenshot 2026-07-23 143623" src="https://github.com/user-attachments/assets/7a418a66-b923-4f7a-b755-6139a3821f90" />


📄 Sample Report
A sample AI-generated Due Diligence Report is available here:
[File.html](https://github.com/user-attachments/files/30353076/File.html)
[Uploa<html><head><meta charset="utf-8"/><title>SheetJS Table Export</title></head><body><table><tr><td data-t="s" data-v="text" id="sjs-A1">text</td></tr><tr><td data-t="s" data-v="# EKO STRIDE INVESTMENT REPORT<br/><br/>## EXECUTIVE SUMMARY<br/><br/>EkoStride is a seed-stage Indian micro-mobility startup developing smart modular electric scooters built from recyclable composites, featuring a closed-loop battery swapping network and IoT-enabled consumer app. The company targets urban commuters in Tier 1 and Tier 2 cities, addressing congestion, first-and-last-mile gaps, and EV battery waste management. With a $15B TAM and $2.5B SAM, EkoStride&apos;s business model combines pay-per-ride fees, corporate subscriptions, and hyperlocal advertising revenue.<br/><br/>Founder Saanchi brings relevant experience from NextGen Mobility Solutions where she led deployment of an IoT-enabled fleet management system scaling to 5,000 daily transit nodes. The seed round of ₹1.5 Crores will fund deployment of 1,000 scooters, regulatory clearance in three new municipal zones, and achievement of operational cash-flow break-even within 14 months. Key strengths include circular manufacturing framework and proprietary telemetry systems, though founder team depth and detailed financial projections remain unclear.<br/><br/>## STARTUP OVERVIEW<br/><br/>- **Name**: EkoStride Mobility Private Limited<br/>- **Industry**: Electric Mobility / Micro-mobility<br/>- **Sector**: Transportation<br/>- **Stage**: Seed<br/>- **Location**: New Delhi, India<br/><br/>## FOUNDER ANALYSIS<br/><br/>- **Founder/CEO**: Saanchi<br/>- **Background**: <br/>  - Product Strategy &amp; Technology Lead at NextGen Mobility Solutions (2023-2025)<br/>  - Led IoT-enabled fleet management system scaling to 5,000 daily transit nodes<br/>  - Experience in lithium-ion battery optimization (25% thermal threshold improvement)<br/>  - Analyzed multi-city commuter routing for battery swapping station placement<br/>- **Education**: B.Tech in Electrical Sciences &amp; Engineering, Premier Technical University<br/>- **Achievements**: 1st Place at National Sustainable Transit Innovation Challenge<br/><br/>## MARKET ANALYSIS<br/><br/>- **Total Addressable Market (TAM)**: $15 Billion<br/>- **Serviceable Available Market (SAM)**: $2.5 Billion<br/>- **Serviceable Obtainable Market (SOM)**: 15% share of core tech-corridor market over 36 months<br/>- **Target Customers**: Urban commuters in tech parks, university clusters, and corporate employee populations across Tier 1 and Tier 2 Indian cities<br/><br/>## FINANCIAL ANALYSIS<br/><br/>- **Funding Sought**: ₹1.5 Crores (Seed round)<br/>- **Use of Funds**: <br/>  - 60% Fleet &amp; Battery Acquisition (manufacturing 1,000 smart modular scooters)<br/>  - 25% Technology Framework Development (cloud architecture, app UI/UX, IoT firmware)<br/>  - 15% General Working Capital (regulatory setup, swap hub leasing, team growth)<br/>- **Milestone**: Achieve operational cash-flow break-even within 14 months of scaling<br/><br/>## CAP TABLE ANALYSIS<br/><br/>- **Pre-Seed Ownership**:<br/>  - Founder (Saanchi): 76.47%<br/>  - Core Tech Co-Founders: 17.65%<br/>  - Unallocated ESOP Pool: 5.88%<br/>- **Post-Seed Ownership** (after ₹1.5 Crore raise at ₹10 Crore post-money):<br/>  - Founder (Saanchi): 65.00%<br/>  - Core Tech Co-Founders: 15.00%<br/>  - Incoming Seed Investors: 15.00%<br/>  - ESOP Pool: 5.00%<br/>- **Key Provisions**: <br/>  - 1x non-participating liquidation preference<br/>  - Broad-based weighted average anti-dilution protection<br/>  - 4-year monthly vesting with 1-year cliff for founder shares<br/><br/>## OBSERVED STRENGTHS<br/><br/>- Mission to decarbonize short-distance urban commuting with clear environmental impact<br/>- Use of circular-source composites for scooter chassis reducing asset depreciation<br/>- Smart modular electric scooters with IoT capabilities for real-time monitoring<br/>- Closed-loop battery swapping network with secondary-life storage partnerships<br/>- Consumer app providing tap-and-go localized access<br/>- Proprietary dynamic telemetry capturing vibration, thermal spikes, and accident impacts<br/>- AI predictive rebalancing algorithms for optimized vehicle redistribution<br/>- Multiple revenue streams (pay-per-ride, corporate subscriptions, B2B advertising)<br/>- Market sizing with defined TAM/SAM/SOM metrics<br/>- Clear use of funds allocation with specific milestones<br/>- Founder vesting schedule specified in cap table<br/>- Anti-dilution protection provisions included<br/><br/>## RISKS<br/><br/>- Scaling manufacturing to 1,000 active fleet nodes within timeline<br/>- Securing regulatory clearance in three additional municipal zones<br/>- Achieving operational cash-flow break-even within 14 months<br/>- Capturing 15% market share of core tech-corridor market within 36 months<br/>- Founder team appears to lack depth beyond single founder<br/><br/>## RED FLAGS<br/><br/>- No co-founder team members identified or detailed<br/>- Missing pilot/traction data (user base, revenue, utilization metrics)<br/>- No detailed financial projections beyond 14-month horizon<br/>- No existing investor information provided<br/>- No IP/patent portfolio documentation provided<br/>- No detailed competitor analysis beyond generic references<br/><br/>## MISSING INFORMATION<br/><br/>- Years of founder&apos;s experience<br/>- Founder certifications<br/>- Patents or IP filings<br/>- Publications or research papers<br/>- Historical fundraising details<br/>- Accelerator participation history<br/>- Exit history<br/>- Regulatory requirements for additional municipal zones<br/>- Validation/certification status of battery recycling process<br/>- Detailed unit economics supporting 60% cost advantage claim<br/>- Customer acquisition cost and lifetime value metrics<br/><br/>## FOLLOW-UP QUESTIONS<br/><br/>- What is your total years of experience in the mobility sector?<br/>- Do you hold any certifications relevant to electric mobility or sustainable engineering?<br/>- Have you filed or been granted any patents related to your technology?<br/>- What is your fundraising history to date?<br/>- Have you participated in any accelerator programs?<br/>- What specific manufacturing capacity and supply chain partners enable 1,000 scooter deployment?<br/>- What regulatory approvals are required for each of the three additional municipal zones?<br/>- How do you plan to achieve cash-flow break-even within 14 months?<br/>- What metrics will measure the 15% market share target?<br/>- What is the status of pilot programs validating your business model?<br/>- How does your closed-loop recycling network compare to industry standards on cost efficiency?<br/>- What are your projected unit economics supporting the 60% cost advantage claim?<br/>- How will you compete against existing micro-mobility providers?<br/>- What is your roadmap for expansion beyond tech-corridors?<br/><br/>## OVERALL RECOMMENDATION<br/><br/>**Proceed with Caution**<br/><br/>While EkoStride demonstrates a compelling mission addressing real urban mobility and environmental challenges in India, several significant risks and information gaps must be addressed before investment. The startup shows promise with its circular manufacturing approach and clear market opportunity, but the single-founder structure, lack of traction data, and missing financial details warrant further investigation.<br/><br/>## DUE DILIGENCE SCORE: 65/100<br/><br/>**Rationale**: EkoStride earns points for its strong environmental mission, clear market sizing, innovative technology stack, and founder with relevant previous experience. However, substantial deductions are made for the lack of co-founders/team details, missing traction metrics, incomplete financial modeling, and absence of competitive/IP analysis. The seed funding request appears reasonable relative to the milestones, but the path to break-even within 14 months seems aggressive without supporting detailed financials. Additional due diligence on manufacturing partnerships, regulatory pathways, and pilot results is essential before proceeding." id="sjs-A2"># EKO STRIDE INVESTMENT REPORT<br/><br/>## EXECUTIVE SUMMARY<br/><br/>EkoStride is a seed-stage Indian micro-mobility startup developing smart modular electric scooters built from recyclable composites, featuring a closed-loop battery swapping network and IoT-enabled consumer app. The company targets urban commuters in Tier 1 and Tier 2 cities, addressing congestion, first-and-last-mile gaps, and EV battery waste management. With a $15B TAM and $2.5B SAM, EkoStride&apos;s business model combines pay-per-ride fees, corporate subscriptions, and hyperlocal advertising revenue.<br/><br/>Founder Saanchi brings relevant experience from NextGen Mobility Solutions where she led deployment of an IoT-enabled fleet management system scaling to 5,000 daily transit nodes. The seed round of ₹1.5 Crores will fund deployment of 1,000 scooters, regulatory clearance in three new municipal zones, and achievement of operational cash-flow break-even within 14 months. Key strengths include circular manufacturing framework and proprietary telemetry systems, though founder team depth and detailed financial projections remain unclear.<br/><br/>## STARTUP OVERVIEW<br/><br/>- **Name**: EkoStride Mobility Private Limited<br/>- **Industry**: Electric Mobility / Micro-mobility<br/>- **Sector**: Transportation<br/>- **Stage**: Seed<br/>- **Location**: New Delhi, India<br/><br/>## FOUNDER ANALYSIS<br/><br/>- **Founder/CEO**: Saanchi<br/>- **Background**: <br/>  - Product Strategy &amp; Technology Lead at NextGen Mobility Solutions (2023-2025)<br/>  - Led IoT-enabled fleet management system scaling to 5,000 daily transit nodes<br/>  - Experience in lithium-ion battery optimization (25% thermal threshold improvement)<br/>  - Analyzed multi-city commuter routing for battery swapping station placement<br/>- **Education**: B.Tech in Electrical Sciences &amp; Engineering, Premier Technical University<br/>- **Achievements**: 1st Place at National Sustainable Transit Innovation Challenge<br/><br/>## MARKET ANALYSIS<br/><br/>- **Total Addressable Market (TAM)**: $15 Billion<br/>- **Serviceable Available Market (SAM)**: $2.5 Billion<br/>- **Serviceable Obtainable Market (SOM)**: 15% share of core tech-corridor market over 36 months<br/>- **Target Customers**: Urban commuters in tech parks, university clusters, and corporate employee populations across Tier 1 and Tier 2 Indian cities<br/><br/>## FINANCIAL ANALYSIS<br/><br/>- **Funding Sought**: ₹1.5 Crores (Seed round)<br/>- **Use of Funds**: <br/>  - 60% Fleet &amp; Battery Acquisition (manufacturing 1,000 smart modular scooters)<br/>  - 25% Technology Framework Development (cloud architecture, app UI/UX, IoT firmware)<br/>  - 15% General Working Capital (regulatory setup, swap hub leasing, team growth)<br/>- **Milestone**: Achieve operational cash-flow break-even within 14 months of scaling<br/><br/>## CAP TABLE ANALYSIS<br/><br/>- **Pre-Seed Ownership**:<br/>  - Founder (Saanchi): 76.47%<br/>  - Core Tech Co-Founders: 17.65%<br/>  - Unallocated ESOP Pool: 5.88%<br/>- **Post-Seed Ownership** (after ₹1.5 Crore raise at ₹10 Crore post-money):<br/>  - Founder (Saanchi): 65.00%<br/>  - Core Tech Co-Founders: 15.00%<br/>  - Incoming Seed Investors: 15.00%<br/>  - ESOP Pool: 5.00%<br/>- **Key Provisions**: <br/>  - 1x non-participating liquidation preference<br/>  - Broad-based weighted average anti-dilution protection<br/>  - 4-year monthly vesting with 1-year cliff for founder shares<br/><br/>## OBSERVED STRENGTHS<br/><br/>- Mission to decarbonize short-distance urban commuting with clear environmental impact<br/>- Use of circular-source composites for scooter chassis reducing asset depreciation<br/>- Smart modular electric scooters with IoT capabilities for real-time monitoring<br/>- Closed-loop battery swapping network with secondary-life storage partnerships<br/>- Consumer app providing tap-and-go localized access<br/>- Proprietary dynamic telemetry capturing vibration, thermal spikes, and accident impacts<br/>- AI predictive rebalancing algorithms for optimized vehicle redistribution<br/>- Multiple revenue streams (pay-per-ride, corporate subscriptions, B2B advertising)<br/>- Market sizing with defined TAM/SAM/SOM metrics<br/>- Clear use of funds allocation with specific milestones<br/>- Founder vesting schedule specified in cap table<br/>- Anti-dilution protection provisions included<br/><br/>## RISKS<br/><br/>- Scaling manufacturing to 1,000 active fleet nodes within timeline<br/>- Securing regulatory clearance in three additional municipal zones<br/>- Achieving operational cash-flow break-even within 14 months<br/>- Capturing 15% market share of core tech-corridor market within 36 months<br/>- Founder team appears to lack depth beyond single founder<br/><br/>## RED FLAGS<br/><br/>- No co-founder team members identified or detailed<br/>- Missing pilot/traction data (user base, revenue, utilization metrics)<br/>- No detailed financial projections beyond 14-month horizon<br/>- No existing investor information provided<br/>- No IP/patent portfolio documentation provided<br/>- No detailed competitor analysis beyond generic references<br/><br/>## MISSING INFORMATION<br/><br/>- Years of founder&apos;s experience<br/>- Founder certifications<br/>- Patents or IP filings<br/>- Publications or research papers<br/>- Historical fundraising details<br/>- Accelerator participation history<br/>- Exit history<br/>- Regulatory requirements for additional municipal zones<br/>- Validation/certification status of battery recycling process<br/>- Detailed unit economics supporting 60% cost advantage claim<br/>- Customer acquisition cost and lifetime value metrics<br/><br/>## FOLLOW-UP QUESTIONS<br/><br/>- What is your total years of experience in the mobility sector?<br/>- Do you hold any certifications relevant to electric mobility or sustainable engineering?<br/>- Have you filed or been granted any patents related to your technology?<br/>- What is your fundraising history to date?<br/>- Have you participated in any accelerator programs?<br/>- What specific manufacturing capacity and supply chain partners enable 1,000 scooter deployment?<br/>- What regulatory approvals are required for each of the three additional municipal zones?<br/>- How do you plan to achieve cash-flow break-even within 14 months?<br/>- What metrics will measure the 15% market share target?<br/>- What is the status of pilot programs validating your business model?<br/>- How does your closed-loop recycling network compare to industry standards on cost efficiency?<br/>- What are your projected unit economics supporting the 60% cost advantage claim?<br/>- How will you compete against existing micro-mobility providers?<br/>- What is your roadmap for expansion beyond tech-corridors?<br/><br/>## OVERALL RECOMMENDATION<br/><br/>**Proceed with Caution**<br/><br/>While EkoStride demonstrates a compelling mission addressing real urban mobility and environmental challenges in India, several significant risks and information gaps must be addressed before investment. The startup shows promise with its circular manufacturing approach and clear market opportunity, but the single-founder structure, lack of traction data, and missing financial details warrant further investigation.<br/><br/>## DUE DILIGENCE SCORE: 65/100<br/><br/>**Rationale**: EkoStride earns points for its strong environmental mission, clear market sizing, innovative technology stack, and founder with relevant previous experience. However, substantial deductions are made for the lack of co-founders/team details, missing traction metrics, incomplete financial modeling, and absence of competitive/IP analysis. The seed funding request appears reasonable relative to the milestones, but the path to break-even within 14 months seems aggressive without supporting detailed financials. Additional due diligence on manufacturing partnerships, regulatory pathways, and pilot results is essential before proceeding.</td></tr></table></body></html>ding File.html…]()



Project Highlights  :  

Built a complete end-to-end AI automation pipeline
Automated startup due diligence using multiple AI agents
Combined document-specific analyses into a single report
Implemented cross-document consistency verification
Generated investor-ready reports automatically
Automated report delivery through email
