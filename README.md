# Group Project 1

## Description

Where to live in Melbourne if you need a place for free outdoor recreational activities area?

Analysis of free open spaces coupled with school locations/population and density

## Getting Started

Files can be downloaded from the below Repo.

https://github.com/au-jr/Group-Project-1.git

* A API Key is required fom GEOAPIFY an should be set have a external file set up next to the main_working Jupyter Notebook. File should be named geoapify and syntax is geoapify_key = "enter api key here"
  
![api_config.png](code_screenshots\api_config.png)


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

![load_pubspae_csv.png](code_screenshots\load_pubspae_csv.png)


### Visualize distribution of public spaces Local Government Area (LGA) Analysis:

We narrowed our focus to public open spaces and created a DataFrame to capture the count of these spaces in each LGA.

![dis_pubspace_pie-bar.png](code_screenshots\dis_pubspace_pie-bar.png)

### Filter for public open spaces

Data was sorted and cleaned ready to have additional data frames merged to it

![open_space_cleaning.png](code_screenshots\open_space_cleaning.png)

### Population Data Integration:

To enrich our analysis, we integrated population data for the LGAs in Victoria. Here's a glimpse:

![load_pop_data.png](code_screenshots\load_pop_data.png)

clean population data

![clean_pop_data.png](code_screenshots\clean_pop_data.png)

### School Data Exploration:

Our journey continued as we explored school data, investigating the distribution of different types of schools across LGAs:
python

Load and clean school information dataset

![clean_school_data.png](code_screenshots\clean_school_data.png)

![clean_school_data2.png](code_screenshots\clean_school_data2.png)

### Geocoding with Geoapify API:

Geocoding LGAs became crucial for our spatial analysis. We utilized the Geoapify API to fetch coordinates:
python

Add columns for latitude and longitude

![map_plot.png](code_screenshots\map_plot.png)

Interactive Map Plotting with HoloViews:

For an interactive touch, we used HoloViews to create a map plot showcasing LGAs and their respective public spaces:
python

Configure the map

![map_plot2.png](code_screenshots\map_plot2.png)

### Final Dataset Export:

Wrapping up our analysis, we compiled the entire dataset and saved it for future reference.

### Additional Data Visualizations:

In the final stretch, we created more visualizations, such as bar charts depicting the number of public spaces, schools, and population density per LGA:
python

![addition_visuals.png](code_screenshots\addition_visuals.png)

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
* VSCode's built in functions
* Most code was generated from EdX Bootcamp class activities
