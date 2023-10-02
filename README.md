# News-Feed Jetpack Components
App demonstrating Clean Architecture using Coroutines and Android Jetpack Components (Room, MVVM Paging, Navigation Components and Live Data).
This is a News-Feed app that keeps the user updated on current news throughout the day. In this project, the components listed below are the ones we used for each spectrum of the project.
Overall, this project was done in Kotlin since we aimed to make an Android App.


# ScreenShots

<img src = "https://github.com/kanch231004/News-Feed/blob/master/screenshots/NewsList%20Page.jpg" width = 260 height = 550/> <img src = "https://github.com/kanch231004/News-Feed/blob/master/screenshots/News%20Detail%20Page.jpg" width = 260 height = 550/>

These screenshots show what the Android app will look like.
These images will update based on the current state of the news is.

# Tech-Stack

* __Retrofit__ : For Network calls
* __Architecture__ : MVVM
* __Coroutines__ for background operations like fetching network response
* __Room database__ : For offline persistence and Paging Library
* __Live Data__ : To notify view for change
* __Dagger__ : For dependency injection
* __Language__ : Kotlin

# Description of functionalities
* __MainActivity.kt__: This file handles API network calls in the Android app. It makes an API call and if it is successful, it returns the result which is the Jetpack Components. Otherwise, it logs it out. 

* __NewsApp.kt__: This file defines the Android app and has the @HiltAdroidApp annotation which indicates it is part of its dependency injection setup. It also initializes the Stetho library for debugging.

* __api/Data.kt__: This file provides data for displaying the listings for the user interface. the pagelist holds items for the user to observe and the network state represents the network request status.

* __api/ResponseModel.kt__: Creates classes for the news data that is later going to be displayed. They represent news articles, their sources, and the news API's response data.

* __api/Status.kt__: Has subclasses that represent the different network states in the app.

* __common/GlideAppModule.kt__: This file configures Glide which is used for image loading for the Android App. It makes sure that the images change when the content is updated.

* __newsSet/AppDatabase.kt__: This file is responsible for managing and getting access to local databases that have news data.
  
# Running the program
1. Install Kotlin through https://kotlinlang.org/docs/tutorials/command-line.html
2. Clone this repository
3. Compile in terminal using this command
`kotlinc MainActivity.kt -include-runtime -d MainActivity.jar`
4. Run the JAR file `java -jar MainActivity.jar`
5. You finally have the app running

# Architecture Diagram
This application strictly follows the below architecture 

<img src = "https://github.com/kanch231004/News-Feed/blob/master/screenshots/Architecture.png" width = 450 />

# API Key
Get your api key from here https://newsapi.org/

Follow instructions in build-gradle (app) to integrate API key to build the project.
