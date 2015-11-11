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
