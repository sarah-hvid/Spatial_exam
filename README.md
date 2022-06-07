# Spatial Analytics Exam - Youth educations in Denmark
 
In this project youth educations in Denmark were explored from a spatial analytical perspective by a municipal level.

## Methods
**OpenCage**\
This project made use of the ```OpenCage``` package's forward geocoding functions. ```OpenCage``` is an API service, which means that the user needs to register to get an API key. The key need to be set in the R environment to reproduce the geocoding conducted in this project. A thorough guide to this process is available within their [vignette](https://cran.r-project.org/web/packages/opencage/vignettes/opencage.html) (Possenreide et al., 2021). ```OpenCage``` was used to gather the coordinates of all institutions and the coordinates of all municipalities in Denmark.\
\
**Mapboxapi**\
This project also makes use of the ```Mapboxapi``` package's distance calculation functions. The user must again register in order to get an API key and set this in the R environment. The steps only need to be performed once and a guide is available [here](http://walker-data.com/MUSAmasterclass/tutorial/) (Walker, 2020). The ```mb_distance()``` function was used to calculate the distance between each institution and municipality. The result was used to find the minimun distance from each municipality to each education type. 

## Usage
In order to run the script certain modules need to be installed. A list of these along with their version can be found in the ```requirements.txt``` file. The folder structure must be the same as in this GitHub repository (ideally, clone the repository).
```bash
git clone https://github.com/sarah-hvid/Spatial_exam.git
cd Spatial exam
unzip data.zip
```
The data used in the assignment was downloaded from Børne- og Undervisningsministeriet (Child- and Teaching ministry) [education statistics](https://uddannelsesstatistik.dk/Pages/Reports/1895.aspx). The raw versions are available in the ```data/raw``` folder before any Excel preprocessing was applied. If the user cannot set an ```OpenCage``` and ```Mapboxapi``` key, all data produced by this script is available in the ```data``` folder. \
The folder structure must be the same as in the GitHub repository. The current working directory when running the script must be the one that contains the ```data``` and ```script``` folder. The script ```Youth_educations.rmd``` contain all code for this project. Running this script will generate all data and outputs of this project.\
\
All outputs of the script may be seen in the ```output``` folder. 

## Results
An interactive map was created with ```Leaflet``` and ```Mapboxapi``` allowing the user to see all youth education institutions in Denmark. The interactivity of the map allows the user to toggle visibility and thereby find relevant or irrelevant educations by municipality. It therefore serves as a tool from several different viewpoints. This project also found that VET educations were generally less available in several municipalities than GE educations. The availability of an education was specified as low if the distance to it from a municipality was greater than 50 kilometers. At least 23 out of 98 municipalities had low-access youth educations. These educations were primarily the Care, health and pedagogy and Food, agriculture and hospitality vocational educations.\
\
**Interactive map**

![image](/output/leaflet_static.png)

**Distance table**

![image](/output/distance_table.png)

**Nordjylland**

![image](/output/nordjylland_main.png)

![image](/output/nordjylland_group.png)

## References
Possenreide, D., Sadler, J., & Salmon, M. (2021). Introduction to opencage [R]. 
  https://cran.r-project.org/web/packages/opencage/vignettes/opencage.html

Walker, K. (2020, October 9). Penn MUSA Masterclass 2020. 
  http://walker-data.com/MUSAmasterclass/tutorial/#421_Obtaining_demographic_data_with_tidycensus

## Contact
Sarah Hvid Andersen (201910230) - 201910230@post.au.dk
