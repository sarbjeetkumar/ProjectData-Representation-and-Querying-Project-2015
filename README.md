## Project Title
####Data-Representation-and-Querying-Project-2015
##Name
####Sarabjeet Kumar

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

####This is the first entry in the dataset in JSON Format , This will give you the rough idea that how the data is laid out using the above headings.

```json
[{
    "ID"  :   1,
  " Area Description" : Chapel Street,
  "Road Name"  : Clonard Road ,
   "Area" :  North/south/east/west,
  "Total Spaces"  : 1,2,5,
  "Dipped footpath"  : True/F,
  "Park Sign"  :  True/False,
  "Road Marking"   :  True/False,
  "Occupied" : True/False,
  "Adjacent Services2"  : Cinema , Cafe , Housing,
  "Latitude" : 53.61029459,
  "Longitude" : -6.186854504,
    
},]
```

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
**GET**     |  The GET method is used to retrieve information from the given server using a given URI. Requests using GET should only retrieve data and should have no other effect on the data. 
**HEAD**    |   Same as GET, but transfers the status line and header section only.
**POST**    |   A POST request is used to send data to the server, for example, customer information, file upload, etc. using HTML forms.
**DELETE**  |  Removes all current representations of the target resource given by a URI.
**CONNECT** |  Establishes a tunnel to the server identified by a given URI.
**OPTIONS** |  Describes the communication options for the target resource.
**TRACE**   |  Performs a message loop-back test along the path to the target resource.





####Pulling the data from the dataset using GET Method , Recieving a list of all Disabled parking bays.

http://fingaldisabledparkingspaces.com/carpark-api/all

using "all" after ".../all/" will return an array of all the disabled car parks , in JSON format.


```json
[
    {
             "ID"  :   1,
      " Area Description" : "Chapel Street",
      "Road Name"  : "Clonard Road" ,
       "Area" :  North/south/east/west,
      "Total Spaces"  : 1,2,5,
      "Dipped footpath"  : True/F,
      "Park Sign"  :  True/False,
      "Road Marking"   :  True/False,
      "Occupied" : True/False,
      "Adjacent Services2"  : Cinema , Cafe , Housing,
      "Latitude" : 53.61029459,
      "Longitude" : -6.186854504,
    },
    {.......}
    
]
```
####Add 
######uniform resource locator 

        http://fingaldisabledparkingspaces.com/carpark-api/add?
   
######use Post Method


Field | Value
------|--------
**"ID"**   | id Number of that row
**" Area Description"**  |  Name of area
**"Road Name"**   |  Name of the road  
**"Area"*   |  North/south/east/west
**"Total Spaces"**  | How many spaces
**"Dipped footpath"**   | True/F
**"Park Sign"**  |  True/False
**"Road Marking"**   |  True/False
**"Occupied"**  | Yes/No
**"Adjacent Services2"**  | Cinema , Cafe , Housing
**"Latitude"**  | The long version of the latitute coordinates
**"Longitude"**  | The long version of the longtitute coordinates


This all feilds must be passed to the body of the request. which **Returns** a json object with response value .When you want to add a new disable car park.

**Response**

````
{
      "ID"  :   1,
      " Area Description" : "Chapel Street",
      "Road Name"  : "Clonard Road" ,
       "Area" :  North,
      "Total Spaces"  : 4,
      "Dipped footpath"  : True,
      "Park Sign"  :  True,
      "Road Marking"   :  True,
      "Occupied" : True/False,
      "Adjacent Services2"  : Cinema, 
      "Latitude" : 53.61029459,
      "Longitude" : -6.186854504,
}
````

####Update Method

#####uniform resource locator (url) <Structure>
    
         http://fingaldisabledparkingspaces.com/carpark-api/update?id=[id number]&fields=[fields]&values=[values]


#####using Put Method
    
    Field | Value
------|--------
**"ID"**   |  id number of that row you want to change
**" fields"**  |  fields you want to change in that row 
**"Values"**   |  The new values of the feilds you want to change/update 

Single values or multiple values can ba change at one time . To update the diable car parks in current area

#####Response
Returns a JSON bject with response is true/false . If the values provided matches with criteria.

```
{
    "response" : true,
    "id": 21,
    " Area Description" : "Chapel Street",
    "Road Name"  : "Clonard Road" ,

}


```


###Conclusion

Due to nature of that dataset , because this dataset belongs to the disable people car park . A user may not delete the entry because you have to give place for the people who needs special needs and user cannot delete that space which is reserverd for disable people.
    



  


