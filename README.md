# CHCAA Data Management "Draft"
We have based our DM metadata structures on [DCAT](https://www.w3.org/TR/vocab-dcat-2/) where we found
it suitable.

## Structure

### Dataset
A Dataset represents a collection of data. This could be a collection of tweets (Twitter), articles
from news papers, historical documents etc. A Dataset can be based on another Dataset where som processing 
has occurred e.g. filtering, stemming etc. The Dataset will the reference the Dataset it is based on as 
well as the code / link to code and a description of how to reproduce the Dataset. For computational heavy
derived Datasets the processed Dataset can be included a well.

### Catalog
A Catalog describes a set a data often grouped together under a specific topic and with a specific purpose
e.g. "Covid-19", "DK-Primary-Election-2018", "Eurovision-2019"

## Considerations
- Ids is now name based to make it easier to understand the relationships when reading manually. This is no ideal if a 
dataset is still in development e.g. if we have a dataset we call js-web-articles-2019-2020 but we end 
including articles until 2021 we need to change the id and all references. And easy fix is just use integer/hex
based id's but this hurts the mnaual readability. 
- When  we base a dataset on another dataset how do we handle that the dataset based on changes? The results could 
then be different the next time   
 

## Inspiration 
 * [DCAT](https://www.w3.org/TR/vocab-dcat-2/) the original DCAT vocabulary
 * [ckanext-dcat](https://github.com/ckan/ckanext-dcat/blob/master/examples/catalog.json) a json example based on DCAT

