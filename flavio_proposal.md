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

When the author writes a text, it is expected that his words will reach a reasonable number of readers, and will influence and bring value to the readers. During the creation of the content, the title is one of the important details that needs to be taken in consideration, because it will normally the first contact the reader will probably have with the article. Thus, to create a good first impression, try to have more people reading the article and interacting with it, choosing a good title is very important.

Some of the most used platforms to spread ideas nowadays are Twitter [6] and Medium [7]. On the first one, normally is posted external urls with its tile, where the users can access and demonstrate its satisfaction with "Likes" or "Retweeting" (shares) the original post. The second one, there is the full content with tags to classify the article and "Applause" (similar to Twitter "Likes") to show the user appretiated the content. And a correlation between these two networks can bring us more valuable information.

The problem to be solved: Predict the number of likes and shares an article receives based on its title; and analyse how the title length and the categories tags had performed.


### Datasets and Inputs
_(approx. 2-3 paragraphs)_

The data used to predict how titles will perform was gathered from the accounts of the non-profit organization FreeCodeCamp on Medium [8] and Twitter [9]. With both social platforms, we could get public information about how the users interacted with the content, such as "Likes" and "Retweets" from Twitter, and "Applause" and categories tags from Medium. 

The reason to correlate the number of "Likes" and "Retweets" from Twitter with a Medium article, was to try to isolate the effect of number of reached readers and number of Medium "Applauses". Because the more the article is shared in different platforms, the more readers it will reach and the more Medium "Applauses" it will receive. Using only the Twitter statistic, it is expected that the articles reached initially almost the same number of readers (that are the followers of the FreeCodeCamp account on Twitter), and the performance and subsequent interactions with the article are limited to other variables like the title of the article, that is exactly what we want to measure.

It was decided to choose FreeCodeCamp account, because we wanted to limit the scope of the subject of the articles and predict better the response on a specif field. The same title can perform well on one category (e.g. Technology), but not necessarly on a different one (e.g. Culinary). Also this account posts as the Tweet content the title of the original article and the url on Medium. 

After getting the articles from FreeCodeCamp written on Medium and shared on Twitter, we reachead a dataset of 719 datapoints. Here are some examples of such correlation:

| Title | Retweet Count | Favorite Count | Medium Hearts | Medium Categories  | Created at | URL |
| --- | --- | --- | --- | --- | --- | --- |
| ES9: JavaScript's state of the art in 2018 | 15 | 48| 618 | Technology, Programming, Tech, Startup, JavaScript | 2018-07-23 17:02:04 | https://medium.freecodecamp.org/es9-javascripts-state-of-art-in-2018-9a350643f29c |
| Here's another way to think about state: How to visually design state in JavaScript | 10 | 30 | 2 | JavaScript, Statecharts, Programming, React, Technology | 2018-07-24 17:02:00 | https://medium.freecodecamp.org/how-to-visually-design-state-in-javascript-3a6a1aadab2b |
| How to understand Gradient Descent, the most popular ML algorithm | 4 | 14 | 102 | Machine Learning, Artificial Intelligence, Data Science, Mathematics, Tech | https://medium.freecodecamp.org/understanding-gradient-descent-the-most-popular-ml-algorithm-a66c0d97307f |


Description:
"retweet_count":
"favorite_count":
"title":
"url":
"mediumHearts":
"mediumCategories":
length: 


### Solution Statement
_(approx. 1 paragraph)_

In this section, clearly describe a solution to the problem. The solution should be applicable to the project domain and appropriate for the dataset(s) or input(s) given. Additionally, describe the solution thoroughly such that it is clear that the solution is quantifiable (the solution can be expressed in mathematical or logical terms) , measurable (the solution can be measured by some metric and clearly observed), and replicable (the solution can be reproduced and occurs more than once).

### Benchmark Model
_(approximately 1-2 paragraphs)_

In this section, provide the details for a benchmark model or result that relates to the domain, problem statement, and intended solution. Ideally, the benchmark model or result contextualizes existing methods or known information in the domain and problem given, which could then be objectively compared to the solution. Describe how the benchmark model or result is measurable (can be measured by some metric and clearly observed) with thorough detail.

### Evaluation Metrics
_(approx. 1-2 paragraphs)_

In this section, propose at least one evaluation metric that can be used to quantify the performance of both the benchmark model and the solution model. The evaluation metric(s) you propose should be appropriate given the context of the data, the problem statement, and the intended solution. Describe how the evaluation metric(s) are derived and provide an example of their mathematical representations (if applicable). Complex evaluation metrics should be clearly defined and quantifiable (can be expressed in mathematical or logical terms).

### Project Design
_(approx. 1 page)_

In this final section, summarize a theoretical workflow for approaching a solution given the problem. Provide thorough discussion for what strategies you may consider employing, what analysis of the data might be required before being used, or which algorithms will be considered for your implementation. The workflow and discussion that you provide should align with the qualities of the previous sections. Additionally, you are encouraged to include small visualizations, pseudocode, or diagrams to aid in describing the project design, but it is not required. The discussion should clearly outline your intended workflow of the capstone project.

### References

[1] eMarketer Report. (2017). US Time Spent with Media: eMarketer’s Updated Estimates for 2017. Accessed 9 Aug. 2018. Available at: https://www.emarketer.com/Report/US-Time-Spent-with-Media-eMarketers-Updated-Estimates-2017/2002142

[2] Common Sense Media. (2015). The Common Sense Census: Media Use by Tweens and Teens. Accessed 9 Aug. 2018. Available at: https://www.commonsensemedia.org/research/the-common-sense-census-media-use-by-tweens-and-teens

[3] Lindgaard, Gitte & Fernandes, Gary & Dudek, Cathy & M. Brown, Judith. (2006). Attention web designers: You have 50 milliseconds to make a good first impression! Behaviour and Information Technology, 25(2), 115-126. Behaviour & IT. 25. 115-126. 10.1080/01449290500330448. 

[4] Shearer, E., Gottfried, J. (2017). News use across social media platforms 2017. Accessed 9 Aug. 2018. Available at: http://www.journalism.org/2017/09/07/news-use-across-social-media-platforms-2017/ 

[5] Missing reference

[6] 

[7] 

[8] 

[9] 

[10] Missing reference

-----------

**Before submitting your proposal, ask yourself. . .**

- Does the proposal you have written follow a well-organized structure similar to that of the project template?
- Is each section (particularly **Solution Statement** and **Project Design**) written in a clear, concise and specific fashion? Are there any ambiguous terms or phrases that need clarification?
- Would the intended audience of your project be able to understand your proposal?
- Have you properly proofread your proposal to assure there are minimal grammatical and spelling mistakes?
- Are all the resources used for this project correctly cited and referenced?

{ "id": 1026876138969333800, "retweet_count": 5, "favorite_count": 10, "text": "How to use JSON padding (and other options) to bypass the Same Origin Policy", "created_at": "2018-08-07 17:02:04", "url": "https://medium.freecodecamp.org/use-jsonp-and-other-alternatives-to-bypass-the-same-origin-policy-17114a5f2016", "mediumHearts": 177, "mediumCategories": ["JavaScript", "HTML", "Web Development", "Tutorial", "Technology"] },
