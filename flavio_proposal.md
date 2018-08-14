# Machine Learning Engineer Nanodegree
## Capstone Proposal
Flávio Henrique de Freitas  
September 15th, 2018

## Proposal
_(approx. 2-3 pages)_

### Domain Background
_(approx. 1-2 paragraphs)_

Social networks websites have become an important communication tool and source of information. The hours spent in average connected per day in the past years is up to 6 hours [1] for adults and 9 for teenagers, while 30% of this time is on social networks [2]. During a normal navigation on such platforms, users are exposed to several posts such as friends' statuses, images, news and more. With such amount of information and variety of content, the time for the user to decide to interact with the content is very small. Gitte at al. [3] suggest that we take around 50 milliseconds to make a good first impression and this has proved to be very powerful in a wide range of contexts.

Besides being a place for connecting with friends and sharing moments of the user's life, a survey has shown that social networks are also used as a source of news and information by 67% of the users [4]. 80% of the articles are read inside the platform and 20% are read on an external site [5]. Part of these posts are articles that can be read on an external website. Typically such posts show the title of the article and sometimes a small part of its content and an image.

Considering the offer of content and competition with so many interesting posts, showing a proper title for the post affects the probability that a user will check the content. This measure has a strong impact on how many readers an article will have and how much of the content will be read. Furthermore, showing the user a content they prefer (to interact) increases the user satisfaction. It is thus important to accurately estimate the interaction rate of articles based on its title.

### Problem Statement
_(approx. 1 paragraph)_

When an author writes a text, it is expected that their words will spread, influence and bring value to the readers. While writing, the title is one of the important details that needs to be taken in consideration, because normally this will the first contact place of their work. Thus, to create a good first impression, try to have more people to read the article and interact with it, choosing a good title is very important.

Some of the most used platforms to spread ideas nowadays are Twitter [6] and Medium [7]. On the first one, normally are posted external urls with its title, where the users can access and demonstrate its satisfaction with "Likes" or "Retweeting" (shares) of the original tweet. The second one has the full text with tags to classify the article and "Applause" (similar to Twitter "Likes") to show how much the users appretiated the content. A correlation between these two networks can bring us more valuable information.

The problem to be solved: Predict the number of likes and shares an article receives based on its title; and analyse how the title length and the categories tags had performed.

### Datasets and Inputs
_(approx. 2-3 paragraphs)_

The data used to predict how titles will perform was gathered from the accounts of the non-profit organization FreeCodeCamp on Medium [8] and Twitter [9]. With both social platforms, it was possible to get public information about how the users interacted with the content, such as "Likes" and "Retweets" from Twitter, and "Applause" from Medium.

The reason to correlate the number of "Likes" and "Retweets" from Twitter with a Medium article, was to try to isolate the effect of number of reached readers and number of Medium "Applauses". Because the more the article is shared in different platforms, the more readers it will reach and the more Medium "Applauses" it will receive. Using only the Twitter statistic, it is expected that the articles reached initially almost the same number of readers (that are the followers of the FreeCodeCamp account on Twitter), and the performance and interactions with it are limited to the characteristics of the tweet, for example, the title of the article, that is exactly what I want to measure.

It was decided to choose FreeCodeCamp account, because the idea is to limit the scope of the subject of the articles and predict better the response on a specif field. The same title can perform well on one category (e.g. Technology), but not necessarly on a different one (e.g. Culinary). Also this account posts as the Tweet content the title of the original article and the URL on Medium.

After getting the articles from FreeCodeCamp written on Medium and shared on Twitter, I reachead a dataset of 719 datapoints. Here are some examples of such correlation:

| Title | Retweet Count | Favorite Count | Medium Hearts | Medium Categories  | Created at | URL |
| --- | --- | --- | --- | --- | --- | --- |
| ES9: JavaScript's state of the art in 2018 | 15 | 48 | 618 | Technology, Programming, Tech, Startup, JavaScript | 2018-07-23 17:02:04 | https://medium.freecodecamp.org/es9-javascripts-state-of-art-in-2018-9a350643f29c |
| Here's another way to think about state: How to visually design state in JavaScript | 10 | 30 | 2 | JavaScript, Statecharts, Programming, React, Technology | 2018-07-24 17:02:00 | https://medium.freecodecamp.org/how-to-visually-design-state-in-javascript-3a6a1aadab2b |
| How to understand Gradient Descent, the most popular ML algorithm | 4 | 14 | 102 | Machine Learning, Artificial Intelligence, Data Science, Mathematics, Tech | 2018-07-24 16:01:18 | https://medium.freecodecamp.org/understanding-gradient-descent-the-most-popular-ml-algorithm-a66c0d97307f |


Description of the dataset fields:

| Field | Description | 
| --- | --- |
| Title | The content of the tweet, FreeCodeCamp normally uses the title of the article from Medium and sometimes the username of the author from Twitter |
| Retweet Count | How many times that tweet was "Retweeted" on Twitter |
| Favorite Count | How many times that tweet was marked as favorite on Twitter |
| Medium Hearts | How many times that article was marked as favorite on Medium |
| Medium Categories | Which tags were used to tag the article on Medium |
| Created at | When the tweet was posted |
| URL | The url of the article on Medium |


### Solution Statement
_(approx. 1 paragraph)_

To try to predict the number of shares and likes of an article, we will define the problem as a classification system. Where the words of the title will be tokens t1, t2, ... tn and the range of the likes and shares will be the output of this classification. We will use algorithms such as Support Vector Machines (SVM), Decision Trees, Gaussian Naive Bayes (GaussianNB), K-Nearest Neighbors and Logistic Regression.

To implement this solution we will use Numpy and Scikit running on default hyperparameters.


### Benchmark Model
_(approximately 1-2 paragraphs)_

To reach a better solution, we will test several supervised algorithms and compare the performance between them.  


### Evaluation Metrics
_(approx. 1-2 paragraphs)_

The benchmark model and solution model will be evaluated, when appropriate, with the F1, accurancy and precision scores.

 - F1 score
 - Accurancy Score
 - Precision Score


### Project Design
_(approx. 1 page)_

The general sequence of steps are as follows:
describe the same as here: https://github.com/flaviohenriquecbc/machine-learning-student-intervention/blob/master/student_intervention.ipynb
a. 
b. 
c.
d.
e.
f.


### References

[1] eMarketer Report. (2017). US Time Spent with Media: eMarketer’s Updated Estimates for 2017. Accessed 9 Aug. 2018. Available at: https://www.emarketer.com/Report/US-Time-Spent-with-Media-eMarketers-Updated-Estimates-2017/2002142

[2] Common Sense Media. (2015). The Common Sense Census: Media Use by Tweens and Teens. Accessed 9 Aug. 2018. Available at: https://www.commonsensemedia.org/research/the-common-sense-census-media-use-by-tweens-and-teens

[3] Lindgaard, Gitte & Fernandes, Gary & Dudek, Cathy & M. Brown, Judith. (2006). Attention web designers: You have 50 milliseconds to make a good first impression! Behaviour and Information Technology, 25(2), 115-126. Behaviour & IT. 25. 115-126. 10.1080/01449290500330448. 

[4] Shearer, E., Gottfried, J. (2017). News use across social media platforms 2017. Accessed 9 Aug. 2018. Available at: http://www.journalism.org/2017/09/07/news-use-across-social-media-platforms-2017/ 

[5] Missing reference

[6] Twitter. Accessed 13 Aug. 2018. Available at: https://www.twitter.com

[7] Medium. Accessed 13 Aug. 2018. Available at: https://www.medium.com

[8] freecodecamp. Accessed 13 Aug. 2018. Available at: https://medium.freecodecamp.org/

[9] freecodecamp.org. Accessed 13 Aug. 2018. Available at: https://twitter.com/freecodecamp

[10] Missing reference

-----------

**Before submitting your proposal, ask yourself. . .**

- Does the proposal you have written follow a well-organized structure similar to that of the project template?
- Is each section (particularly **Solution Statement** and **Project Design**) written in a clear, concise and specific fashion? Are there any ambiguous terms or phrases that need clarification?
- Would the intended audience of your project be able to understand your proposal?
- Have you properly proofread your proposal to assure there are minimal grammatical and spelling mistakes?
- Are all the resources used for this project correctly cited and referenced?

{ "id": 1026876138969333800, "retweet_count": 5, "favorite_count": 10, "text": "How to use JSON padding (and other options) to bypass the Same Origin Policy", "created_at": "2018-08-07 17:02:04", "url": "https://medium.freecodecamp.org/use-jsonp-and-other-alternatives-to-bypass-the-same-origin-policy-17114a5f2016", "mediumHearts": 177, "mediumCategories": ["JavaScript", "HTML", "Web Development", "Tutorial", "Technology"] },
