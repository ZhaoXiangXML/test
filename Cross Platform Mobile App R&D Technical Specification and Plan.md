# Cross Platform Mobile App R&D Technical Specification and Plan

Shawn Zhao

Dec 12th, 2014

## 1. Brief of Requirement

The target of this R&D project is to build Cross Platform Mobile based on [Apache Cordova](http://cordova.apache.org/).

Apache Cordova enables build app with HTML5 for UI and business logic, and access native functions via plugins written by native languages (Java, Objective-C, C#, etc.).

The goal is to create iOS, Android and Windows Phone 8 apps with the same UI and business logic code base, and create native plugins that future projects can reuse. When the project goes mature, future projects should only write UI and business logic code once for all platforms, without worry about native languages or device differences.

The project contains three major tasks:

 * Find or create native plugins on each platform
 * Port existing HTML5 version of Call Management Hershey Wedding to Cordova based native apps
 * Implement Zohaib's new UI design
 
The project is going to be developed and tested on the following platforms:

 * iOS 7.0+
 * Android 4.0+
 * Windows Phone 8 and 8.1
 * browser (Google Chrome Desktop)

The browser version is to make develop UI and business logic easier, it's not intended to be published to the end users.

On Android, [Crosswalk](https://crosswalk-project.org/) will be used for batter HTML5 capability.
 
The apps will be distributed as download packages for each platform. Automatic update of HTML5 code should be implemented as a later process of this project.
 
Most part of the Call Management Hershey Wedding code can be reused, except where to access database or camera.

## 2. Project Architecture

On HTML5 side, AngularJS will be used for app framework, Bootstrap will be used for UI.

On native side, Cordova Plugin will be used. Some functions are already created by the Cordova team or open source community, yet some need to be developed by oursleves.

The following table shows the native functions we need and possible solutions:

 | Possible Solution                        | Remarks 
 ----------------- | ---------------------------- | ------------------ 
Database | [Cordova-SQLitePlugin](https://github.com/brodysoft/Cordova-SQLitePlugin) |
Camera | [cordova-plugin-camera](https://github.com/apache/cordova-plugin-camera) | Might need to customize it to have better stability on Android
Device | Customize base on [cordova-plugin-device](https://github.com/apache/cordova-plugin-device) | Add Device Code support on iOS
Network Information | [cordova-plugin-network-information](https://github.com/apache/cordova-plugin-network-information) |
AES Encryption | Create our own |
Remote Logging | Create our own |
Geolocation | Customize based on [cordova-plugin-geolocation](https://github.com/apache/cordova-plugin-geolocation) | Baidu [Android Loc SDK](http://developer.baidu.com/map/index.php?title=android-locsdk) for Android
Map | Baidu Map [JavaScript API Extreme](http://developer.baidu.com/map/index.php?title=jsextreme) | Baidu Map does not provide Windows Phone Native SDK, so the JS version has to be used. Not included in this project.
Crash Reporting | [Crittercism](http://docs.crittercism.com/development_platforms/phonegap.html) | Need to customize for Windows Phone

## 3. Develop Plan

Plan of Dec 2014:

 * Setup development environment for iOS, Android (4 hours)
 * Setup project Structure, install existing plugins (4 hours)
 * Move existing Call Management Hershey Wedding code into project (1 hour)
 * Customize Camera Plugin for Android, update Call Management to use this Camera plugin (8 hours)
 * Rewrite Database related code to use SQLite plugin (12 hours, cooperate with Sugar)

By the end of Dec 2014, we should have fully functional Cordova version of Call Management Hershey Wedding for iOS and Android, and ready to be tested by end users.

Plan of first half of Jan 2015:

 * Customize Device and Network Information plugin for any missing function (4 hours)
 * Add Crash Reporting (2 hours)
 * Test and debug on iOS and Android (8 hours)
 * Customize Geolocation, use Baidu's SDK for Android (4 hours)
 * Create AES encryption plugin and encrypt upload transmission (4 hours)
 * Create remote logging plugin (4 hours)
 
By the mid of Jan 2015, we should have all functions of our existing native apps but map.

In the mean time (from early Dec 2014), I should also cooperate with Zohaib for the new UI design. The design should be finished by the end of Dec 2014 and the implement should be finsihed by the end of Jan 2015:

 * Define requirements, list items to design (2 hours)
 * Communicate with Zohaib for the design and static HTML page implement process (8 hours)
 * Integrate Zohaib's static HTML page with logic code (8 hours, cooperate with Sugar)
 * Test and debug on iOS and Android (6 hours)
 * Automatic update of HTML5 code iOS and Android (4 hours)

The iOS and Android part of the project takes 83 hours of my time in total.

The Windows Phone 8 part is pending for now, it should be done as a separated project later.

By the end of Jan 2015, we should have all the new UI integrated. And we should have enough experience and code base to do business project.
