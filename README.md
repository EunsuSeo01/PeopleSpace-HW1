# PeopleSpace HW1
## 1. Web Scraping
Purpose
- I want to know the relationship between badge and discount rate and the number of reviews.
The target variable is the badge (like Etsy’s Pick).
The predictor variables (used to predict the target variable) are discount rate and the number of reviews.

Content
- I web-scraped the data on the product name, original price, discounted price, number of reviews, and badge in ‘books movies and music’ category on the website 'Etsy'.
I have scraped a total of 100 pages, and the total data size is 6400.  

## 2. Data Manipulation
To calculate Discount Rate
- I used the original price and the discounted price to find the discount rate of the product. The equation is as follows.  
```(Original Price - Discounted Price) / Original Price * 100```

To get nemeric Review Counts
- I wrote a code to remove parentheses and remove commas between numbers to get the number of reviews only numeric values.
```df['Review Counts'] = pd.to_numeric(df['Review Counts'].apply(lambda x: re.sub(r'[^\d.]', '', x)), errors='coerce')```

To find out the correlation between the categorical variable and numeric variables
- Since the data on the badge was stored as a categorical variable, either 'No badge' or 'Etsy's Pick', I went through the process of changing it to 0 and 1 respectively to turn it into a numeric variable.

## 3. Visualization
![image](https://github.com/EunsuSeo01/PeopleSpace-HW1/assets/87434861/3b6ba302-14e5-43de-a44d-403803c076ec)  
![image](https://github.com/EunsuSeo01/PeopleSpace-HW1/assets/87434861/f94870f4-326c-409a-909b-453afaf5e862)
![image](https://github.com/EunsuSeo01/PeopleSpace-HW1/assets/87434861/87e91a4a-c8c4-4499-8f77-130d63bd97f3)
![image](https://github.com/EunsuSeo01/PeopleSpace-HW1/assets/87434861/f9f3ea6e-c4f2-4fa8-9721-752cd71c7544)
![image](https://github.com/EunsuSeo01/PeopleSpace-HW1/assets/87434861/c606c641-22bc-4331-ab60-366b4bc11a4f)
![image](https://github.com/EunsuSeo01/PeopleSpace-HW1/assets/87434861/37abd325-6369-4853-a1cd-b6f800fdc6c8)
![image](https://github.com/EunsuSeo01/PeopleSpace-HW1/assets/87434861/344cce01-1dfe-4746-b4a4-0929c7da9278)


## 4. Business Intelligence Questions


EDA Guide: [PS-HW1-EDA-Guide-EunSuSeo.pdf](https://github.com/EunsuSeo01/PeopleSpace-HW1/files/14126865/PS-HW1-EDA-Guide-EunSuSeo.pdf)
