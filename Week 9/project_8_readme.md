# Project 8 - Pentesting Live Targets

Time spent: 12 hours spent in total

> Objective: Identify vulnerabilities in three different versions of the Globitek website: blue, green, and red.

The six possible exploits are:
* Username Enumeration
* Insecure Direct Object Reference (IDOR)
* SQL Injection (SQLi)
* Cross-Site Scripting (XSS)
* Cross-Site Request Forgery (CSRF)
* Session Hijacking/Fixation

Each version of the site has been given two of the six vulnerabilities. (In other words, all six of the exploits should be assignable to one of the sites.)

## Blue


Vulnerability #1: SQLi Injection

This vulnerability can be executed by inserting {/blue/public/salesperson.php?id=%27%20OR%20SLEEP(5)=0--%27} to a specific user. We can see that most of the data input received by these websites is being sanitized properly. This cannot be executed in the other websites.

![](https://github.com/lcano8/Codepath/blob/master/Week%209/SQL%20injection.gif)

References:[SQL-Injection](https://guides.codepath.org/websecurity/SQL-Injection)


Vulnerability #2: Session Hijacking/Fixation

We use the SSID from the red website to gain access to the blue website. We never input our credentials for the blue website, but it still logs us in after we logging to the red website.

![](https://github.com/lcano8/Codepath/blob/master/Week%209/Session%20Hijacking.gif)

References:[Session Fixation](https://guides.codepath.com/websecurity/Session-Fixation)


## Green


Vulnerability #1: User Unemeration

The developer uses a slightly different error message for non-existent users. We see that when we try to log in with the user jmonroe99 we get the error message in bold. If we try other users their message does not show in bold. 

 ![](https://github.com/lcano8/Codepath/blob/master/Week%209/User%20enumaration.gif)


Vulnerability #2: Cross-site scripting

The site is vulnerable to a stored XSS. We can insert blind xss to the feedback form. This gets activated when an administrator views the feedback. 

 ![](https://github.com/lcano8/Codepath/blob/master/Week%209/Cross-site%20scripting.gif)
References:[Cross-site Scripting](https://guides.codepath.com/websecurity/Cross-Site-Scripting)


## Red

Vulnerability #1: Insecure Direct Object reference

The sensitive data is two user id's. We have a range from 1-11, the blue and green website do not show the last two users. 

![](https://github.com/lcano8/Codepath/blob/master/Week%209/IDOR.gif)
References:[IDOR](https://guides.codepath.com/websecurity/Insecure-Direct-Object-Reference)


Vulnerability #2: Cross-Site Request Forgery

The website does not check the CSRF token authenticity. The token can be change and it will still allow editing with the wrong CSRF token.

![](https://github.com/lcano8/Codepath/blob/master/Week%209/CSRF.gif)
References:[CSRF](https://guides.codepath.com/websecurity/Cross-Site-Request-Forgery#csrf-post-request-attack)
## Notes

Describe any challenges encountered while doing the work

The user enumariation and IDOR challenges were simpler to complete. With some of these challenges the issue is knowing what to look for what needs to be modified.
