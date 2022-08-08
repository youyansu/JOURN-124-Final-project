# Journalist and media worker deaths since 1992
## By Yansu Tan
## Summary
My dataset
## Source
My data of journalists and media workers killed since 1992 comes from [Committee to Protect Journalists (CPJ)](https://cpj.org/data/). [CPJ](https://cpj.org/about/) is an independent non-profit that defends press freedom and supports the rights of journalists worldwide.
### [Methodology](https://cpj.org/data-methodology/)
A few key things that are important in our data analysis:
1. CPJ excludes journalists that "were clearly not killed for their journalism, or died in an accident/weather event or because of illness – even if the accident was work-related." 
2. CPJ researchers independently investigate and verify the circumstances behind each death by interviewing the victim's friends, families, and colleagues to learn about the details of each death. Such details include whether the journalist was on assignment at time of death, whether they had published content that could attract hostility, whether they had previous received threats, etc. 
  * CPJ "considers a case “confirmed” as work-related only when it appears certain that a journalist was murdered in direct reprisal for his or her work; in combat or crossfire; or while carrying out a dangerous assignment." 
  * In cases where CPJ cannot confirm whether the death of the journalist as clear motives but has a potential link to journalism, CPJ classifies it as "unconfirmed".
3. Since 2003, CPJ started recording the work-related deaths of translators, drivers, fixers, security guards, and administrative workers as they recognized the importance of these figures to journalism. CPJ classifes these figures as "media workers".
4. CPJ constantly monitors the judicial process for each confirmed murder case. There are three categories of impuntiy: "complete impunity" (no convictions have been obtained), "partial justice" (some but not all of those responsible have been convicted; typically, assassins are convicted but not those who ordered the killing), and "full justice" (everyone responsible is convicted, including perpetrators and those who commissioned them).
5. This data excludes the more than sixty journalists currently missing. CPJ categorizes cases as "missing" if the boy of the reporter is not found.
### Additional source: 
1. Press Freedom Index, compiled by Reporters Without Borders (RSF)](https://rsf.org/en/index): The press freedom index is a snapshot of the level of press freedom experienced by journalists and media in 180 countries and territories each year, based on the definition of "press freedom" by RSF. PFI ranges from 0-100, with 0 being the least amount of press freedom and 100 the most. According to RSF, "This score is calculated on the basis of two components: a quantitative tally of abuses against journalists in connection with their work, and against media outlets; a qualitative analysis of the situation in each country or territory based on the responses of press freedom specialists (including journalists, researchers, academics and human rights defenders) to an RSF questionnaire available in 23 languages." Read more about the [methodology](https://rsf.org/en/index-methodologie-2022?year=2022&data_type=general) here.
2. [Corruptions Perceptions Index](https://www.transparency.org/en/cpi/2021): This is an index by Transparency.org to gauge the 
### Potential interview sources
1. Chrissy Heckart
 * chrissy@risctraining.org
 * Chrissy Heckart is Deputy Director at [Reporters Instructed in Saving Colleagues](https://risctraining.org/). This is a program that trains freelance journalists in safety and self-protection in war zones. I think her perspective as a source for this story adds a lot of human element to the number side of the story, and it informs the reader on what the "solution" is to the "problem".
2. Hesna Al Ghaoui
 * info@hesna.hu
 * For more than a decade, Hesna worked as a foreign-editor, reporter and a war correspondent for the Hungarian Television, and has reported from more than twenty countries, among them several combat zones. As a long time journalist in combat zones or other dangerous places to report from, she has a lot of anecdotal stories to share about safety for journalists.
 
## Key questions to answer:
1. In which countries do journalism deaths take place?
 * First, I made a pivot table with "country" as the row and "full name" as the value, summarized by "COUNTA". Then copy the table and paste only values in another sheet. Then sort the "COUNTA of fullName" column from Z to A. This gives the countries with the highest number of deaths. 
 * I also used this data to create the following [choropleth map](https://www.datawrapper.de/_/Y4tO7/).

![Y4tO7-journalist-and-media-worker-deaths-since-1992](https://user-images.githubusercontent.com/109619753/183368621-556c0456-1d95-4e0c-9f91-5b99374acc67.png)

2. How does the number of journalist deaths relate to the freedom of press of the country they were reporting on in the year they died?
 * If we were to answer this question using the Press Freedom Index, the major problem in answering this question with graphs is the fact that there are four variables involved: year, country, number of deaths, and PFI, since the PFI varies depending on year for each country. Hence, I specifically looked at the three countries with the most number of deaths. 
 
3. Is there a historical trend? What differs from reporting today compared to 30 years ago?
To answer this question, I wanted to also show the type of journalist, i.e. freelancer, staff reporter, or media worker. To combine the columns "type" and "employedAs", I used the IF function to create a new column "type of journalist". In AP2, enter the function =IF(I2="Journalist",M2,I2), then select autofill.
Next, create a pivot table with the row as "year", column as "type of journalist", and value as "full name", summarized by "COUNTA".
<img width="552" alt="Screenshot 2022-08-08 at 2 51 49 AM" src="https://user-images.githubusercontent.com/109619753/183390959-809876fb-06da-4965-972c-bc4dcde694f5.png">
Enter this data into datawrapper to create the [following chart](https://www.datawrapper.de/_/wdnjy/).

![journalist-and-media-worker-deaths-by-job-type-since-1992](https://user-images.githubusercontent.com/109619753/183393820-49230ab5-8964-4033-9c7a-29f7b1729eea.png)

4. Does the gender of the journalist play a role?

5. What percentage of cases has been given due justice?






