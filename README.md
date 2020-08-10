# Hundreds of congressional representatives have resigned from office since commencement of 57th Congress

Final project by Jenny Lee

## CSV Files
* [Congressional resignations](https://github.com/fivethirtyeight/data/blob/master/congress-resignations/congressional_resignations.csv) from March 4, 1901, to January 15, 2018. The original data I used.
* [Data](https://drive.google.com/file/d/1Yxf7bFymtZ4GGZ_duEtOx91Bpg6lOi1Q/view?usp=sharing) extracted from PDF with Tabula.
* How I used the [congressional resignation data](https://drive.google.com/file/d/1s1gSyPSnKuRNKU5AwsITe75ttZBe5igI/view?usp=sharing) in Google spreadsheets. The data I interrogated.

## Introduction
“What is the purpose of data journalism?” I asked myself as I began my process for finding a compelling data set for my final project. My goal for this project was to find a meaningful, relevant set of data that I could adequately contextualize in a way that would make it appear timely in today’s society. I began my research for a data set based on brainstormed topics that I had a preexisting interest in, as I felt that this would aid me later on in my analyses and interpretations of the data. I thought that I would also be better equipped to identify certain trends in the data should they aise if I already had a working understanding of the topic and data I was looking for. As such, I gravitated toward topics such as recent mortality rates in the United States, terminology concerning the Black Lives Matter movement (e.g. how many people searched “BLM” over the past few months), Supreme Court data centered around both cases and justices, and executive orders that had been issued by the past few presidents.

## Finding a Data Set
As I became more and more frustrated with both the lack of publicly-available information concerning these very specific topics I was exploring, as well as my inability to thoroughly interrogate the data I was able to gather on said topics, I realized that my approach to this project had been completely misconstrued. As a data journalist-in-training, I had short-sightedly attempted to first seek out an angle I wanted my story to tell and then proceeded to seek out data that would perfectly align with this frame. However, this does not adhere to journalistic standards of integrity, because I was imposing my own biases and opinions onto the data, trying to mold the numbers and statistics in a way that would match my perspective on the issue. Because of this, I was hitting various roadblocks, and I was unable to ask creative questions to the gathered information.

After about two days of continuous searching for a data set, I decided to scrap all of my progress and start over with a fresh eye. Although this was initially a very frustrating step to take, as it felt like I was throwing all of my work down the drain, I knew it was a necessary one nonetheless. I decided to take a look at the FiveThirtyEight data repository that Professor Rue had provided as a resource to the class, and I began to look through the different data sets. This time, rather than looking for a data set that would be easy to interpret and analyze at the surface level, I tried to look for a data set that would challenge my technical abilities that I had learned throughout this semester. That is, I wanted a data set that would allow me to experiment with as many of the data-sorting platforms and methods as possible, even if it meant that my analyses may take longer to dissect.

I came across a data set containing information about congressional resignations that had taken place since March 4, 1901, which was the first session of the 57th Congress. I was intrigued by this large data set, as it had a plethora of different values being evaluated, which meant that I would have more to interrogate the data about. The data, which was located in a repository on Github, was provided in a CSV file, but the reasons for resignation column was coded as different letters that corresponded to a specific reason, as seen in Figure 1. This categorizing table was located in the README file in the repository, rather than as a CSV file. I thought this would be the perfect opportunity to practice the PDF-extracting techniques that we had reviewed in class using Tabula.

## Tabula
I exported the Github webpage containing the categorizing table as a PDF, and then I uploaded this PDF to Tabula. Once the PDF was in Tabula, I manually selected the table and made sure all the values were in order, as seen in Figure 2. I downloaded the table as a CSV file then imported it to a new Google spreadsheet, along with the main data concerning congressional resignations.

## Google Spreadsheets
Before interrogating the data, I wanted to further practice the spreadsheet-related techniques we had learned in class this semester. Specifically, I remember I had struggled most with mastering the “VLOOKUP” function. As such, I decided to use the categorizing table, which contained the coded letters for the resignation reasons, in order to list the full reasons on the actual spreadsheet, rather than just a letter. My initial formula was: =VLOOKUP(H2,Sheet2!$A$2:B11,2,false). After dragging this function down the entire column of the spreadsheet, I used the “copy + paste values only” process to lock in the fully-listed reasons so that they do not consist of formulas that only work if the inputted factors remain unchanged.

I was now ready to interrogate the data with pivot tables. The first table I created was simply viewing how many times each source of information that had been listed in the data set had covered congressional resignation. The screenshot of this pivot table, pictured in Figure 3, shows the top 24 news sources that most frequently covered the congressional resignations — I was unable to take a screenshot of the entire table, which amounted to a total of 102 rows of data. The settings I imputed into the pivot table editor can be found in Figure 4.

The next pivot table I created observed the number of Democratic, Republican, and total representatives who resigned from each Congress. Figure 5 shows the first 25 rows of this data table, starting with the most recent congressional term (115th). The settings for this pivotal table are shown in Figure 6. One way I evaluated this data was through sorting the “Grand Total” column by descending order (A to Z), which led me to find that the 93rd Congress had the largest overall number of resignations (34). The 95th Congress had the most amount of Democratic resignations (19), whereas the most Republicans resigned during the 93rd Congress (17).

From here, I wanted to learn more about the reasons for resignation — this was where the column I had created through the “VLOOKUP” function came as a great help. I was able to generate a pivot table showing the frequency of each listed reason from the different categorial limitations that were shown in Figure 1. According to this pivot table, pictured in Figure 7, the most common reason why a representative resigned from their office was because of an election and/or appointment to another public office. “Left early” was listed as the second most-common reason, and a transition to the “private sector” of politics was listed as the third reason. I have included the settings used for this pivot table in Figure 8.

The final pivot table I created looked at these listed reasons further broken down based on political party affiliation, as demonstrated in Figure 9. I wanted to see which reasons were more common for Democratic members of Congress versus more common for Republican members of Congress. I found that Democratic representatives were much more likely to resign due to leaving early or being elected to another office. There were no areas in which the Republican representatives were substantially more likely to resign in terms of numbers. Something that surprised and interested me from this pivot table was that a total of 357 Democratic representatives have resigned from office, while 258 Republican have resigned — this is nearly a 100-person difference. However, perhaps more shocking than this disparity is how a total number of 615 total members of Congress have resigned since 1901. The settings used to generate this pivot table can be found in Figure 10.

## Data Wrapper
After generating these pivot tables, I felt that I had a better understanding of the data I was working with. I felt comfortable enough to proceed to Data Wrapper, where I wanted to further visualize and analyze some of the data into graphs and charts. 

My main goal for creating visualizations of my data on Data Wrapper was to more clearly be able to compare the differences between Democratic representatives and Republican representatives. As such, I first created a comparative, split bar chart, as illustrated in Figure 11, that used the data from my last-mentioned pivot table (Figure 9), which juxtaposed the different reasons for which Democratic versus Republican members of Congress have resigned. One benefit of using this chart was that I was able to visually see how certain reasons were much more prominent for a certain political party — however, a main drawback I found with my chart was that a majority of the space did not contain large enough values to be effectively visualized (e.g. values between 0-6). Even so, I appreciate the technique because I was able to learn how to analyze the same data I generated in a pivot table through a different process of thinking about it on Data Wrapper.

The second chart I generated was a multi-donut chart, as seen in Figure 12,  featuring two different charts that showed the different effects that a certain factor of the dataset had on contrasting demographic variables — specifically, Democrats versus Republicans. This donut chart was inspired by and expanded on the first pivot table I created (Figure 3), which looked at the extent to which each listed organization covered congressional resignations. For this data chart, I further broke down the data to see how this coverage played out between Democratic resignations versus Repblican resignations. Unfortunately, I was not able to include all of the included news outlets, as there were over 100 listed, and a large majority of these had only been sourced for one resignation in the entire dataset. As such, I made the choice to investigate the top 14 sources that had reported on congressional resignations the most often. I chose 14 because this was also the number of organizations that were listed three or more times — this indicated to me that a particular news source must have a consistent, at least to some extent, interest in congressional matters and thus may provide me with deeper insights on potential trends and analyses as a controlled group.

The most frequently-cited source for congressional resignations by the dataset’s creator was U.S. Congress, which makes sense to me, particularly since many of the representatives who resigned did so in order to work in another public office — as such, information about their new position is probably available from the U.S. Congress. However, I was more surprised to find that the New York Times was the second-most cited source for congressional resignations, especially because this publication, similar to a majority of newsrooms in the United States, is commercially-driven, and thus may have an underlying agenda and/or frame through which they present stories and facts. The same reasoning can be applied to the Washington Post, which was also one of the most prominent sources of information. The last thing worth mentioning in regards to these donut charts is the section titled “Other.” The publications/organizations included in this category are: CQ Almanac, USA Today, Roll Call, Politico, U.S. Senate, Los Angeles Times, CNN, and Indianapolis Star. Although the frequencies of these organizations were significant enough for them to be included in the chart data, they were not substantial enough to necessitate their own section of the donut chart (there was also not enough space). This chart, overall, was very effective in allowing me to view the different monopoly over politics-related information that certain news companies have, as well as how coverage of congressional matters as a whole may be currently distributed in the United States.

## Final Thoughts
The final project was a very interesting and insightful experience, and I feel that I have greatly improved my familiarity with various different types of fundamental data journalism-centric tools. I had a really great time in Journalism 124, and I truly appreciate all of the knowledge and information I was able to obtain this summer!


# Appendix
## Figure 1
![categorizing table](https://lh6.googleusercontent.com/Zj7ODWeOwBsT9x_rhxNvlpWTTXQfthBswnwLuBHH7eJbmL0wcxFKqS_PekISkO6zNGQSyUMdsjhpwYGjRcnlRmvEkg0yzETTEgqeIO86nT9C7XuoOU-vT8bjojCkaIAnScEGwHw_)

## Figure 2
![Tabula table](https://lh6.googleusercontent.com/G15UquXiLcOJYXtdI2e_4qtZj8T8eFYzoua0U0aOwO5osHzH7QjtUvamZgB7Cn51NBo5d_qooY-E7WFKj8Zfbk4rObmcNBm2GEqQL3Z548ciNSzImZBS-XdDwothi9Pn1w_uImnV)

## Figure 3
![Pivot Table 1](https://lh3.googleusercontent.com/liS38zFvoD5LjDS9SCOS9Q3RYNpKhKupW7sLTHrl0OL_ctO73Dv1qV0J4udqb4IYc940k_1xhQTx9YzE21Dg8ZECajSlGXomypTRAYJA)

## Figure 4
![Pivot Table Editor Settings](https://lh3.googleusercontent.com/_OvELg2AlupV26nOY-95DZ72U8gByfvnIcSRoGoJUsrHoYbaIwxTipCHPKt265YZWaBGepyeM4NftDySlQLmcKZ_qz2z36S6I_AMTkTGiAwRUg6I8VVdWtyn2FiH-DsSBos2aOEr)

## Figure 5
![Pivot Table 2](https://lh6.googleusercontent.com/aQ9DubnRWUWxSYGEh0DvcWWKCExN8duvcv17qumnjVqcnZSzQUtsLT7gRPTr4oiH1BVicC7wal--C0tYeN-ik_hlP7XpUq7GaJPtzErmD3lCcLFC9lF5MUO3i9A4FDXBVp5k9yJq)

## Figure 6
![Pivot Table Editor Settings](https://lh3.googleusercontent.com/EZHW_6dH1QMWQ4XuvGVRA-OoEA7rjmbhP2Kk5xCoU_t7--V-kw2NNwPBkXOfTDBx1DSMMmW1iQgN-nqNd1EQfdcCMSAWCWiEYqUZWma4uJ8L68w2Bm38PW-wZG6vfhE_VzCgl8B1)

## Figure 7
![Pivote Table 3](https://lh6.googleusercontent.com/aoBw2PlHdwhazPwMO3cH0_19_TR-x2uEA8DaYqvYjd5wXUoOfENAI6WJf1Txjh-cIe719rNrm3qDe7pH6pO_5bki3K5NBEdCWjdlWM2GuA_PX9v3OdDvA6Qd4NOO9W0A-ctqVFDa)

## Figure 8
![Pivot Table Editor Settings](https://lh6.googleusercontent.com/YYC1d9RSYJcR2_9EayOhi0ys-qnVOFrPljGuiRapcmq0dWPPJzyY0jEoTkZbATMvB6aSkKNCsYx46T07zmthx4EB7lNRg4wU460DyVIf09S7NJReLsVQP8f2iQCPhIu4wfboSDPM)

## Figure 9
![Pivot Table 4](https://lh4.googleusercontent.com/7WZiHadzHfRaWkSzPYAdS5E8bQ3uV12Zrdamd_0VlRGuNdJOEIYUuM3ljBDNvOUoYUvm6bp1UM0v-N3vQPzxSPK-8lNtWQFM2pkqAW8rSX-zLX1H3f68s5TqV9c7P_-k-tAJDTOO)

## Figure 10
![Pivot Table Editor Settings](https://lh4.googleusercontent.com/XJJvENkAALRGYQACmmxMY8xN0wh-R-W9Pm55r2jURfOUd5lCghlKShO631Ga6JZn549dsGIxSqQL4Oco5TNRxVTFIx5wHQ7XnTXbAhYMkuOjvgoLcqJLVbOGQ0Jop-4mJEBOg9nK)

## Figure 11
<iframe title="More Democratic members of Congress have resigned over the past century than Republican members of Congress" aria-label="Split Bars" id="datawrapper-chart-6Ti0K" src="https://datawrapper.dwcdn.net/6Ti0K/1/" scrolling="no" frameborder="0" style="width: 0; min-width: 100% !important; border: none;" height="1136"></iframe><script type="text/javascript">!function(){"use strict";window.addEventListener("message",(function(a){if(void 0!==a.data["datawrapper-height"])for(var e in a.data["datawrapper-height"]){var t=document.getElementById("datawrapper-chart-"+e)||document.querySelector("iframe[src*='"+e+"']");t&&(t.style.height=a.data["datawrapper-height"][e]+"px")}}))}();
</script>

## Figure 12
<iframe title="More than 80% of the Democratic and Republican congressional resignations were covered by 14 out of 102 listed sources" aria-label="chart" id="datawrapper-chart-rkZsx" src="https://datawrapper.dwcdn.net/rkZsx/1/" scrolling="no" frameborder="0" style="width: 0; min-width: 100% !important; border: none;" height="768"></iframe><script type="text/javascript">!function(){"use strict";window.addEventListener("message",(function(a){if(void 0!==a.data["datawrapper-height"])for(var e in a.data["datawrapper-height"]){var t=document.getElementById("datawrapper-chart-"+e)||document.querySelector("iframe[src*='"+e+"']");t&&(t.style.height=a.data["datawrapper-height"][e]+"px")}}))}();
</script>
