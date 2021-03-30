# HiddenMarkovModel

# Project 2:  Hidden Markov Model 

## Probabilistic states and transitions
1. Set up a new git repository in your GitHub account
2. Pick a text corpus dataset such as
https://www.kaggle.com/kingburrito666/shakespeare-plays
or from https://github.com/niderhoff/nlp-datasets
3. Choose a programming language (Python, C/C++, Java)
4. Formulate ideas on how machine learning can be used to learn word correlations and distributions within the dataset
5. Build a Hidden Markov Model to be able to programmatically
1. Generate new text from the text corpus
2. Perform text prediction given a sequence of words
6. Document your process and results
7. Commit your source code, documentation and other supporting files to the git repository in GitHub GRAPHICAL MODELS
---
# Data:
- link to download data: https://www.kaggle.com/therohk/examine-the-examiner?select=examiner-date-tokens.csv
- The Examiner - Spam Clickbait Catalog
- 6 Years of Crowd Sourced Journalism
- This dataset contains the headlines of 3.08 million Articles written by ~21000 authors over six years.
While the Examiner was never praised for its quality, it consistently churned out 1000s of articles per day over several years.
At their height in 2011, The Examiner was ranked highly in search results and had enormous shares on social media.
At a certain point, it was the tenth largest site on mobile and was attracting twenty million unique visitors a month.
As a platform driven towards advert revenue, most of their content was rushed, unsourced and factually sparse.
It still manages to paint a colourful picture about the trending topics over a long period of time.

---

## Step-1 Setup environment
## Step-2 Importing NEWS headlines data to dataframe
## Step-3 Pre-processing data
### Building stop words library 
- which are a collection of english that which are too common and would affect our model as these words are mostly repeated in sentences, they have higher probabilities and lesser meaning while we generate new text, also there are risks of infinite looping during text generation such as in my case I faced this: `King of King of King of King of` 
### Processing each line of headlines data
- We need to remove all the special characters
- Convert to lower case
- then we remove the stop words from headlines
## Step-4 Calculating Word Frequencies
- we can use this function to calculate immediately next word's frequencies or also the second next following word's frequencies
## Step-5 Calculating Probabilities
- we can use this function to calculate immediately next word's probabilities or also the second next following word's probabilities
## Step-6 Building probability distributions
-Here by using above methods, we need next word probabilities and second next word probabilities
## Step-7 Complete the sentence Method
- It takes a line as input with atleast two words and by using the last word and penultimate word we predict the following word using next word probabilities and second next word probabilities respectively. This continues until we reach the no of words to be predicted limit, which is passed as a parameter
## Results of Auto Sentence Completion
- Input: `10 free` Output: `10 free food fun wine events weekend week april`
- Input: `top pop` Output: `top pop music awards 2011 2010 season 2 episode 2 recap spoilers`
#### We could generate some good predictions although some parts of it doesn't make sense but still we have a good sentence formation

## Step-8 Generate New Headlines method
- If we specify how many headlines we need along with how many how many words, it randomly generates new headlines for us 
## Results of Generating Random Headlines 
-Input: 4 lines and 7 words each
-Output:
- `incomplete untruthful shares trade secrets new jersey city book`
- `62nd annual national primetime day park show weekend 2`
- `disagreements says report may 1 2010 part 2 3`
- `wwii pilots wins first national chicago round 1 2 `
### Again, we have randomly generated headlines with good sentence structures with few errors in it.

