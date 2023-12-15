# iaxo-axion-limits
IAXO Axion Limits

The purpose of this website is to document a summer internship at the University of Zaragoza in the field of nuclear and particle physics, specifically within the axions group. During the internship, improvements were made to the code for plotting experiments, and an interactive application was created to label the graphs.

The graphs presented here are the results of the code, featuring the Axion Photon Coupling without its projections.

**Creator: Daniel Martinez Miravete**

# Basic Plot
---
[<img align="right" height="250" src="Javat/plots/Labeled/AxionPhoton_large_panorama.svg">](https://github.com/DanielMartinezMiravete/Axion_Limits_Memory/blob/main/Javat/plots/Labeled/AxionPhoton_large_panoramalabeled.svg)

## Basic plot without proyections

### [Download (.pdf)](https://github.com/DanielMartinezMiravete/Axion_Limits_Memory/blob/main/Javat/plots/Labeled/AxionPhoton_large_panoramalabeled.pdf)
### [Download (.png)](https://github.com/DanielMartinezMiravete/Axion_Limits_Memory/blob/main/Javat/plots/Labeled/AxionPhoton_large_panorama.png)
### [Download (.svg)](https://github.com/DanielMartinezMiravete/Axion_Limits_Memory/blob/main/Javat/plots/Labeled/AxionPhoton_large_panorama.svg)

### &nbsp;

# Close up General Plot
---
[<img align="right" height="250" src="Javat/plots/Labeled/AxionPhoton_panorama.svg">](https://github.com/DanielMartinezMiravete/Axion_Limits_Memory/blob/main/Javat/plots/Labeled/AxionPhoton_panoramalabeled.svg)

## Close up General plot without proyections

### [Download (.pdf)](https://github.com/DanielMartinezMiravete/Axion_Limits_Memory/blob/main/Javat/plots/Labeled/AxionPhoton_panoramalabeled.pdf)
### [Download (.png)](https://github.com/DanielMartinezMiravete/Axion_Limits_Memory/blob/main/Javat/plots/Labeled/AxionPhoton_panorama.png)
### [Download (.svg)](https://github.com/DanielMartinezMiravete/Axion_Limits_Memory/blob/main/Javat/plots/Labeled/AxionPhoton_panorama.svg)

### &nbsp;

# Close up Helioscopes Plot
---
[<img align="right" height="250" src="Javat/plots/Labeled/AxionPhoton_helioscopes.svg">](https://github.com/DanielMartinezMiravete/Axion_Limits_Memory/blob/main/Javat/plots/Labeled/AxionPhoton_helioscopes.svg)

## Close up Helioscopes plot without proyections

### [Download (.pdf)](https://github.com/DanielMartinezMiravete/Axion_Limits_Memory/blob/main/Javat/plots/Labeled/AxionPhoton_helioscopeslabeled.pdf)
### [Download (.png)](https://github.com/DanielMartinezMiravete/Axion_Limits_Memory/blob/main/Javat/plots/Labeled/AxionPhoton_helioscopes.png)
### [Download (.svg)](https://github.com/DanielMartinezMiravete/Axion_Limits_Memory/blob/main/Javat/plots/Labeled/AxionPhoton_helioscopes.svg)

### &nbsp;
# Close up Halocopes Plot
---
[<img align="right" height="250" src="Javat/plots/Labeled/AxionPhoton_haloscopes.svg">](https://github.com/DanielMartinezMiravete/Axion_limts_Mermory/blob/main/Javat/plots/Labeled/AxionPhoton_haloscopes.svg)

## Close up Haloscopes plot without proyections

### [Download (.pdf)](https://github.com/DanielMartinezMiravete/Axion_Limits_Memory/blob/main/Javat/plots/Labeled/AxionPhoton_haloscopeslabeled.pdf)
### [Download (.png)](https://github.com/DanielMartinezMiravete/Axion_Limits_Memory/blob/main/Javat/plots/Labeled/AxionPhoton_haloscopes.png) 
### [Download (.svg)](https://github.com/DanielMartinezMiravete/Axion_Limits_Memory/blob/main/Javat/plots/Labeled/AxionPhoton_haloscopes.svg)
For the haloscopes, there are additional graphs zooming in on different areas.
### &nbsp;

---

To recreate these images, we need to execute the Python program called "PlotAxionPhoton.py" as follows:
```
python3 PlotAxionPhoton.py    #To plot all the plots from Axion Photon 
```
This will plot all types of graphs listed without their projections. To include the projections, we should modify the "Projections" parameter in PlotAxionPhoton.py and set it to True.
These graphs are generated directly without labels since we have a web application capable of adding them interactively, if you want to generated them with labels on it, we had to go to the script called AxionPlot and decomment the line 90.

([Label's APP]([http://htmlpreview.github.io/?https://github.com/DanielMartinezMiravete/Axion_Limits_Memory/blob/main/Javat/index.html](https://danielmartinezmiravete.github.io/Labels-App/)))

You can start the app by opening the HTML script called 'index.html'
This application is only capable of modifying SVG files, which are generated automatically along with the PDFs when running the Python script. Instructions for the webpage are provided within the webpage itself.

There are known bugs such as the app cannot interpret LaTeX. If you have several labels on it and if you want to move a label other than the last label, the coordinates will replace the coordinates of the last label written

As additional information, to interact with the database, you need to use different functions implemented in the script called 'DataBaseGag.py'.
This repository contains Python scripts for interacting with the AxionsGag database. The database is used to manage information about various experiments related to axion research. Below, you'll find instructions on how to use the provided functions to work with the database.

## Function Descriptions

1. **CreateDB():**
   - Use this function to create the AxionsGag database if it doesn't exist.
   - Call it only once to initialize the database.

2. **CreateTable():**
   - This function is used to create a table called "Axions" inside the database.
   - You should call it once to set up the table structure.

3. **InsertRow(name, type, path, LP, P, Helios, Halos, LSW, projection):**
   - Insert a single row into the "Axions" table.
   - Provide values for columns like name, type, path, large_panorama, panorama, helioscopes, haloscopes, lswexps, and projection.

4. **ReadRows():**
   - Retrieve and print all rows from the "Axions" table.
   - Displays all data stored in the table.

5. **InsertRows(axionexps):**
   - Insert multiple rows into the "Axions" table at once.
   - Provide a list of lists (axionexps) where each inner list represents a row of data.

6. **ReadOrdered(field):**
   - Retrieve and print rows from the "Axions" table sorted by a specified field.
   - Pass a field name as an argument to sort the rows in ascending order based on that field.

7. **Search(field, token):**
   - Search for rows in the "Axions" table that match specific criteria.
   - Provide a field name and a token value to find matching rows based on that criteria.
   - Returns a list of lists with matching data.

8. **Search_Names(field, token):**
   - Similar to the Search function but returns a list of names (the first column) of matching rows.

9. **Update(name, field, value):**
   - Update a specific field's value in a row with a given name.
   - Specify the name of the row, the field to update, and the new value.

10. **DeleteRow(name):**
    - Delete a row from the "Axions" table by specifying the name of the row to delete.

## Getting Started

To interact with the database, follow these steps:

1. Download the repository and navigate to the appropriate directory.
2. Make sure you have SQLite installed or install it if necessary.
3. Modify the file paths in the script to match your directory structure.
4. Uncomment the function calls at the end of the script to execute them and interact with the database.

Please refer to the script for specific usage examples of each function.

## Known Issues

- The application cannot interpret LaTeX.
- When working with multiple labels, moving a label other than the last label will replace the coordinates of the last label written.

