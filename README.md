## Silver Silence and Golden Speech
### Spoiler Detection in Book Reviews

![spoiler](https://github.com/PsychOpilio/NF_Capstone_Spoiler_Detection/blob/main/spoiler.gif)

This project on spoiler detection in book reviews is in collaboration with [GHabeck](https://github.com/GHabeck); visit his profile for completive material/ models.

Consulting customer reviews to come to a decision whether to buy the crime novel or not and in the process stumbling over the solution that the gardener killed the housemaid  - spoilers are every reader’s nightmare. 
To address this issue and save readers from future spoiler experiences, our project aims at training text classification algorithms to automatically detect plot twists in book reviews. 

The data for this project are available at [UCSD Book Graph](https://sites.google.com/eng.ucsd.edu/ucsdbookgraph/home). 
The dataset contains more than 1.3 million reviews of about 25,000 booky by 19,000 users. Besides the review text with marked spoilers, the dataset includes features on spoiler labels, reviewer ID, book ID, overall book rating and timestamp. Metadata like genre, title, etc. are also available.

Since this is our first NLP project, we set our focus on trying out and getting familiar with different approaches of text preprocessing and text classification, of which only the most promising are uploaded here. Interestingly, ML algorithms like random forests outperformed neural network models.

On the whole, model performances are, at this point, not satisfying yet. At this stage, a balanced random forest trained with whole reviews (as compared with sentence-wise training) in combination with genre metadata produces the best results. 
But we'll keep track and continuously work on model improvements! 

### Table of Contents
[Data Acquisition](https://github.com/PsychOpilio/NF_Capstone_Spoiler_Detection/blob/main/Data.ipynb)

[Standard Preprocessing](https://github.com/PsychOpilio/NF_Capstone_Spoiler_Detection/blob/main/Preprocessing.ipynb)

[Exploratory Data Analysis](https://github.com/PsychOpilio/NF_Capstone_Spoiler_Detection/blob/main/EDA.ipynb)

[Text Preprocessing](models/Text_Preprocessing.ipynb)
