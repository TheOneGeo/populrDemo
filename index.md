<h1 align="center">populr.uk Demo</h1>
<p align="center">
populr provides nightclubs with data analytics and monthly breakdowns while also streaming real-time data to clubbers, allowing them to better plan their evening. 
</p>

<p align="center">
Like most start-ups, this one was born from a problem, not knowing when to go to a nightclub. Too early and you will be forced to pay for expensive drinks in an empty venue, and too late and you will be forced to stand in line, a cold affair in the UK. 
</p>

<p align="center">
The start-up is ready to launch, and I already have over ten subscribed nightclubs. However, finding the right time to launch can be difficult because the nightclub industry has been heavily affected by the Coronavirus pandemic.  
</p>

<p align="center">
To best demonstrate how it works, I will break it into two parts: the nightclub facing side and the user side.  
</p>

<h2 align="center">Nightclub-Facing</h2>

<p align="center">
To allow nightclubs to record data throughout the night easily, I created an Android app that was designed to be easy to use. The app was developed using Flutter and is run on Android devices we provide to nightclubs. They choose how to use them, although most commonly they give the phones to the people working at the doors. They can increment and decrement the occupants and provide estimates for the length of the line. At the request of the nightclubs, I added the functionality to count males and females separately; however, this information is just for estimated analytical purposes and is never shared with the general public. The app was designed to allow multiple sources of data manipulation as some nightclubs have multiple entrances, so the app sends increment or decrement GraphQL mutations and never directly change the count.
</p>

<p align="center">
First, nightclubs have to log in with pre-assigned credentials. 
</p>

<p align="center">
  <img src="https://user-images.githubusercontent.com/24978137/146473514-f27bee3d-ad21-44f5-a2bc-28db91284c8d.png">
</p>

<p align="center">
Then they are met with their mobile dashboard, where the number of occupants is clearly visible along with buttons that allow them to increment and decrement. 
</p>

<p align="center">
  <img src="https://user-images.githubusercontent.com/24978137/146473509-aff23fff-d13d-43b3-b4e9-bdd4d16cfdd1.png">
</p>

<p align="center">
A swipe left allows nightclubs to mutate the value of their estimated queue length. We also give them the option to change the value that they increment and decrement by, as some venues are larger than others.
</p>

<p align="center">
  <img src="https://user-images.githubusercontent.com/24978137/146473512-81df559a-5cfc-499b-8f85-6b57be33c0a8.png">
</p>

<p align="center">
This allows for easy expansion. If a new nightclub joins, all I need to do is send them some Android phones and give them login credentials. We collect and store all of this data and then provide monthly reports that contain monthly, weekly and daily breakdowns and comparisons with visualisations that allow nightclubs to run their business better. 
  
Instead of relying on analytics tools such as Google Analytics, I created a script which collects only a limited amount of user information. The script posts that data to a MongoDB database which specific nightclubs can then view on their dashboard. By not using third-party solutions, I can split the data by nightclub and serve it directly to them as a feature. 
  
Giving nightclubs KPIs and supporting visualisations will provide them with insights into their business and ideas for improving it. 
</p>

<img align="center" src="https://user-images.githubusercontent.com/24978137/204086493-500ff4d7-2913-41ed-9796-917674c38245.png">
<img align="center" src="https://user-images.githubusercontent.com/24978137/204086533-153a6ace-bd93-448a-8239-2c690166b1c5.png">
<img align="center" src="https://user-images.githubusercontent.com/24978137/204086685-a7cbac3a-f639-4be3-a81c-7898b81cbc50.png">

<h2 align="center">User-Facing</h2>

<p align="center">
The user-facing side does not have an app yet but instead has a webpage created using React. Using GraphQL subscriptions to supply users with real-time data, they receive the most up-to-date information about every nightclub that has subscribed. 
</p>

<video align="center" src="https://user-images.githubusercontent.com/24978137/146474559-204ea1e9-c838-4509-acbf-691db4049d87.mp4">
</video>

<h2 align="center">Primary Technologies Used</h2>

<p align="center">
Flutter, React, GraphQL, AWS: Kinesis, DynamoDB, Amplify, AppSync, Cognito, S3
</p>


