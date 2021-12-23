# phase-1-project

PickTheDate app 
This web app helps friends to pick the best date to meet.

A User creates an event, adds a title, and selects a range of dates to select from.
Each user can open created event and select the days from the list when they can participate. 
The system shows the weather for each day to help the user to make a decision.
The system determines the most attendant day and shows how many people voted for it, and how many have participated
Also, the system displays the chart with aggregated data for each day (how popular is each day). The system also displays the table when each user who voted can attend the event. 

Each user name must be unique. Users can change or delete a participant from the event.


User Stories:
As User I can create an event and set the date range so other users can choose the date
As User I can select dates when I can participate in the event.
As User I can edit attendants data for each participant 
As User I can check the forecast for every day to make my decision easier
As User I can see a summary about each event (how many people participated and what is the most popular date)
As User I can delete participant record from the total scope
As User I can delete event
As user I can switch between events to check their attendance state




MVP:
1. As user I can create an event 
2. As User I can select dates 
3. As User I can see summary about the event 


Challenges:
1. Combine all together and build the project from the ground
2. Make the project look and feel professional. 
3. Create an HTML page the way it would be easier to manipulate elements from the DOM
4. Organized data in db.js the way it would be easier to work with it


Meet requirements: 
1. API: request weather forecase for dates
2. One HTML:
            there is nav bar with two tabs : "new event" and "view events" 
            when tab is selected the I will clean the innerHTML of main <div> and create new elements with JS
3. Listeners:   DOMContentLoaded, 
                click - switch between items in nav bar, 
                submit - form  when create new event and with user participation
3.Interactivity: 

5. Keep your code DR: do my best)). Use functions and object


API:
The weather forecast for particular data rande (from [start date] to [end date]) will be requested through API
From requested data, the max and min day temperature and the weather status (sunny, rainy) will be used  in the app.


API for the weather forecast for selected dates : 
https://rapidapi.com/aerisweather-aerisweather/api/aerisweather1/

{
  method: 'GET',
  url: 'https://aerisweather1.p.rapidapi.com/forecasts/cairo,eg',
  params: {from: '2021-12-24', to: '2021-21-20'},
  headers: {
    'x-rapidapi-host': 'aerisweather1.p.rapidapi.com',
    'x-rapidapi-key': 'SIGN-UP-FOR-KEY'
  }
};


Response data
{
"success":true
"error":NULL
"response":[
0:{4 items
"loc":{...}
"interval":"day"
"periods":[
0:{...}92 items
1:{...}92 items
2:{...}92 items
3:{...}92 items
4:{...}92 items
5:{...}92 items
6:{...}92 items
]
"profile":{
"tz":"Africa/Cairo"
"elevM":21
"elevFT":69
}
}
]
}