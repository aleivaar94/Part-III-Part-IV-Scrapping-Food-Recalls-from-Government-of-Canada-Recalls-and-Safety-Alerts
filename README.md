![Python](https://img.shields.io/badge/python-3670A0?style=for-the-badge&logo=python&logoColor=ffdd54) ![Jupyter Notebook](https://img.shields.io/badge/jupyter-%23FA0F00.svg?style=for-the-badge&logo=jupyter&logoColor=white)

# Analyzing and Visualizing Government of Canada Recalls 2011-2022

A food recall is the removal of a food product from the market to avoid further sale or use, or the correction of its label at any point in the supply chain. It's the industry's responsibility to remove the recalled food from the marketplace, while the Canadian Food Inspection Agency's (CFIA) role is to inform the consumers, oversee implementation the recall and verify that the industry removed the product from the marketplace.

In this project, I analyze food recalls from 2022 to 2011 that were previously web scrapped from from the Government of Canada Recalls and Safety Alerts [website](https://recalls-rappels.canada.ca/en/search/site?search_api_fulltext=&archived=1&f%5B0%5D=category%3A144&page=0). See [Part I & Part II](https://github.com/aleivaar94/Part-I-Part-II-Scrapping-Food-Recalls-from-Government-of-Canada-Recalls-and-Safety-Alerts) of this project that describes the web scrapping process.


<sub><sup>*Recalls before 2011 are [archived](https://epe.lac-bac.gc.ca/100/206/301/cfia-acia/2011-09-21/www.inspection.gc.ca/english/corpaffr/recarapp/recal2e.shtml). Recalls from 2006-1997 are no longer available in the archive.</sup></sub>

<sub><sup>To learn more about CFIA's food recall system, click [here](https://inspection.canada.ca/food-safety-for-consumers/canada-s-food-safety-system/how-we-decide-to-recall-a-food-product/eng/1332206599275/1332207914673).</sup></sub>

## Demo
![demo](https://github.com/aleivaar94/Part-III-Part-IV-Scrapping-Food-Recalls-from-Government-of-Canada-Recalls-and-Safety-Alerts/blob/master/Power-BI/CFIA-recalls-2022.gif)



## Methodology

Web scrapping succesfully extracted the `title`, `date`, `recall issue`, `audience`, `company`, `province(s)`, and `recall class`.

![image](https://github.com/aleivaar94/Part-III-Part-IV-Scrapping-Food-Recalls-from-Government-of-Canada-Recalls-and-Safety-Alerts/blob/master/images/title-extract.png)

But the product or brand is extracted from the title column by identifying patterns. For example, the brand can be extracted from any words that come before “brand” in the title. This is extracted using a defined regex function.

Likewise, from the `title` column we can extract the specific hazard after the words “recalled due to”. 

Further data cleaning and replacing of values is done.

## Results

### Part III

A total of 3893 food safety recalls were cleaned for analysis in part IV.

### Part IV

Insights and analysis are presented in a Power BI story/dashboard. You can download the Power BI file below.

## Future Work

Natural language processing could be used to provide a more efficient data extraction and cleaning of each recall. This will be a project in the future, which would be beneficial to update the statistics as the years pass.

## **Workflow**

Follow the jupyter notebooks in the order below:

`1. Part-III.1-cleaning-recalls.ipynb`

`2. Part-III.2-cleaning-recalls.ipynb`

`3. Part-IV-analyzing-recalls.ipynb`