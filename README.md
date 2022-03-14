#  :rocket: Alura-Challenge-BI--2nd-Edition :computer:
Alura is a coding school from Brazil that offers courses and challenges occasionally. This challenge has 4 weeks of duration and is about Business Inteligence, using mainly Power BI.

# :clapper:	1st Week - Alura films
In this case there is the IMDB dataset which contains more than 1000 movies, the main goal is to explore the data and it visualization to deliver information that helps the decision making of Alura films.

##  :link: Dataset
The dataset is available on the following link:

https://drive.google.com/drive/folders/1fBIECPox4nXVeuIfD5y8k7Vvdy1Omzj8

## :broom:	 Data cleaning
- Removal of null values from movie titles
- Change the text format to number format for columns that are numeric, eg: Gross

## :bar_chart: Dashboard and Data analysis

From the dataset there is some analysis as follow:

Metrics:
- Gross
- IMDB Rating
- Number of votes

Charts:
- Number of titles by main star
- Gross percentage by genre

A table showing Gross and director, and also a search by movie.

This is the dashboard of Alura films, It´s also available in the following link:

https://app.powerbi.com/view?r=eyJrIjoiYWEwMWRmNTQtMzRhYi00MzI3LTlhZDgtNzNhMTBhMGI1ZmVmIiwidCI6ImZlYmViNjkyLTZjNzUtNDVkZS1iN2FjLTY3YjEwNmQzZWNjNyJ9&pageName=ReportSection
 
![2022-03-10 (3)](https://user-images.githubusercontent.com/82055743/157682860-8e067e03-1800-40c3-8fb9-b9242b573c63.png)



And the mobile version were created as well:

![Design sem nome (4)](https://user-images.githubusercontent.com/82055743/157675283-e5b557e1-45e2-42ee-9707-82acb03dbc87.png)


## :heavy_check_mark:	Conclusions
There are relevant conclusions in this dashboard:
- Top 3 gross by genre are:
  - Action
  - Drama
  - Animation
  
The action gross is bigger than the sum of drama and action.

- Top 3 Main Stars according to the number of titles:
  - Tom Hanks
  - Robert De Niro
  - Al Pacino
  
- Top 3 Directors:
  - Steven Spielberg
  - Anthony Russo
  - Christopher Nolan

# :plate_with_cutlery:	2nd Week - Alura food
In this case there is the dataset from Zomato that is an Indian multinational restaurant aggregator and food delivery company. The goal is analyse the Indian food market to deliver information that helps the decision making of Alura food in India.

## :link: Dataset
The dataset is made by json files from Zomato API, available on the following link:

https://drive.google.com/drive/folders/1v_Y7TBObGEEtj4C9ku4GvmlX0x9TTZd-

## :broom: Data cleaning 
- Removal of restaurant id duplicated
- Removal of restaurant id null values
- Change the text format to number format for columns that are numeric

## :bar_chart: Dashboard and Data analysis

The dataset is avaliable in json files, so the first step is open the json files and open the sublists. After that, there are the following analysis:

- Replace Goa that is a state of India by Pangim that is its capital - It's used to the map location due to Goa is a city in other country
- Filter only India as country

This is the dashboard of Alura food, It´s also available in the following link:

https://app.powerbi.com/view?r=eyJrIjoiN2Q1OWY4MDItN2MzYi00ZTkxLWFkNTEtZjUzMjVjYzBmMjg3IiwidCI6ImZlYmViNjkyLTZjNzUtNDVkZS1iN2FjLTY3YjEwNmQzZWNjNyJ9&pageName=ReportSection

![Alura_food_dashboard](https://user-images.githubusercontent.com/82055743/155982872-b57014cb-86ba-41c1-a8b1-19ed781635a4.png)

And the mobile version were created as well:

![Design sem nome (3)](https://user-images.githubusercontent.com/82055743/157649665-a186a19f-1f52-4dfd-b180-002a1b6294b5.png)


## :heavy_check_mark: Conclusions
There are relevant conclusions in this dashboard:
- Top 3 cusines:
  - North Indian
  - Chinese
  - Fast Food
  
The number of restaurants with North Indian cusine is bigger than the sum of Chinese an Fast Food.

- Top 3 cities:
  - New Delhi
  - Gurgaon
  - Noida
  
New Delhi has 5 times more restaurants than the second city Gurgaon  

#  :icecream:	3rd Week - Alura Skimo
In this case there is the dataset from Alura skimo, that is an ice cream company. The goal is analyse the skimo sales database to deliver information that helps the decision making of Alura skimo.

## :link: Dataset
The dataset is a dump of sql files, available on this link 

https://drive.google.com/drive/folders/106j-3sbhHp5CiWNxQWZDydKKoRgPc70z

The first step is create a database with the following code:

CREATE DATABASE iii_semana

After that, using MySQL and restoring a database:

![restore dump](https://user-images.githubusercontent.com/82055743/157261712-4dc693e1-b2a6-4b96-bd34-11e999936806.png)

Finally, the database is on schemas:

![create database](https://user-images.githubusercontent.com/82055743/157262273-2caaa13d-7d16-424d-bfe4-7dc78deffa53.png)

The last step is load the database on PowerBI.

## :broom: Data cleaning
- Change the text format to number format for columns that are numeric
- Removal of id produto (product id) number 239, because there isn't values of preço (price), custo (cost) and categoria (category), probably it is a mistake

## :bar_chart: Data analysis and Dashboard
There are some columns that had to be imported to make some measures:

The price product is imported from the 'iii_semana produtos'[PREÇO] to 'iii_semana produtos'[Price product] using the following formula:


Price product = LOOKUPVALUE( 'iii_semana produtos'[PREÇO], 'iii_semana produtos'[ID Produto],  'iii_semana itens_pedido'[ID Produto])

Other columns are created in iii_semana itens_pedido table :


Partial revenue = 'iii_semana itens_pedido'[Price product] * 'iii_semana itens_pedido'[Quantidade_Vendida]


Cost product = LOOKUPVALUE('iii_semana produtos'[CUSTO DO PRODUTO],'iii_semana produtos'[ID Produto], 'iii_semana itens_pedido'[ID Produto])


Partial cost = 'iii_semana itens_pedido'[Cost product] * 'iii_semana itens_pedido'[Quantidade_Vendida]


Partial profit = 'iii_semana itens_pedido'[Partial revenue] -'iii_semana itens_pedido'[Partial cost] 


Category name = LOOKUPVALUE('iii_semana produtos'[Category name],'iii_semana produtos'[ID Produto], 'iii_semana itens_pedido'[ID Produto])

Measures are created for the following metrics:
- Average Ticket Price
- Amount of sales
- Revenue
- Cost 
- Profit

And charts to:
- Revenue by category
- Revenue by sales person
- Partial profit, revenue and cost by trimester


The dashboard is avaiable on the following link:

https://app.powerbi.com/view?r=eyJrIjoiY2YyNWVkYzktNzYxZS00NDNjLThkZTctMmNkMWQ5ODA2OWRkIiwidCI6ImZlYmViNjkyLTZjNzUtNDVkZS1iN2FjLTY3YjEwNmQzZWNjNyJ9


![dashboard_skimo](https://user-images.githubusercontent.com/82055743/157416800-f49307c6-41e8-4a98-a7c9-2062deb81e01.png)

And the mobile version were created as well:


![Design sem nome](https://user-images.githubusercontent.com/82055743/157643024-5a2dda3e-e897-446a-907c-acfc6aabff97.png)


## :heavy_check_mark: Conclusions

- Top 3 best seller categories:
  - Milk ice cream 
  - Fuit ice cream
  - Fuit popsicle

Milk ice cream sells more than a half of the total categories.

- Top 3 revenue by salesperson:
  - Expedita Joaquina
  - Bruno Gadelha
  - Lírio Gonçalves
 
 Each one has almost the same sales amount.
 
- Seasonal component:
  - The profit, cost and revenue are bigger during the first trimester, and almost the same in the other 3 trimesters.

# 📌 4th Week - Improvements and latest revision

- Improvement of all weeks
- Insertion of dashboards mobile version
- Latest revision


