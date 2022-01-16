# Overview
In this analysis, the goal was to figure out if there is a bias in Amazon product reviews between Vine reviews and non-Vine reviews. Vine is a program run by Amazon in which certain Amazon customers are selected to try products and post reviews about the product. Vine users recieve free products in exchange for their review. The service is designed to help product sellers build product awareness and boost sales. Specifically, I was interested in whether Vine reviewers give a higher proportion of 5-star reviews. Given the size of Amazon product review data sets, I loaded the data set into Google Colab and performed the analysis with Apache Pyspark. For more detail on how the analysis was performed, take a look at at the Vine_Review_Analysis.ipynb file in this repository. Lastly, it should be noted that there are numerous product categories that could be used for this analysis, but for this analysis our data contained musical instrument products.

# Analysis</br>

#### Preparation
Before taking a look at the results, let's take a look at how we filtered the original data set to fit our needs. The first step was to select only the data pieces that we were interested in. Below is a screenshot of what the original data frame looked like. </br></br>

![Screen Shot 2022-01-16 at 10 47 12 AM](https://user-images.githubusercontent.com/90878911/149669393-15ff4525-b0e8-437b-bdc4-0bc7bc380700.png)</br></br>

From here, I wanted to make sure that the reviews I was looking at were quality reviews. When a review is posted on Amazon, there is an option for other users to vote whether or not they thought the review was helpful. So, I filtered the initial data frame to only include products that had 20 or more votes AND 50% or more of those were "helpful" votes. Finally, I split that data frame into two data frames: one that included Vine reviews only, and another that included non-Vine reviews only. Here are those data frames. </br>

![Screen Shot 2022-01-16 at 11 01 40 AM](https://user-images.githubusercontent.com/90878911/149669970-de427c78-4feb-42c8-94c4-62dc096e66c8.png) ![Screen Shot 2022-01-16 at 11 02 06 AM](https://user-images.githubusercontent.com/90878911/149670030-2c75dc4e-47a9-4346-a847-c4f3077b9906.png)</br>

#### Results

![Screen Shot 2022-01-16 at 11 25 24 AM](https://user-images.githubusercontent.com/90878911/149670858-9f9bbbfa-12eb-4c84-a7c7-a243044eeece.png)</br></br>

# Summary

The results show almost no difference in the proportion of 5-star reviews between Vine reviewers and non-Vine reviewers. This bodes well for both Amazon, the customer, and the company supplying the products. Amazon can feel confident that their Vine reviewers are being objective in their assessments despite getting the product for free, customers can feel confident that Vine reviewers aren't artificially inflating or deflating product reviews compared to paying customers, and the companies who make the products can feel confident that they are getting exposure without misrepresenting the quality or usefulness of their product. 

While this anlaysis is useful, there is a lot of room for further analysis. For example, a two-sample t-test would be a great way to evaluate whether there is a statistically significant difference between mean star rating of Vine reviewers and non-Vine reviewers. Additionally, there are a number of review data sets that span numerous product categories. This analysis could be performance across multiple categories established findings that are more broadly applicable.




