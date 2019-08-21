<img src="https://bit.ly/2VnXWr2" alt="Ironhack Logo" width="100"/>

# Please archive the emails for me
*Chao-Ting, Chang*

*[Data Analytics, Barcelona & June 2019]*

## Content
- [Project Description](#project-description)
- [Hypotheses / Questions](#hypotheses-/-questions)
- [Dataset](#dataset)
- [Cleaning](#cleaning)
- [Analysis](#analysis)
- [Model Training and Evaluation](#model-training-and-evaluation)
- [Conclusion](#conclusion)
- [Future Work](#future-work)
- [Links](#links)

<a name="project-description"></a>

## Project Description
This project aims to do an automatic income email detection, cleaning and classification. The application of this project is to reduce the time for customer service agents when companies receive emails from clients.  

The detection part includes to detect the email language. The cleaning part aims to do the text cleaning, email content cleaning, the email title (receiver, date and time, etc) cleaning or even email translation. The classification part is focused on transfering the text into different array (Tfidf), testing different machine learning methods and hyperparameter tunning. 

<a name="hypotheses-/-questions"></a>

## Hypotheses / Questions
* Can I classify my email using NLP? Does only using title is good enough to predict?  

<a name="dataset"></a>

## Dataset
* Personal gmail: As I can't find a proper email dataset, I am going to use my emails from gmail to see if I can do something.

<a name="cleaning"></a>

## Cleaning
* **Title/Label Etraction:** The gmail file is as mbox type, which is a mixture of html and encoded text. One of the main challenge in this project is to clean the email as the format I want. However, as it is really too complicated to finish the cleaning in short time, I decided to only extract the title and gmail pre-defined label.  
* **Title/Label Cleaning:** After the extraction of email titles and labels, the next thing is to clean the encoded text. As my gmail contains emails in Chinese, English and Spanish (and few in Franch and other languages), I decided to only choose English and Spanish emails and clean the garbled code.  


<a name="analysis"></a>

## Analysis  
After cleaning and group the emails, I found out that 80% of them are just classified as income emails, which is useless for me. Therefore I'd use unsupervised learning to cluster my emails using different methods. The methods I used is as followed:
* **Vectorizer:** CountVectorizer, TfidfVectorizer, Word2Vec
* **Unsupervised learning:** Kmean, DBSCAN
* **Semisupervised learning**

<a name="model-training-and-evaluation"></a>

## Model Training and Evaluation
As I am using unsupervised learning, it is difficult to tell which model performs better. It seems that by using Kmean and Countvectorizer, the given clusters are more sepearted and reasonable. Besides, by looking at the silhouette score, we can tell that the clusters are overlapping. In the other word, the clusters are not clearly separated. From the result of DBSCAN with different minimum sample size, we know that it seems that my emails can be separated into two or three groupds.


<a name="conclusion"></a>

## Conclusion
* Summarize your results. What do they mean?
* What can you say about your hypotheses?
* Interpret your findings in terms of the human-understandable question you try to answer.

<a name="future-work"></a>

## Future Work
Address any questions you were unable to answer, or any next steps or future extensions to your project.

<a name="workflow"></a>


## Links
Include the links to your repository, slides and trello. Feel free to include any other links associated to your project. 

[Repository](https://github.com/ChaotingChang/Project-Week-8-Final-Project)  
[Slides](https://docs.google.com/presentation/d/1_31WyJRuZVAzHJ3LNYqA1qXgcb4BPY4LoYQ3RQYOI2A/edit#slide=id.p1)  
[Trello](https://trello.com/invite/b/tmDxpkjY/9a2f4ce2fa925dd477db7fdca7ae0bf5/projecweek8finalproject)  
