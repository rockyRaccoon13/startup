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
- **Service**
  - Backend service with endpoints for:
    - login
    - retrieving reviews/data/userProfile
    - submitting reviews/data/userProfile
  - Third party service for getting random movie quote
- **DB/Login** - Store users, reviews, and review data. Register and login users. Credentials securely stored in database. Can't publish/like review unless authenticated.
- **WebSocket** - updates number of likes on reviews and avg ratings on media pages, updates recent reviews page. Broadcasts changes to all users


## HTML deliverable

For this deliverable I built out the structure of my application using HTML.

I did so over several days (in the span of Monday through Saturday of one week). I worked on my html several days but did not commit very often. For the next deliverable I will try to commit more often


- [x] **HTML pages** - 6 HTML pages that represent the login page, browse page, review page, edit review page, profile page, edit profile page.
- [x] **Links** - Menu at top of each page. Browse review links to user profile and review page. Review page and profile page link to respective edit pages (will be implemented only for current user).
- [x] **Text** - User profiles and reviews are represented as text.
- [x] **Images** - Included image on login screen as well as logo in header and head (displays on browser tab) of each page.
- [x] **DB/Login** - Input boxes and 2 submit buttons for login/create account. The user profiles and reviews represent data pulled from the database.
- [x] **WebSocket** - The list of reviews on browse Review will be updated in real time to include new reviews.
