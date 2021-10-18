# Understand The Performance of Airbnb in Rio de Janeiro by Using Python
Exploratory Data Analysis on Rio de Janeiro Airbnb dataset 2021
![image](https://user-images.githubusercontent.com/8090224/137777584-59d7b2d8-b67c-4a77-ab8b-1456cab38c3a.png)

# Introduction to Airbnb

[Airbnb](https://airbnb.com/) is the **biggest hotel franchise in the world**, the interesting part about it is that **they have no hotels at all!**

Through an innovative way of finding accommodation, Airbnb connects people who want to travel (and to accommodate somewhere) to house hosts who want to rent their places.

By the end of 2018, ten years after its foundation, Airbnb had already **hosted over 300 million people** from all over the world, challenging traditional hotel brands to reinvent themselves.

In addition to this, the startup also has a culture of handling **free data** on the internet, you can download them from the website [Inside Airbnb](http://insideairbnb.com/get-the-data.html) and have access to data from **some of the biggest cities in the world**, which allows you to build countless projects and *Data Science* solutions.

Take a look at some of Airbnb numbers:

![img](https://miro.medium.com/max/700/0*GnbgjWjYD1_Oj1MA.png)

Intro to The Airbnb Community from [Shirley Chen](https://medium.com/analytics-vidhya/how-to-analyze-airbnb-performance-data-in-the-right-way-b83f3dad1458)

By the way, this set is the “summarized” version from Airbnb. On the same page, we downloaded the file `listing.csv`, there is a longer version called `listing.csv.gz` with the **full** dataset.

# Presenting Rio de Janeiro

Located on the Guanabara Bay in southern Brazil, Rio de Janeiro is one of the most densely populated cities in the world and is also considered one of the most beautiful cities in the world. Rio de Janeiro has been nicknamed *Cidade Maravilhosa*—Marvelous City—for its sandy beaches, steep mountains, tropical forest, and bay-side location.

Rio de Janeiro is one of the most visited cities in the Southern Hemisphere and is known for its natural settings, Carnival, samba, bossa nova, and balneario beaches[11] such as Barra da Tijuca, Copacabana, Ipanema, and Leblon. In addition to the beaches, some of the most famous landmarks include the giant statue of Christ the Redeemer atop Corcovado mountain, named one of the New Seven Wonders of the World; Sugarloaf Mountain with its cable car; the Sambódromo (Sambadrome), a permanent grandstand-lined parade avenue which is used during Carnival; and Maracanã Stadium, one of the world's largest football stadiums.

**Given the city’s context, let’s start our analysis.**

# Obtaining the Data

One of the main reasons why Python is great is for how many libraries and packages it has, today we will be using four libraries to analyze our *dataset*, these are:

```
1. pandas - Used to manipulate our dataset.
2. matplotlib - Used to plot our histograms.
3. seaborn - Used to plot our heatmap.
4. plotly - Used to plot our interactive map.
```

# **Variables dictionary**

- `id` — the id number generate to identify the place.
- `name`— name of the place announced.
- `host_id`— the id number of the place’s host.
- `host_name`— host’s name.
- `neighbourhood_group` — this column has no valid data.
- `neighbourhood` — neighbourhood’s name.
- `latitude` — property’s latitude coordinate.
- `longitude` — property’s longitude coordinate.
- `room_type` — type of room offered.
- `price` — price to rent the place.
- `minimum_nights` — minimum amount of nights to book the place.
- `number_of_reviews` — amount of reviews the place has.
- `last_review` — last review’s date.
- `reviews_per_month` — amount of reviews per month.
- `calculated_host_listings_count` — amount of properties the host owns.
- `availability_365` — amount of available days for booking in a year.

# What’s the average renting price?
now that we have a clean DataFrame, we can check our average booking price. To do this we can use the .mean() method, in which will print the mean value among all the values in the price column.
![image](https://user-images.githubusercontent.com/8090224/137781922-0ed0da71-ce05-452a-8c12-0b223e06e165.png)

# What Type of Places are Rented the Most in Rio de Janeiro?

The column `room_type` contains all the kinds of places you can rent in Airbnb, there are quite a few options available. By using the method `value.counts()` we can check which is the most popular type of Airbnb property renting in Rio.

![image](https://user-images.githubusercontent.com/8090224/137783615-bf09f1c0-79b9-4ee8-9b35-59da39aa5709.png)

As our analysis shows, the most popular room type in Rio is the entire home or apartment. Thus if you live in Rio and want to rent your place, you should probably invest in whole-home/apartment rentals or maybe private rooms.

# What’s the average of minimum nights in Rio?

We can also check the average of minimum nights required for booking in Rio. To do this we can use the `.mean()` method. 

![image](https://user-images.githubusercontent.com/8090224/137784482-ec966612-794e-4ac1-91fe-156d6b5b3163.png)

The average minimum number of nights in a property in Rio is equivalent to approximately 4, Which indicates that people usually stay in a property in Rio in half a week, which can be the first days or a weekend.

- # Airbnb Distribution in Rio
![image](https://user-images.githubusercontent.com/8090224/137785573-97e7b550-0be4-4c7b-9321-eb7507ac3e3a.png)

- # Distribution by price
By the way, since we are provided with latitude and longitude, we can plot a distribution map. Let `x=longitude` and `y=latitude`. The redder it gets means it is more expensive.

![image](https://user-images.githubusercontent.com/8090224/137785840-8e68bf9f-629f-4497-8147-a4d056b55f09.png)

  
## A cloud of words to better understand Rio, using the complete dataset provided by Inside Airbnb!
![image](https://user-images.githubusercontent.com/8090224/137786014-ebfa1c7f-85bf-43ee-a1cc-fb6bc8822105.png)
  

  

  

