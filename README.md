# Ionic 4 - News API App with Detail Page

I updated the app developed by Baljeet Singh: [Creating News Application With Ionic 4 and Angular](https://youtu.be/NJ9C7iY9350)

<img src="" />

## SET UP

--dry-run allows you to preview the files that will be created
ionic start ionic4-angular-news tabs --type=angular
ionic g page news 
ionic g page news-single


## ADD NEWS PAGE TO TAB

1. At tabs.module.ts, Import NewsPageModule --> Code Lines: 24 + 13 
2. At tabs.router.module.ts, change Home path to News --> Code Lines: 11, 16, 42, 49
3. At tabs.page.html, change href and label --> Code Lines: 4 + 6


## SET UP API SERVICE & NEWS PAGE

ionic g service services/news

1. At environment.ts, create a constant for API's URL and Key. --> Code Lines: 6 - 8
2. At app.module.ts, import HttpClientModule --> Code Lines: 11 + 16
3. At news.service.ts: 
 a) import HttpClient and add it as constructor's param
 b) import environment and create variables for API's URL and Key  
 c) create getData function
4. At news.page.ts:
 a) import NewsService and add it as constructor's param
 b) subscribe to getData function
5. At news.page.html, add ionic cards to display news articles


## SET UP NEWS-DETAIL PAGE

1. At news.service.ts, create new var for current article --> Code Lines: 13
2. At news.page.html, add a click listener to ion-card --> Code Lines: 9
3. At news.page.ts:
 a) Import Router and add it as constructor's param
 b) Create click listener function "goDetailView"
4. At news-detail.page.ts:
 a) import News Service and add it as constructor's param
 b) Create a variable to hold article's data --> Code Lines: 12
5. At news-detail.page.html, create ionic cards and add back button

## Contributors
Baljeet Singh