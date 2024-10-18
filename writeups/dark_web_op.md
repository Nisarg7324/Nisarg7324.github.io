# Introduction to Dark Web Operations Capstone Writeup

This writeup is for Introduction to Dark Web Operations Capstone which is a part of Security Blue Team's Introduction to Dark Web Operations course.

Link to the course - [Introduction to Dark Web Operations](https://www.securityblue.team/courses/introduction-to-dark-web-operations)

## Challenge

```
Hi Investigator, we need you...

Last month we were informed about a huge drug trafficking network that was taking place in the UK through the TOR network, in response to this situation we set to work and managed to dismantle their main TOR marketplace to stop drugs reaching the streets of the UK. However, we were informed that one of the creators of this network managed to evade us and is now continuing to carry out this type of activity. This is where you come in. We think we have found the site that this individual uses to "tell their stories" regarding criminal activity.

We need you to find evidence that will allow us to identify this subject, relate it to the drug trafficking crimes, and bring them to justice. We know this is a difficult task, but we are confident in your abilities and we are sure that you will succeed.

1] Gain access to the site (We're sure there's some way for users to gain valid credentials fairly easily).
2] Find evidence that the individual is involved in drug trafficking.
3] Find any information about the next shipment that is coming in, so we can seize it.




-------------++---------------++---------------++---------------++--------------

                    _********************_
=================== \  CHALLENGE REPORT  / ====================
                      ******************
  _________________________________________________   
 |   ___                                           | 
 |  |    \          __      ___  _____  _____      | 
 |  | |\  \        / /     Â´ _ `Â´  __ `Â´  ___`     | 
 |  | | \  \  /\  / /     | | | | !_/ /! Â´--.      | 
 |  | | /  /\/  \/ / ___  | | | |  __/  `--. Â¡     |
 |  | !/  /\  /\  / Â´   ` ! !_! ! |    /`--Â´ !     |
 |  !____/  \/  \/  `---Â´  `___Â´!_!    `----Â´      |
 |                                           (SBT).|
  ------------------------------------------------- 


 Known Info:
===================				      
[*] DWebsite:  5xdv6dqxv2bsbmlgttsq3ma3nw6ffa2zhqbl7o4w46p32wsqulzrtsqd.onion


 Requested Info:
==============================
1) What command is used in the Console to generate valid credentials?
2) What is the suspect's site username?
3) What is the suspect's first and last name?
4) What country is the suspect currently living in?
5) What is the date of the first post related to drug trafficking?
6) What is the date of the latest post related to drug trafficking?
7) What type of encoding has been used on the site content?
8) When is the next drug shipment coming into the UK?
9) What are the GPS coordinates of the shipment delivery location?  
10) What is the name of the seaport where the shipment is being delivered?
```

## Tools Required

It is clear from the challenge that we will navigate to the .onion site. Hence, in order to navigate to .onion site, we will require Tor Browser. For added safety, I also suggest using a VPN before connecting to the Tor network.

For this capstone, I have used Tor Browser and ProtonVPN. You may choose the VPN of your choice.

Download Tor Browser from [here](https://www.torproject.org/download/)
Download ProtonVPN from [here](https://protonvpn.com/)

## Solution

### Visit the .onion site

First, connect to the VPN. Then open the Tor Browser and connect to the Tor network.

Copy and paste the provided .onion link in the Tor Browser. Hit Enter. This will open up a webpage as shown in the image below.

![URL Landing Page](./images/url_landing_page.png)

On this webpage, click on the "GO TO THE CHALLENGE" button. This will lead to a login page as shown in the image below.

![Login Page](./images/darkforum_login_page.png)

### Finding Login Credentials

Based on the questions in the requested info, it is clear that we need to find a function for the console, that will generate login credentials for this website.

Right-click anywhere on the page and click Inspect. This will open up a console. You will see various tabs that you can navigate to. Click on the Debugger tab. In this tab, we can search for any keyword across all the loaded scripts.
