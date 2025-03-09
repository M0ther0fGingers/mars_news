# mars_news
Module 11 Challenge

The mars_news repo contains a folder with the jupyter notebook files, a Readme, and subfolder, Output. 

# part_1_mars_news.ipynb: 
This file contains the code to access and scrape the mars_news website.
 - A find_all function is used to access all text. 
 - A for loop extracts the titles and previews for each article from the text, then adds them to a dictionary.
 - A list is created to hold the extracted data. 
 - The list is printed and the browser closed. 

# part_2_mars_news.ipynb: 
This file contins the code to access and scrape the data from the mars rover, Curiosity.
 - Step 1: Access the website. created a variable url to store the website. 
 - Step 2: Scrape the website. 
   - Used Beautifulsoup to create an html.parser
   - A find_all is used to gather all the rows in attribute data-row.
 - Step 3: Store the data
   - A for loop extracts the individual cells from the rows and writes them to a dictionary. 
   - The dictionary is stored as a list and converted into a dataframe. 
   - The extraction step created tuple data. An extra step was added to split the tuples usisng a lambda function.
 - Step 4: The data types were converted to prepare for analysis. 
   - terrestrial_date was converted to datetime. 
   - sol, ls, and month were converted to integers. 
   - min_temp and pressure were converted to floats. 
 - Step 5: Analyze the data
   - This section uses .groupby and .mean functions to create graphs for deeper analysis followed by an written analysis. 
   - Note: According to the website science.nasa.gov, the Curiosity measures atmospheric pressure in the unit Pascals (Pa). Source: NASA (2012, November 15). Pressure Cycles on Mars. NASA.gov. Retrieved March 9, 2025, from https://science.nasa.gov/resource/pressure-cycles-on-mars/
 - Step6: The data is saved as a .csv file in the Output folder. 

# Output folder
Contains mars_news_2.csv which is the temps_list_df table. 