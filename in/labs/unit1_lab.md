<img src="https://s3.amazonaws.com/python-ga/images/GA_Cog_Medium_White_RGB.png"/>

# Unit 1 Lab: Variables

## Overview

Welcome to the first unit lab!

Throughout the course, there is a lab at the end of each unit. Each lab builds upon the prior.
**At the end of Unit 5’s lab, you’re going to have an app that asks the user to search for a twitter user. Your app will then search for that user on Twitter and print the search results. **

**This app will be able to:**

- Search for any twitter user
- Present a table of results of key attributes of the user: follower count, friend count, location, profile photo, etc
- Specific user pages displaying more information about the user
- Word clouds of the most used words in the tweets from a given user

For example, if a user searches in your app for “Nike”, your app can get a list of results: 
“Nike,” “Nike UK” “Nike Basketball,” “Nike Football”. 

Your app can also tell the user that Nike has 814k followers, is based in Beaverton Oregon and has tweeted 36630 times. 

You can then have a look at a word cloud of the most recent 200 tweets.

Throughout the course, there is a lab at the end of each unit. Each lab builds upon the last.

**It’s going to be awesome!**

## Deliverables

Right now, let’s set up some variables and print out their values. You’re going to build this locally on your computer.

1. Create a new folder on your Desktop called "twitter_app". That folder is where we’ll keep all the files we create for our unit labs.
2. Create a .py file called twitter_app.py. You’ll write all of your code in this file.
3. Run the file from the command line to check your work. On your laptop, you can run the file from your command line with the following command:

```
python twitter_app.py
```

**Hint:** Make sure you’re printing something out with the print statement! Otherwise, you won’t see any output from running your program.

## Overview

By the end of this, you will have a twitter_app.py file that prints out: "The number of followers for Nike is 800000."

## Directions

Our first goal is just to get the app printing out username and follower count. We'll hard-code in some values for now.

1. Create a variable `username` and set it to `Nike`
2. Create a variable `follower_count` to hold the followers count and set it to `800000`.
3. Make a `print` statement that says, `The number of followers for <username> is <follower_count>`. 
It should call your new variables, so for example, `The number of followers for Nike is 800000`.