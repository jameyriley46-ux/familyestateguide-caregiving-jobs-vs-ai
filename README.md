# Caregiving Jobs vs. AI: Projections, Wages and AI-Exposure Scores for Elder-Care Occupations

BLS 2025-35 employment projections, OEWS May 2025 wages and four AI-exposure/care measures (BLS relative AI exposure, Microsoft AI applicability, Anthropic observed exposure, O*NET 'Assisting and Caring for Others') for 14 hands-on care occupations and 11 high-exposure office/tech comparison occupations.

**Live page:** https://familyestateguide.com/estate-planning-data/caregiving-jobs-vs-ai/  
**Publisher:** Family Estate Guide (https://familyestateguide.com)  
**Version:** 1.0.0 (2026-10-02)  
**License:** CC BY 4.0 (data). See LICENSE.

> Not legal, tax, financial or medical advice. Figures are estimates with sampling error; legal rules change. Verify anything important with the original source or a qualified professional.

## Files

| File | Rows | Contents |
|---|---|---|
| `data/caregiving-jobs-vs-ai.csv` | 25 | 25 occupations (14 'Hands-on care', 11 comparison), national data only. |

Blank cells mean not available, not published or not applicable; they are never zero.

## Data dictionary

### `data/caregiving-jobs-vs-ai.csv`

| Column | Description |
|---|---|
| `group` | 'Hands-on care' or 'Comparison: high AI exposure office/tech' (comparison set hand-picked for contrast, not a random sample). |
| `soc` | 2018 Standard Occupational Classification code. |
| `title` | BLS occupation title. |
| `emp_2025_k` | Employment 2025, thousands (BLS Employment Projections 2025-35). |
| `emp_2035_k` | Projected employment 2035, thousands. |
| `change_k` | Projected change 2025-35, thousands. |
| `change_pct` | Projected change 2025-35, percent. |
| `annual_openings_k` | Average annual occupational openings 2025-35, thousands. |
| `median_wage_2025_ep` | Median annual wage as published in the projections file, USD. |
| `oews_may2025_hourly_median` | OEWS May 2025 national median hourly wage, USD. |
| `oews_may2025_annual_median` | OEWS May 2025 national median annual wage, USD. |
| `oews_may2025_employment` | OEWS May 2025 national employment. |
| `education` | Typical entry-level education (BLS). |
| `bls_relative_ai_exposure` | BLS relative AI exposure category (Low / Moderate / High / Very high), from BLS ai-exposure-categories.xlsx (2025-35). |
| `msft_ai_applicability` | Microsoft 'Working with AI' AI applicability score (v1.1), rounded to 3 decimals (Tomlinson et al. 2025, CC BY 4.0). |
| `anthropic_observed_exposure` | Anthropic Economic Index 'observed exposure' (0-1), rounded to 3 decimals (Massenkoff & McCrory 2026, CC-BY). Blank where Anthropic has no score (e.g., 31-1120). |
| `onet_assisting_caring_importance_1to5` | O*NET 31.0 Work Activity 4.A.4.a.5 'Assisting and Caring for Others', Importance scale 1-5; averaged across O*NET-SOC codes (31-1121 and 31-1122 averaged for 31-1120). O*NET is CC BY 4.0. |
| `bls_factor_note` | BLS Employment Projections Table 1.12 factor note (text, truncated to 300 characters). |
| `msft_percentile_among_all_occ` | Percentile of msft_ai_applicability among all occupations in the Microsoft file (calculated by FEG). |
| `anthropic_percentile_among_all_occ` | Percentile of anthropic_observed_exposure among all occupations in the Anthropic file (calculated by FEG). |

## Sources

- U.S. Bureau of Labor Statistics, Employment Projections 2025-35: AI exposure categories (https://www.bls.gov/emp/ind-occ-matrix/ai-exposure-categories.xlsx) and occupation tables 1.2 / 1.12 (https://www.bls.gov/emp/ind-occ-matrix/occupation.xlsx), released Aug 27, 2026. Public domain.
- U.S. Bureau of Labor Statistics, Occupational Employment and Wage Statistics (OEWS), May 2025 estimates (state file oesm25st.zip, national file oesm25nat.zip). https://www.bls.gov/oes/tables.htm . Public domain (U.S. government work).
- Microsoft Research, 'Working with AI' AI applicability scores, https://github.com/microsoft/working-with-ai (ai_applicability_scores.csv, retrieved Oct 1, 2026). Tomlinson, K., Jaffe, S., Wang, W., Counts, S., & Suri, S. (2025). Working with AI: Measuring the Applicability of Generative AI to Occupations. arXiv:2507.07935. Licensed CC BY 4.0.
- Anthropic, Economic Index, labor_market_impacts/job_exposure.csv, https://huggingface.co/datasets/Anthropic/EconomicIndex (retrieved Oct 1, 2026). Massenkoff, M. & McCrory, P. (2026). Labor market impacts of AI: A new measure and early evidence. https://www.anthropic.com/research/labor-market-impacts . Data released under CC-BY (per the dataset README).
- O*NET 31.0 Database, U.S. Department of Labor, Employment and Training Administration (USDOL/ETA), https://www.onetcenter.org/database.html . Used under the CC BY 4.0 license. This dataset includes information from O*NET 31.0 by USDOL/ETA; FEG modified it (averaged codes).

## Methodology

- Occupation list chosen by FEG. Code matching: BLS reports 31-1120 as an aggregate; OEWS uses 31-1120; Microsoft has 31-1120; Anthropic has no 31-1120/1121/1122 rows (left blank); O*NET 31-1121 and 31-1122 averaged for 31-1120.
- Percentiles = share of all occupations in the source file with a score less than or equal to the occupation's score.

## Limitations

- AI-exposure scores measure task overlap or observed AI usage, not job loss. Microsoft and Anthropic both state their measures should not be read as job replacement.
- BLS rates home health aides Moderate and several clinical/social-work occupations High; the simple 'care is AI-proof' story is not fully supported.
- Projections are BLS 2025-35; Anthropic's own report compares against the older 2024-34 projections.
- National data only.

## Rights review and exclusions

Family Estate Guide publishes here only its own compiled data and U.S. government public-domain data (Census, BLS, CMS, DOL), plus third-party data that is under CC BY or a compatible open license, with attribution. Third-party copyrighted or non-commercial-licensed data is excluded.

- None. Third-party columns were checked: Microsoft 'Working with AI' data is CC BY 4.0, the Anthropic Economic Index data is released under CC-BY, and O*NET is CC BY 4.0. All are compatible with redistribution under CC BY 4.0 with attribution, given in Sources. Changes made: rounding, code averaging and percentile calculation.
- Note: the Anthropic Hugging Face card lists 'license: mit' in its metadata while its README says 'Data released under CC-BY'. Both permit redistribution with attribution.

## How to cite

Family Estate Guide (2026). *Caregiving Jobs vs. AI: Projections, Wages and AI-Exposure Scores for Elder-Care Occupations* (Version 1.0.0) [Data set]. https://familyestateguide.com/estate-planning-data/caregiving-jobs-vs-ai/ . GitHub: https://github.com/jameyriley46-ux/familyestateguide-caregiving-jobs-vs-ai

A Zenodo DOI will be added here once version 1.0.0 is released and archived. Machine-readable citation: `CITATION.cff`.

Please link to the live page when you use the data.

## License

Data in this repository is licensed under the Creative Commons Attribution 4.0 International license (CC BY 4.0). Underlying U.S. government data is public domain; third-party CC BY data keeps its original attribution requirements (see Sources).
