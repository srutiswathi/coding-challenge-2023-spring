# ACM Research coding challenge (Spring 2023)

This semester's challenge is especially open-ended. [Please refer to this dataset](https://www.kaggle.com/datasets/deepu1109/star-dataset) on Kaggle called "Star dataset to predict star types".  It contains information about 240 stars and various properties taken from "Stars and Galaxies" by Seeds and Backman. Each row contains 7 pieces of information about a star, such as its temperature, luminosity, radius, absolute magnitude, star type, star color, and spectral class.

Please note that the star type, denoted as integers, are translated as the following:
- Brown Dwarf -> Star Type = 0
- Red Dwarf -> Star Type = 1
- White Dwarf -> Star Type = 2
- Main Sequence -> Star Type = 3
- Supergiant -> Star Type = 4
- Hypergiant -> Star Type = 5

---

## INSTRUCTIONS: Please read this carefully, do not skim this!

- What is the most common star type in the data?
- What common patterns do you notice between any two properties? Ex: Is there a relationship between the star color and temperature?
- What properties are the most influential in classifying a star's type?
- Can you make a similar graph as the one shown in Kaggle to showcase the data as a Hertzsprung-Russell Diagram?
- Train a machine learning model to then predict the star type of a row of data (without the star type field) and find the model's accuracy.
Bonus: Can you find the row of data that most closely resembles our star, the Sun?



Background

- I am new to Python and Data Analysis as I have only taken Edx courses on basic python skills. However, I am a fast learner and with the time I have had, I was able to look at a few sources and come to some sort of an idea in terms of where I could start to answer this open ended question. 

Source: 
https://www.geeksforgeeks.org/matplotlib-pyplot-title-in-python/
https://www.geeksforgeeks.org/python-find-most-frequent-element-in-a-list/

Questions:

1. What is the most common star type in data?

This can be found using simple lines of code that will run through a loop to find out which star type (using the integers assigned) is common. 

import pandas as pd
df = pd.read_csv(r'C:\Users\srutikarthikeyan\Desktop\6 class csv.csv')
def most_frequent(df):
    counter = 0
    num = df[0]
     
    for i in df:
        curr_frequency = df.count(i)
        if(curr_frequency> counter):
            counter = curr_frequency
            num = i
 
    return num
 
print(most_frequent(df))
