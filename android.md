# Q-Quatics FishBase Guide

## Technical Documentation

### GETTING STARTED

Q-Quatics FishBase Guide Android was developed using Android Studio. This project uses Kotlin as the Programming Language, Android Studio Layout Editor for the Interface, and Gradle for connecting different Third-Party Libraries. The target and compiled SDK Version is 30 with a minimum SDK version of 26.
For more information on the IDE and system requirements to enable you to work on the source code, it is available [here](https://developer.android.com/)

### INSTALLATION AND DEVELOPMENT

In order to start the development, first you need to start Android Studio. Import the Q-Quatics FishBase Guide project and then wait for the build to finish.

### PROGRAMMING LANGUAGE

Q-Quatics FishBase Guide Android uses Kotlin for development

### MINIMUM VERSION

Q-Quatics FishBase Guide can run on Android Systems with minimum SDK version 26. It may encounter multiple issues on lower SDK versions.

### APPLICATION ID

se.fishbase.qquatics

### DEBUGGING

We use a few debugging tools to test Q-Quatics FishBase Guide functionalities.
We also use Android Virtual Device in Android Studio in order to test the Native Apps in different screen sizes and SDK Versions. 

<!-- ### WEB API
Giga Play Web API -->

### THIRD-PARTY LIBRARIES

Most of the third-party libraries are integrated using Gradle. They can be added by searching library names found in the Dependencies tab in the Project Structure window.

##### Important Libraries
**Android Lifecycle** - Used to manage data and connections between activities and fragments.
**Google Play Services** - Used for SMS Retriever and Auto-update features.

##### Firebase Platform Libraries.
**Firebase/Analytics** - Used for App Analytics.
**Firebase/Crashlytics** - Used to identify causes of crashes from users.
**Firebase/Performance** - Used to monitor app performance.
**Firebase/Firestore** - Used to store and sync data in real-time for mobile apps.

##### UI Libraries
**Glide** - Used for displaying images.
**Pagination** - Used to display multiple query data in a page-like structure.
**Jetpack Compose** - Used for simplifying the navigation between fragments. 

##### Other Useful Libraries 
**Android Navigation: Kotlin** - Used to manage connections between different screens and layouts.
**Esperando & GSON** - Used to connect shared data between activies.
**Dagger-Hilt** - Used for easier data management between activities.
**Karumi/Dexter** - Used to simplify permission requests and access.
**Coroutine** - Used to execute code asyncronously.

### IMPORTANT CLASSES

#### Activities/Fragments

- **MainActivity** - handles the main activity container which will display all the core.

- **Splash Screen Fragment** - handles the display of the splash screen logo that appears on every start up.
  ##### Fragment/ViewModel Methods

- **Choose Location Fragment** - handles the display where users will select a country or choose to use their current location provided they have location services.
  ##### Fragment/ViewModel Methods
  - `checkIfDownloaded()`
  - `checkPermission()`
  - `showCountryChooser()`
  - `fetchAllCountries()`
  - `searchCountries()`
  - `checkLocationPermission()`
  - `checkIfGpsIsEnabled()`
  - `fetchIso3Code()`
  - `filterCountry()`
  - `addCountriesToDB()`
  
- **Choose Country Fragment** - handles the display where users will choose their country on a drop-down list.
  ##### Fragment/ViewModel Methods
  
- **Search Fragment** - handles the display where users can input the name and search for the fish and their species that are native to the selected country.
  ##### Fragment/ViewModel Methods
  - `getAppVersion()`
  - `fetchSpeciesByCountryCode()`
  - `fetchCommonNamesByCountryCode()`
  - `addSpeciesToDB()`
  - `addCommonNamesToDB()`
  - `search()`
  - `getSpecies()`
  - `getCommonNames()`
  - `getCommonNamesAddRes()`
  - `getSpeciesAddRes()`
  - `getSearchedSpecies()`

- **Details Fragment** - handles the display of the descriptive data for the selected fish species.
  ##### Fragment/ViewModel Methods
  - `fetchCountries()`
  - `fetchSpecies()`
  - `fetchCommonNames()`
  - `getMonths()`
  - `determineMonthRanges()`

- **Length Guide Fragment**
  ##### Fragment/ViewModel Methods

- **Listing Fragment** - handles the display of the search query in a card list.
  ##### Fragment/ViewModel Methods
  - `onSearch()`
  
- **Web View Fragment** - handles the display of a web view container inside the app.
  ##### Fragment/ViewModel Methods
  - `loadWebpage()`

### ARCHITECTURE USED

Q-Quatics FishBase Guide Android follows and uses the Model-View-ViewModel Architecture (MVVM). It consists of an xml file which is the UI layout definition for the screen, a Fragment that is the UI controller that displays the data, and the ViewModel, a class that prepares the data for viewing in the Fragment and reacts to user interactions.

[here](https://drive.google.com/file/d/1ikD6dEHvLZIGkIyTN_1Zs-iRh_RnZbgy/view?usp=sharing)