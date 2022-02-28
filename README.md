# AmazonScraper-API

An API created to serve needed information / details of a particular product from the Amazon market store.

### Endpoints :

(1) ``` /products/:productId ``` : Lists all product details of the product id parsed as a parameter.<br/>
Some of the major important properties include:
- Name
- Brand
- Pricing
- Availability_status
- Average Rating
- Description
- Customization options
- Seller_id
- Seller_name <br/>

For instance : https://vsh-amzn-scrapper.herokuapp.com/products/B08JQN8DGZ

(2) ``` /products/:productId/reviews ``` : Lists all product reviews listed of the product id parsed as a parameter.<br/>
Some of the major important properties include:
- Average_Rating
- Total_ratings
- Total_reviews
- Ratings percentage for each star (i.e. 5_star_ratings, 5_star_percentage)
- Top_positive_review
- Top_critical_review
- Other reviews<br/>

For instance : https://vsh-amzn-scrapper.herokuapp.com/products/B08JQN8DGZ/reviews

(3) ``` /products/:productId/offers ``` : Lists any offers that are live on the product id passed as a parameter. <br/>
For instance : https://vsh-amzn-scrapper.herokuapp.com/products/B08JQN8DGZ/offers

(4) ``` /search/:searchQuery ``` : Lists the generated results after a natural query to the Amazon Marketplace Search Engine. <br/>
For instance : https://vsh-amzn-scrapper.herokuapp.com/search/teapots
<br /> <br />
<i> Please give the site some load, or reload if you get any error.</i>

### How to find ProductID : <br/>

Globally Amazon URL's follow the same pattern : 
```
amazon.countrycode/prod-name-somedetails/dp/productId?mid...
```
Therefore the product id resides right besides dp/. As can be seen in the below example : <br/>
![image](https://user-images.githubusercontent.com/59518168/155880718-a9179d4d-25af-478b-9cf4-7be9083a2081.png)

### Note : 
This project uses [ScraperAPI](https://www.scraperapi.com/) to scrap Amazon's website that passes plain web data from which the important stuff is parsed as JSON into my API.

