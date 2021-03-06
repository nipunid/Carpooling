# Carpooling
Carpooling is the sharing of car journeys so that more than one person travels in a car and prevents others from having to drive to a location themselves. Job employees here are specifically targeted.

# Description
Carpooling is an android and iOS application that manages everything from one area to another, making it easy for people to work together, with many benefits such as ease of transportation, saving money, reducing pollution, and reducing traffic congestion.

Many mobile apps can rent a vehicle online. But there is a substantial rental cost for the car. Also, if they use their own vehicle, it will take as much time as the cost of petrol. It takes more time as they get stuck in considerable traffic while traveling in their car. This will reduce the time-consuming process as the traffic congestion on the road will be significantly reduced when several people travel together for work in a vehicle.

#### Software Requirements
- React Native
- NodeJS
- MongoDB
- Visual Studio Code

#### Future Work
Develop the entire system by adding Add Admin Panel, Location sharing between users, Developing a strategy to send a notification message between passenger & Driver, etc.

#### Motivation
- This will help provide a proper process for the people going for employment to arrange the transport as required.
- Various types of mobile applications are used for transportation in Sri Lanka. Take uber, pick me, for example. But those apps do book their car. No mobile app has ever been designed to bring this kind of people together. This allows car owners to see where they are going and where they want to go after putting themselves into the area around them. It will enable you to build a relationship between the vehicle owner and the passenger and travel together with a group of people.

# Features
-  Email Authentication
-  After registering with the app, the user goes to the document adding the page, considering whether he is a driver or a passenger.
-  User Passenger goes to National Id & Profile photo adding page, and User driver goes to License & Profile Photo adding page.
-  The user can log in to the Home page.
-  You can fill in the details for the relevant day from the Home page. You can add those details separately as Passenger & Driver.
-  Email Verification,  Forgot Password, One-Time Password
-  If the user is a passenger through the Request Screen, he can add Pick Places and Drop Places and look at the drivers going to the area around him.
-  Others can be rated.
-  Total Hire can be calculated according to Distance.
-  User is a very useful application.
-  Android Version is a very simple and user-friendly application.
-  It can be used for the transportation of employees.

# Installation & Use Steps

#### Install
```
- expo install
- npm install
```
#### Run
- Download the Expo app on your phone after running *expo start* in VS code terminal 
```
- expo start
```
- After that scan, the QR code & can be set up on your mobile phone.

# Screenshots

1. Splash Page
<img src="https://github.com/nipunid/Carpooling/blob/main/Frontend_ReactNative/assets/splash.jpeg?raw=true" alt="drawing" style="width:150px;"/>

2. Login Page
<div>
<img src="https://github.com/nipunid/Carpooling/blob/main/Frontend_ReactNative/assets/Sign_in.jpeg?raw=true" alt="drawing" style="width:150px;"/>
</div>

3. Register Page
<div>
  <img src="https://github.com/nipunid/Carpooling/blob/main/Frontend_ReactNative/assets/Signup_01.jpeg?raw=true" alt="drawing" style="width:150px;"/>
  <img src="https://github.com/nipunid/Carpooling/blob/main/Frontend_ReactNative/assets/Signup.jpeg?raw=true" alt="drawing" style="width:150px;"/>
</div>

4. Home Page
<div>
  <img src="https://github.com/nipunid/Carpooling/blob/main/Frontend_ReactNative/assets/Home_03%20(3).jpeg?raw=true" alt="drawing" style="width:150px;"/>
  <img src="https://github.com/nipunid/Carpooling/blob/main/Frontend_ReactNative/assets/Home_04.jpeg?raw=true" alt="drawing" style="width:150px;"/>
</div>

5. Request Page
<div>
  <img src="https://github.com/nipunid/Carpooling/blob/main/Frontend_ReactNative/assets/Add_01.jpeg?raw=true" alt="drawing" style="width:150px;"/>
  <img src="https://github.com/nipunid/Carpooling/blob/main/Frontend_ReactNative/assets/Destination.jpeg?raw=true" alt="drawing" style="width:150px;"/>
  <img src="https://github.com/nipunid/Carpooling/blob/main/Frontend_ReactNative/assets/Destination_02.jpeg?raw=true" alt="drawing" style="width:150px;"/>
</div>

6. Places Auto Complete page, Rating & Calculate Hire Page
<div>
  <img src="https://github.com/nipunid/Carpooling/blob/main/Frontend_ReactNative/assets/googleplace_02.jpeg?raw=true" alt="drawing" style="width:150px;"/>
  <img src="https://github.com/nipunid/Carpooling/blob/main/Frontend_ReactNative/assets/rate_03.jpeg?raw=true" alt="drawing" style="width:150px;"/>
  <img src="https://github.com/nipunid/Carpooling/blob/main/Frontend_ReactNative/assets/calculate_03.jpeg?raw=true" alt="drawing" style="width:150px;"/>
  
</div>

# Schemas
#### users
```
{
  name: String,
  email: String,
  password: String,
  address: String,
  roles: [String] // enum 'passenger', 'driver', 'admin',
  identityCard: String // photo url
  drivingLicense: String // photo url
}
```

#### vehicles
```
{
  type: String, // enum 'motorbike', 'threewheeler', 'bus', 'car', 'van', 'suv',
  passengers: Number,
  registrationCert: String // photo url
}
```

#### rides
```
{
  type: String // enum 'passenger', 'driver'
  user: ObjectId,
  from: {
    lat: Number, 
    lon: Number
  },
  to: {
    lat: Number, 
    lon: Number
  },
  passengers: Number,
  time: Date
}
```

#### reviews
```
{
  user: ObjectId,
  about: ObjectId,
  rating: Number,
  comment: String
}
```
