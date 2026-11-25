# UK Entry-Level Data Analyst Market: Pay, Rent & Job Volume

A 3-page Power BI report analysing 244 live entry-level data analyst listings across six UK locations to weigh up advertised starting pay, regional rent costs, and active job volume.

## Motivation
After finishing my Maths & Finance degree, I wanted a practical way to decide where to focus my job applications, and to get more hands-on practice building a multi-page Power BI report from scratch on real data. 

Because I am based in Doncaster and currently pay £200/month to stay at home, I wanted to see how relocating to a major city actually compares to staying local once housing costs are factored in.

## Methodology & Data Model
- **Job Listings:** A snapshot of entry-level data analyst roles across six UK locations, cleaned and shaped in **Power Query**.
- **Cost of Living & Rent Benchmarks:** Combined advertised starting wages with online cost-of-living and rental estimates for each city. Doncaster's housing cost is capped at **£200/month** to reflect my actual baseline living arrangement at home.
- **Looking Beyond Net Pay:** Rather than stopping at salary minus rent, I plotted **post-rent monthly surplus against total job volume** per city. A high surplus on paper isn't much use if there are barely any entry-level roles available to apply for.
- **DAX Measures:** Built custom measures (`AVERAGEX`, `SELECTEDVALUE`, and dynamic filtering) across a relational star-schema model to compare gross pay, housing deductions, and listing density interactively.

## Key Takeaway & Application Strategy
Rather than just picking a single "winning" city, the Opportunity Frontier scatter plot helped me decide how to split my time when applying for roles:
- **Ruling Out London Relocations:** Even though London holds the largest share of entry-level listings, the rent is so high that it wipes out any real chance of getting a head start on savings, making it hard to justify spending time applying there when I didn't want to relocate down south anyway.
- **Balancing Volume & Take-Home Pay:** **Manchester** stands out as one of the strongest options if relocating, pairing a high volume of entry-level openings with a reasonable post-rent take-home pay, alongside other balanced northern cities like Newcastle and Sheffield.
- **Staying Alert Locally & Remotely:** Local openings in Doncaster are much more limited, so I couldn't rely on them exclusively, but keeping an eye out for local or remote roles meant that if one came up, I could protect my take-home pay by staying at home. Ultimately, that's what I ended up doing, landing a remote role that lets me stay based in Doncaster.

## Limitations & Drawbacks
While this was a genuinely insightful exercise for structuring my job search, there are a few clear drawbacks to keep in mind:
- **Sample Size (n = 244):** The dataset is a point-in-time snapshot rather than a full-year longitudinal view of the UK market.
- **Role & Wage Variance:** "Entry-level" covers a fairly wide mix of titles and responsibilities, and advertised salary bands vary in how specific they are from one listing to the next.
- **Commuting Costs Excluded:** The model focuses on local rent benchmarks and does not factor in the option of commuting (for example, commuting from Doncaster into nearby cities like Leeds or Sheffield would be far cheaper than paying to live there, and would be doable).
- **Personal City Preferences:** Numbers only tell part of the story. Personal preference for a city's lifestyle, social connections, and day-to-day environment isn't captured in a scatter plot.

## Repository Contents
- `UK_Career_Economics.pbix` - Full interactive Power BI report file
- `UK_Career_Economics_Report.pdf` - Static 3-page export of the dashboard
