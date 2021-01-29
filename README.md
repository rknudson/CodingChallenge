# CodingChallenge

## Overview
This is a coding challenge that is intended to give a high level overview of some basic tech skills. By the end of it, if you have succeeded you will have a Single Page Angular application that calls a .Net Core endpoint and fetches some hard-coded data. 

## Prerequisites
- You will need the following installed before you get started
	- [DotNet core SDK](https://download.visualstudio.microsoft.com/download/pr/75483251-b77a-41a9-9ea2-05fb1668e148/2c27ea12ec2c93434c447f4009f2c2d2/dotnet-sdk-5.0.102-win-x64.exe)
	- A [git client](https://git-scm.com/downloads)
	- [Visual Studio Code](https://code.visualstudio.com/)

## The Challenge
Follow these steps one at a time. 

### Clone the Repo
In this section, you will 
- Clone this repository
- Create a new branch that is named your name
### Create an App
In this section, you will create a .Net Core API and an Angular SPA
- Follow [these instructions](https://docs.microsoft.com/en-us/aspnet/core/client-side/spa/angular?view=aspnetcore-5.0&tabs=netcore-cli) to Create a new app
	- Use the .Net Core CLI tab to run your app (not Visual Studio)
	- You can stop once you reach the section titled "Run ng commands" 
	- Once you are done, you should have an application that shows a few tabs running locally

### Create a Page
In this section, you will add a new API Endpoint and a new page to the application you crated before. 
- Create an endpoint
	- Create a new Controller. You can Copy `WeatherForecastController.cs` and Rename it, and all it's contents to `ChallengeController`
	- Create a new POCO (Similar to WeatherForecast) called `Challenge` with the properties `Message` of type string and `TodaysDate` of type DateTime
	- In the GET method for `ChallengeController.cs` return a new `Challenge` object that has today's date for the `TodaysDate` property and "Hello World" for the `Message` property 
- Create a component
	- Copy the `fetch-data` component from the angular app and paste a copy into the `app` folder. Rename the copied contents `fetch-challenge`
	- In the new Component, change the `WeatherForecast` interface to match your `Challenge` interface from the server
	- Change all things `WeatherForecast` to `Challenge` 
	- In the HTML, change the table to render `todaysDate` and `message`
	- Add a new route `fetch-challenge` that renders your component 
	- Add a link in the header that navigates to your route

### Test your app
Once you've done all these steps, you will likely need to restart your server. Adding a new server endpoint will mean that it will need to be restarted. Once you restart your server, navigate to the `localhost` URL it provides and make sure that your new page renders Today's Date, as well as the Hello World message.
### Submit your Code
Now that your app is done and tested, commit your changes and push the branch to the remote git server. 

## Congratulations! 
Sit back and take pride in your accomplishments! 