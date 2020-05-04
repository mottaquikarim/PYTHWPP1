<img src="https://s3.amazonaws.com/python-ga/images/GA_Cog_Medium_White_RGB.png"/>

# Unit 2 Lab: Advanced Control Flow

## Overview
Welcome to the second unit lab! Remember, our goal is that at the end of the third lab, you’re going to have an app that searches for twitter users and creates a word cloud of their tweets for any twitter user.

Right now, you have a variable to hold a username, a variable to hold the count of the followers, and a print statement to show the user.

Next, let’s set up the functions and control flow to print out the values of our variables.

------------

## Deliverables

You're going to continue building this locally from the last lab. You'll write all of your code in the same `twitter_app.py` file.

Run the file from the command line to check your work.

Reminder: On your laptop, you can run the file from your command line with the following command:
`python twitter_app.py`

Hint: Make sure you are printing something out with the print statement! Otherwise, you won't see any output from running your program!

## Requirements

By the end of this, you will have edited your existing `twitter_app.py`. 

At the top, you will have a variable called `search_or_followers`, this is what you can change if you want your program to do different things.

Your app will be able to:

- Print a twitter username
- Print the number of followers
- Print a sentence which says: `The number of followers for <username> is <follower_count>`  
- Print a list of twitter usernames
- Give the user a choice if they want to print details about lots of twitter users (emulating a search) or details about a specific user (emulating a profile page)

---

## Requirements

If `search_or_followers` is equal to 1, your app will then print:

        Nike

        Nike UK

        Nike Basketball


If `search_or_followers` is equal to 2, your app will then print:
      
    The number of followers for Nike is 800000

If `search_or_followers` is equal to 3, your app will then print:

    This is not a valid choice please choose 1 or 2.

## Directions - part 1

You'll add to and change the code you wrote for the Unit 1 lab, so leave your two variable declarations at the top of your program and don't delete the print statement!

1. Our program's going to get pretty complex. Let's have a definite starting point. At the bottom of your program, create one function and call it `main`. Just leave a `pass` variable in there for now. From here, we'll call everything else.

2. In programming, if you have a `main` function, you can set it to automatically run when you start the program. In Python, there's a section of code that does this for us. At the very bottom of your file, put this code:

```
if __name__ == "__main__":
    main()
```


---

## Directions - part 2

1. Now let’s get started. Create a variable at the top of the file called `search_or_followers` and set it to `1`.
2. 
  - In the `main` function we want to create a conditional statement that looks at the `search_or_followers` variable and decides whether to print out a list of twitter users or basic profile information about one user. 
  - Create an `if-elif-else` statement that compares `search_or_followers` to `1` and `2`. 
  - Use the `pass` variable underneath all three levels for the moment as we haven’t made the functions yet

3. Create a function that is called `print_twitter_user_profile` that takes in a `username` and a `follower_count` parameters. Move the print statement from lab 1 into this function.
When called this function should print `'The number of followers for {username} is {follower_count}.'`
4. Create a function that is called `list_search_results` that takes in a list called `search_results` as a parameter. 
When called this function should loop through each element of `search_results` and print each one with a little bit of blank space (one tab) i.e. 

           Nike
     
---

## Directions - part 3

6. We’re going to need some fake search results so underneath the variables from unit-1 create a list called `fake_search_results` with three usernames in i.e. `['Nike', 'Nike UK', 'Nike Football']`
7. If `search_or_followers` equals `1` then call `list_search_result` and use the global `fake_search_results` variable as the argument. 
8. If `search_or_followers` equals `2` then call `print_twitter_user_profile` and use the global variables from unit one as the arguments.
9. If `search_or_followers` equals `3` then print `This is not a valid choice please choose 1 or 2`.
10. Run the program and experiment changing the `search_or_ratings` variable.