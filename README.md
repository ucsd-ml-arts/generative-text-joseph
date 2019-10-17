# Project 1 Generative Text

Joseph Chang, jdchang@ucsd.edu

## Abstract

The goal of this project is to generate rap lyrics from Kanye West which can be used for future song ideas or matched with other music. The model used for this project is a GRU RNN. Model architecture and training parameters are manipulated to optimize the model to generate the most sensible and accurate lyrics. The dataset used is Kanye West Rap Verses from Kaggle which is a compilation of 243 Songs and 364 Verses.


Include your abstract here. This should be one paragraph clearly describing your concept, method, and results. This should tell us what architecture/approach you used. Also describe your creative goals, and whether you were successful in achieving them. Also could describe future directions.

## Model/Data

Briefly describe the files that are included with your repository:
- trained models
- training data (or link to training data). what is your corpus?

## Code

Your code for generating your project:
- training_code.py or training_code.ipynb - your training code
- generative_code.py or generative_code.ipynb - your generation code

## Results

- Documentation of your generative text in an effective form. A file with your generated text (.pdf, .doc, .txt). 

Temperature most optimal at 1.0. Above 1.0 starts producing words that aren't real. Below has little noticable difference, but it is definitely closer to the original lyrics' order which we want to avoid for this project.

GRU  30 eopchs loss: 0.0689 (2 layer rnn)
LSTM 30 epochs loss: 0.0669 (2 layer rnn)
GRU  30 eopchs loss: 0.0685 (3 layer rnn)
LSTM 30 epochs loss: 0.0661 (3 layer rnn)

## Technical Notes

Any implementation details or notes we need to repeat your work. 
- Does this code require other pip packages, software, etc?
- Does it run on some other (non-datahub) platform? (CoLab, etc.)

## Reference

https://www.kaggle.com/viccalexander/kanyewestverses

References to any papers, techniques, repositories you used:
- Papers
  - [This is a paper](this_is_the_link.pdf)
- Repositories
- Blog posts
