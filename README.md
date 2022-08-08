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

From this map, we can see that there are actually very few countries that are exempt from this list. Most journalism deaths occur in the middle east, in central and south America, and in the Indian subcontinent. Countries that have the most journalist deaths are: Iraq (283), Syria (154), the Philippines (153), Mexico (149), and Pakistan (96).

2. Is there a historical trend? What differs from reporting today compared to 30 years ago?
To answer this question, I wanted to also show the type of journalist, i.e. freelancer, staff reporter, or media worker. To combine the columns "type" and "employedAs", I used the IF function to create a new column "type of journalist". In AP2, enter the function =IF(I2="Journalist",M2,I2), then select autofill.
Next, create a pivot table with the row as "year", column as "type of journalist", and value as "full name", summarized by "COUNTA".
<img width="552" alt="Screenshot 2022-08-08 at 2 51 49 AM" src="https://user-images.githubusercontent.com/109619753/183390959-809876fb-06da-4965-972c-bc4dcde694f5.png">

Enter this data into datawrapper to create [chart](https://www.datawrapper.de/_/wdnjy/).

![wdnjy-journalist-and-media-worker-deaths-by-job-type-since-1992](https://user-images.githubusercontent.com/109619753/183418017-5bf919ae-9bd4-4c74-b2e7-f8b663ee92db.png)

There has been more deaths occurring in the 2010s, with also a peak in 2006 ad 2007, perhaps due to increased U.S. involvement in the Iraqi war, which would attract more reporters. We also saw a lot of media worker deaths in those two years. From 2019 onwards, there is a sharp fall in the number of deaths, most potentially due to COVID. 

3. What does the gender distribution look like?
I created a pivot table with "gender" as row and "full name" as value, summarized by COUNTA. While 579 entries were missing gender data, there were 116 recorded female journalists killed and 1468 male journalists killed. The ratio is 12.66, male to female. 

<img width="391" alt="Screenshot 2022-08-08 at 4 44 52 AM" src="https://user-images.githubusercontent.com/109619753/183410726-2263e676-99cf-49a2-a2f2-5dcdcd083ba2.png">

Most journalists killed were men. However, this may not necessary mean that female journalists are less targeted than male journalists. We would need to verify if that is true by comparing the numbers to the total number of male and female journalist reporters in war zones or countries with tight censorship. This is because there might be more male journalists covering war zones, perhaps because news organizations tend to prefer hiring male journalists as staff reporters for war zones. 

4. What percentage of cases has been given due justice?
 * I created a pivot table with year in "row", "impunity murder" in column, and "full name" in value, summarized by "COUNTA". Then I used the data to create the following [chart](https://www.datawrapper.de/_/nYE1z/).

![nYE1z-impunity-in-journalist-deaths-cases-since-1992](https://user-images.githubusercontent.com/109619753/183418069-644f7593-b1a4-47fe-b471-e4b4a7222323.png)

The majority of 
5. What percentage of 






