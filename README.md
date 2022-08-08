# Journalist and media worker deaths since 1992
## By Yansu Tan
## Summary
Due to the broadness of the dataset, my preliminary data analysis opens up possibilites of further stories with more detailed datasets and specific case studies. First, we can see that contrary to the common belief that journalists are most often killed in authoritarian and war torn countries, a lot of journalist deaths actually occur in democracies, with the example of the Philippines, which has proven to be a dangerous place for journalists. The data also shows that journalist deaths can reflect the individual political and social situations of the countries where the death occurred. In addition, most journalist deaths occur in democracies, which begs the question of why governments are murdering journalists and suppressing freedom of press. This can lead to longer opinion pieces or feature stories on the relationship between freedom of press and democracies, i.e. are democratic governments serving its democratic interests, or are they using methods to control elections for their own interests? Second, the data shows a clear surge in the deaths of media workers in 2006 and 2007. Media workers includ translators, fixers, drivers, and adminstrative assistants. Since these are crucial igures in assisting international journalism, their safety should be considered an ethical responsibility of international news organizations. Further analysis as to why media worker deaths increased in 2006 to 2007 can provide insight into the international journalism industry.
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
1. Press Freedom Index, compiled by Reporters Without Borders [(RSF)](https://rsf.org/en/index): The press freedom index is a snapshot of the level of press freedom experienced by journalists and media in 180 countries and territories each year, based on the definition of "press freedom" by RSF. PFI ranges from 0-100, with 0 being the least amount of press freedom and 100 the most. According to RSF, "This score is calculated on the basis of two components: a quantitative tally of abuses against journalists in connection with their work, and against media outlets; a qualitative analysis of the situation in each country or territory based on the responses of press freedom specialists (including journalists, researchers, academics and human rights defenders) to an RSF questionnaire available in 23 languages." Read more about the [methodology](https://rsf.org/en/index-methodologie-2022?year=2022&data_type=general) here.
2. [Corruptions Perceptions Index](https://www.transparency.org/en/cpi/2021): This is an index by Transparency.org to gauge the corruption levels worldwide. It would be interesting to see if journalism deaths correlate to corruption of the government in the countries where deaths occur. 

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
 * To answer this question, I wanted to also show the type of journalist, i.e. freelancer, staff reporter, or media worker. To combine the columns "type" and "employedAs", I used the IF function to create a new column "type of journalist". In AP2, enter the function =IF(I2="Journalist",M2,I2), then select autofill.
 * Next, create a pivot table with the row as "year", column as "type of journalist", and value as "full name", summarized by "COUNTA".
<img width="552" alt="Screenshot 2022-08-08 at 2 51 49 AM" src="https://user-images.githubusercontent.com/109619753/183390959-809876fb-06da-4965-972c-bc4dcde694f5.png">

 * Enter this data into datawrapper to create [chart](https://www.datawrapper.de/_/wdnjy/).

![wdnjy-journalist-and-media-worker-deaths-by-job-type-since-1992](https://user-images.githubusercontent.com/109619753/183418017-5bf919ae-9bd4-4c74-b2e7-f8b663ee92db.png)

 * There has been more deaths occurring in the 2010s, with also a peak in 2006 ad 2007, perhaps due to increased U.S. involvement in the Iraqi war, which would attract more reporters. We also saw a lot of media worker deaths in those two years. From 2019 onwards, there is a sharp fall in the number of deaths, most potentially due to COVID. 

3. What does the gender distribution look like?
 * I created a pivot table with "gender" as row and "full name" as value, summarized by COUNTA. While 579 entries were missing gender data, there were 116 recorded female journalists killed and 1468 male journalists killed. The ratio is 12.66, male to female. 

<img width="391" alt="Screenshot 2022-08-08 at 4 44 52 AM" src="https://user-images.githubusercontent.com/109619753/183410726-2263e676-99cf-49a2-a2f2-5dcdcd083ba2.png">

 * Most journalists killed were men. However, this may not necessary mean that female journalists are less targeted than male journalists. We would need to verify if that is true by comparing the numbers to the total number of male and female journalist reporters in war zones or countries with tight censorship. This is because there might be more male journalists covering war zones, perhaps because news organizations tend to prefer hiring male journalists as staff reporters for war zones. 

4. What percentage of cases has been given due justice?
 * I created a pivot table with year in "row", "impunity murder" in column, and "full name" in value, summarized by "COUNTA". Then I used the data to create the following [chart](https://www.datawrapper.de/_/nYE1z/).

![nYE1z-impunity-in-journalist-deaths-cases-since-1992](https://user-images.githubusercontent.com/109619753/183418069-644f7593-b1a4-47fe-b471-e4b4a7222323.png)

 * An overwhelming majority of cases have received complete impunity, with the anomalies being 2009 and 2015, when the number of cases that received partial impunity surged. There was a significant increase in cases that received full impunity in these years too. Notably, almost all cases after the pandemic have received complete impunity. 

5. What types of death occured the most in the countries with most deaths?
I created a pivot table with "country" in row, "type of death" in column, and "full name" in value, summarized by COUNTA. I filtered out countries to keep the top ten countries with the most deaths (which was obtained in the answer to question 1).

Then I used the data in the table to create the [cluster bar chart](https://www.datawrapper.de/_/S4OSk/).

![S4OSk-journalism-deaths-in-top-10-countries-with-deaths](https://user-images.githubusercontent.com/109619753/183427851-b58e71c6-2afc-459e-af26-894cf9fd5382.png)

From the bar chart, we can see that the number of journalism deaths can be reflected in the situation of the country. Not all journalism deaths are the result of direct war zone conflict. For instance, the Philippines do not have a major ongoing war, and this is reflected in the number of deaths caused by murder, and none by crossfire. Backed by the Filipino congress, the Filipino president, Rodrigo Duterte, has launched countless verbal attacks and judicial harrassment targeting any media that is deemed to critical of the government. In 2020, dozens of radio stations and TV channels closed paritially due to the political situation.






