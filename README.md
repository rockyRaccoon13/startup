# startup - ***MovieLog***
Startup application for BYU CS 260

# Specification Deliverable

### Elevator Pitch
Would you like to share your enthusiasm for a particular movie with your friends? Want to know what people are saying about the latest blockbuster? The MovieLog application allows you to read and publish reviews so you can hear opinions on the latest films. 

### Design

**sign in page** 

![signInPage](/descimages/signInPage.jpeg)


**Reviews Page**

![previewReviewsPage](/descimages/previewReviewsPage.jpeg)


**User Profile**

![userProfilePage](/descimages/userProfilePage.jpeg)


**Individual Review Page**

![singleReviewPage](/descimages/singleReviewPage.jpeg)


**Publish/Edit Review** 

![newEditReviewPage](/descimages/newEditReviewPage.jpeg)




### Key Features
* Publish your own movie review
* View a page filled with hot reviews
* read full reviews
* ability to like a review
* abilty to view a user's profile containg all their reviews


  

### Technologies

- **HTML** - Uses correct HTML structure for application. 5 HTML pages (see images aobve). Hyperlinks.
- **CSS** - Application styling that looks good on different screen sizes, uses good whitespace, color choice and contrast.
- **React** - Provides login, reviews display, applying likes
- **Service** - Backend service with endpoints for:
  - login
  - retrieving reviews/data/userProfile
  - submitting reviews/data/userProfile
- **DB/Login** - Store users, reviews, and review data. Register and login users. Credentials securely stored in database. Can't publish/like review unless authenticated.
- **WebSocket** - updates number of likes on reviews and avg ratings on media pages, updates recent reviews page. Broadcasts changes to all users
