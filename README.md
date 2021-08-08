# Flights JSON
##### _- You are a click away from generating the JSON required for list of scheduled flights_
#
[![Available Flights](https://images.financialexpress.com/2019/02/airfares.png)](https://images.financialexpress.com/2019/02/airfares.png)

##### Steps to generate array of scheduled flights with size n (n is default set to 1000)
- Open https://www.json-generator.com/
- Copy the code from flightsDataGenerator file and paste it into the editor (json-generator.com)
- Click on generate 


The above code generates an array of 1000 flight scheduled between current date and 1st of September 2021, with each entry unique. If you are viewing this article anytime after 1st of September 2021, please go ahead and change the dates accordingly. Please review docs section for more information. 
 
### DOCS
##### Sample Data with n=1
n denotes total number of scheduled flights data that you want in an array
```sh
 [{
    "airlines": {
      "id": "airindia", 
      "name": "Air India",
      "logo": "https://1000logos.net/wp-content/uploads/2020/09/Air-India-logo-1024x614.png"
    },
    "from": {
      "IATA_code": "HYD",
      "ICAO_code": "VOHY",
      "airport_name": "Hyderabad International Airport",
      "city_name": "Hyderabad"
    },
    "to": {
      "IATA_code": "BOM",
      "ICAO_code": "VABB",
      "airport_name": "Chhatrapati Shivaji International Airport",
      "city_name": "Mumbai"
    },
    "departure": "2021-09-14T23:07:02.050Z",
    "arrival": "2021-09-15T01:21:02.050Z",
    "price": 3654
  }]
```

| Key | Description |
| ------ | ------ |
| airlines | Randomly generated object that is picked up from array of airlines configured. Complete list of airlines is available in airlines file [/airlines][PlDb] |
| from | Randomly generated object that is picked up from array of airports configured. Complete list of airlines is available in airlines file [/airports][PlGh] |
| to | same as from key |
| departure | Departure data and time is randomly generated between today and the end day that you configure |
| arrival | Arraival is randomly calculated by adding few hours to the departure time  |
| price | Price is generated based on min and max value that you configure within the function |


Mentions:
Airport data collected from https://github.com/ashhadulislam/JSON-Airports-India/edit/master/airports.json
