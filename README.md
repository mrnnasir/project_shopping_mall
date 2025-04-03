# Shopping Mall

This is an Individual Formative Assessment project for Data Analysis and Machine Learning with AI course arranged by Code Institue. Hence, primary objective of this project is to learn and internalize how to prepare the data for detail understanding.

This is a hypothetical project for the **ABC Marketing Company**, who would like to understand the customer buying behavior, which shopping mall has highest rate of incoming customers and sales, customers payment method and role of age and month.

This document will provide you the understanding in a simple way about how the analysis has been conducted from data collection, process to data visualization. If you need any information regarding the project, you may refer to this document to get a clear understanding.

# ![CI logo](https://codeinstitute.s3.amazonaws.com/fullstack/ci_logo_small.png)


## Dataset Content
* Describe your dataset. Choose a dataset of reasonable size to avoid exceeding the repository's maximum size of 100Gb.

I collected the dataset from Kaggle, where numerous public dataset can be found to practice or learn about the real world scenarios. The dataset I had gathered for this specfic project has about 100000 rows of data that is comprised of information about following columns,

    * Invoice_no
    * Customer_id
    * Gender
    * Age
    * Category
    * Quantity
    * Price
    * Payment_method
    * Invoice_date
    * Shopping_mall

For the purpose the research and getting meaningful output, I have randomly seleceted 10000 rows as a sample dataset and dropped Invoice_no and Customer_ID columns. Furthermore, to make it simpler to understand I renamed Invoice_date column to Datetime and added two more columns Year and Month to the dataset, so that I can make necessary analysis on year and month level. Therefore, in the final dataset you will see following columns,

    * Gender
    * Age
    * Category
    * Quantity
    * Price
    * Payment_method
    * Datetime
    * Shopping_mall
    * Year
    * Month

This sample dataset has no NULL values, indentation is corrected, spelling mistakes have been corrected and data type of each column is correctly formatted.


## Business Requirements
* Describe your business requirements
A marketing company wants to find out which shopping mall(s) usually customers prefer to go for shopping, so that the marketing company can set their marketing strategy and allocate resources accordingly. They want to explore what medium customers mostly use to pay for goods. It can help them to contemplate as to how customer behavior can be used to produce business gain. Finding out which product(s) are mostly bought and if age has any impact on product purchasing can help them deep dive why some specific products are outselling rests. Company can cunduct further research and analysis to explore the avenues of promoting list sold product groups. Since age is important factor, company is very keen to know if age has any significant impact on purchasing behavior. Additionally, company would like to know if product purchasing pattern changes over the period of months to figure out when would be the high time to allocate resources for doing the necessary campaign.


## Hypothesis and how to validate?
* List here your project hypothesis(es) and how you envision validating it (them) 
- Customer may mostly pay cash and then debit card.
    - Correlation between shopping mall with payment method
- Customer pay the most for clothing, food & beverage, cosmetics and books
    - Correlation between shopping mall and category
    - Correlation between category and price on quarterly average (approx.)
- Costomer may shop mostly clothing, food & beverage and cosmetics
    - Correlation between category and quantity
    - Correlation between category and price on average
- 50% of all named shopping malls should have similar performance report
    - Correlation between shopping mall and quantity of each year for 3 years
    - Correlation between shopping mall and gender
- Younger aged customer may pay more for book, food & beverage & older people may spend more money to clothing, cosmetics and technology
    - Correlation between average price and category on age level
- Young people tend to buy more products than older people
    - Correlation between age and quantity on an average
- Male may pay more for gadgets than female, while female pays more for clothing and cosmetics
    - Correlation between average price and category on age level for male and female


## Project Plan
* Outline the high-level steps taken for the analysis.
* How was the data managed throughout the collection, processing, analysis and interpretation steps?
* Why did you choose the research methodologies you used?

I manipulated the data from different columns of the dataset to get the expected output. I correlated data from one column with the one or more columns. Sometime, I used groupby method or query for capturing the required dataset in order to produce the necessary output. I needed to use concatenate after striping certain column(s) and reformulated the working dataset for deep diving in order to investigate if there is any trends occuring. For example, I splitted Datetime column dataset to per year dataset to check if there is any significant devation happening over year in product selling.

In order to ensure all the details are covered, I used **Agile Methodology** and used **kanban board** to track the progress of tasks. It is a great tools as it offers very simple way of navigating and tracking the progression of project works. This helps me easily identify if there is any outstanding tasks or bugs or issues to be taken care of.


## The rationale to map the business requirements to the Data Visualisations
* List your business requirements and a rationale to map them to the Data Visualisations
- Customer may mostly pay cash and then debit card.
    - Using Seaborn Bar plot i see that, my hypothsis is partially correct as most used payment option is Cash. But 2nd most used option is credit card not debit bard.

- Customer pay the most for clothing, food & beverage, cosmetics and books
    - Matplotlib Bar Horizontal chart shows that customers mostly pay clothing, but 2nd and 3rd largest are shoes and technology, which is a surprising revelation.
    - Plotly Scatter chart shows that expenditure for clothing and shoes are considerably stable while for technology, I see some picks. From another Plotly Scatter plot, I see that quantity sale of technology product is the lowest. This shows, customers have appeal towards tech products.

- Costomer may shop mostly clothing, food & beverage and cosmetics
    - Matplotlib Bar chart shows that customers mostly shop clothing, ood & beverage and cosmetics. Research output seem to be aligned with my hypothesis.
    - Plotly Scatter chart shows that customers mostly shop clothing. However, though food & beverage and cosmetics are combinedly holding 2nd position in terms of quantity sold, these  products are not among the top three in term of price(or revenue for shop owner).

- 50% of all named shopping malls should have similar performance report
    - Using Seaborn Scatter plot, we see that Kanyon and Mall of Istanbul are competing with each other very closely and their competitor is Metrocity. Rests are far behind. So, I can say that 20% of malls are performing really well. If I am being very generous, I can say it is 30%. So, my hypotheis in this regard is incorrect.
    - Apparently both Plotly Scatter and Bar chart re-emphasize the earlier claim. Since Kanyon and Mall of Istanbul malls have highest quantity sold and price(or revenues), it is kind evident that these malls has more customers than others.

- Younger aged customer may pay more for book, food & beverage & older people may spend more money to clothing, cosmetics and technology
    - From Plotly Box plot, I see that interest across all ages have been around clothing, shoes and technology, whereas rest of the product remained same though price varies. So, my hypotheis is not correct.

- Young people tend to buy more products than older people
    - Seaborn Heat chart is used to see if there is any correlation between age and quantity or price. I see that age factor is not proportionately influencing quantity and no relation exists with price factor. However, there is a very strong positive relation exists between quantity and price, as expected. So, my hypostheis is incorrect.

- Male may pay more for gadgets or technology than female, while female pays more for clothing and cosmetics
    - From Plotly Box plot, I see that both male and female have similar interest in clothing, shoes and technology. So, I can safely say that my hypothesis is partially correct.


## Analysis techniques used
* List the data analysis methods used and explain limitations or alternative approaches.
* How did you structure the data analysis techniques. Justify your response.
* Did the data limit you, and did you use an alternative approach to meet these challenges?
* How did you use generative AI tools to help with ideation, design thinking and code optimisation?

I used descriptive analytics for this project. This dataset doesn't comprise of sufficent amonunt of other data to investigate and isolate the specific reason(s) of such occurance. As an example, from my sample dataset I see that out of 10 shopping mall only two have the highest in sales and customer visit, which is just 20% when I was expecting at least 50% of shopping mall would have similar performance level. So, my hypothesis was not correct. 

To identify the reason, we need more information on the shopping mall, like size, location, facilities, avalability of parking area, accessability, atmosphere, target group, availability of alternatives etc. Unfortunately, these information are not available to conduct a rigourus analysis through diagnostic and predictive analysis. However, this dataset can help visualize the ABC Marketing Company that which shopping mall to target, what offer they can make, what could be their target group and how much impact time of the year has on the sales. However, as mentioned earlier, for better analysis purposes I split Datetime column of the dataset to Month and Year columns. This is to check deviation on sales and customer visit not only on yearly scale but on monthly level too.

I used youtube and other websites to find out how data visualization can be interactive, meaningful and attractive to the audiences. I didn't need to use any generative AI for this project, however, I revisited course content several times as it is hard to recall all the functions and methods.


## Ethical considerations
* Were there any data privacy, bias or fairness issues with the data?
* How did you overcome any legal or societal issues?

Since the data has been collected from Kaggle, a public domain, I am not certain about the biasness or fairness of the data. Again, as the data has been collected from public domain, it is safe to avoid any legal issues. Additionally, dataset doesn't contain any personal data of customers.


## Unfixed Bugs
* Please mention unfixed bugs and why they were not fixed. This section should include shortcomings of the frameworks or technologies used. Although time can be a significant variable to consider, paucity of time and difficulty understanding implementation are not valid reasons to leave bugs unfixed.
* Did you recognise gaps in your knowledge, and how did you address them?
* If applicable, include evidence of feedback received (from peers or instructors) and how it improved your approach or understanding.

I didn't have any major issues except for two. First is, after creating the cleaned sample dataset Datetime column reversed to object format, not sure how and why. However, I changed it back to datetime format and continued the analysis. Second is, when I tried to plotly to check the output, I was getting an error of 'nbformat' missing. So, I installed it but forgot to restart the kernel. So, the problem remained. Later, after having a chat with John, I relized what I forgot to do and fixed it.


## Development Roadmap
* What challenges did you face, and what strategies were used to overcome these challenges?
* What new skills or tools do you plan to learn next based on your project experience? 

I need to spend more time on Machine learning and data visualization. I need to have a good grasp on when and what plot is the best for visualzation. Also, I need to hone my skills in writing functions to better manupulate the data as per requirements.


## Main Data Analysis Libraries
* Here you should list the libraries you used in the project and provide an example(s) of how you used these libraries.

- Pandas
- Numpy
- Matplotlib
- Plotly
- Seaborn
- VS Code
- Jupyter notebook
- Python version - 3.12.8
- Github as repository
- Kanban board as Agile methodology


## Credits 

* In this section, you need to reference where you got your content, media and extra help from. It is common practice to use code from other repositories and tutorials, however, it is important to be very specific about these sources to avoid plagiarism. 
* You can break the credits section up into Content and Media, depending on what you have included in your project. 

- Kaggle - Dataset collection
- Youtube - To get idea how to use color in the graph
- Various websites - How to fix 'nbformat' issue
- LMS - To gather knowledge about what functions and visualization tools to use

### Content 

- The text for the Home page was taken from Wikipedia Article A
- Instructions on how to implement form validation on the Sign-Up page was taken from [Specific YouTube Tutorial](https://www.youtube.com/)
- The icons in the footer were taken from [Font Awesome](https://fontawesome.com/)

### Media

- The photos used on the home and sign-up page are from This Open-Source site
- The images used for the gallery page were taken from this other open-source site



## Acknowledgements (optional)
* Thank the people who provided support through this project.
- John
- Vasi