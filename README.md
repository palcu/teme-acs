TL;DR - It's illegal in Romania to buy homework.

Update: RoliSoft has provided me with a new, more legal [approapch](https://github.com/palcu/teme-acs/issues/2)

# Description

Auction website for students at ACS where people can sell and buy homework.

# Values

* security
* privacy
* democracy
* community

# Business plan

### We will take 30% of every transaction done on the website.

Studenți la ACS pe an în anul 1 sunt 450 calculatore
    
În anul 3 dispare o grupă pe serie (3 x 25 studenți), în anul 2 sunt tot la fel de delăsători, așa că îi scad de acolo.

Studenți totali: 450 + 375 + 375 + 375 = 1.575 studenți.

Materii grele:

    * anul 1
        * sem 2:
            * SD
                * 4 teme x 3 serii = 12 teme
                * 100 - 250 lei / temă
    * anul 2
        * sem 1:
            * OOP
                * 4 teme x 2 serii = 8 teme
                * 100 - 150 lei / temă
        * sem 2:
            * PA
                * 4 teme total
                * 100 - 200 lei / temă
            * PC
                * 4 teme total
                * e ușor... nu știm
            * PP
                * 4 + 3 = 11 teme
                * 200 - 400 lei / temă

Total teme pe care un student tocilar le-ar face în 2 ani: 20 teme.

În total, fiecare student trebuie să facă aprox jumătate din acele teme ca să intre în examen, adică 10. Înmulțim cu numărul 15.000 de teme pe 2 ani, adică 7.500 teme pe an.

Câte teme se cumpără?! Vrem să aflăm.

Toate temele au deadline. Mă gândesc că putem opri licitația cu 48 de ore înainte și să așteptăm banii. Dacă în 24 de ore nu plătește, următorul va lua tema.

# Plan

* Django REST website with static pages
* nice clean front page with 
    * testimonials from students
    * a research on how people get more money for their homework
    * our privacy mission
    * a counter for homework / happy students
* profiles for each user where we put a trust badge
* decide on the quirks of the auction system (minimum raise sum, etc.)
* should we allow comments?!
* for sellers homework submissions should be verified by _trusted authorities_
    * we also should run the anti-pliagiarism system on their submissions with our archive
* provide a deadline for sending the money, after the auction finished
* when we receive the money send the homework
    * by email?!
    * put it on S3 and give them a download link?!
    * make them SSH the server and destroy it afterwards?!
* registration by invites (the it builds hype, but doesn't necesarly stop the teachers)

## Auction system

* homework should be categorized (year, semester, object, serie), which will help if multiple people want to sell the same homework (maybe some will sell the same homework in different programming languages)
* homework should be split in verified and un-verified (you may say you will do a homework
* alerts when your bid is detroned
* alerts when the homework you want is posted
* maybe allow blind-auctions for the hardcore months
* gauges for the __MOST WANTED__ homework, leaderboard for sellers
* maybe subscription system?!

## Payments

* obviously Bitcoin for those who want to be truly anonymous (we could post links to them)
* a Paypal account for the others
* card payments?! pe firmă/persoană fizică?!
* how do we pay back the sellers?!

# Technology stack

* Python3/Django1.6
* AWS
* integrate a payment processor (PayU?!)
* .com anonymous domain

# Legal issues

* research if we could be sued
* students could repeat the year if someone learns that their homework is copied

#### Legal decision

After discussing with my parents, there isn't a legal way for me, to make a company, and buy homework from the students which make it. I must make a transaction with them, where the goods are sold and they must pay taxes on it. Just putting up an auction website and letting students deal themselves with the transactions, cannot guarantee that I claim my 30% part. If I say that I have done all the homework, then it's illegal for me to pull out the money from the company and pay my "subcontractors".

# Initial investment

* anonymous .com domain
* time coding up the website

# Launching

* make fake accounts and payments in the database
* send invites from an anonymous email to smart guys
* to promote it, send a forward from that email from a fake email account (maybe even impersonate someone) and be scandalized that this website is up

# Future business

* meditații
    * admitere
    * olimpiadă
* blogging platform?!
