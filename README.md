# Group Project 1

## Description

Where to live in Melbourne if you need a place for free outdoor recreational activities area?

Analysis of free open spaces coupled with school locations/population and density

## Getting Started

Files can be downloaded from the below Repo.

https://github.com/au-jr/Group-Project-1.git

### Dependencies

* Python version 3.7.13
* hvplot.pandas
* pandas
* requests
* json
* numpy
* matplotlib.pyplot

### Executing program

* Once downloaded the the Jupyter Notebook file will be ready to execute through VScode or Jupyter Lab
* Do Not adjust any folders with in the repo.

## Workflow

In this project, we set out to explore the dynamics of public spaces, population distribution, and educational facilities across various Local Government Areas (LGAs) in Victoria, Australia. Let's dive into the journey we took:

Data Exploration and Preparation:

We kicked off the project by loading our primary dataset, which contains information about public spaces in Victoria.

### Load public spaces dataset
csv_path = 'data/VPA_Open_Space.csv'
information_df = pd.read_csv(csv_path)


### Visualize distribution of public spaces
... (Code for bar charts and pie charts)
Local Government Area (LGA) Analysis:

We narrowed our focus to public open spaces and created a DataFrame to capture the count of these spaces in each LGA:
python

### Filter for public open spaces
information_df_parks_df = information_df.loc[(information_df['OS_TYPE'] == 'Public open space')]
... (Code for creating LGA-specific DataFrames)
### Population Data Integration:

To enrich our analysis, we integrated population data for the LGAs in Victoria. Here's a glimpse:
python
Copy code
Load population data
lga_information_path = pd.read_excel('data/LGA_ABS_data_21_22.xlsx', ...)
lga_information = pd.DataFrame(lga_information_path)
... (Code for data cleaning and merging)
### School Data Exploration:

Our journey continued as we explored school data, investigating the distribution of different types of schools across LGAs:
python

Load school information dataset
school_csv_path = 'data/dv309_schoollocations2021.csv'
school_read_csv = pd.read_csv(school_csv_path, encoding='cp1252')
school_count_df = pd.DataFrame(school_read_csv)
... (Code for filtering and grouping school data)
### Geocoding with Geoapify API:

Geocoding LGAs became crucial for our spatial analysis. We utilized the Geoapify API to fetch coordinates:
python

Add columns for latitude and longitude
Location_merged_map_ploting["Lat"] = ""
Location_merged_map_ploting["Lon"] = ""
... (Code for geocoding with Geoapify API)
Interactive Map Plotting with HoloViews:

For an interactive touch, we used HoloViews to create a map plot showcasing LGAs and their respective public spaces:
python

Configure the map
map_plot_2 = Location_merged_map_ploting.hvplot.points(
    "Lon", "Lat", geo=True, tiles="OSM", ...
)
... (Code for additional map-related configurations)
### Final Dataset Export:

Wrapping up our analysis, we compiled the entire dataset and saved it for future reference:
python

### Save the complete dataset to Excel
schools_park_vic_data_df.to_excel('data/Complete_Dataset.xlsx')
Additional Data Visualizations:

In the final stretch, we created more visualizations, such as bar charts depicting the number of public spaces, schools, and population density per LGA:
python

... (Code for additional bar charts and visualizations)
### Conclusion:

Our exploration provides a comprehensive view of the urban landscape in Victoria, unraveling patterns in public spaces, population distribution, and educational facilities. Feel free to check out the figures saved in the "figures" directory for a visual representation of our findings.
And there you have it! A glimpse into our project journey exploring the heart of Victoria, one dataset at a time.

## Presentation



### Powerpoint Slides PDF Location

### Figures

![Categories_of_Public_Spaces](figures\Categories_of_Public_Spaces.png)
![LGA_Location_Map.png](figures\LGA_Location_Map.png)
![lga_open_spaces.png](figures\lga_open_spaces.png)
![LGAvsPopulation.png](figures\LGAvsPopulation.png)
![Owner_Space_Type.png](figures\Owner_Space_Type.png)
![Owners_of_Green_Spacese.png](figures\Owners_of_Green_Spacese.png)
![pop_change_vs_schools_comparison.png](figures\pop_change_vs_schools_comparison.png)
![schoolsvsLGAvsOpenSpaces.png](figures\schoolsvsLGAvsOpenSpaces.png)
![spaces_vs_pop_change.png](figures\spaces_vs_pop_change.png)
![spaces_vs_schools_comparison.png](figures\spaces_vs_schools_comparison.png)



## Authors

Contributors names and contact info

*   John Robertson
     - Email: john.f.robertson93@gmail.com
*   James Eastman
     - Email: james.eastman.1987@gmail.com
*   Sonal Bhosle
     - Email: sonalvbhosle@yahoo.com
*   Laura Liu
     - Email: liuruilaura@gmail.com

## Acknowledgments

Inspiration, code snippets, etc.

* Victorian Open Space Data - Victorian Planning Authority. (2019)
     * URL - https://discover.data.vic.gov.au/dataset/open-space

* Victorian School Data - Department of Education. (2021)
     * URL - https://discover.data.vic.gov.au/dataset/school-locations-2021/resource/97c05fd1-8671-4f0a-9f91-e8d57a1c1135
  
* Australian Bureau of Statistics. (2021-22). Regional population. ABS. 
     * URL - https://www.abs.gov.au/statistics/people/population/regional-population/latest-release.
  
* ChatGPT was used for debugging
* VSCode's built in functions also helped to build
* Most code was generated from class activities
