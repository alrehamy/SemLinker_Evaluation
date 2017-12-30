# Trip Advisor
This is a collection of user reviews ingested from TripAdvisor website and stored as a spreadsheet file, it consists of 19998 records described by 17 attributes. Each record represents a user review published on the tourism website www.tripadvisor.com, and represents the user feedback about specific restaurant in London, UK. The original attributes are:

uniq_id : the unique identifier of the review.

url : The URL of the review page.

restaurant_id : The restaurant identifier in TripAdvisor database.

restaurant_location : The city name of the restaurant geolocation

name : The full name of the restaurant.

category : The category of the place (fixed as restaurant).

title : The title of the review.

review_date : the date of posting the review.

review_text: the review text, i.e. the actual user feedback.

author : The name of reviewer

author_url : The URL page of the reviewer.

location : The city name of the reviewer.

rating : The total rating of the user on scale 1-5.

food : The food quality rating on scale 1-5.

value : The value for money rating on scale 1-5.

service : The serving quality rating on scale 1-5.

visited_on : The date of users visit to the restaurant.


# Tagging
During SemLinker evaluation, we tagged this dataset with the concept sc:Review, a default SCHEMA abstract concept. We use the following ontological properties to describe the tagging concept:

sc:identifier, the internal identifier of a review record.

sc:url, the actual URL of the review.

geo:location (extension), describes the location of the reviewed establishment.

sc:name, describes the name of the reviewed establishment.

sc:about, describes the category of the reviewed establishment (hotel, restaurant ...etc).

sc:headline, describes the title of the review.

sc:dateCreated, the time of publishing the review.

sc:reviewBody, the actual review text.

sc:reviewRating, describes the rating score of the reviewed establishment.

dc:date, describes the time when the reviewer has visited the establishment.


As described in SemLinker paper, the system only require a tagging step, i.e., using the GUI to select  the concept sc:Review for the input dataset, and, upon connecting the dataset to SemLinker, the following RDF triple is automatically generated and added to the ontology:

TripAdvisor_v.1.0 M:isInstanceOf :Review .

To this end, its SemLinker responsibility to map TripAdvisor attributes to their semantically equivalent ontological properties in sc:Review. In optimal performance, SemLinker should output the following mappings:


sc:identifier M:mapsTo IJ:uniq_id .

sc:url M:mapsTo IJ:url .

geo:location M:mapsTo IJ:restaurant_location .

sc:name M:mapsTo IJ:name.

sc:about M:mapsTo IJ:category . 

sc:headline M:mapsTo IJ:title .

sc:dateCreated M:mapsTo IJ:review_date .

sc:reviewBody M:mapsTo IJ:review_text .

sc:reviewRating M:mapsTo IJ:rating .

dc:date M:mapsTo IJ:visited_on.


For the namespace IJ, I refers to the global identifier of the dataset, and J refers to its physical schema version. For example http://www.tripadvisor.com/v1.0/
