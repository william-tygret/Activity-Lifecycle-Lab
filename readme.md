
---

| Title | Type | Duration | Name | City |
| --- | --- | --- | --- | --- |
| Activity Lifecycle | Lab | "1:00" | James Davis | NYC |

---  
# Activity Lifecycle Lab

## Introduction

Below, you will find three scenarios, and questions following each one.

To the best of your ability, answer the questions **in english**, not in code.

Below the scenarios, you will find a few questions. Answer those however you'd like.

Answer the questions by editing this readme, pushing your changes to your forked repo, and making a pull request.

## Exercise  


####Scenario 1:

Let’s say you made a To Do list app, where you can add things to a list and cross them off. You decide to cross some items off the list and mark them as complete.

When you rotate the device, the things you marked as complete are no longer crossed off.

**Question**: Why did this happen?
<br />Answer: When you change orientation it restarts the activity

**Question**: How do you fix this issue?
<br />Answer: save info in a bundle and set it to an onCreate, so everytime it opens it will access that bundle


####Scenario 2:

The Amazon Kindle Android app allows you to open and read eBooks. You discovered a bug! You opened a book, and read it from the beginning up to page 68. Then, you left the app and closed it completely so you can do other things.

When you opened the app again, and opened the book, it started from page 1 (and not page 68 where you left off)!

**Question**: How would you fix this issue?
<br />**Answer**: using Shared Preferences: set the onPause method to reference the Shared Preference to save the page number the reader is at. Create a method in onResume that references that saved page number and display the page that the reader left off on.


####Scenario 3:

Facebook for Android added a feature last year where, if you started writing a comment on someone’s post and decided not to do so, the app would save a draft of it just in case you changed your mind.

Take this scenario. On a post on Facebook, you click the “comment” button (which opens a new CommentActivity). You start writing a comment, and then change your mind by pressing the back key (which closes the CommentActivity). You click on the “comment” button again, and in the newly-opened CommentActivity, the comment you were writing is still there.

**Question**: How would you implement this feature? Be specific; what lifecycle methods would you use in CommentActivity, and what techniques would you use?
<br />**Answer**: onPause with Shared Preferences, save the data, onResume use Shared Preferences to repopulate the string that the user previously commented



In your own words…
==================

**Question**: What are the methods of the Activity Lifecycle?
<br />**Answer**: onCreate --> onStart --> onResume,  onPause --> onStop --> onDestroy

**Question**: What order are the methods called?
<br />**Answer**: ^^^^^^^

**Question**: What is a bundle?
<br />**Answer**: an object that saves and can transfer your data in a SavedInstanceState

**Question**: How do you get the Shared Preferences of an app?
<br />**Answer**: declare new Shared Oreference object, then initialize it with getSharedPreferences() 
