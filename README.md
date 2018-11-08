# Housing rentals
There are so many houses being rented today. Through many different pages. Especially in the big cities everyone wants to get a nice place to live. With huge demand there is a chance that people who rent out their places might raise prices to a critical point. This is not very good. So i wondered if there were any way to calculate what at fair rent is for a house. Machine learning to the rescue! In this notebook I have scraped one of the largest danish sites for renting out houses and tried to predict the cost of rental.

## Interpolating house prices
Using addresses on the scraped houses it is possible to gelocoate the houses (longitude/latitude). These coordinates can be further converted in east and north coordinates. Using this data we can predict house prices for any location in Denmark and map these prices visually. This is done through the following steps: 
 1. Geolocate houses
 2. Convert lat/lon to coordinates
 3. Calculate coordinates (with a certain spatial difference) for all of Denmark (here restricted to Zealand due to computational issues)
 4. Train a KNN-regressor on coordinates and house price data
 5. Predict house prices for all coordinates on Zealand
 6. Convert all coordinates to a grid of polygons
 7. Map these coordinates and prices onto the Zealand area
 
See the corresponding visualisation in the notebook

The project is not entirely finished, but will be soon. The data right now is rather sparse because it scraping takes a long time!
