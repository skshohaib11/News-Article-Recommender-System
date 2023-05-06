# Recommendation of news articles or blog post to users
Design a recommendation system that can suggest personalized news articles or blog posts to users based on their reading history and interests. The system should be able to learn and adapt to the user's preferences over time and provide relevant and engaging content.

## What is Recommendation system?
Recommendation systems are built to predict what users might like, especially when there are lots of choices available. They can explicitly offer those recommendations to users (e.g., Amazon or Netflix, the classic examples), or they might work behind the scenes to choose which content to surface without giving the user a choice.

Why Recommendation system?
 * Benefits users in finding items of their interest.
 * Help item providers in delivering their items to the right user.
 * Identity products that are most relevant to users.
 *Personalized content.

Help websites to improve user engagement.

## Types of Recommendation Systems.
* Popularity-Based Recommendation 
* Classification Mode Based Recommendation 
* Content-Based Recommendation
* Collaborative Filtering

## 1. Popularity-Based Recommendation:
#### It is a type of recommendation system which works on the principle of popularity and or anything which is in trend. These systems check about the product or movie which are in trend or are most popular among the users and directly recommend those.
  
  #### Merits of popularity based recommendation system:
  * It does not suffer from cold start problems which means on day 1 of the business also it can recommend products on various different filters.
  * There is no need for the user's historical data.

  #### Demerits of popularity based recommendation system:
  * Not personalized. 
  * The system would recommend the same sort of products/movies which are solely based upon popularity to every other user.
  
  #### Example:
  * Google News: News filtered by trending and most popular news.
  * YouTube: Trending videos.
  
## 2. Classification Mode Based Recommendation:
  #### The model that uses features of both products as well as users to predict whether a user will like a product or not.
  ![image](https://user-images.githubusercontent.com/113972606/236634342-ffbada4e-59f3-4592-bc70-6dbee5ac0334.png)
  #### The output can be either 0 or 1. If the user likes it then 1 and vice-versa.
  
  #### Limitations of Classification Mode Based Recommendation:
   * It is a rigorous task to collect a high volume of information about different users and also products.
   * Also, if the collection is done then also it can be difficult to classify. 
   * Flexibility issue.
 
## 3. Content-Based Recommendation System
  #### It is another type of recommendation system which works on the principle of similar content. If a user is watching a movie, then the system will check      about other movies of similar content or the same genre of the movie the user is watching. There are various fundamentals attributes that are used to compute the similarity while checking about similar content. 

 To explain more about how exactly the system works, an example is stated below: 
 ![image](https://user-images.githubusercontent.com/113972606/236634548-f4eff44f-fdd7-4a36-86db-a15f8b92a4a7.png)
Figure 1 image shows the different models of one plus phone. If a person is looking for one plus 7 mobile then, one plus 7T and one plus  7 Pro is recommended to the user. 

#### But how is it recommended? 
  To check the similarity between the products or mobile phone in this example, the system computes distances between them. One plus 7 and One plus 7T both have 8Gb ram and 48MP primary camera. 
#### If the similarity is to be checked between both the products, Euclidean distance is calculated. Here, distance is calculated based on ram and camera;
![image](https://user-images.githubusercontent.com/113972606/236634623-48df411d-f0e5-4cc0-b4f2-b4511cbdb90a.png)
![image](https://user-images.githubusercontent.com/113972606/236634632-94b62ca5-7c4d-4520-a025-760cd2d62466.png)
* Euclidean distance between (7T,7) is 0 whereas Euclidean distance between (7pro,7) is 4 which means one plus 7 and one plus 7T have similarities in them whereas one plus 7Pro and 7 are not similar products. 
* In order to explain the concept through this example, only the basic thing (camera and ram) was taken but there is no restriction. We can compute distance calculation for any of the features of the product. The basic principle remains the same if the distance between both is 0, they are likely to have similar content.
* There are different scenarios where we need to check about the similarities, so there are different metrics to be used. For computing the similarity between numeric data, Euclidean distance is used, for textual data, cosine similarity is calculated and for categorical data, Jaccard similarity is computed.

#### Cosine Similarity: Cosine of the angle between the two vectors of the item, vectors of A and B is calculated for imputing similarity. If the vectors are closer, then small will be the angle and large will be the cosine. 
![image](https://user-images.githubusercontent.com/113972606/236634696-2ac37003-327b-4980-9581-8cd37e8b0f70.png)

#### Jaccard Similarity: Users who have rated item A and B divided by the total number of users who have rated either A or B gives us the similarity. It is used for comparing the similarity. 
![image](https://user-images.githubusercontent.com/113972606/236634762-24a251f8-baa5-413f-ad58-35047e9f06ca.png)

#### Merits:
  * There is no requirement for much of the user’s data.
  * We just need item data that enable us to start giving recommendations to users.
  * A content-based recommender engine does not depend on the user’s data, so even if a new user comes in, we can recommend the user as long as we have the user       data to build his profile.
  * It does not suffer from a cold start.

#### Demerits:
 *  Items data should be in good volume.
 * Features should be available to compute the similarity.
 
## 3. Collaborative Filtering:
#### It is considered to be one of the very smart recommender systems that work on the similarity between different users and also items that are widely used as an e-commerce website and also online movie websites. It checks about the taste of similar users and does recommendations. 
#### The similarity is not restricted to the taste of the user moreover there can be consideration of similarity between different items also. The system will give more efficient recommendations if we have a large volume of information about users and items.
![image](https://user-images.githubusercontent.com/113972606/236634911-f2b18dbb-dd99-4610-a389-b42e16781ed7.png)
Figure 2 shows the two different users and their interests along with the similarity between the taste of both the users. It is found that both Jil and Megan have similar tastes so Jill's interest is recommended to Megan and vice versa. 
This is the way collaborative filtering works. Mainly, there are two approaches used in collaborative filtering stated below;
#### a) User-based nearest-neighbor collaborative filtering:
![image](https://user-images.githubusercontent.com/113972606/236634976-3376d359-2280-4f1e-8183-67d1a0292b60.png)
Figure 3 shows user-user collaborative filtering where there are three users A, B and C respectively and their interest in fruit. The system finds out the users who have the same sort of taste of purchasing products and similarity between users is computed based upon the purchase behavior. User A and User C are similar because they have purchased similar products.
#### b) Item-based nearest-neighbor collaborative filtering:
![image](https://user-images.githubusercontent.com/113972606/236635035-5b32a09e-9d91-4500-9033-82d2641fd5ce.png)
Figure 4 shows user X, Y, and Z respectively. The system checks the items that are similar to the items the user bought. The similarity between different items is computed based on the items and not the users for the prediction. Users X and Y both purchased items A and B so they are found to have similar tastes.

#### Limitations
  * Enough users required to find a match. To overcome such cold start problems, often hybrid approaches are made use of between CF and Content-based matching.
  * Even if there are many users and many items that are to be recommended often, problems can arise of user and rating matrix to be sparse and will become challenging to find out about the users who have rated the same item.
  * The problem in recommending items to the user due to sparsity problems.
  



 
