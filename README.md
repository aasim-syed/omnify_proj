## Omnify  assigment |  Weather - React App | using weatherStack API

### This is the  proj i did with weatherStack API but none of the deploying platforms are able to access the API (Stackoverflow many peeps had same issue)

## Author:

- **A. Syed Aasim** - **[Portfolio Website](https://syed-aasim.vercel.app)**, **[Linkedin](https://www.linkedin.com/in/micheal-scott-fanboy/)**

## Images📷 (responsive as well lol)
![WhatsApp Image 2023-05-23 at 22 17 48](https://github.com/aasim-syed/omnify_proj/assets/70385414/5e55b18d-d087-4085-98e8-922337947eba)
![WhatsApp Image 2023-05-23 at 22 18 10](https://github.com/aasim-syed/omnify_proj/assets/70385414/3e7805f6-063b-45fe-81f0-1e7d6a1d5924)
![WhatsApp Image 2023-05-23 at 22 18 57](https://github.com/aasim-syed/omnify_proj/assets/70385414/f5e63473-b708-43e4-8cad-feba7fa31c0b)


## Duration breakdown 
- #### **Creation of the DisplayWeather.js : 1 hr (debugging and stuff)**
- #### **Creation of the Header : 30  mins (debugging and stuff)**
- #### **Building to fetch API from endpoint using JS : 1 hrs (debugging and stuff)**

#### **Fixing API on deployment : 1 hr (debugging and stuff)**
- #### **Final touches : 30 hr (debugging and stuff)**

### [Demo Link](https://omnify-proj.vercel.app/) 🔗




<br/>

## Techstack used and deployed on Vercel and netlify: 

- #### **React JS**
- #### **CSS **
- #### **weatherstack API**
- #### **NodeJS**


<br/>


<br/>

## Available Scripts:

#### `npm start`

#### `npm test`

#### `npm run build`

#### `npm run eject`

<br/>


``` const getWeatherData = async (latitude, longitude,city) => {
    try {
      const res = await axios.get(
        "http://api.weatherstack.com/current?access_key=e8d32583cba8ed6191c399efc7eb9c1a&query=" +
          city+
          latitude +
          "," +
          longitude
      );
      const data = res.data;
      console.log(res)
    setWeatherData({
        temperature: data.current.temperature ,
        description: data.current.weather_descriptions[0],
        location: data.location.name,
        region: data.location.region,
        country: data.location.country,
        wind_speed: data.current.wind_speed,
        pressure: data.current.pressure,
        precip: data.current.precip,
        humidity: data.current.humidity,
        img: data.current.weather_icons,
      });
      
    } catch (error) {
        console.log('no se pudo')
    }
    
    

  };



