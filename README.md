# GetCustomerInformationsFromACMESystemViaUiPath
The robot gets customer informations from ACME System and writes it to Excel sheet.

Firstly, the robot gets the user information to log in to the ACME system (https://acme-test.uipath.com/login) from the user. The ACME system is a platform created by UiPath that stores different types of information for trials. You must have an ACME account for this process and beyond. The robot, which logs in with the user information it has received, goes to the Work Items tab on the main page and transfers the data to the data table with data scraping. 

![Work Items](https://user-images.githubusercontent.com/64749586/164914901-e6bdb2d5-c8a1-4083-9a46-a482f7342f87.JPG)

With Basic LinQ queries, the data in the data table is filtered. Data, where "Description" column is equal to "Calculate Client Security Hash" and "Type" column, is equal to "WI5" is filtered. For each filtered data, the "Work Item Details" page is accessed and the data gets with the "Get Text" activity. 

![Work Item Details](https://user-images.githubusercontent.com/64749586/164914928-a29be3d2-7a9c-4942-932e-9829c1abb72e.JPG)

The received data is saved in a new data table. The Date variable kept in the data table is written in the new column using Turkish month names. The saved data table is written to the Excel file.

![ACME çıktı excel](https://user-images.githubusercontent.com/64749586/164914938-17d59210-86b6-4bec-b076-871e66575588.JPG)
