## Silver Silence and Golden Speech
### Spoiler Detection in Book Reviews

![spoiler](https://github.com/PsychOpilio/NF_Capstone_Spoiler_Detection/blob/main/spoiler.gif)

This project on spoiler detection in book reviews is in collaboration with [GHabeck](https://github.com/GHabeck); visit his profile for completive material/ models.

Consulting customer reviews to come to a decision whether to buy the crime novel or not and in the process stumbling over the solution that the gardener killed the housemaid  - spoilers are every reader’s nightmare. 
To address this issue and save readers from future spoiler experiences, our project aims at training text classification algorithms to automatically detect plot twists in book reviews. 

The data for this project are available at [UCSD Book Graph](https://sites.google.com/eng.ucsd.edu/ucsdbookgraph/home). 
The dataset contains more than 1.3 million reviews of about 25,000 booky by 19,000 users. Besides the review text with marked spoilers, the dataset includes features on spoiler labels, reviewer ID, book ID, overall book rating and timestamp. Metadata like genre, title, etc. are also available.

Since this is our first NLP project, we set our focus on trying out and getting familiar with different approaches of text preprocessing and text classification, of which only the most promising are uploaded here. Interestingly, ML algorithms like random forests outperformed neural network models.

On the whole, model performances are, at this point, not satisfying yet.
But we'll keep track and continuously work on model improvements! 

### Table of Contents
[Data Acquisition](https://github.com/PsychOpilio/NF_Capstone_Spoiler_Detection/blob/main/Data.ipynb)

[Standard Preprocessing](https://github.com/PsychOpilio/NF_Capstone_Spoiler_Detection/blob/main/Preprocessing.ipynb)

[Exploratory Data Analysis](https://github.com/PsychOpilio/NF_Capstone_Spoiler_Detection/blob/main/EDA.ipynb)

[Text Preprocessing](models/Text_Preprocessing.ipynb)

[Models (Baseline SGD, ULMFiT, Balanced Random Forest)](models)

### Summary of results

|                                           | review-wise or sentence-wise training? | training data downsampled ? | including metadata?     | overall accuracy | spoiler recall | spoiler precision | non-spoiler recall | non-spoiler precision |
|-------------------------------------------|----------------------------------------|-----------------------------|-------------------------|------------------|----------------|-------------------|--------------------|-----------------------|
| Stochastic Gradient Classifier (Baseline) | review-wise                            | no                          | no                      | .91              | .40            | .36               | .95                | .95                   |
| Stochastic Gradient Classifier (Baseline) | sentence-wise                          | no                          | no                      | .96              | .53            | .39               | .97                | .98                   |
| Stochastic Gradient Classifier            | review-wise                            | yes                         | no                      | .70              | .89            | .65               | .52                | .83                   |
| Stochastic Gradient Classifier            | sentence-wise                          | yes                         | no                      | .84              | .68            | .52               | .87                | .93                   |
| Stochastic Gradient Classifier            | review-wise                            | yes                         | yes (1 feature)         | .76              | .68            | .18               | .77                | .97                   |
| Stochastic Gradient Classifier            | sentence-wise                          | yes                         | yes (1 feature)         | .52              | .72            | .05               | .52                | .98                   |
| Balanced Random Forest                    | review-wise                            | yes                         | no                      | .63              | .95            | .16               | .61                | .99                   |
| Balanced Random Forest                    | sentence-wise                          | yes                         | no                      | .58              | .92            | .07               | .57                | 1.00                  |
| Balanced Random Forest                    | review-wise                            | yes                         | yes (1 feature)         | .82              | .86            | .26               | .81                | .99                   |
| Balanced Random Forest                    | review-wise                            | yes                         | yes (separate features) | .65              | .94            | .16               | .63                | .99                   |
| Balanced Random Forest                    | sentence-wise                          | yes                         | yes (1 feature)         | .96              | .12            | .29               | .99                | .97                   |
| ULMFiT                                    | review-wise                            | no                          | no                      | .07              |                |                   |                    |                       |
