
https://github.com/user-attachments/assets/e012de9c-e591-4542-8c58-8b1fbcfbb4bd
# ai-startup-due-diligence-analyzer
Multi-agent AI workflow built with n8n that analyzes startup documents and generates automated due diligence reports for investors.


AI Startup Due Diligence Analyzer using n8n

Multi-Agent AI Workflow for Automated Startup Due Diligence

An end-to-end AI workflow built with n8n that automates the startup due diligence process. Instead of manually reviewing multiple startup documents, the workflow analyzes them using specialized AI agents and generates a comprehensive due diligence report highlighting key insights, risks, inconsistencies, and investment considerations.

🚀 Project Overview

Investors often receive multiple documents before evaluating a startup, such as founder resumes, pitch decks, cap tables, and financial models. Reviewing these documents manually is time-consuming and information is often scattered across files.

This workflow automates the entire process by collecting all required documents, analyzing each one individually, combining the findings, and generating a structured due diligence report.

The final report provides a clear overview of the startup along with potential risks, inconsistencies, missing information, and questions that investors can ask before making a decision.

🚀 Workflow Overview
Startup submits required documents through a Google Form
Documents are uploaded to Google Drive
n8n downloads each uploaded PDF
Specialized AI agents analyze each document independently
Individual summaries are generated
Results are merged into a single analysis
AI generates a final Due Diligence Report
Report is converted into PDF
Final report is automatically emailed to the investor


📂 Documents Analyzed
Founder Resume(s)
Pitch Deck
Cap Table
Financial Model


🤖 AI Analysis Includes
Startup Summary
Founder Background Analysis
Business Model Overview
Market Opportunity
Financial Analysis
Cap Table Analysis
Key Risks
Red Flags
Document Inconsistencies
Missing Information
Questions to Ask the Founders
Final Investment Verdict


🛠️ Tech Stack
n8n
Open router API 
Google Forms
Google Drive API
Gmail API
Google Docs (for report generation)
PDF Conversion


⚠️ Challenges Faced

While building this workflow, I encountered several practical challenges beyond prompt engineering.

Managing long prompts became difficult as new features were added.
AI responses were inconsistent and difficult to parse reliably.
Maintaining a standardized output format across multiple agents.
Handling conflicting information across different startup documents.
Combining multiple AI-generated analyses into one coherent report.
Managing Google Drive upload delays and file availability.
Handling binary data and document conversions.
Generating PDFs while preserving report formatting.
Ensuring reliable communication between workflow nodes.

One important realization was that the AI models were rarely the actual problem. Most debugging time was spent handling integrations, data flow, and workflow reliability.

💡 Why Multiple AI Agents?

Instead of relying on a single AI model for the entire workflow, this project uses specialized AI agents.

Different startup documents require different types of analysis. A financial model demands numerical reasoning, while a founder resume requires profile evaluation and a pitch deck focuses on business strategy.

Using specialized agents improves consistency, reduces prompt complexity, and produces more focused analyses before combining everything into the final report.

📸 Screenshots

n8n Workflow

<img width="925" height="395" alt="Screenshot 2026-07-23 143623" src="https://github.com/user-attachments/assets/59e7239b-b62b-4f22-92cd-1fd72b6ef9c1" />


🎥 Demo

A complete walkthrough of the workflow is available below.



https://github.com/user-attachments/assets/d4f2eaa3-da1d-4892-b8bb-3c8fa5dc9b3b




📄 Sample Due Diligence Report

View a sample AI-generated due diligence report:

[File.html](https://github.com/user-attachments/files/30352826/File.html)
<html><head><meta charset="utf-8"/><title>SheetJS Table Export</title></head><body><table><tr><td data-t="s" data-v="text" id="sjs-A1">text</td></tr><tr><td data-t="s" data-v="# EKO STRIDE INVESTMENT REPORT<br/><br/>## EXECUTIVE SUMMARY<br/><br/>EkoStride is a seed-stage Indian micro-mobility startup developing smart modular electric scooters built from recyclable composites, featuring a closed-loop battery swapping network and IoT-enabled consumer app. The company targets urban commuters in Tier 1 and Tier 2 cities, addressing congestion, first-and-last-mile gaps, and EV battery waste management. With a $15B TAM and $2.5B SAM, EkoStride&apos;s business model combines pay-per-ride fees, corporate subscriptions, and hyperlocal advertising revenue.<br/><br/>Founder Saanchi brings relevant experience from NextGen Mobility Solutions where she led deployment of an IoT-enabled fleet management system scaling to 5,000 daily transit nodes. The seed round of ₹1.5 Crores will fund deployment of 1,000 scooters, regulatory clearance in three new municipal zones, and achievement of operational cash-flow break-even within 14 months. Key strengths include circular manufacturing framework and proprietary telemetry systems, though founder team depth and detailed financial projections remain unclear.<br/><br/>## STARTUP OVERVIEW<br/><br/>- **Name**: EkoStride Mobility Private Limited<br/>- **Industry**: Electric Mobility / Micro-mobility<br/>- **Sector**: Transportation<br/>- **Stage**: Seed<br/>- **Location**: New Delhi, India<br/><br/>## FOUNDER ANALYSIS<br/><br/>- **Founder/CEO**: Saanchi<br/>- **Background**: <br/>  - Product Strategy &amp; Technology Lead at NextGen Mobility Solutions (2023-2025)<br/>  - Led IoT-enabled fleet management system scaling to 5,000 daily transit nodes<br/>  - Experience in lithium-ion battery optimization (25% thermal threshold improvement)<br/>  - Analyzed multi-city commuter routing for battery swapping station placement<br/>- **Education**: B.Tech in Electrical Sciences &amp; Engineering, Premier Technical University<br/>- **Achievements**: 1st Place at National Sustainable Transit Innovation Challenge<br/><br/>## MARKET ANALYSIS<br/><br/>- **Total Addressable Market (TAM)**: $15 Billion<br/>- **Serviceable Available Market (SAM)**: $2.5 Billion<br/>- **Serviceable Obtainable Market (SOM)**: 15% share of core tech-corridor market over 36 months<br/>- **Target Customers**: Urban commuters in tech parks, university clusters, and corporate employee populations across Tier 1 and Tier 2 Indian cities<br/><br/>## FINANCIAL ANALYSIS<br/><br/>- **Funding Sought**: ₹1.5 Crores (Seed round)<br/>- **Use of Funds**: <br/>  - 60% Fleet &amp; Battery Acquisition (manufacturing 1,000 smart modular scooters)<br/>  - 25% Technology Framework Development (cloud architecture, app UI/UX, IoT firmware)<br/>  - 15% General Working Capital (regulatory setup, swap hub leasing, team growth)<br/>- **Milestone**: Achieve operational cash-flow break-even within 14 months of scaling<br/><br/>## CAP TABLE ANALYSIS<br/><br/>- **Pre-Seed Ownership**:<br/>  - Founder (Saanchi): 76.47%<br/>  - Core Tech Co-Founders: 17.65%<br/>  - Unallocated ESOP Pool: 5.88%<br/>- **Post-Seed Ownership** (after ₹1.5 Crore raise at ₹10 Crore post-money):<br/>  - Founder (Saanchi): 65.00%<br/>  - Core Tech Co-Founders: 15.00%<br/>  - Incoming Seed Investors: 15.00%<br/>  - ESOP Pool: 5.00%<br/>- **Key Provisions**: <br/>  - 1x non-participating liquidation preference<br/>  - Broad-based weighted average anti-dilution protection<br/>  - 4-year monthly vesting with 1-year cliff for founder shares<br/><br/>## OBSERVED STRENGTHS<br/><br/>- Mission to decarbonize short-distance urban commuting with clear environmental impact<br/>- Use of circular-source composites for scooter chassis reducing asset depreciation<br/>- Smart modular electric scooters with IoT capabilities for real-time monitoring<br/>- Closed-loop battery swapping network with secondary-life storage partnerships<br/>- Consumer app providing tap-and-go localized access<br/>- Proprietary dynamic telemetry capturing vibration, thermal spikes, and accident impacts<br/>- AI predictive rebalancing algorithms for optimized vehicle redistribution<br/>- Multiple revenue streams (pay-per-ride, corporate subscriptions, B2B advertising)<br/>- Market sizing with defined TAM/SAM/SOM metrics<br/>- Clear use of funds allocation with specific milestones<br/>- Founder vesting schedule specified in cap table<br/>- Anti-dilution protection provisions included<br/><br/>## RISKS<br/><br/>- Scaling manufacturing to 1,000 active fleet nodes within timeline<br/>- Securing regulatory clearance in three additional municipal zones<br/>- Achieving operational cash-flow break-even within 14 months<br/>- Capturing 15% market share of core tech-corridor market within 36 months<br/>- Founder team appears to lack depth beyond single founder<br/><br/>## RED FLAGS<br/><br/>- No co-founder team members identified or detailed<br/>- Missing pilot/traction data (user base, revenue, utilization metrics)<br/>- No detailed financial projections beyond 14-month horizon<br/>- No existing investor information provided<br/>- No IP/patent portfolio documentation provided<br/>- No detailed competitor analysis beyond generic references<br/><br/>## MISSING INFORMATION<br/><br/>- Years of founder&apos;s experience<br/>- Founder certifications<br/>- Patents or IP filings<br/>- Publications or research papers<br/>- Historical fundraising details<br/>- Accelerator participation history<br/>- Exit history<br/>- Regulatory requirements for additional municipal zones<br/>- Validation/certification status of battery recycling process<br/>- Detailed unit economics supporting 60% cost advantage claim<br/>- Customer acquisition cost and lifetime value metrics<br/><br/>## FOLLOW-UP QUESTIONS<br/><br/>- What is your total years of experience in the mobility sector?<br/>- Do you hold any certifications relevant to electric mobility or sustainable engineering?<br/>- Have you filed or been granted any patents related to your technology?<br/>- What is your fundraising history to date?<br/>- Have you participated in any accelerator programs?<br/>- What specific manufacturing capacity and supply chain partners enable 1,000 scooter deployment?<br/>- What regulatory approvals are required for each of the three additional municipal zones?<br/>- How do you plan to achieve cash-flow break-even within 14 months?<br/>- What metrics will measure the 15% market share target?<br/>- What is the status of pilot programs validating your business model?<br/>- How does your closed-loop recycling network compare to industry standards on cost efficiency?<br/>- What are your projected unit economics supporting the 60% cost advantage claim?<br/>- How will you compete against existing micro-mobility providers?<br/>- What is your roadmap for expansion beyond tech-corridors?<br/><br/>## OVERALL RECOMMENDATION<br/><br/>**Proceed with Caution**<br/><br/>While EkoStride demonstrates a compelling mission addressing real urban mobility and environmental challenges in India, several significant risks and information gaps must be addressed before investment. The startup shows promise with its circular manufacturing approach and clear market opportunity, but the single-founder structure, lack of traction data, and missing financial details warrant further investigation.<br/><br/>## DUE DILIGENCE SCORE: 65/100<br/><br/>**Rationale**: EkoStride earns points for its strong environmental mission, clear market sizing, innovative technology stack, and founder with relevant previous experience. However, substantial deductions are made for the lack of co-founders/team details, missing traction metrics, incomplete financial modeling, and absence of competitive/IP analysis. The seed funding request appears reasonable relative to the milestones, but the path to break-even within 14 months seems aggressive without supporting detailed financials. Additional due diligence on manufacturing partnerships, regulatory pathways, and pilot results is essential before proceeding." id="sjs-A2"># EKO STRIDE INVESTMENT REPORT<br/><br/>## EXECUTIVE SUMMARY<br/><br/>EkoStride is a seed-stage Indian micro-mobility startup developing smart modular electric scooters built from recyclable composites, featuring a closed-loop battery swapping network and IoT-enabled consumer app. The company targets urban commuters in Tier 1 and Tier 2 cities, addressing congestion, first-and-last-mile gaps, and EV battery waste management. With a $15B TAM and $2.5B SAM, EkoStride&apos;s business model combines pay-per-ride fees, corporate subscriptions, and hyperlocal advertising revenue.<br/><br/>Founder Saanchi brings relevant experience from NextGen Mobility Solutions where she led deployment of an IoT-enabled fleet management system scaling to 5,000 daily transit nodes. The seed round of ₹1.5 Crores will fund deployment of 1,000 scooters, regulatory clearance in three new municipal zones, and achievement of operational cash-flow break-even within 14 months. Key strengths include circular manufacturing framework and proprietary telemetry systems, though founder team depth and detailed financial projections remain unclear.<br/><br/>## STARTUP OVERVIEW<br/><br/>- **Name**: EkoStride Mobility Private Limited<br/>- **Industry**: Electric Mobility / Micro-mobility<br/>- **Sector**: Transportation<br/>- **Stage**: Seed<br/>- **Location**: New Delhi, India<br/><br/>## FOUNDER ANALYSIS<br/><br/>- **Founder/CEO**: Saanchi<br/>- **Background**: <br/>  - Product Strategy &amp; Technology Lead at NextGen Mobility Solutions (2023-2025)<br/>  - Led IoT-enabled fleet management system scaling to 5,000 daily transit nodes<br/>  - Experience in lithium-ion battery optimization (25% thermal threshold improvement)<br/>  - Analyzed multi-city commuter routing for battery swapping station placement<br/>- **Education**: B.Tech in Electrical Sciences &amp; Engineering, Premier Technical University<br/>- **Achievements**: 1st Place at National Sustainable Transit Innovation Challenge<br/><br/>## MARKET ANALYSIS<br/><br/>- **Total Addressable Market (TAM)**: $15 Billion<br/>- **Serviceable Available Market (SAM)**: $2.5 Billion<br/>- **Serviceable Obtainable Market (SOM)**: 15% share of core tech-corridor market over 36 months<br/>- **Target Customers**: Urban commuters in tech parks, university clusters, and corporate employee populations across Tier 1 and Tier 2 Indian cities<br/><br/>## FINANCIAL ANALYSIS<br/><br/>- **Funding Sought**: ₹1.5 Crores (Seed round)<br/>- **Use of Funds**: <br/>  - 60% Fleet &amp; Battery Acquisition (manufacturing 1,000 smart modular scooters)<br/>  - 25% Technology Framework Development (cloud architecture, app UI/UX, IoT firmware)<br/>  - 15% General Working Capital (regulatory setup, swap hub leasing, team growth)<br/>- **Milestone**: Achieve operational cash-flow break-even within 14 months of scaling<br/><br/>## CAP TABLE ANALYSIS<br/><br/>- **Pre-Seed Ownership**:<br/>  - Founder (Saanchi): 76.47%<br/>  - Core Tech Co-Founders: 17.65%<br/>  - Unallocated ESOP Pool: 5.88%<br/>- **Post-Seed Ownership** (after ₹1.5 Crore raise at ₹10 Crore post-money):<br/>  - Founder (Saanchi): 65.00%<br/>  - Core Tech Co-Founders: 15.00%<br/>  - Incoming Seed Investors: 15.00%<br/>  - ESOP Pool: 5.00%<br/>- **Key Provisions**: <br/>  - 1x non-participating liquidation preference<br/>  - Broad-based weighted average anti-dilution protection<br/>  - 4-year monthly vesting with 1-year cliff for founder shares<br/><br/>## OBSERVED STRENGTHS<br/><br/>- Mission to decarbonize short-distance urban commuting with clear environmental impact<br/>- Use of circular-source composites for scooter chassis reducing asset depreciation<br/>- Smart modular electric scooters with IoT capabilities for real-time monitoring<br/>- Closed-loop battery swapping network with secondary-life storage partnerships<br/>- Consumer app providing tap-and-go localized access<br/>- Proprietary dynamic telemetry capturing vibration, thermal spikes, and accident impacts<br/>- AI predictive rebalancing algorithms for optimized vehicle redistribution<br/>- Multiple revenue streams (pay-per-ride, corporate subscriptions, B2B advertising)<br/>- Market sizing with defined TAM/SAM/SOM metrics<br/>- Clear use of funds allocation with specific milestones<br/>- Founder vesting schedule specified in cap table<br/>- Anti-dilution protection provisions included<br/><br/>## RISKS<br/><br/>- Scaling manufacturing to 1,000 active fleet nodes within timeline<br/>- Securing regulatory clearance in three additional municipal zones<br/>- Achieving operational cash-flow break-even within 14 months<br/>- Capturing 15% market share of core tech-corridor market within 36 months<br/>- Founder team appears to lack depth beyond single founder<br/><br/>## RED FLAGS<br/><br/>- No co-founder team members identified or detailed<br/>- Missing pilot/traction data (user base, revenue, utilization metrics)<br/>- No detailed financial projections beyond 14-month horizon<br/>- No existing investor information provided<br/>- No IP/patent portfolio documentation provided<br/>- No detailed competitor analysis beyond generic references<br/><br/>## MISSING INFORMATION<br/><br/>- Years of founder&apos;s experience<br/>- Founder certifications<br/>- Patents or IP filings<br/>- Publications or research papers<br/>- Historical fundraising details<br/>- Accelerator participation history<br/>- Exit history<br/>- Regulatory requirements for additional municipal zones<br/>- Validation/certification status of battery recycling process<br/>- Detailed unit economics supporting 60% cost advantage claim<br/>- Customer acquisition cost and lifetime value metrics<br/><br/>## FOLLOW-UP QUESTIONS<br/><br/>- What is your total years of experience in the mobility sector?<br/>- Do you hold any certifications relevant to electric mobility or sustainable engineering?<br/>- Have you filed or been granted any patents related to your technology?<br/>- What is your fundraising history to date?<br/>- Have you participated in any accelerator programs?<br/>- What specific manufacturing capacity and supply chain partners enable 1,000 scooter deployment?<br/>- What regulatory approvals are required for each of the three additional municipal zones?<br/>- How do you plan to achieve cash-flow break-even within 14 months?<br/>- What metrics will measure the 15% market share target?<br/>- What is the status of pilot programs validating your business model?<br/>- How does your closed-loop recycling network compare to industry standards on cost efficiency?<br/>- What are your projected unit economics supporting the 60% cost advantage claim?<br/>- How will you compete against existing micro-mobility providers?<br/>- What is your roadmap for expansion beyond tech-corridors?<br/><br/>## OVERALL RECOMMENDATION<br/><br/>**Proceed with Caution**<br/><br/>While EkoStride demonstrates a compelling mission addressing real urban mobility and environmental challenges in India, several significant risks and information gaps must be addressed before investment. The startup shows promise with its circular manufacturing approach and clear market opportunity, but the single-founder structure, lack of traction data, and missing financial details warrant further investigation.<br/><br/>## DUE DILIGENCE SCORE: 65/100<br/><br/>**Rationale**: EkoStride earns points for its strong environmental mission, clear market sizing, innovative technology stack, and founder with relevant previous experience. However, substantial deductions are made for the lack of co-founders/team details, missing traction metrics, incomplete financial modeling, and absence of competitive/IP analysis. The seed funding request appears reasonable relative to the milestones, but the path to break-even within 14 months seems aggressive without supporting detailed financials. Additional due diligence on manufacturing partnerships, regulatory pathways, and pilot results is essential before proceeding.</td></tr></table></body></html>



💡 Learnings :  
Designing multi-agent AI workflows
Prompt engineering for document analysis
AI output standardization
Workflow orchestration with n8n
Document automation
Handling API limitations and workflow reliability
Building production-style automation pipelines


🌟 Highlights : 
Built a complete end-to-end AI due diligence workflow
Automated startup document analysis
Combined insights from multiple documents into one structured report
Implemented specialized AI agents for different document types
Automatically generated and delivered investor-ready reports
Identified risks, inconsistencies, and missing information before investment decisions


📌 Future Improvements : 
Support additional startup documents
Code workflow over non-code workflow
Integrate live market and competitor research
Add startup scoring and investment ranking
Store reports in a searchable database
Build a web dashboard for investors
Add human review and feedback loop
Implement retry and validation mechanisms for improved workflow reliability
