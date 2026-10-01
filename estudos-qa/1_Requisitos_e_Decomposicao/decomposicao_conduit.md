# Site Decomposition: Conduit Web Application

**Context:** This document outlines the structural decomposition of the Conduit web application (Logged-In User State). The objective is to break down the system into its core modules, sub-modules, and specific features to establish a clear foundation for future test case design, planning, and execution.

---

## 1. Home Page
* **1.1 Your Feed**
  * 1.1.1 View Article
    * Link to User Profile
    * Like Button
    * Article Info (Title and Description)
    * Tags
* **1.2 Global Feed**
  * 1.2.1 View Article
    * Link to User Profile
    * Like Button
    * Article Info (Title and Description)
    * Tags

## 2. New Article Page
* 2.1 Article Title Field
* 2.2 'What's this article about?' Field
* 2.3 Write Article Field (Markdown support)
* 2.4 Enter Tags Field
* 2.5 Publish Article Button

## 3. Settings Page
* **3.1 Your Settings**
  * 3.1.1 URL of Profile Picture Field
  * 3.1.2 Username Field
  * 3.1.3 Bio Field
  * 3.1.4 Email Field
  * 3.1.5 New Password Field
  * 3.1.6 Update Settings Button
  * 3.1.7 Logout Button (Or click here to logout)

## 4. User Profile Page
* **4.1 Header**
  * 4.1.1 Bio
* **4.2 My Posts**
  * 4.2.1 Link to User Profile
  * 4.2.2 Like Button
  * 4.2.3 Article Info (Title and Description)
  * 4.2.4 Tags
* **4.3 Favorited Posts**
  * 4.3.1 Link to User Profile
  * 4.3.2 Like Button
  * 4.3.3 Article Info (Title and Description)
  * 4.3.4 Tags
* 4.4 Edit Profile Settings Button

## 5. Article Page
* **5.1 Header**
  * 5.1.1 Article Title
  * 5.1.2 Date
  * 5.1.3 Author's Name
  * 5.1.4 Follow Author Button
  * 5.1.5 Favorite Article Button
* 5.2 Article Text Content
* 5.3 Tags
* **5.4 Comments Section**
  * 5.4.1 Comment Text
  * 5.4.2 User's Profile Link
  * 5.4.3 Post Date
  * 5.4.4 Write a Comment Field