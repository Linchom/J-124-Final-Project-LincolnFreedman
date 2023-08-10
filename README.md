# Data Analysis & Story Pitch - US Government Financial Assistance Awards for Artificial Intelligence
### By Lincoln Freedman
## Sourcing
For this project I analyzed a dataset from ["usaspending.gov"](https://www.usaspending.gov/search/?hash=1f759e15d305dbdaf91a5228b721d085) which lists every financial assistance award by the US government tagged with the keyword artificial intelligence (note: this data does not include contracts). 

### Potential Interview Contacts
1) Sethuraman Panchanathan
    * Phone Number: (703) 292-8000
    * Email: spanchan@nsf.gov
    * Panchanathan is the director of the US National Science Foundation, which is the federal agency that awarded the most money in AI related grants by a wide margin. As such, I feel that he could have some valuable things to say about where this money is going, and why it is the right place.
2) Regina Barzilay
    * Phone Number: (617) 258-5706
    * Email: regina@csail.mit.edu
    *  Barzilay is noted as a "Distinguished Professor for AI" in the MIT AI+D faculty website. Seeing as a large majority of funds were awarded to institutions of higher education, with MIT itself receiving 12 grants, I feel that speaking to an expert from this institution about how the money is used and why it is important could be very instructive. 
### Other Potential Sources
1) ["Stanford Artificial Intelligence Index Report 2023"](https://aiindex.stanford.edu/wp-content/uploads/2023/04/HAI_AI-Index-Report_2023.pdf)
    * A very current report by a reliable source which includes data about the total money spent by the federal government on AI 
    * Includes some demographic analyses of how various groups feel about the advance of AI
2) ["US State Department Report on Artificial Intelligence"](https://www.state.gov/artificial-intelligence/_) 
    * Outlines the Fed's motivation for increased expenditures on AI research grants evident in this data, especially from a foreign policy perspective
    * Describes some legal policies which the govt. has implemented on the subject of AI
## Story Summary
As the global buzz around AI technology increases, my findings show that the US federal government has been spending vastly more on AI related grants each year since 2018. Many departments of the government are involved in funding a variety of AI research and development projects in fields such as agriculture, defense, energy, and especially medicine. Approximately three quarters of these financial assistance awards are going to institutions of higher education, including private Universities, which account for more than $400 million of the ~$2 billion that have been awarded in total. <br>

One danger of the rapid rise of AI technologies that has been repeatedly referenced by objectors is that it could quickly displace many working class people from their jobs while enriching a class of technocrat elites. Even as the Senate Judiciary Committee met just two months ago with OpenAI CEO Sam Altman, as well as other industry leaders and experts, to discuss the need for AI regulation, the bureaucrats in charge of awarding money for AI research may be moving in the opposite direction by investing with accelerating intensity into the development of these technologies. <br>

Furthermore, the data shows that AI research grants are heavily biased towards wealthier states like Massachusetts and California compared to poorer ones like Ohio. This is unsurprising, considering that many awards are going to prestigious private Universities like MIT. This investment pattern could lead to an exacerbation of income inequality, as educated students from wealthy states are bolstered by federal money to research and develop technologies which will allow them to replace workers with machines in the coming years. I feel that this data could definitely be part of a bigger story on this topic.

## Data Analysis Process

### Data Analysis Questions
**1. What is the total amount of US govt. funding for AI? How many Awards is this spread across? What is the mean and median amount per award?** <br>
Step By Step Process: 
First, create a new pivot table. Then select total_funding_amount under the values tab and summarize by sum. This will display a single number for the total amount of money given by the US govt. in AI related awards (note: this is not within a limited time frame). As shown below, the figure is $2,029,561,987.
<img width="1211" alt="Screenshot 2023-08-10 024053" src="https://github.com/Linchom/J-124-Final-Project-LincolnFreedman/assets/55606828/e8cd24f3-727b-4a03-973d-cddbf8fa88d6">
Next, simply scroll to the bottom of the original sheet and observe the total number of rows filled with data. This number shows how many awards the aforementioned ~$2 billion is spread across. As shown below the figure is 2,540.
<img width="1085" alt="Screenshot 2023-08-10 025919" src="https://github.com/Linchom/J-124-Final-Project-LincolnFreedman/assets/55606828/e904b85e-32b4-410a-bd42-29e5c13c5f17">

With these two figures, it is easy to find the mean dollar amount of an award by simply dividing $2,029,561,987 by 2,540. The quotient is $799,040. In order to find the median, change the existing pivot table to be summarized by median instead of sum. As shown below, the figure is $318,000.
<img width="1206" alt="Screenshot 2023-08-10 031355" src="https://github.com/Linchom/J-124-Final-Project-LincolnFreedman/assets/55606828/e521a39b-d456-45bb-8384-b05b2b0893b9">

**2. When were the majority of AI related awards given out?** <br>
Step By Step Process:
First, create a pivot table and add an award_base_action_date sorting function in the values tab. Set it to be summarized by countA in order to tally every value that is not blank. Next, add an award_base_action_date_fiscal_year sorting function under the rows tab. This displays the data more cleanly in a year by year format rather than having to see each individual date. The pivot table will now display the number of AI related awards that were issued in each year, except years in which none were issued (which is every year before 2007). As shown below, the numbers of awards were relatively low until 2018, after which they drastically increased each year. 
<img width="1228" alt="Screenshot 2023-08-10 033052" src="https://github.com/Linchom/J-124-Final-Project-LincolnFreedman/assets/55606828/287b1e5a-7b5b-4a82-9243-41a8b17bf5c4">
In order to display the total amount of funding which was awarded each year in dollars, change the sorting function in the values tab to total_funding_amount and set it to be summarized by sum. As shown below, $770,073,410 and $436,359,725 were awarded in 2022 and 2023 (so far) respectively, accounting for a combined total of 59.4% of the total amount of funds awarded across all years.
<img width="1243" alt="Screenshot 2023-08-10 034029" src="https://github.com/Linchom/J-124-Final-Project-LincolnFreedman/assets/55606828/c057cb4c-a3c2-49e8-8329-7483d784bd28">

**3. What Branches of the US govt. are dispensing the most awards?** <br>
Step By Step Process:
First, create a pivot table and add a total_funding_amount sorting function under the values tab. Set it to be summarized by sum. Next, add an awarding_agency_name sorting function under the rows tab. Set it to be sorted by the sum of total_funding_amount and display in descending order. Every govt. agency that is referenced in the dataset will now appear next to the total amount of funds that they awarded in AI related financial assistance. As shown below, the National Science Foundation awarded the most at more than $750 million, followed closely by the Department of Health and Human Services which awarded over $600 million. Confusingly, the Departments of Defense and Agriculture are in positions 3 and 4. 
<img width="1218" alt="Screenshot 2023-08-10 035852" src="https://github.com/Linchom/J-124-Final-Project-LincolnFreedman/assets/55606828/b901bc78-db2e-458a-b4cb-a24d93b9af5a">

**4. What types of organizations are receiving these awards?** <br>
Step By Step Process:
First, create a pivot table and add a total_funding_amount sorting function under the values tab. Set it to be summarized by sum. Next, add a business_types_description sorting function under the rows tab. Set it to be sorted by the sum of total_funding_amount and display in descending order. Every type of recipient that is referenced in the dataset will now appear next to the total amount of funds that they have been awarded in AI related financial assistance. As shown below, various forms of higher education institutions (public, private, historically black, etc.) have recieved approximately 75% of the total US govt. AI related funding. Small Businesses and Nonprofits make up a majority of the remainder.
<img width="1217" alt="Screenshot 2023-08-10 040907" src="https://github.com/Linchom/J-124-Final-Project-LincolnFreedman/assets/55606828/9bbbae78-49ed-4e5b-8bfa-a020baeab167">

**5. In what regions of the country are the majority of these funds pooling?** <br>
Step By Step Process:
First, create a pivot table and add a total_funding_amount sorting function under the values tab. Set it to be summarized by sum. Next, add a recipient_state_name sorting function under the rows tab. Set it to be sorted by the sum of total_funding_amount and display in descending order. Every state that is referenced in the dataset will now appear next to the total amount of funds that it has recieved in AI related govt. funding. Unsurprisingly, California is at the top of the list by more than double the second highest. Though larger states generally received more funding, this is evidently not the only factor at play, as Ohio, for example, received less funding than the District of Columbia, of which it has 15 times the population.
<img width="1277" alt="Screenshot 2023-08-10 044939" src="https://github.com/Linchom/J-124-Final-Project-LincolnFreedman/assets/55606828/acc64db9-58bc-4798-b2d8-bf06091d3d06">

## Data Visualization
![9IV4A-total-funds-awarded-by-us-govt-for-ai-research-development-by-state](https://github.com/Linchom/J-124-Final-Project-LincolnFreedman/assets/55606828/4a19db73-31ec-4d94-866a-43b1e018ee7a)

