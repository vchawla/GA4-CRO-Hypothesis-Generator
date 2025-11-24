# GA4 → CRO Prompt Engine (Google Sheet)

A compact workflow that converts GA4 exports into a single structured prompt for ChatGPT to generate CRO hypotheses, A/B test ideas, uplift ranges, and confidence levels. The goal is speed and repeatability: paste GA4 numbers, produce a ready-to-run prompt, iterate with context, and arrive at testable hypotheses faster.

## What this repo contains
- Google Sheet template for structured GA4 data input  
- Formula to generate one consolidated prompt covering all sections  
- Example screenshot of generated hypotheses  
- Notes, limitations, and enhancement ideas for client-grade CRO projects  

## Quick start
1. Make a copy of the Google Sheet template:  
   **(https://docs.google.com/spreadsheets/d/1Yux7iyn9afgDraGfA8R5FNODQ-1rfmzmIml4ZkxWR0k/edit)**

2. Export GA4 data for the period you want to analyze (90 days recommended) and paste the values into the corresponding sheet sections (A to E).

3. The sheet automatically builds a single consolidated prompt that includes:
   - Overall metrics  
   - Device performance  
   - Funnel metrics by device  
   - Page level metrics by device  
   - Notes about bugs, UX changes, and traffic context  

4. Copy the final generated prompt and paste it into ChatGPT. Request 3–6 CRO hypotheses with rationale, A/B test ideas, uplift ranges, and confidence levels.

5. Review the initial output and add extra context like UI layout, screenshots, or functionality notes to refine the hypotheses. A few iterations usually produce high quality, client-ready ideas.

## Important notes and limitations
- Ideal for high level hypothesis generation. More granular insights require event-level and segment-specific data.  
- Every website has its own UX patterns and layout variations which should be added as context to improve accuracy.  
- Always check GA4 sampling before exporting data. Sampling can distort funnel metrics.  
- Adding user recordings, heatmaps, surveys, or support tickets can strengthen reasoning.  
- Device specific UX constraints and page templates should be documented and fed into the prompt.  

## Suggested enhancements for client projects
- Automate GA4 data extraction using BigQuery or API to avoid manual work and sampling issues.  
- Add prompt fields for device-specific UX notes, screenshots, and page-level nuances.  
- Expand the input sections to accept segment filters and micro-conversion metrics.  
- Integrate heatmap or session recording summaries to support hypothesis reasoning.  

## Example use case
The workflow was tested using three months of GA4 demo data from the Google Merchandise Store. The sheet produced a consolidated prompt and ChatGPT generated an initial hypothesis set. After adding visual context and refining through a few iterations, the final hypotheses were client ready and created significantly faster than doing the analysis manually.

## Screenshot
A screenshot of the generated hypotheses is included in the repository.

## License

MIT
