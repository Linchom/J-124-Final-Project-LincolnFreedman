# Data Analysis & Story Pitch - US Government Financial Assistance Awards for Artificial Intelligence
Analysis of dataset from usaspending.gov which lists every financial assistance award by the US government tagged with the keyword artificial intelligence
### By Lincoln Freedman
## Sourcing


### Other Potential Sources

## Story Summary


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
