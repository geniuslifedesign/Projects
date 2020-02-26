## Introduction

For this Capstone project, I am creating a hypothetical scenario for a A Philadelphia tourism company would like to improve the tourist product and service they are selling to travelers leading to increased revenue. 

The idea behind this project to produce optimize travel and sightseeing packages for a historical city such as Phildelphia.

## Business Understanding

Tuscany is one of the most visited tourist destinations on earth, but
A Philadelphia tourism company would like to improve the tourist product and service they are selling to travelers.
Policy makers, government and municipality departments will be capable of better understanding the tourist’s habits, preferences, behavior patterns, and needs. This way they can improve the tourist product and service they are selling to travelers. Starting from marketing the service and finishing with infrastructure improvements.

Another large group is the business managers like providers of hospitality and travel services. Destination managers, product developers, travel agents, tour managers, hotel and restaurant managers are among the position which can achieve sweet impact to their overall performance. Last but not least are the transportation planners. Their job is crucial for citizens and travelers to be served in the most efficient way.

## Personalized Marketing and Customer Segmentation

People in some way tend to appreciate travel experience personalization. Customer segmentation entails dividing all your customers according to their preferences and adaptation of the general stack of services to satisfy the needs of every group. Thus, the key idea is to find one solution that would fit all cases. In its turn, personalization is a trick that allows providing a specific service to a particular person. Thus, personalization makes this process deeper.

## Data Requirements

I'll exploit geolocation data to gain a better understanding of tourist’s habits, preferences, behavior patterns, and needs. This informaion can improve the tourist product and create a more engaging tourists experience.

I utilizing web scraping tool to extract a list of Zipcodes, Districts and Neighborhood wilipedia pages

I will use ?  to get the geo coordinates to query Foursquare data for these neighborshoods.

I visualized the map of Toronto using Folium package

Using Foursquare API to get data related to these neighborhoods to gain a better understanding the tourist’s preferences, location, behavior patterns, and needs.

## Data Preparation

Next, I use Foursquare API to pull the list of top 100 venues within 500 meters radius. I have created a Foursquare developer account in order to obtain account ID and API key to pull the data. From Foursquare, I am able to pull the names, categories, latitude and longitude of the venues. With this data, I can also check how many unique categories that I can get from these venues. Then, I analyze each neighborhood by grouping the rows by neighborhood and taking the mean on the frequency of occurrence of each venue category. This is to prepare clustering to be done later.

Here, I made a justification to specifically look for “Thai restaurants”. Previously, when I ran the model, I was looking for “Asian restaurants” but there are very few results (maybe due to Foursquare categorization) so I looked for the restaurants closest to Burmese cuisine taste (side note: Burmese food and Thai food are very similar in taste, so my justification is that if there are people who enjoyed Thai food, they likely are going to enjoy Burmese food too!)

Lastly, I performed the clustering method by using k-means clustering. K-means clustering algorithm identifies k number of centeriods, and then allocates every data point to the nearest cluster, while keeping the centroids as small as possible. It is one of the simplest and popular unsupervised machine learning algorithms and it is highly suited for this project as well. I have clustered the neighborhoods in Toronto into 3 clusters based on their frequency of occurrence for “Thai food”. Based on the results (the concentration of clusters), I will be able to recommend the ideal location to open the restaurant.

## Segmentation and Clustering

In the following plots we display the findings from applying the k-means clustering method to the data we were provided by Vodafone. Tourists were clustered based on traits extracted from both their behaviours during their journeys in Tuscany and the nature of the locations they visited.

For examples, from the Vodafone data, we extracted the starting and ending locations of their trips, how long they spent at every stop, where they stopped, and how long they spent in total in and outside of Tuscany. By using open source data to extract points of interests, cities, and the geographic landscape for each of the locations, we were able to capture tourists’ preferences.

What emerges from the results are groups of tourists who follow a similar behaviour. Every cluster is coloured the same and each dot is average location of a tourist during the whole duration of his stay in Tuscany.

We performed the clustering analysis on tourists from all countries over the summer and post-summer seasons, as well as tourists from Germany in the summer and United States in the post-summer seasons.Enter season and country values below to view the graphical displays of each clustering analysis followed by descriptions.

Results from the three approaches can be compared and validated and thus provide a holistic picture of tourist movements

## Evaluation

## Recommendations

Policy makers, government and municipality departments will be capable of better understanding the tourist’s habits, preferences, behavior patterns, and needs. This way they can improve the tourist product and service they are selling to travelers. Starting from marketing the service and finishing with infrastructure improvements.

Another large group is the business managers like providers of hospitality and travel services. Destination managers, product developers, travel agents, tour managers, hotel and restaurant managers are among the position which can achieve sweet impact to their overall performance. Last but not least are the transportation planners. Their job is crucial for citizens and travelers to be served in the most efficient way.

## Conclusion

Once you have the data, the entrepreneurial spirit should do the rest. Geolocation big data might give you information location, consumer preferences, traffic flow, locations and so on. The mining of unstructured data can give us not just quantitative but also qualitative information on what tourists experience on a particular destination, what they need, what they like or dislike. The rest is a lot of work to be done.

## References

List of neighborhoods in Toronto: https://en.wikipedia.org/wiki/List_of_postal_codes_of_Canada:_M

Foursquare Developer Documentation: https://developer.foursquare.com/docs

All codes for this project can be found here: https://github.com/zinkohlaing/Coursera_Capstone/



Big Data provides two kinds of information that include structured and unstructured data. The data collected from websites and social networking sites such as Facebook and Twitter, blogs, and forums will have unstructured information and will be based on individual opinion. Interpreting the unstructured data and acquiring relevant insights is a big challenge facing the tourism industry.

If you would like to get a bit deeper, just try TripAdvisor that is full of unstructured data in the form of tourists comments. This way you'll get their sentiment to the particular destination, location, facility, etc.