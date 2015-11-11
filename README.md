# Project Title
##Data-Representation-and-Querying-Project-2015
#Name
###Sarabjeet Kumar

##Introduction
This project is using the dataset '**Disabled parking bays on streets and roads of the Fingal County Council**' which can be found at the following url https://data.gov.ie/dataset/disabled-parking-spaces. Although the data is only based on information from the Fingal county council.

##About the dataset.
The dataset is recived originally in the CSV (comma separated values) , and can be downloaded from url https://data.gov.ie/dataset/disabled-parking-spaces.

The data has 1186 rows , Which cover's all the disabled parking bays on streets and roads with the Fingal County Council administrative area. The dataset contains 12 columns.

**Type of information can be retrieved with each field**

Field | Value
------|--------
**"ID"**   |  1
**" Area Description"**  |  Chapel Street
**"Road Name"**   |  Clonard Road 
 **"Area"*   |  North/south/east/west
**"Total Spaces"**  | 1,2,5
**"Dipped footpath"**   | True/F
**"Park Sign"**  |  True/False
**"Road Marking"**   |  True/False
**"Occupied"**  | True/False
**"Adjacent Services2"**  | Cinema , Cafe , Housing
**"Latitude"**  | 53.61029459
**"Longitude"**  | -6.186854504

**For more information about fields you can click**  [Me] (https://data.gov.ie/dataset/disabled-parking-spaces)

####URL(Uniform Resource Locator)

https://data.gov.ie/disabled-parking-spaces/156

**url** | **Values**    | **url** |  **Values**
---------|------------|-----------------|----------
**http** | Protocal   |  **data.gov.ie** | domain name 
**disabled-parking-spaces** | Path    |   **Port** | 80
**156**  | Parameter |    


####Http Request methods.
***Methods* | **interpretation**
------------|---------------------
**Get**     |  The GET method is used to retrieve information from the given server using a given URI. Requests using GET should only retrieve data and should have no other effect on the data.        


####This is the first entry in the dataset in JSON Format , This will give you the rougph idea that how the data is laid out using the above headings.

```json
[{
    "ID"  :   1
  " Area Description" : Chapel Street
  "Road Name"  : Clonard Road 
   "Area" :  North/south/east/west
  "Total Spaces"  : 1,2,5
  "Dipped footpath"  : True/F
  "Park Sign"  :  True/False
  "Road Marking"   :  True/False
  "Occupied" : True/False
  "Adjacent Services2"  : Cinema , Cafe , Housing
  "Latitude" : 53.61029459
  "Longitude" : -6.186854504

},]
```
####Pulling the data from the dataset using , Recieving a list of all Disabled parking bays.










  


