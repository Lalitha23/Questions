# Interview Questions
## Full Stack Interview Question and Answers

1.	What is the most influential book or blog post you’ve read regarding web development?

Answer:

Most influential blog I have read regarding web development is
https://www.codeproject.com/Chapters/2/Web-Development.aspx - There are many articles and cool features explained in this blog. I got so much inspiration to develop on a personal project which I’m working on currently. I feel this is the one of the best sites for beginners to learn.
Also, I like the way my Android phone displays news sections very elegantly and gives me lots of options to personalize them. I would like to work/develop on something like this in future which help people personalize their experience



2.	Tell me about a web application you have built. Why did you choose to build it? What did you learn? What challenges did you face and how did you overcome them?

Answer:

I have built a Restaurant Menu web application using Flask framework, Python and Postgre SQL. The web app shows menu of restaurants stored in DB. Users can see the menu, login using and create/edit/delete their own restaurant menus. Authentication is provided by OAuth, users can login in this site using their Gmail and Facebook accounts.
Also I have hosted this website on Linux server configured on Amazon Lightsail. While configuring linux server I have taken care of security issues like closing the default SSH port, creating new key pair for the new SSH port and enabling firewall etc.

I choose to do this project because it includes all the features/technologies that a Full stack developer needs in the current technology trend. While doing this project I have not only learned new technologies like Flask but also learned how to protect my site using OAuth providers and hosting the website.

I did face many challenges while building this application specially while adding the OAuth providers and while hosting the website too. Since, this project is built while I was doing my nanodegree course at Udacity, I had help from mentors/discussion forums and investigated few things on different websites.


3.	Write a function in Python that takes a list of strings and returns a single string that is an HTML unordered list (<ul>...</ul>) of those strings. You should include a brief explanation of your code. Then, what would you have to consider if the original list was provided by user input?

Answer:
'''python
 def html_ullist(\*list_of_string):
      ul_list = ‘<ul>’
      for s in (list_of_strings):
          ul_list += “\n” + ‘<li>%s</li>’  %s

      ul_list += ‘</ul>’
      return ul_list
'''
The code above takes a list of strings and iterates through them adding each item in the list between <li></li> and wrapping everything again in <ul></ul>. A new line character \n is added to each line for formatting the output.

If the string is provided as user input ideally I will check if the user input is a string, but here in my code I’m passing everything as string of arguments so nothing needs to be checked.

Reference: Attaching files of actual code and test results that are done by me while answering this question.

4.	List 2-3 attacks that web applications are vulnerable to. How do these attacks work? How can we prevent those attacks?

Answer:
Vulnerable attacks for web applications includes:

SQL Injection:
It the most common type of vulnerability where the attacker will submit a database SQL command which is executed by web application to modify/expose the database. With SQL injection, attacker will gain access to customer information.

Cross-site Request Forgery:
It is a malicious attack that tricks the user’s web browser to perform undesired actions like clicking a link or download an image and perform unknown actions to users authenticated session to gain access to user’s information.


Some of the methods to prevent these attacks include - testing the applications regularly, using Web Application Firewalls to monitor and potential attacks. Appending unpredictable tokens at each request and associate them in user’s sessions etc.

Reference sites used:
https://www.instartlogic.com/blog/4-common-web-application-security-attacks-and-what-you-can-do-prevent-them
https://www.veracode.com/security/web-application-vulnerabilities



5.	Here is some starter code for a Flask Web Application. Expand on that and include a route that simulates rolling two dice and returns the result in JSON. You should include a brief explanation of your code.
'''
   from flask import Flask
   from flask import jsonify
   app = Flask(__name__)

   import json
   import random

   @app.route('/')
   def hello_world():
      return 'Hello World!'

   @app.route(‘/roll_dice/JSON’)
   def roll_two_dice():
       return jsonify(dice1=random.randint(1,6), dice2=random.randint(1,6))


   if __name__ == '__main__':
     app.debug = True
     app.run()
'''
Tried implementing random rolling of two dice using random.randint() function which generates any number between 1-6. Returned it using jsonify to roll_dice page.

References:
http://flask.pocoo.org/docs/0.12/api/#flask.json.jsonify
https://stackoverflow.com/questions/23598952/rolling-two-dice-and-tabulating-outcomes


6.	If you were to start your full-stack developer position today, what would be your goals a year from now?

Answer:

My short-term goal would be get well versed with full stack development technologies (atleast one) that are being used on the job and learn writing proficient code. I believe that this will help me to contribute to the project that are useful to customers through the company.
