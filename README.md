# weiboNER
Chinese social media (Weibo) corpus rearrangement, taking the word as the basic unit instead of character.
## Data source
We follow the dataset of [Chinese Named Entity Recognition for Social Media](https://github.com/hltcoe/golden-horse), which contains several types of weiboNER corpus.   
The corresponding location information is annotated in the above data, which indicates the inclusion relation of characters between words. Some of these examples are given below:  
```
大0  B-ORG.NOM  
学1  I-ORG.NOM  
同0  O  
宿0  B-LOC.NOM  
舍1  I-LOC.NOM  
三0  O  
年1  O  
```
## Data conversion
First, we concatenate the characters according to their positional characteristics, just as the following example:  
```
大学
同
宿舍
三年 
```
In order to express the richer annotation features, we then translate the BIO to BMES tag, the final corpus format is shown below:  
```
大学  S-ORG.NOM 
同    O
宿舍  S-LOC-NOM
三年  O
```
#Citation
Please cite:  


