# Data Report Demo Project

this is a replica of a project for work. The purpose of this project was to gather data from different sources into a single report that could be used by multiple stakeholders within the Press.

The code in this repo has been left largely unedited. The only edits are the removal of files that include sales or personnel data. The data files that are included include information that is accessible to the public. All screenshots are taken from the live report and have been edited to redact potentially sensitive sales information.

### Software

### Background and Overview
This project emerged from a need within Marketing, Sales, and Acquisitions to better understand the performance of our frontlist titles and how to respond to changes within the academic publishing industry that pulled us away from our previous business model into one that was more oriented towards open access. As OA became more important we wanted to understand:
- If sales were no longer a reliable indicator of performance what other types of indicators were available to users to determine success?
- What types of books (e.g. Business & Economics, Humanities, Health Science) performed better in that OA world?
We assembled a working group to understand what data was available and what data points needed to be gathered. From there we mapped out those resources and started assembling the raw data.
 Once the data was available I transformed, mostly using python scripts, it to clean and normalize it as much as possible. Once the data was cleaned I pulled the local files into Tableau and set about workshopping different presentation formats. We ultimately opted to minimize the visual complexity of the final reports as much as possible. What came out of this were two reports, one that looked at book impacts and performance, and one that looked at subject performance.
Once the final reports were ready we opted to move the data into an RDS. I opted to use a database for security (we didn't want sales information traveling with the Tableau workbook) and for greater consistency during data updates. I used an RDS because it's relatively easy to set up, integrates easily with Tableau, and I'm familiar with the AWS environment so the learning curve was pretty flat. We selected Tableau as our visualization for three reasons. First, MIT has a Tableau license so we could use the secure MIT Tableau server to host the final Tableau workbook and data files. This also meant we had the option to require Kerberos authentication for users to access the final reports. We also wanted a user-friendly presentation software given that these reports were intended to be used across different departments with different degrees of technical proficiency.


### Takeaways
There were a few key takeaways from this project:
Understanding how to talk about data across departments. Understanding what questions to ask, how to frame a problem, and how to make data projects feel accessible to everyone involved. 
The importance of a data QA and reproducibility. All data cleaning and transforming took place in python. This was a significant change from our previous reliance on using software like Excel to edit data files prior to analysis. Scripting all data transformations was key to reproducibility and good documentation. It also lessened the potential for introducing errors and helped preserve the integrity of the data we were pulling in. 



# Data Report Demo Project

this is a replica of a project for work. The purpose of this project was to gather data from different sources into a single report that could be used by multiple stakeholders within the Press.

The code in this repo has been left largely unedited. The only edits are the removal of files that include sales or personnel data. The data files that are included include information that is accessible to the public. All screenshots are taken from the live report and have been edited to redact potentially sensitive sales information.

### Software

### Background and Overview
This project emerged from a need within Marketing, Sales, and Acquisitions to better understand the performance of our frontlist titles and how to respond to changes within the academic publishing industry that pulled us away from our previous business model into one that was more oriented towards open access. As OA became more important we wanted to understand:
- If sales were no longer a reliable indicator of performance what other types of indicators were available to users to determine success?
- What types of books (e.g. Business & Economics, Humanities, Health Science) performed better in that OA world?
We assembled a working group to understand what data was available and what data points needed to be gathered. From there we mapped out those resources and started assembling the raw data.
 Once the data was available I transformed, mostly using python scripts, it to clean and normalize it as much as possible. Once the data was cleaned I pulled the local files into Tableau and set about workshopping different presentation formats. We ultimately opted to minimize the visual complexity of the final reports as much as possible. What came out of this were two reports, one that looked at book impacts and performance, and one that looked at subject performance.
Once the final reports were ready we opted to move the data into an RDS. I opted to use a database for security (we didn't want sales information traveling with the Tableau workbook) and for greater consistency during data updates. I used an RDS because it's relatively easy to set up, integrates easily with Tableau, and I'm familiar with the AWS environment so the learning curve was pretty flat. We selected Tableau as our visualization for three reasons. First, MIT has a Tableau license so we could use the secure MIT Tableau server to host the final Tableau workbook and data files. This also meant we had the option to require Kerberos authentication for users to access the final reports. We also wanted a user-friendly presentation software given that these reports were intended to be used across different departments with different degrees of technical proficiency.


### Takeaways
There were a few key takeaways from this project:
Understanding how to talk about data across departments. Understanding what questions to ask, how to frame a problem, and how to make data projects feel accessible to everyone involved. 
The importance of a data QA and reproducibility. All data cleaning and transforming took place in python. This was a significant change from our previous reliance on using software like Excel to edit data files prior to analysis. Scripting all data transformations was key to reproducibility and good documentation. It also lessened the potential for introducing errors and helped preserve the integrity of the data we were pulling in. 



