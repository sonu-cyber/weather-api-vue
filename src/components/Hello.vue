<template>
  <div class="hello">
    <h1>{{ msg }}</h1>

    <div v-for="data_arr in arr" :key="data_arr[0].id">
      Data.base:{{ data_arr[0].index }}
    </div>
  </div>
</template>

<script>
import { numberLiteralTypeAnnotation } from "@babel/types";

export default {
  name: "Hello",
  props: {
    msg: String,
    num: Number,
  },
  data() {
    result: [];
  },
  mounted() {
    //return{
    const card_0 = document.createElement("div");
    const card_1 = document.createElement("div");
    const card_2 = document.createElement("div");
    const card_3 = document.createElement("div");
    const card_4 = document.createElement("div");
    const card_5 = document.createElement("div");
    const card_6 = document.createElement("div");
    const card_7 = document.createElement("div");
    const card_8 = document.createElement("div");
    const card_9 = document.createElement("div");
    const card_10 = document.createElement("div");
    const card_11 = document.createElement("div");
    const card_12 = document.createElement("div");

    //Add classes to cards

    card_0.classList.add("card-0");
    card_1.classList.add("card-1");
    card_2.classList.add("card-2");
    card_3.classList.add("card-3");
    card_4.classList.add("card-4");
    card_5.classList.add("card-5");
    card_6.classList.add("card-6");
    card_7.classList.add("card-7");
    card_8.classList.add("card-8");
    card_9.classList.add("card-9");
    card_10.classList.add("card-10");
    card_11.classList.add("card-11");
    card_12.classList.add("card-12");

    //Define constants
    //const app = document.querySelector("#app");
    const array = [];

    //Define more constants
    const longitude = document.createElement("p");
    const latitude = document.createElement("p");
    //get the array of objects
    const arr_stations = document.createElement("div");
    const arr_id = document.createElement("p");
    const arr_main = document.createElement("p");
    const arr_description = document.createElement("p");
    const arr_icon = document.createElement("p");
    const arr_temp = document.createElement("p");
    const arr_temp_min = document.createElement("p");
    const arr_temp_max = document.createElement("p");
    const arr_feels_like = document.createElement("p");
    const arr_humidity = document.createElement("p");
    const arr_4 = document.createElement("p");
    const arr_speed = document.createElement("p");
    const arr_deg = document.createElement("p");
    const arr_gust = document.createElement("p");
    const arr_all = document.createElement("p");
    const arr_7 = document.createElement("p");
    const arr_id_8 = document.createElement("p");
    const arr_type = document.createElement("p");
    const arr_sunrise = document.createElement("p");
    const arr_sunset = document.createElement("p");
    const arr_country = document.createElement("p");
    const arr_9 = document.createElement("p");
    const arr_10 = document.createElement("p");
    const arr_11 = document.createElement("p");
    const arr_12 = document.createElement("p");

    const weather_api_res = async () => {
      try {
        const res = await fetch(
          "https://api.openweathermap.org/data/2.5/weather?q=london,uk&APPID=93dde9f3522583d6a4a162552949e8fe&units=metric"
        );
        console.log("res in json format is:", res);
        const data = await res.json();
        console.log("data about weather: ", data);
        //Get some data from the json o/new Promise(function(resolve, reject) {
        console.log("data.base: ", data.base);
        console.log("data.main: ", data.main);
        console.log("data.main.temp ", data.main.temp);
        console.log("data.weather.length: ", data.weather.length);
        // Get data printed on the browser
        //convert the object into an array
        const data_arr = Object.values(data);
        console.log("data_arr", data_arr);
        console.log("Stations: ", data_arr[2]);
        this.result = data_arr;
        //Loop through the array obtained from above
        data_arr.forEach((arr, index, data_arr) => {
          console.log("index", index);
          console.log("The array:", arr);
          console.log("data_arr[index]", data_arr[index]);
          if (index !== undefined) {
            if (index === 0) {
              if (arr !== undefined) {
              } //if index 0 ends
              //Get latitude & Longitude, index=0

              longitude.classList.add("longitude");
              if (arr.lon !== undefined) {
                longitude.textContent = `Longitude: ${arr.lon}`;
              }
              latitude.classList.add("latitude");
              if (arr.lat !== undefined) {
                latitude.textContent = `Latitude: ${arr.lat}`;
              }
            } //if index=0 ends
            //Get index=1
            if (index === 1) {
              for (let arr_obj in arr) {
                console.log("arr[arr_obj]is: ", arr[arr_obj]);
                console.log("arr[arr_obj].id", arr[arr_obj].id);
                arr_id.classList.add("arr-id");
                arr_id.textContent = `Id: ${arr[arr_obj].id} `;
                arr_main.classList.add("arr-main");
                arr_main.textContent = `Main: ${arr[arr_obj].main} `;
                arr_description.classList.add("arr-description");
                arr_description.textContent = `Desc: ${arr[arr_obj].description} `;
                arr_icon.classList.add("arr-icon");
                arr_icon.textContent = `Icon: ${arr[arr_obj].icon} `;
              }
            }
            //Get Object from index=2
            if (index === 2) {
              arr_stations.classList.add("arr-stations");
              arr_stations.textContent = `Base: ${arr}`;
            }
            if (index === 3) {
              arr_temp.classList.add("arr-temp-min");
              arr_temp.textContent = `Temp: ${arr.temp} `;
              arr_temp_min.classList.add("arr-temp-min");
              arr_temp_min.textContent = `Temp_Min: ${arr.temp_min} `;
              arr_temp_max.classList.add("arr-temp-max");
              arr_temp_max.textContent = `Temp_Max: ${arr.temp_max} `;
              arr_feels_like.classList.add("arr-feels-like");
              arr_feels_like.textContent = `Feels_Like: ${arr.feels_like} `;
              arr_humidity.classList.add("arr-humidity");
              arr_humidity.textContent = `Humidity: ${arr.humidity} `;
              console.log("arr.temp", arr.temp);
            }
            //index=4
            if (index === 4) {
              arr_4.classList.add("arr-4");
              arr_4.textContent = `Visibility: ${arr}`;
            }
            //index=5
            if (index === 5) {
              arr_speed.classList.add("arr-speed");
              arr_speed.textContent = `Wind Speed: ${arr.speed} `;
              arr_deg.classList.add("arr-deg");
              arr_deg.textContent = `Deg: ${arr.deg}`;
              arr_gust.classList.add("arr-gust");
              arr_gust.textContent = `Gust: ${arr.gust}`;
            }
            if (index === 6) {
              arr_all.classList.add("arr-all");
              arr_all.textContent = `Clouds: ${arr.all}`;
            }
            if (index === 7) {
              arr_7.classList.add("arr-7");
              arr_7.textContent = `Coord dt: ${arr}`;
            }
            if (index === 8) {
              arr_id_8.classList.add("arr-id-8");
              arr_id_8.textContent = `Id: ${arr.id} `;
              arr_type.classList.add("arr-type");
              arr_type.textContent = `Type: ${arr.type} `;
              arr_sunrise.classList.add("arr-sunrise");
              arr_sunrise.textContent = `Sunrise: ${arr.sunrise} `;
              arr_sunset.classList.add("arr-sunset");
              arr_sunset.textContent = `Sunset: ${arr.sunset} `;
              arr_country.classList.add("arr-country");
              arr_country.textContent = `Country: ${arr.country} `;
            }
            if (index === 9) {
              arr_9.classList.add("arr-9");
              arr_9.textContent = `Time Zone: ${arr}`;
              console.log(arr_9);
            }
            if (index === 10) {
              arr_10.classList.add("arr-10");
              arr_10.textContent = `Coord Id: ${arr}`;
              console.log(arr_10);
            }
            if (index === 11) {
              arr_11.classList.add("arr-11");
              arr_11.textContent = `City: ${arr}`;
              console.log(arr_11);
            }
            if (index === 12) {
              arr_12.classList.add("arr-12");
              arr_12.textContent += `Clouds Coord: ${arr}`;
              console.log(arr_12);
            }
            //Append to cards
            card_0.append(longitude, latitude);
            card_1.append(arr_id, arr_main, arr_description, arr_icon);
            card_2.append(arr_stations);
            card_3.append(
              arr_temp,
              arr_temp_min,
              arr_temp_max,
              arr_feels_like,
              arr_humidity
            );
            card_4.append(arr_4);
            card_5.append(arr_speed, arr_deg, arr_gust);
            card_6.append(arr_all);
            card_7.append(arr_7);
            card_8.append(
              arr_id_8,
              arr_type,
              arr_sunrise,
              arr_sunset,
              arr_country
            );
            card_9.append(arr_9);
            card_10.append(arr_10);
            card_11.append(arr_11);
            card_12.append(arr_12);
            app.append(
              card_0,
              card_1,
              card_2,
              card_3,
              card_4,
              card_5,
              card_6,
              card_7,
              card_8,
              card_9,
              card_10,
              card_11,
              card_12
            );
          } //if index undefined ends
        }); //forEach ends
      } catch (e) {
        console.log("Error occured", e);
      }
    }; //async ends
    weather_api_res();
    //} //return
  }, //data fn ends
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style>
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}
h1 {
  color: #6eaac5;
  margin: 20px;
  font-family: Georgia, "Times New Roman", Times, serif;
  border: none;
  padding: 20px;
}

#app {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  padding: 10px;
  margin: 10px 20px;
}

div > .p-h1 {
  display: flex;
  flex-direction: column;
  justify-content: center;
  text-align: center;
  color: #eb7842;
  font-size: 42px;
  padding: 10px;
  margin-bottom: 20px;
}

p {
  display: flex;
  flex-direction: column;
  font-size: 24px;
  font-family: Georgia, "Times New Roman", Times, serif;
}

.card-0,
.card-1,
.card-2,
.card-3,
.card-4,
.card-5,
.card-6,
.card-7,
.card-8,
.card-9,
.card-10,
.card-11,
.card-12 {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  width: 40vw;
  height: 40vh;
  padding: 10px;
  font-size: 28px;
  border-radius: 5px;
  box-shadow: 7px 7px #aaa;
  margin-bottom: 25px;
  transition: all 3s;
}

@media screen and (max-width: 1200px) {
  .card-0,
  .card-1,
  .card-2,
  .card-3,
  .card-4,
  .card-5,
  .card-6,
  .card-7,
  .card-8,
  .card-9,
  .card-10,
  .card-11,
  .card-12 {
    font-size: 24px;
    font-family: cursive;
  }
  p {
    font-size: 24px;
  }
  div > .p-h1 {
    font-size: 28px;
  }
}

@media screen and (max-width: 595px) {
  .card-0,
  .card-1,
  .card-2,
  .card-3,
  .card-4,
  .card-5,
  .card-6,
  .card-7,
  .card-8,
  .card-9,
  .card-10,
  .card-11,
  .card-12 {
    font-size: 20px;
    font-family: cursive;
  }
  p {
    font-size: 20px;
  }
  div > .p-h1 {
    font-size: 22px;
  }
}
@media screen and (max-width: 470px) {
  .card-0,
  .card-1,
  .card-2,
  .card-3,
  .card-4,
  .card-5,
  .card-6,
  .card-7,
  .card-8,
  .card-9,
  .card-10,
  .card-11,
  .card-12 {
    font-size: 18px;
  }
  p {
    font-size: 18px;
  }
  div > .p-h1 {
    font-size: 22px;
  }
}
@media screen and (max-width: 390px) {
  .card-0,
  .card-1,
  .card-2,
  .card-3,
  .card-4,
  .card-5,
  .card-6,
  .card-7,
  .card-8,
  .card-9,
  .card-10,
  .card-11,
  .card-12 {
    font-size: 16px;
  }
  p {
    font-size: 16px;
  }
  div > .p-h1 {
    font-size: 20px;
  }
}
@media screen and (max-width: 330px) {
  .card-0,
  .card-1,
  .card-2,
  .card-3,
  .card-4,
  .card-5,
  .card-6,
  .card-7,
  .card-8,
  .card-9,
  .card-10,
  .card-11,
  .card-12 {
    font-size: 14px;
  }
  p {
    font-size: 14px;
  }
  div > .p-h1 {
    font-size: 18px;
  }
}
@media screen and (max-width: 250px) {
  .card-0,
  .card-1,
  .card-2,
  .card-3,
  .card-4,
  .card-5,
  .card-6,
  .card-7,
  .card-8,
  .card-9,
  .card-10,
  .card-11,
  .card-12 {
    font-size: 12px;
  }
  p {
    font-size: 12px;
  }
  div > .p-h1 {
    font-size: 16px;
  }
}
@media screen and (max-width: 190px) {
  .card-0,
  .card-1,
  .card-2,
  .card-3,
  .card-4,
  .card-5,
  .card-6,
  .card-7,
  .card-8,
  .card-9,
  .card-10,
  .card-11,
  .card-12 {
    font-size: 10px;
    min-width: 50px;
    overflow: auto;
    border: none;
  }
  p {
    font-size: 8px;
  }
  div > .p-h1 {
    font-size: 10px;
  }
}

.card-0 {
  color: #92b767;
  border: 3px solid #a9dd6d;
}

.card-1 {
  color: #f5665b;
  border: 3px solid #f5665b;
}

.card-2 {
  color: #9e7d7b;
  border: 3px solid #9e7d7b;
}

.card-3 {
  color: #8e68d0;
  border: 3px solid #8e68d0;
}

.card-4 {
  color: #92b767;
  border: 3px solid #92b767;
}

.card-5 {
  color: #9575ce;
  border: 3px solid #9575ce;
}

.card-6 {
  color: #6eaac5;
  border: 3px solid #6eaac5;
}

.card-7 {
  color: #ceb467;
  border: 3px solid #ceb467;
}

.card-8 {
  color: #ca8c75;
  border: 3px solid #ca8c75;
}

.card-9 {
  color: #f5665b;
  border: 3px solid #f5665b;
}

.card-10 {
  color: #ceb467;
  border: 3px solid #ceb467;
}

.card-11 {
  color: #8bc34a;
  border: 3px solid #8bc34a;
}

.card-12 {
  color: #a18ebb;
  border: 3px solid #a18ebb;
}

.array-index {
  display: flex;
  justify-content: center;
  align-items: center;
  color: #2196f3;
}

.latitude,
.longitude {
  display: flex;
  justify-content: center;
  align-items: center;
}

.card-0:hover,
.card-1:hover,
.card-2:hover,
.card-3:hover,
.card-4:hover,
.card-5:hover,
.card-6:hover,
.card-7:hover,
.card-8:hover,
.card-9:hover,
.card-10:hover,
.card-11:hover,
.card-12:hover {
  transition-timing-function: ease-in-out;
  color: rgb(255, 102, 0);
  transform: scale(1.1);
}
</style>
