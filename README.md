# Data Report Demo Project

This is a replica of a project I did earlier this year for work. The purpose of this project was to gather data from different sources - internal and external - into a single report or reports that could be used by multiple stakeholders within the Press.

The code in this repo has been left largely unedited. The only edits are the removal of files that include sales or personnel data. The data files that are included include information that is publicly accessible. All screenshots are taken from the live report and have been edited to redact potentially sensitive sales information. Some code has been removed for security, including any loading scripts. 

### Files
- "Clean_and_Join_Data.ipynb" Cleaned and joined sales data going back to FY19. 
- "Read_And_Clean_Usage.ipynb": Used for monthly sales data updates. 
- "Read_And_Clean_Usage.ipynb": Clean usage data pulled from third-party platform. Also used to clean citation data gathered from Dimension DB. 



### Software Used
- Python (Data cleaning transforming)
- SQL/Python (Data Loading)*
- Amazon RDS (Database)
- Tableau (Visualization)
*We ended up loading via SQL Workbench after scripting the data loads.

### Background and Overview
This project emerged from a need within our organization, especially Marketing, Sales, and Acquisitions, to better understand the performance of our newer titles and how to respond to market changes and changes within the academic publishing industry that pulled us away from our established business model into one that was more oriented towards Open Access (OA) publishing. As OA became more important, we wanted to look at two key questions:
- If sales were no longer a reliable indicator of performance what other types of indicators were available to users to determine success?
- What types of books (e.g. Business & Economics, Humanities, Health Science) performed better/worse in that OA world?

The project was conceived in mid-2022. We began by assembling a working group to understand the basic questions we wanted the data to answer. We also wanted to understand what data was available and what data points needed to be gathered. From there we mapped out those resources and started assembling the raw data. The data sources included:
- Title level metadata (Internal)
- Sales data (Internal)
- Platform usage/download data (Internal)
- Google Analytics website traffic data (External) 
- Citation data (External)
- Altmetric data (External)


Once the raw data was available I transformed it, mostly using python scripts, to clean and normalize it as much as possible. Once the data was cleaned I pulled the local files into Tableau and set about workshopping different presentation formats. We circulated draft versions among the working group for feedback. We ultimately opted to minimize the visual complexity of the final reports as much as possible. What came out of this were two reports, one that looked at book impacts and performance, and one that looked at subject performance.
Once the final reports were ready we opted to move the data into an RDS. I opted to use a database for security (we didn't want sales information traveling with the Tableau workbook) and for greater consistency during data updates. I used an RDS because it's relatively easy to set up, integrates easily with Tableau, and I'm familiar with the AWS environment so the learning curve was pretty flat. The data load was initially scripted but, for simplicity, I ended up loading via MySQL Workbench. Loading via Workbench was also helpful sidestepping some issues associated with RDS user permissions issues. 

We selected Tableau as our visualization software for three reasons. First, MIT has a Tableau license so we could use the secure MIT Tableau server to host the final Tableau workbook and data files. This also meant we had the option to require Kerberos authentication for users accessing the final reports. We also wanted a user-friendly presentation software given that these reports were intended to be used across different departments with different degrees of technical proficiency.


### Takeaways
There were a few key takeaways from this project:
- Understanding how to talk about data across departments. Understanding what questions to ask, how to frame a problem, and how to make data projects feel accessible to everyone involved. 
- The importance of a data QA and reproducibility. All data cleaning and transforming took place in python. This was a significant change from our previous reliance on using software like Excel to manually edit data files prior to analysis. Scripting all data transformations was key to reproducibility and reliable documentation. It also lessened the potential for introducing errors and helped preserve the integrity of the data we were pulling in. 
- The data only tells part of the story. We relied on the expertise of different people throughout our organization to help us tell a story with the data. In that respect this project underscored the collaborative nature of most analytics projects. 




