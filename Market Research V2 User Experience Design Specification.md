# Market Research User Experience Design Specification

Shawn Zhao

Dec 18th, 2014

## 1. Project Background

Beijing Field Power Info-Tech Co. Ltd is an independent software developer and service provider in China, with the logo shown in the cover page.

As the business plan, File Power is developing a system called Market Research. The system is designed for collecting market data from stores like the supermarkets. The target clients are the market survey agencies like AC Nelson. The target users are the surveyor teams of the clients. The users should collect the raw data from the stores, input them in the app, and upload them to back-end server.

The system (app) itself should support both English and Chinese, but the Chinese is majority, such as the name of store. 

### 1.1 Brief of Requirement

The Market Research system will be implemented with [Apache Cordova](http://cordova.apache.org/) for iOS 7+, Android 4.0+ and Windows Phone 8+. [AngularJS](https://angularjs.org/) and [Bootstrap](http://getbootstrap.com/) will be used, any design should be able to easily implement by AugularJS and Bootstrap without any problem.

The designer is supposed to make the app looks tidy, professional and easy to understand. The design should match the flat design style, as well as the alignement of Field Power logo.

The design should be adopted to large screen phones, including Samsung Note 3, Samsung Note 3 Lite, iPhone 5/6/6+, and other smaller yet popular phones. The design should use the [responsive web design](http://en.wikipedia.org/wiki/Responsive_web_design) approach so it can fit any phone or tablet resolution. Like what Apple did in iPhone 6/6+ Mail app, we intend to display more data on large screens, however hide certain details on small screens. Alternative layout should be applied for tablets (e.g. iPad) and large phone in landscape mode (e.g. iPhone 6+), like the iOS Mail app.

The most important is to create the convenience of end user’s experience. The design should be convenient for users to browse, inquire, input and edit data. It’s better to avoid large images to ensure the system performance.

The designer must transfer all copyright and intellectual property rights to us. He/she should also not violate any third party’s rights. An agreement must be signed before project start, and this article must be agreed by both sides.

The designer's tasks includes:

1. Design app icons
2. Design function icons
3. Design splash screens
4. Design function screens

## 2. Icons Design Specification

### 2.1 App Icons

App icons should match requirement of each platform. Each icon should be design for resolution of 1024*1024 and should be able to scale down without lose recognition.

App icons to design include:

1. Market Research
2. Training
3. Order Management
4. Building Inspection
5. Warehouse Take
6. Stock Take

### 2.2 Function Icons

Function icons should be delivered in vector format like the [Bootstrap Glyphicons](http://getbootstrap.com/components/#glyphicons). Each icon should be design for resolution of 1024*1024 and should be able to scale down without lose recognition.

Function icons to design include:

1. Plan
2. Inspect Store
3. Review Data
4. Notices
5. Diary
6. Submit Data
7. About
8. Product
9. Shelf
10. Special Price
11. Remarks
12. Questionnaire
13. Promotions
14. Snapshot
15. Comment
16. Count Stock
17. Fill Order
18. Inspect Layout
19. Inspect Poster
20. Register Trainee
21. Stores On Map
22. Start Training
23. (For a Supervisor to) Review Team Performance
24. Update Store Information (Name, Address, etc.)
25. View Store Sales

## 3. Screens Design Specification

### 3.1 Splash Screens

Splash screens should be delivered in PNG format in each required resolutions for all three platforms.

The splash screens should be simple, an image with Field Power logo should do it. It's better not to contain app's title so they can be the same for different apps.

### 3.2 Function Screens

Functions screens should be responsive. System default font on each platform should be used.

#### 3.2.1 Primary Menu

Primary Menu is the first screen after app launch. There should be icons for all secondary modules and title of the app (in text). Better to show the Field Power logo too.

![Primary Menu](/PrimaryMenu.png)

There should a way to show a number or a "check mark" for each module.

The number of sub-module icons is variable from 4 to 12.

#### 3.2.2 Secondary Menu

Secondary Menu should show icons for all tertiary modules and title of this secondary module. A subtitle should be displayed for a store name and a date. There should also be a "save" button.

![Secondary Menu](/SecondaryMenu.png)

There should a way to show a number or a "check mark" for each module.

The number of sub-module icons is variable from 4 to 12.

#### 3.2.3 Plan

User should be able to view his plan of today and 7 days after today.

Plan of each date should be on one page, user should be able to change date.

![Plan](/Plan.png)

There should be an "edit" icon. By pressing edit, a screen for edit plan should show with a list of stores. Each store should come with a combo box or similar so user can select store for the given date.

#### 3.2.4 Store List

List of all stores the user should inspect. The store names are grouped and ordered in alphabetical order. The title of each group is the first letter of store name.

![Store List](/StoreList.png)

On large screens store address should also be displayed in the list.

User should be able to show a popup with some store detail. The platform default alert/dialog will be used for the popup.

#### 3.2.5 Review Data

List of all inspects the user has already done. The items should be grouped by store or grouped by date. There should be a way to trigger the two modes.

When group by store, store name should be in group title, each item should display the date and inspect status.

When group by date, date should be in group title, each item should display the store name and inspect status.

Statuses of inspect includes:

 * Undone
 * Edited
 * Submitted
 * Confirmed
 * Removed
 * Delivered

User should be able to delete an inspect log from this screen.
 
#### 3.2.6 Notice

Notices are short messages downloaded from server.

New messages should have special style.

#### 3.2.7 Diary

User can view and edit his/her diary for today and next 7 days. One diary for one day.

Should be able to view, edit, delete and save diary from this screen.

The screen should contain three parts:

* Date Selection
* Text field for view/edit diary
* Daily performance view

The designer should provide two ways for select date:

* Select a date from a week, for small screens or
* Select a date in a calendar, for large screens

User should also be able to view his/her daily performance from this screen, including:

* What stores are planed but not inspected
* What stores are not planed but inspected
* What stores are planed and inspected

#### 3.2.8 Loading

A loading popup should show when loading data from server or uploading data to server.

It should contain a title, a subtitle and an loading indicator.

#### 3.2.9 About

In this section user should be able to see:

 * App name
 * Description of the app
 * App Version
 * Field Power Logo
 * A "Contact Support" button

#### 3.2.10 Product

User can check the product information on this page.

A list of product is displayed on this page, with a long name for each product.

User should be able to edit each product's price, shelf and offtake.

Products are grouped by product category, each category contains one or more products. Each page displayes products within the same category. User should be able to change product category.

![Product](/Product.png)

The style of an input field should be changed if the number in it was changed.

There should be a save button on this page.

#### 3.2.11 Shelf

Similar to Product, but each line should only contain a short title and one input field.

![Shelf](/Shelf.png)

#### 3.2.12 Promotions

Similar to Shelf, but each line should only contain a short title and an on/off switch.

![Promotions](/Promotion.png)

#### 3.2.13 Questionnaire

A questionnaire require the customer to fill. Each question is scored from 1 to 5. After finish the customer is asked to sign on the device screen.

#### 3.2.14 Remarks

Note other worthy things in text. Can view, add, edit and delete remarks.

#### 3.2.15 Snapshot

Take photo of the store, view, add and delete photo.

Should contain both thumbnails view and large image view

Each photo should come with a photo description (non-editable), should be displayed in both thumbnails view and large image view.

#### 3.2.16 Customer List

List of all customers. Similar to store list but with logo for each customer. The names are grouped and ordered in alphabetical order. The title of each group is the first letter of customer name.

A placeholder image should be used of customer logo not available.

## 4. Summary

There are 6 app icons and 25 function icons to design, 1 splash screen and 16 function screens to design and implement.

The price and timeline should be agreed by both sides before start.

The designer should delivery the following items upon finish of each milestione:

* Design source file in PNG or other format
* SVG/PNG or other format of slices used in implement
* All copyright and intellectual property rights of the design
