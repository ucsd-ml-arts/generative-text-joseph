# Project 1 Generative Text

Joseph Chang, jdchang@ucsd.edu

## Abstract

The goal of this project is to generate oldie song lyrics inspired by Bobby Darin. These can be used for future song ideas or matched with other music. In particular, we want to test the results of using modern words as our starting phrase to see how the generator reacts. To have Bobby Darin singing about iPhones or new technology he never saw would be interesting. It would make his voice present today even though he is no longer alive. The method used for this project is a LSTM RNN with a 3 layer LSTM architecture. RNNs are optimal for language prediction as it understands every word based on the previous word's understanding. It has persistence. In our case, the model architecture and training parameters are adjusted to optimize the model to generate the most sensible and accurate lyrics while retaining a sense of randomness so the model is not overfitted. A webscraper is used to create the Bobby Darin lyrics dataset which is a compilation of 300 songs. The lyrics are processed to be lowercase only to avoid having missing uppercase letters.


## Model/Data

training
- Contains all training checkpoints
Project_1.ipynb
- Contains code for processing dataset, training model, generating lyrics, saving to .txt file
WebScraper.pynb
- Contains code for scraping a specific artist's lyrics from Genius using Genius API and outputting results in a .txt file
bobby-darin-lyrics.txt
- Contains lyrics to 300 of Bobby Darin's songs
bobby-darin-lyrics-generated.txt
- Contains lyrics generated by trained model

## Code

WebScraper.pynb 
- Genius lyrics web scraping code
- The lyrics are processed to be lowercase only to avoid having missing uppercase letters.
Project_1.pynb 
- Training and generation code
- Temperature is most optimal at 1.0. Above 1.0 starts producing words that aren't real. Below has little noticable difference, but it is much closer to the original lyrics which we want to avoid.
- The resulting loss was recorded for combinations of GRU and LSTM. It was concluded LSTMs are have lower loss and are more effective.
GRU  30 eopchs loss: 0.0689 (2 layer rnn)
LSTM 30 epochs loss: 0.0669 (2 layer rnn)
GRU  30 eopchs loss: 0.0685 (3 layer rnn)
LSTM 30 epochs loss: 0.0661 (3 layer rnn)
- The number of epochs was increased from 3 to 30 epochs which lowered the loss.
- Decided to use a 3-layer LSTM which was the best balance between overfitting and underfitting.


## Results

The goal of this project is to seed Bobby Darin lyrics with our own phrase or word.

Seed word: iphones

Attempt 1
--------------
iphones gonna be mine
this evenin'
'bout a quarter to nine

get it!
ahhh, ah
oh!

oh, the stars
are gonna twinkle and shine
this very evenin'
'bout a quarter to nine

both these lovin' arms
are gonna tenderly twine
this evenin' around you
quarter to nine

i know i won't be late
'cause at half-past eight
i will hurry there
i'm gonna be waitin' where the lane begins evenin'
'bout a quarter to nine

my lovin' arms
are gonna tenderly twine
all around you
'round a quarter to nine

i know i won't be late
'cause at half-past eight
i will hurry there
i'm gonna be waitin' where the lane begins
waitin' on you on needles and pins

and then
the world is gonna be mine
this evenin'
'bout a quar eight
i'll be waitin' there
i'll be waitin' where quarter to nine

my lovin' arms
are gonna tenderly twine
this evenin' around you
quarter to nine

i know i won't be late
'cause at half past eight
i'll be waitin' there
i'll be waitin'-f-past eight
i will hurry there
i'm gonna be waitin' where the lane begins
waitin' 

Attempt 2
--------------
iphones and pins

and then
the world is gonna be mine
this evenin'
'bout a quarter to nine!

thank you

one, two, three!

the stars
are gonna twinkle and shine
this very evenin'
'bout a quarter to nine

both these lovin' arms
are gonna tenderly twine
all around you
'round a quarter to h
oh!

oh, the stars
are gonna twinkle and shine
this very evenin'
'bout a quarter to nine

both t evenin'
'bout a quarter to nine

get it!
ahhh, ah
oh!

oh, the stars
are gonna twinkle and shine
this very evenin' around you
quarter to nine

i know i won't be late
'cause at half-past eight
i will hurry there
i'm gonna be waitin' where the lane begins
waitin' for you on needles and pins

and then
the world is gonna be mine
this evenin'
'bout a quarter to nine!

thank you

one, two, three!

the stars
are gonna twinkle and shine
this very evenin'
'bout a quarter to nine

both these lovin' arms
are gonna tenderly twine
all around you
'round a quarter to nine

i know i won't be late
'cause at half past eight
i'll be w

## Technical Notes

This implementation requires signing up for a free account that authorizes access to the Genius API. Sign up [here](https://genius.com/api-clients). After signing up, you should receive a Client ID. Replace the Client ID in WebScraper.ipynb with your new ID.

## Reference

- [LyricsGenius](https://github.com/johnwmillr/LyricsGenius): Reference for writing own webscraping code

