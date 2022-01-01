# OBAE_project

The OBAE project is a database done with Postgresql, Python and Jupyter Lab that has as a main purpose to search specific books of one or many libraries by name and categories.

## psycopg2
psycopg2 has as a main purpose to be a PostgreSQL database adapter for Python.

### Usage ###
```` 
con = psycopg2.connect(database="store_database", user="cindy", password="Flamingosis01.", host="localhost", port="5432") cur = con.cursor()
```` 
## folium
folium is a Python library that has as a main purpose to show maps in Python/Jupyter Lab

### Usage ###
```` 
m_1 = folium.Map(location=[52.379189, 4.899431], tiles='openstreetmap', zoom_start=12)

for index,row in Sunday_opening_libraries.iterrows():
    lat = row["lat"]
    lon = row["lng"]
    name = row["name"]
    opening_days = row ["opening_weekends"]
    opening_hours = row ["opening_hours"]
    map_displayed_info = '{} : {} : {}'.format(name, opening_days, opening_hours)
    folium.Marker([lat,lon],popup=map_displayed_info).add_to(m_1)
    
m_2 = folium.Map(location=[52.379189, 4.899431], tiles='openstreetmap', zoom_start=13)

for index,row in find_restaurants.iterrows():
    lat = row["lat"]
    lon = row["lng"]
    name = row["name"]
    address= row ["address"]
    opening_hours = row ["opening_hours"]
    map_displayed_info = '{} : {} : {}'.format(name, address, opening_hours)
    folium.Marker([lat,lon],popup=map_displayed_info).add_to(m_2)

m_3 = folium.Map(location=[52.379189, 4.899431], tiles='openstreetmap', zoom_start=12)

for index,row in find_book.iterrows():
    lat = row["lat"]
    lon = row["lng"]
    title= row ["title"]
    name = row["name"]
    map_displayed_info = '{} : {}'.format(name, title)
    folium.Marker([lat,lon],popup=map_displayed_info).add_to(m_3)

m_4 = folium.Map(location=[52.379189, 4.899431], tiles='openstreetmap', zoom_start=12)

for index,row in find_book_category.iterrows():
    lat = row["lat"]
    lon = row["lng"]
    title= row ["title"]
    name = row["name"]
    map_displayed_info = '{} : {}'.format(name, title)
    folium.Marker([lat,lon],popup=map_displayed_info).add_to(m_4)
```` 

# Installation of all libraries
Use for all libraries the package manager pip to install .

## Instructions

### psycopg2

Terminal:

Python 2: pip install psycopg2
//Python 3 : pip3 install psycopg2

Jupyter Lab:

Python 2: %pip install psycopg2
//Python 3 : %pip3 install psycopg2

### folium

Terminal:

Python 2: pip install folium 
//Python 3: pip3 install folium

Jupyter Lab:

Python 2: %pip install folium 
//Python 3: %pip3 install folium


# Contributing
Pull requests are welcome. For major changes, please open an issue first to discuss what you would like to change.

Please make sure to update tests as appropriate.
