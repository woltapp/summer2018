# Wolt Summer 2018 - Coding Exercise
## *"Digging into data"*

**In short**: your task is to create something interesting from datasets available in Wolt's [summer2018-repository](https://github.com/woltapp/summer2018). Yes, that is the only requirement - you decide the rest.

*summer2018*-repository contains two interesting JSON packages: *restaurants.json* and *orders.json*. Combined these two files include information about 75 (fictional) restaurants located in Helsinki and approx. 10k orders which were made during one week in January 2018. Data is a bit similar to what we use internally at Wolt. 

If you are especially interested about frontend development, you might considering showing those skills and visualizing data. If digging numbers is your thing, feel free to run some analysis. You can also write a command-line application that processes, mangles, combines or transforms data some way .

Take a look at what is inside those files we know you will quickly come up with ideas what to build on top of it.

**Few examples what you could create:**

- Show all restaurants on a map. Maybe clicking on a restaurant on a map could show details about it?
- Write a command-line application that calculates interesting numbers from data sets, e.g. most popular restaurants and dishes, top users, min. and max. delivery distances or perhaps how much money was spent per order (on average). 
- Design database models (relational / NoSQL) and develop an application that imports datasets to a database
- Create a view that shows all restaurants on a list / carousel / grid with the possibility to see menus.
- Find a route to visit 5 nearest restaurants from any given location in the shortest time


Have a better idea? Go for it. Web, mobile or backend - your choice. More important than **what** you decide to develop is **how** you do it. Clean code with a good structure will always make a great impression. 

## Technology

Since most of Wolt’s tech is built using Python and JavaScript (let us not forget Typescript), we will really appreciate if you can use one of those languages. But… our developers also love Java, Scala, and if you are into mobile – Swift and Kotlin. 

You are allowed to use any 3rd party library and include them as a part of your task submission.

## Returning the task

Send us a link to your GitHub repo or bundle everything into a Zip archive and mail it to [summerjobs@wolt.com](summerjobs@wolt.co). Remember that it is easier for us to review your task if we can test / run it.

A good check before sending you task is to clone the repository / unzip the Zip archive into a new folder and check that building and running the project works, using the steps you define in readme.md. Forgotten dependencies and instructions can sometimes happen even to the best of us.

## Datasets

You do not have to utilize both datasets, using just one (e.g. restaurants) is ok.

### restaurants.json

Contains a list of 75 restaurants located in Helsinki centre area. 
- All restaurants are open at the same time (every day, 10.00 - 20.00)
- *city_slug* is an ID for a city.*localized_city_name* is what needs to be displayed on the user interface
- *currency* uses ISO 4217 format
    - https://en.wikipedia.org/wiki/ISO_4217
- *timezone* uses tz database format
    - https://en.wikipedia.org/wiki/List_of_tz_database_time_zones
```
  {
         "city_slug": "helsinki",
         "currency": "EUR",
         "description": "Aliquid porro aperiam facere. Quidem vitae ducimus quod minima at nesciunt sint provident. Debitis et distinctio commodi dolorum impedit iste.",
         "id": "772560444769",
         "localized_city_name": "Helsinki",
         "location": {
             "lat": 60.176042,
             "lon": 24.936967
         },
         "name": "Nasty Carnitas",
         "phone_number": "0721954213",
         "timezone": "Helsinki/Europe"
     }
```
### orders.json
Contains a list of orders made between 8.1.-14.1.2018. 

- *time_received* (UTC timestamp) is when the restaurant received the order.
- *time_completed* (UTC timestamp) is when the order was delivered to the customer
- *customer.location* is customer’s location on the map
- An order doesn’t contain currency data (*price*). Currency of a restaurant will be used (^ see restaurant data).
- An order can include many different (menu) items. A customer can also buy multiple pieces of the same item (*quantity*)
- *restaurant_id* refers to *id*-fields in *restaurants.json*
```
   {
          "customer": {
              "first_name": "Lotta",
              "id": "221272963361",
              "last_name": "Peltosaari",
              "location": {
                  "lat": 60.16158,
                  "lon": 24.941292
              }
          },
          "id": "242676101671",
          "items": [
              {
                  "id": "182392348383",
                  "name": "1. pesto mozzarella stick",
                  "price": 12.99,
                  "quantity": 1
              },
              {
                  "id": "251594033937",
                  "name": "2. zucchini tacos",
                  "price": 11.0,
                  "quantity": 2
              }
          ],
          "restaurant_id": "772560444769",
          "time_completed": 1515431521,
          "time_received": 1515429361
      }
```

#### Any questions about the task? Send them to *summerjobs@wolt.com* 
