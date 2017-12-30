# Schema Evolution Simulations

In order to evaluate SemLinker’s efficiency in handling schema evolutions in the physical schemas of the datasets used in the system’s experiments, we simulate multiple evolutions in the physical schemas of all the datasets except for HAR1, HAR2, and HAR3. We adopt new semantical and structural changes in the physical schema of a particular dataset, the result new physical schema version is labeled as new version. In following we describe the evolution details of each dataset in the evaluation scenarios:

# Trip Advisor Version 1.0 (original)

uniq_id → sc:identifier

url → sc:url

restaurant_location → geo:location 

name → sc:name

category → sc:about

title → sc:headline

review_date → sc:dateCreated

review_text → sc:reviewBody

rating → sc:reviewRating

visited_on → dc:date


# Trip Advisor Version 2.0 (Evolved Schema, Sematic only)

uniq_id → sc:identifier

url → sc:url

restaurant_location → geo:location 

name → sc:name

category → sc:about

title → sc:headline

review_date → sc:dateCreated

review_text → sc:reviewBody

rating → sc:reviewRating

visited_on → dc:date


# Trip Advisor Version 3.0 (Evolved Schema, Sematic only)

uniq_id → dc:identifer

url → sc:url

restaurant_location → geo:location 

place_qualified_name → sc:name

category → sc:about

title → sc:headline

review_datetime → sc:dateCreated

place_review_body → sc:reviewBody

place_bubles → sc:reviewRating

visited_on → dc:date


# Trip Advisor Version 4.0 (Evolved Schema, Sematic only)

uniq_id → dc:identifer

url → sc:url

restaurant_location → geo:location 

poiName → sc:name

category → sc:about

title → sc:headline

poiDate→ sc:dateCreated

poiReview → sc:reviewBody

poiScore → sc:reviewRating

visited_on → dc:date



# Tourpedia V 1.0 (Original)

id → dc: identifier

language → dc:language

place → x

id → sc:identifier

name → sc:name

location → geo:location

category → sc:about

polarity → dc:extent

rating → sc:reviewRating

source → dc:source

text → sc:reviewBody

time → sc:dateCreated

wordsCount → sc:wordcount


# Tourpedia V 1.2 (Evolved Schema, Semantic and Structural)

id → dc: identifier

iso_lang_code → dc:language

place → x

id → sc:identifier

place_name → sc:name

found_in → geo:location

type → sc:about

polarity → dc:extent

score → sc:reviewRating

platform → dc:source

review_text → sc:reviewBody

posted_on → sc:dateCreated

length → sc:wordCount



# Tourpedia V 1.3 (Evolved Schema, Semantic and Structural)

id → dc: identifier

locale → dc:language

place → x

id → sc:identifier

published_for → sc:name

city → geo:location

type → sc:about

polarity → dc:extent

published_rate → sc:reviewRating

publisher → dc:source

published_text → sc:reviewBody

published_on → sc:dateCreated

published_text_size → sc:wordCount



# OpenPubs V 1.0 (Original)

fas_id → dc:identifier

name → sc:name

address →  vcard:street_address

postcode → vcard:postal_code

easting → geo:point

northing → geo:point

latitude → geo:latitude

longitude → geo:logitude

local_authority → vcard:locality


# OpenPubs V 2.0 (Evolved Schema, Semantic and Structural)

est_id → dc:identifier

est_name → sc:name

est_full_information →  vcard:street_address

est_zip → vcard:postal_code

est_geo_clock→ geo:point

est_geo_clock  → geo:point

est_geolocation → geo:latitude

est_geolocation → geo:logitude

est_region → vcard:locality


# OpenPubs V 3.0 (Evolved Schema, Semantic and Structural)

id → dc:identifier

name → sc:name

address →  vcard:street_address

zip_code → vcard:postal_code

map_degree → geo:point

map_degree → geo:point

location → geo:latitude

location → geo:logitude

administrative → vcard:locality


# OpenPubs V 4.0 (Evolved Schema, Semantic and Structural)

id → dc:identifier

name → sc:name

info →  vcard:street_address

zipcode → vcard:postal_code

east_location → geo:point

north_location → geo:point

coordinate_1→ geo:latitude

coordinate_2 → geo:logitude

region → vcard:locality


# OpenPostCode V 1.0 (Original)

id(extension) → dc:identifier

postcode → vcard:postal-code

Easting → geo:point

Northing → geo:point

country → vcard:country

Latitude → geo:latitude

Longitude → geo:longitude


# OpenPostCode V 1.1 (Evolved Schema, Semantic and Structural)

id→ dc:identifier

postcode → vcard:postal-code

map_point → geo:point

map_point → geo:point

country → vcard:country

geolocation→ geo:latitude

geolocation → geo:longitude


