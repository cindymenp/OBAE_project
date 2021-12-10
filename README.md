# OBAE_project

The OBAE project is a database done with Postgresql, Python and Jupyter Lab that has as a main purpose to search specific books of one or many libraries by name and categories.

## psycopg2
psycopg2 has as a main purpose to be a PostgreSQL database adapter for Python.

### Usage
con = psycopg2.connect(database="store_database", user="cindy", password="Flamingosis01.", host="localhost", port="5432") cur = con.cursor()

## folium
folium is a Python library that has as a main purpose to show maps in Python/Jupyter Lab

### Usage
m_1 = folium.Map(location=[52.370216, 4.895168], tiles='openstreetmap', zoom_start=10)

for index, row in stores_data.iterrows(): lat = row["lat"] lon = row["lng"] name = row["store"] postal_code = row["postal_code"] map_displayed_info = '{} {}'.format(name, postal_code) folium.Marker([lat, lon], popup=map_displayed_info).add_to(m_1) print(m_1)

m_2 = folium.Map(location=[52.370216, 4.895168], tiles='openstreetmap', zoom_start=10)

for index, row in find_categories.iterrows(): lat = row["lat"] lon = row["lng"] name = row["store"] categories = row["category"] map_displayed_info1 = '{} : {}'.format(name, categories) folium.Marker([lat, lon], popup=map_displayed_info1).add_to(m_2) print(m_2)

m_3 =folium.Map(location=[52.370216, 4.895168], tiles='openstreetmap', zoom_start=10)

for index, row in find_items.iterrows(): lat = row["lat"] lon = row["lng"] name = row["store"] items = row["item"] map_displayed_info2 = '{} : {}'.format(name, items) folium.Marker([lat, lon], popup=map_displayed_info2).add_to(m_3) print (m_3)


Installation of all libraries
Use for all libraries the package manager pip to install .

Contributing
Pull requests are welcome. For major changes, please open an issue first to discuss what you would like to change.

Please make sure to update tests as appropriate.
