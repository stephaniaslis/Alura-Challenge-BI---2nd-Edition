# Alura-Challenge-BI--2nd-Edition
Alura is a coding school from Brazil that offers courses and challenges occasionally. This challenge has 4 weeks of duration and is about Business Inteligence, using mainly Power BI.

# 1st Week - Alura films
In this case there is the IMDB dataset which contains more than 1000 movies, the main goal is to explore the data and it visualization to deliver information that helps the decision making of Alura films.

## Dataset
https://drive.google.com/drive/folders/1fBIECPox4nXVeuIfD5y8k7Vvdy1Omzj8

## Data cleaning
- Removal of null values from movie titles
- Change the text format to number format for columns that are numeric, eg: Gross

## Dashboard

This is the dasboard of Alura films, It´s also avaiable in the following link:

https://app.powerbi.com/view?r=eyJrIjoiZGQ4ZTNiYjEtMTI5Yi00N2Q1LTkzMjEtY2ZmNjhlYjM4MGM4IiwidCI6ImZlYmViNjkyLTZjNzUtNDVkZS1iN2FjLTY3YjEwNmQzZWNjNyJ9

In this dashboard there are plots for number of title by main star, gross percentage by genre. There are othes informations as IMDB Rating average and number of votes.

![Main](https://user-images.githubusercontent.com/82055743/155108542-787005c1-4885-4741-a7cd-5e87e759af39.png)

There is a sheet of director and gross that can be ordered:

![Director_gross](https://user-images.githubusercontent.com/82055743/155115413-9118453f-5420-4cd1-a129-3d2796421b2e.png)

And it´s possible search by an especific title:

![Movie](https://user-images.githubusercontent.com/82055743/155115469-72f465d9-be42-469a-993c-72f04f6e8c5d.png)

## Conclusions
There are relevant conclusions in this dasboard:
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

# 2nd Week - Alura food
In this case there is the dataset from Zomato that is an Indian multinational restaurant aggregator and food delivery company. The goal is analyse the Indian food market to deliver information that helps the decision making of Alura food in India.

## Dataset
The dataset is made by json files from Zomato API. 
https://drive.google.com/drive/folders/1v_Y7TBObGEEtj4C9ku4GvmlX0x9TTZd-

## Data cleaning
- Open the json files and open sublists
- Removal of duplicates of restaurant id
- Removal of null values from restaurant id
- Change the text format to number format for columns that are numeric
- Replace Goa that is a state of India by Pangim that is its capital - It's used to the map location due to Goa is a city in other country
- Filter only India as country

## Dashboard

This is the dasboard of Alura food, It´s also avaiable in the following link:
https://app.powerbi.com/view?r=eyJrIjoiN2Q1OWY4MDItN2MzYi00ZTkxLWFkNTEtZjUzMjVjYzBmMjg3IiwidCI6ImZlYmViNjkyLTZjNzUtNDVkZS1iN2FjLTY3YjEwNmQzZWNjNyJ9&pageName=ReportSection

![Alura_food_dashboard](https://user-images.githubusercontent.com/82055743/155982872-b57014cb-86ba-41c1-a8b1-19ed781635a4.png)

And segmented by city:

![Alura_food_dashboard_nd](https://user-images.githubusercontent.com/82055743/155985227-4249926f-9be3-49a6-a5ea-54cafea1addb.png)

## Conclusions
There are relevant conclusions in this dasboard:
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

# 3rd Week - Alura Skimo
In this case there is the dataset from Alura skimo that is an ice cream company. The goal is analyse the skimo sales database to deliver information that helps the decision making of Alura skimo.

## Dataset
The dataset is a dump of sql files. The first step is create a database with the following code

CREATE DATABASE iii_semana

After that use MySQL and restoring a database:

![restore dump](https://user-images.githubusercontent.com/82055743/157261712-4dc693e1-b2a6-4b96-bd34-11e999936806.png)

Finally the database will be on schemas:

![create database](https://user-images.githubusercontent.com/82055743/157262273-2caaa13d-7d16-424d-bfe4-7dc78deffa53.png)

The last step is load the database on PowerBI.

## Data cleaning

## Dashboard

## Conclusions


