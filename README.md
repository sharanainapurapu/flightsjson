# Flights JSON

- Open https://www.json-generator.com/
- Copy paste the below code
- Click on generate 

```sh
[
  '{{repeat(1000)}}',
  {
    airlines: function () { 
      var airlines = [ 
        {
          id: 'spicejet',
          name: 'SpiceJet',
          logo: 'https://1000logos.net/wp-content/uploads/2021/07/SpiceJet-Logo.png'
        },
        {
          id: 'indigo',
          name: 'Indigo',
          logo: 'https://www.logo.wine/a/logo/IndiGo/IndiGo-Logo.wine.svg'
        },
        {
          id: 'goair',
          name: 'Go Air',
          logo: 'https://www.nextbigbrand.in/wp-content/uploads/2019/02/goair-e1550296161606.png'
        }, 
        {
          id: 'airasia',
          name: 'Air Asia',
          logo: 'https://upload.wikimedia.org/wikipedia/commons/f/f5/AirAsia_New_Logo.svg'
        },
        {
          id: 'airindia',
          name: 'Air India',
          logo: 'https://1000logos.net/wp-content/uploads/2020/09/Air-India-logo-1024x614.png'
        }
      ];      
      var minLength = 0;
      var maxLength = airlines.length - 1;
      return airlines[Math.ceil(Math.random() * (maxLength - minLength) + minLength)];
    },
    from: function () {
      var airports = [
        {
          "IATA_code": "MAA",
          "ICAO_code": "VOMM",
          "airport_name": "Chennai International Airport",
          "city_name": "Chennai"
        },
        {
          "IATA_code": "HYD",
          "ICAO_code": "VOHY",
          "airport_name": "Hyderabad International Airport",
          "city_name": "Hyderabad"
        },
        {
          "IATA_code": "DEL",
          "ICAO_code": "VIDP",
          "airport_name": "Indira Gandhi International Airport",
          "city_name": "New Delhi"
        },
        {
          "IATA_code": "BOM",
          "ICAO_code": "VABB",
          "airport_name": "Chhatrapati Shivaji International Airport",
          "city_name": "Mumbai"
        },
        {
          "IATA_code": "CJB",
          "ICAO_code": "VOCB",
          "airport_name": "Peelamedu Airport",
          "city_name": "Coimbatore"
        },
        {
          "IATA_code": "VGA",
          "ICAO_code": "VOBZ",
          "airport_name": "Vijayawada Airport",
          "city_name": "Vijayawada"
        },
        {
          "IATA_code": "BLR",
          "ICAO_code": "VOBG",
          "airport_name": "Bengaluru International Airport",
          "city_name": "Bangalore"
        }
      ];                            
      var minLength = 0;
      var maxLength = airports.length - 1;
      return airports[Math.ceil(Math.random() * (maxLength - minLength) + minLength)];
    },    
    to: function () {
      var airports = [
        {
          "IATA_code": "MAA",
          "ICAO_code": "VOMM",
          "airport_name": "Chennai International Airport",
          "city_name": "Chennai"
        },
        {
          "IATA_code": "HYD",
          "ICAO_code": "VOHY",
          "airport_name": "Hyderabad International Airport",
          "city_name": "Hyderabad"
        },
        {
          "IATA_code": "DEL",
          "ICAO_code": "VIDP",
          "airport_name": "Indira Gandhi International Airport",
          "city_name": "New Delhi"
        },
        {
          "IATA_code": "BOM",
          "ICAO_code": "VABB",
          "airport_name": "Chhatrapati Shivaji International Airport",
          "city_name": "Mumbai"
        },
        {
          "IATA_code": "CJB",
          "ICAO_code": "VOCB",
          "airport_name": "Peelamedu Airport",
          "city_name": "Coimbatore"
        },
        {
          "IATA_code": "VGA",
          "ICAO_code": "VOBZ",
          "airport_name": "Vijayawada Airport",
          "city_name": "Vijayawada"
        },
        {
          "IATA_code": "BLR",
          "ICAO_code": "VOBG",
          "airport_name": "Bengaluru International Airport",
          "city_name": "Bangalore"
        }
      ];  
      var minLength = 0;
      var maxLength = airports.length - 1;
      return airports[Math.ceil(Math.random() * (maxLength - minLength) + minLength)];
    }, 
    departure: function () {
      var startDate = new Date(); 
      var endDate = new Date(2021, 9, 1);
      return new Date(startDate.getTime() + Math.random() * (endDate.getTime() - startDate.getTime()));
    },       
    arrival: function() { 
      var arrivalDetails = new Date(this.departure);
      var hoursDiff = Math.ceil(Math.random() * 3);
      var minutesDiff = Math.ceil(Math.random() * 20);
      arrivalDetails.setHours(arrivalDetails.getHours() + hoursDiff);
      arrivalDetails.setMinutes(arrivalDetails.getMinutes() + minutesDiff);
      return arrivalDetails;                        
    },
    price: function () { 
      var minPrice = 2500;
      var maxPrice = 10000;
      return Math.ceil(Math.random() * (maxPrice - minPrice) + minPrice);
    }
    
  }
]
```

The above code generates an array of 1000 flight scheduled between current date and 1st of September 2021, with, each entry unique. If you are viewing this article anytime after 1st of September 2021, please go ahead and change the dates accordingly. 

```sh
  {
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
  }
```
