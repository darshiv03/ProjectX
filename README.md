# ProjectX

## Group Members: 
[Darshan Shivakumar](https://www.linkedin.com/in/darshan-shivakumar-32289919b/)<br>
Aditya Sundar<br>
[Debashish Sahoo](https://github.com/debashishsahoo)<br>

## Project Overview:

The project’s main purpose is to display laptops and mobile phones from multiple e-commerce websites on a single app for users to compare and select the best product according to their preference. ProjectX will enable the user to carefully curate a number of websites before settling on their dream product at the right value.

## Project Functionalities:

* **Login and Registration System** - Register a new user, Login with a user, Logout of a user.
* **Product Search** - Search for a laptop or phone from multiple retailers.
* **Search Filtering** - Filter search by Price & Retailer.
* **Search history** - View history of all searches made on the website.
* **Shopping cart** - Add product to cart, View cart, Remove specific product from cart, Remove all products from cart, Print PDF of cart.

## Project walkthrough:

**1) Web Scraping**: 


Web scraping refers to the extraction of data from a website. To perform this task, we made use of the Python-based Beautiful Soup library. It allows us to parse through the HTML code of a website and extract the required information. 

To perform web scraping, a comprehensive knowledge of the various HTML tags is necessary, as the data you intend to scrape is embedded within these various tags. The web browser’s ‘Inspect Element’ feature comes into hand here, which allows you to view the HTML code of any section of the web page that you’re currently viewing. This helps us decipher the location of the information we intend to extract.

Our project borrows data from renowned Japanese retailers, namely Yodobashi Camera, Bic Camera, Nojima, Yamada Denki, Kakaku and Rakuten, and Apple. For each e-commerce website, we programmed a code that recursively parsed through hundreds of pages of product results and extracted the product’s name, price, URL and image.

**2) Search Algorithm**:

By incorporating Python-MySQL connectivity, we first developed a search algorithm that takes the user’s search input and displays details of relevant products from our database. We made use of MySQL’s full-text search feature, which displays all closely-matched records from the database, and ranks them by relevance. Before performing a full-text search with a particular field of a table, we need to create a full-text index of that field.

**3) Say Hi to Django**:

Our website is basically a product of a Django-based project. Django is a free-to-use high-level Python Web framework that encourages clean rapid project developments, by using the model-template-views architectural pattern.

Once we obtained all the product details and developed the search algorithm, we incorporated it into a new Django project and continued to develop our project further.

We created a Django project called projectx, created an app within project named searchapp, and then successfully ran the project

**4) Product Search**

Our website provides you with a beautiful search bar, that lets you search for your desired product. The results are displayed in a very attractive manner- clearly showing the products’ images, names, prices & the name of the retailer that sells the product. Clicking on the product name instantly takes you to the product’s original link from the retailer.

To program our search queries, we used Django’s raw function, that lets us execute raw SQL queries on Django models.

**5) Filtering Search results**:

The product results can be further narrowed down using our smart filtering system, which allows the user to filter their searches: (1) By Retailer & (2) By Price.

**6) Search History**:

This functionality allows us to see the history of all searches made (as well as the date and time of the search) when no user is logged in, and also the search history of each specific user when he/she is logged in!

**7) Login and Registration System**:

New user registrations can be made by visiting the ‘Sign Up’ page. It is as simple as entering the relevant fields such as username, name, email and password, and proceeding to click the Register button. Failure to correctly re-enter your password, leaving fields empty, or signing up with a username that already exists, will give you an appropriate error message. To avoid accounts with duplicate usernames, we add every new user’s details to a new MySQL table userlist to our database. And by using simple Python-MySQL connectivity, we make the program check through the list of users to avoid duplicate registrations. By entering their username and password, the user can successfully login. Entering invalid credentials will give you an appropriate error message.

Once logged in, the user is redirected to the home page where he/she is welcomed with their first name! Logged in users can enjoy the benefit of the shopping cart feature, which will be explained at detail in a later section.

**8) Shopping cart**:

This feature allows a registered user to add a product to their shopping cart, by simply clicking the Add to Cart button next to a product. Users can view their cart by visiting the ‘My Cart’ page. Here, they also have the ability to (1) remove any product from their cart, (2) remove all products from the cart, and (3) to print a PDF of their cart. The shopping cart is an exclusive feature only  available to registered users when they’re logged in. 

To store the cart details of a particular user, we designed the program to create a new MySQL table for every registered user under their username. Every time a user adds an item to their cart, the corresponding product details are added to the user’s own table on our database. And every time someone deletes products from their cart, they are also removed from the database table.

## Programming Languages used:

- Django  
- Python   	   
- HTML    
- CSS     
- JavaScript  

## License & Code Re-Use
The code for this project is released under the [GPL-3.0 License](./LICENSE). We ask that you please include a link back to this GitHub repository.

## Project official sources:

1) [Yodobashi Camera](https://www.yodobashi.com/)<br>
2) [Yamada-Denki Co., Ltd](https://www.yamada-denkiweb.com/)<br>
3) [Rakuten Group, Inc](https://www.rakuten.co.jp/)<br>
4) [Kakaku.com, Inc](https://kakaku.com/)<br>
5) [Bic Camera, Inc](https://www.biccamera.com/bc/main/)<br>
6) [Nojima Corporation](https://www.nojima.co.jp/)<br>
7) [Apple Inc](https://www.apple.com/jp/shop)

## Open Source Framework used:

Bootstrap : https://getbootstrap.com/



