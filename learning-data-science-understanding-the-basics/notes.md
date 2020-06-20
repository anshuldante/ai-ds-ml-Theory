# Data Science Basics

## Tools of the trade

* Hadoop
* Python
* R
* MapReduce: batches
* Apache Spark: realtime

## Usage of the tools

* Storing: Hadoop, Cassandra and PostGreSql
* Scrubbing: Python
* Analyzing: Python and R

## Some good Data-science questions

* What do we know about our customers?
* How can we deliver a better product?
* Why are we better than our competitors?
* What would happen if we left the market?

## Traditional Databases

* Online Transaction Processing (OLTP)
* Real-time data

## Data Warehouse

* Online Analytical Processing (OLAP)

## On an e-comm site

* You want your RDBMS to be fast and efficient since this will be used in real-time by customers.
* A script is run to upload all of the data from a day to the DWH in one shot.
* DWH is optimised for data analysis.
* Let's say you get acquired, the parent company keeps the data of all of their websites in 1 DWH.
* They'll have to do an ETL (extract, transform and load) to upload your data into their DWH.
* They'll pull all of the data from your site, have a data analyst transform the data to match their schema
   and then load it into their DWH.
* Many companies see Hadoop as a replacement for their DWH, they'll change the ETL scripts to load the data from WFH to Hadoop.
* The driver here is that Hadoop clusters are much cheaper than DWH.

## RDBMS Challenges

* Aren't very flexible
* Require schema
* Require planning and knowledge of the data in advance.
* Data formats are a challenge.
* Requires relations as well.

## NoSQL DBs are supposed to have the following properties

* Non-relational
* Schema-less
* Cluster-friendly
* Open-source
* *Hadoop is built on HBase which is an open-source NOSQL DB.*
* *Big data PROBLEM, with the emphasis on the problems with managing a lot of data.*

## The 4 Vs

* Volume: pretty simple to answer: if you're collecting PetaBytes of data each day, you've qualified for big data.
* Variety: somewhat trickier:
  * Stock exchanges have a lot of data, they have velocity and volume, but no variety, no Big data.
  * The best example is: auto-driving cars: having to process video, audio, maps and other related data to be able to drive safely.
* Velocity
* Veracity
* **For a data related problem to be classified as a Big Data PROBLEM, it should have all 4 Vs.**

## Types of Data

  1. Structured: follows a specific format and a specific order (Data model): Cheap, inflexible and requires a lot of design.
      * Spread-sheet.
  2. Semi-structured: address stored in your DB and the carrier's DB, the field values will be same but the names will differ.
  3. Un-Structured: some analysts think that 80% of one's data is un-structured. Images, videos, audio, various text doc formats.
     Can be used to get various insights about the customers and send them better promotions, incentivize customers that refer a lot of their friends.

## Cleaning up data

* Arguments to keep all data:
  * Hard to know what you'll need later
  * Cheaper to just keep all Data
  * Time consuming to delete.
* Arguments to delete data:
  * Important to deal with the garbage: the more garbage data you have the harder it gets to get interesting results.
  * Harder get get better insights: the garbage data is called Noise.
* Comparison:
  * No right answer here
  * The DS team just has to find what works for them.
  * More data means more noise and more filtering required and more time spent on analysing data.
  * Throwing away means cleaner data but time spent on cleaning it and there is a chance that you'll throw away somewhat useful data
    that you might regret throwing away in the future.
  * Making a decision is important and make it early, changing the policy every now and then is not a great idea.

## Applying statistics to data

* Shouldn't always believe statistics, in the end, it is like story telling, could have facts, fiction and fantasy.
* Eg. politics: 1 guy says the average voter income has gone up by 5000 in the last 4 years,
  the other guys says average middle-class family income has gone down by 10000.
  The first guy took the mean of all voter incomes. The second guy is talking about the median of all families.
  The first stat is not that great, because the income could've been taken up by the wealthiest.
  But since the number of families hasn't really changed, the median shouldn't change either.

## Probability practical usage: an analysis done by a biotech company to find out the reasons for people not participating in a clinical trial

* 20% less likely if needles or blood tests are required.
* 30% less likely, if they have to fast the night before.
  * Q1. Blood tests are 10% more accurate but blood tests mean fewer participants.
  * Q2. Would it be better to have blood or saliva tests seeing that having blood tests means fewer tests: more people mean more results,
      so better to take saliva tests.
  * Q3. Would it be better to take more samples and do multiple tests for the same participant, since that gets you more accurate results?
    **Result**: Would've been best to take the test which gets you the max number of participants and then run multiple test for the less accurate ones.
* *Probability leads to some unexpected places: who would've thought that the less accurate test would lead to better results.*
* *It can be a great vehicle for new interesting questions: thinking about more tests for the less accurate results.*
* *Don't be discouraged for running into more questions after answering some.*

## Correlation: recommendations**

* Measuring the degree to which 2 things are related.
* Usually between 0 and 1.
* 1 = strongly correlated. Eg height and weight, temp and ice-cream.
* 0 = Negative correlation. Eg. Car weight and mileage, for a runner: speed and going uphill.
* -1 = inverse correlation.
* Positive and negative both are a great way to show relationships.
* Correlation Coefficient: DS teams looked into LinkedId data to find acquaintances
  * Same school
  * Jobs shared
  * Groups or interests shared.
    * Eg. You're looking for a job and another guy from your company is doing the same,
      Since they know that you're both looking out and where you work, that's enough to make a correlation.
      And to suggest a connection.
  * Connections of connections with the same skills.
  * More likely to be connected to people who work in the same building, or with the same skills.
  * More similar interests: more likely-hood of you knowing the person.
  * Correlation can also hep question the assumptions:
    * Eg. The people who spend the most may not be your happiest customers.
         They may have unrealistic expectations and may be more likely to switch or leave negative feedback.
    * You might find ways to get your happiest customers to spend more.
    * Or find ways to make high-spenders happier to get them so stay.
* In general, correlation doesn't imply causation.
* There may be a third factor which is impacting the correlation.
* Eg. Someone's grand parents live in a old age retirement community., the mortality rate and percentage there is very high.
  * So a correlation can be that the community is a very dangerous one. But the real reason here is the average age of the community
  * And it's a normal happy community, this is one instance where correlation doesn't mean causation.
* Say the DS team finds that the sales go much higher in January, they meet-up to find the cause:
  * Questions: More money, why would people run more in cold weather, new year resolutions, new customers, kinds of shoes.
  * Reports tell that most of these are new customers, buying expensive shoes.
  * Effect: the team sells Gift Cards in December this year, send promotions to last year's new customers.
  * But it made almost no difference in the sales, so they went back to look into more reports.
  * The reports concluded that these were new customers and new runners.
  * They asked a new question: are these new customers trying out running to get in shape.
  * The new promo next year was more around new year's resolutions, telling people to keep running, sending running guides and fitness trackers.
  * Spurious correlation is essentially fake relation.
  * The best way to avoid spurious correlation is to use the scientific method and ask good questions.

## Predictive analysis**

* Using data analytics to predict the future, very closely associated with DS,
  sometimes even used interchangeably, but PA is just one more technique.
* The more data you have, the more powerful and accurate your predictive analytics will be.
* The quality of analysis also depends on how well your DS team has analysed your data.

## Challenges**

* *Building monuments of data waiting for the results to come.*
* *Orgs focus on capabilities and spend a lot of money on hardware and stuff and then have nothing left for the DS team.*
* *DS teams are exploratory, data is not the product, just the means to get analytics and there's no prize to having the biggest data clusters.*
  * Having a chef knife doesn't make you a chef. The DS team can often get more done with multiple ope-source tools than a paid single one.
* *A good DS team will be very messy, they'll use various different tools to collect and scrub data.*
* *Invest in training and expertise not in the hardware.*
