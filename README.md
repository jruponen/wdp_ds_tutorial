# Quick tutorial for Data Scientists

## Step 1: Create Project

1. Login to http://datascience.ibm.com
2. From top menu options, select Projects (All Projects)
3. Press Create Project and enter project details:
- Project name: Precipitation Analysis
- Description: Sample project
- Spark Service: (Select your Spark service instance from the dropdown list)
4. Leave other fields to defaults and press Create

## Step 2: Copy a sample Notebook from community to your project
1. From top memu options, select Community
2. Under Community, select Notebooks
3. In the Search field, enter "precip"
4. Click on the "Analyze precipitation data" notebook to open it
5. Quickly review what's in it and then select Copy option from the top
6. On the "Create Notebook" page, make sure you have selected
- your project "Precipitation Analysis"
- your spark instance
7. Press Create Notebook

## Step 3: Analyze data
1. From top menu options, select Projects
2. Select your project "Precipitation Analysis"
3. Note, that in your project you now have one notebook ("Analyze precipitation data") but no data assets
4. Open the notebook by clicking it
5. In the top row, select [Edit] button (pencil icon)

At this point you should notice that rest of the steps on below are also described in the notebook itself!

6. Open link https://cdsax.cloudant.com/public-samples/test/precipitation.csv to download sample data on your computer
7. In the top row, select [Find and Add Data] option (files tab will open on the right side)
8. Drag and drop the downloaded precipitation.csv file from your computer in this files tab
9. The data is now copied to the Object Storage behind the DSx
10. In the notebook, under "3. Access data" section you see an empty cell... place your cursor inside this cell
11. On the files tab, under precipitation.csv press the "Insert to code" drop down and select "Insert Pandas data frame"
12. You now have the data source defined in the cell... make the following changes
- Change the second last line from
    df_data_1 = pd.read_csv(get_object_storage_file_with_credentials
  to
   precipitation_df = pd.read_csv(get_object_storage_file_with_credentials
- Delete the last line
   df_data_1.head()
13. In the notebook menu select Cell > All Output > Clear
14. In the notebook menu bar there is a Run button, press it to execute the cell your cursor is currently at
15. Keep pressing the Run button one by one and watch the notebook cells being executed and the data being analyzed
