# NSFW Classifier
This project is started due to interactions between large communities among different channels in Rocket Chat, there was a need for support of an optional moderation service for offensive content (automated content moderation) for channels which can be deployed by an administrator on their sole discretion.

The Model basically classifies input image in 2 broad categories: 
1. NSFW(Not Safe for Work)
2. SFW(Safe for Work)

#  Data Collection And Organization
The data can be found below.

1. https://www.kaggle.com/omeret/nsfw-nsafe & https://www.kaggle.com/omeret/nsfw-safe.

2. [B Praneeth 's Data](https://archive.org/details/NudeNet_classifier_dataset_v1) . He did an awesome job in collection 
of data . The data is for three classes <br>
   * Nude 
   * Sexy 
   *  Safe 
   1. But the problem is I need more categories for my problem . So I made a simple [tool](https://github.com/deepanshu-yadav/NSFW-Classifier/blob/master/classification_tool.ipynb) that is helpful for sub classifying the above Nude Images. You just keep all the training samples in one folder and run and run it in a jupyter notebook.
I classified a few thousands of these , but then i realized that it would take a while to gather huge data. For class **Safe For Work** i sampled randomly from his huge dataset.
   2. Further More I also made a [tool](https://github.com/deepanshu-yadav/NSFW-Classifier/blob/master/useful_scripts/useful_scripts/example.py) that takes a screenshot of the screen and saves it into a folder. It becomes handy when you want to deliberately put  difficult examples in your dataset.   

The above tools proved helpful but did not solved the problem of gathering large number of examples for training. Therefore scraping was necessary.

3. [Bazarov 's Dataset](https://github.com/EBazarov/nsfw_data_source_urls) . For collecting  set of nude images I included the the sub category in the list he provided namely: <br>
   * Female genitalia
   * Male genitalia 
   * Breasts <br>
By now I had enough examples of class **nude.** <br>


4. [ Alex's Dataset](https://github.com/alex000kim/nsfw_data_scraper/tree/master/raw_data) . For classes **animated** and **porn** i scraped the data from here.
  

5.  [Instagram Scrapper](https://github.com/rarcega/instagram-scraper) For class **Semi Nude** I used his tool to scrape few Instagram pages that regularly post arousing images of men and women.