# Data-rep-project
#### Name: Conor Tighe.

## Overview:

In this respiratory I will be describing how I would design an API, the concepts for this project will be based around the
[App4Gaps competition](https://www.youtube.com/watch?v=M2WpRGjqpaM). The data and direction of the API will be taken from [This Irish government source](https://data.gov.ie/data). The API enables the data to be retrieved and manipulated in real time, I will not be implementing the API or making a app for it in this respiratory.

---

## Protocol:

The protocol used is HTTP, otherwise known as The Hypertext Transfer Protocol. This is the basses for all world wide web communication and how servers and clients interact. When the URL in entered into the browser, a command is sent to a web server to find the requested web page and then return it.

---

## Dataset:

The data that my API will provide will be based around Galway City facility's that are available to the public. The first dataset is Galway City Tennis Courts, This will supply relevant information on the location to who ever may need it through the API. The second dataset will be Galway City Basketball Courts which will supply the location too. Both datasets come in .CSV format. Both CSV and JSON files of the data can be found above.

### Key/Values:

####      BasketBall-
|     Key    |     Value     |
| :--------: | :-----------: |
|  OBJECTID  |   Unique ID   |
|     X      |    X Pos      |
|     Y      |    Y Pos      |
| BCOURTLOC  |   Location    |
| Lat        |  latitude     |
| Long       | longitude     |
| EastITM    | Inter_Mapping |
| NorthITM   | Inter_Mapping |
| EastIG     |  Mapping      |
| NorthIG    |  Mapping      |


####      Tennis-
|     Key    |     Value     |
| :--------: | :-----------: |
|  OBJECTID  |   Unique ID   |
|     X      |    X Pos      |
|     Y      |    Y Pos      |
| TCOURTLOC  |   Location    |
| Lat        |  latitude     |
| Long       | longitude     |
| EastITM    | Inter_Mapping |
| NorthITM   | Inter_Mapping |
| EastIG     |  Mapping      |
| NorthIG    |  Mapping      |
                    
                    
                    

---

## Audience:

My API will target a young audiance. Since Galway City is famous for being largely populated by students this API would reach out to the ones who want to exercise, pass time and save money. This data could also branch off into children, familys, athletes etc.

---

## HTTP Methods:

There are a number of methods available in HTTP to manipulate a dataset. I will be covering the ones relivent to my API below.


| GET | Retrieve filtered data |
| :---|----------------------- |

The following URL will search for a tennis court by ID: http://galwayCourts.com/Tennis/id=1

#### Result:

```javascript
 {
    "X":-9.047858919161463,
    "Y":53.293817364909,
    "OBJECTID":1,
    "TCOURTLOCN":"Crestwood, Ballinfoyle",
    "Lat":53.293817,
    "Long":-9.04786,
    "EastITM":530141.785686,
    "NorthITM":727569.417144,
    "EastIG":130175.933245,
    "NorthIG":227540.743063
  },
```

The datasets can be combined to search for locations with both courts: http://galwayCourts.com/Tennis+Basketball/TCOURTLOCN+BCOURTLOCN="Westside+Sports+Ground"

#### Result:

```javascript
 {
    "X":-9.078127993983678,
    "Y":53.27598037081983,
    "OBJECTID":3,
    "TCOURTLOCN":"Westside Sports Ground",
    "Lat":53.27598,
    "Long":-9.078129,
    "EastITM":528093.953805,
    "NorthITM":725614.783135,
    "EastIG":128127.665587,
    "NorthIG":225585.677502
  },
  
   {
    "X":-9.077736823020551,
    "Y":53.27609987826149,
    "OBJECTID":1,
    "BCOURTLOCN":"Westside Sports Ground",
    "Lat":53.276,
    "Long":-9.078,
    "EastITM":528080.679,
    "NorthITM":725654.603,
    "EastIG":128114.388,
    "NorthIG":225625.506
  },
```

| POST | Send details |
| :----|---------- |

The edition of an admin to oversee the datasets could be implemented using POST, the admin could login with this URL:
http://galwayCourts.com/login

```javascript
 {
    "Username": admin,
    "Password": myPassword
  },
```

The admin could add or remove items from the dataset if a court was opened or closed using the methods and URLs below:
http://galwayCourts.com/Tennis/new
http://galwayCourts.com/Basketball/delete

| POST | Add new court |
| :----|-------------- |

| DELETE | Remove court |
| :----|--------------- |

---
