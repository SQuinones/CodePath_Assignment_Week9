# CodePath_Assignment_Week9

# Project 8 - Pentesting Live Targets

Time spent: 8 hours spent in total

> Objective: Identify vulnerabilities in three different versions of the Globitek website: blue, green, and red.

The six possible exploits are:

* Username Enumeration
* Insecure Direct Object Reference (IDOR)
* SQL Injection (SQLi)
* Cross-Site Scripting (XSS)
* Cross-Site Request Forgery (CSRF)
* Session Hijacking/Fixation

Each color is vulnerable to only 2 of the 6 possible exploits. First discover which color has the specific vulnerability, then write a short description of how to exploit it, and finally demonstrate it using screenshots compiled into a GIF.


## Green

Vulnerability #1: Username Enumeration

Description:

User enumeration is when a malicious actor can use brute-force techniques to either guess or confirm valid users in a system. User enumeration is often a web application vulnerability, though it can also be found in any system that requires user authentication. Two of the most common areas where user enumeration occurs are in a site's login page and its ‘Forgot Password' functionality

In this case escenario go to the main login. If the wrong password is entered and the user exists, the error is bold. If the wrong password is entered and the user does not exist, the error just plain text. 

![Green_user_enume](https://user-images.githubusercontent.com/78192383/163407608-867e8f98-bb7b-455d-9382-30c21c481eb0.gif)


Vulnerability #2: 

Description:

An attacker can use XSS to send a malicious script to an unsuspecting user. The end user’s browser has no way to know that the script should not be trusted, and will execute the script. Because it thinks the script came from a trusted source, the malicious script can access any cookies, session tokens, or other sensitive information retained by the browser and used with that site.

![Green_XSS](https://user-images.githubusercontent.com/78192383/163409978-6b810ea8-3ebc-4db7-9318-91de8e7a0f8c.gif)


## Red

Vulnerability #1: Insecure Direct Object Reference

Description: Insecure Direct Object Reference occurs when a application exposes a reference to an internal implementation object. Using this way, it reveals the real identifier and format/pattern used of the element in the storage backend side. 

In this case, use the public find a Salesperson tool to look for someone. After a Salesperson is found, use the id parameter in the url to look for other people in the system. Doing that allows to see sensitive information.

![Red_Insecure_direct](https://user-images.githubusercontent.com/78192383/163411496-336d1ca9-5aef-4d29-b175-401a8f2fc8bd.gif)


Vulnerability #2: 

Description:CSRFs are typically conducted using malicious social engineering, such as an email or link that tricks the victim into sending a forged request to a server. As the unsuspecting user is authenticated by their application at the time of the attack, it’s impossible to distinguish a legitimate request from a forged one. CSRF vulnerabilities can lead to severe attacks, including full account takeovers.

In this case escenario I create a malicious form. And create an Admin. When a logged in user goes the malicious website, the salesperson with id 1 has their information updated. 

![CSRF_red](https://user-images.githubusercontent.com/78192383/163418076-066d5b50-d644-46a9-abce-49b1f8a2994a.gif)



