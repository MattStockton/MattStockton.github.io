---
title: My bank password is 'sort-of' hashed
---

Yesterday, I called Fidelity to get help with my account. Before I was connected to a human, I was asked to enter my username, and then my password using the phone keypad. I did a double-take when I started entering my password. Clearly, my password isn't all numbers --- Are they really just storing my password encrypted rather than storing it hashed? That would make me uncomfortable, but I needed to get a thing done, so I keyed in my password. 

Later on, I started thinking through the problem. How could they allow me to key in my password using a phone keypad and verify it, if my password is allowed to have non-digits in it? Let's give Fidelity the benefit of the doubt and assume that they are not storing it plan-text or just encrypted --- let's assume they are storing a hash. 

Let's then look at a simple example. Pretend my password is 'password'. For me to be able to login to their website, Fidelity needs to store some hash of the word 'password'. When I enter my password on the phone keypad, I need to enter the corresponding digits, so I would enter: 72779673.

At this point, how does Fidelity verify my password? If they stored the hash of 'password', then they would need to re-construct the word 'password' from 72779673 and then verify that. Then the problem becomes how do they re-construct the word 'password' from 72779673? 

For most digits on the keypad, there are 7 possible alphanumeric values it could represent. For example, the number 3 could represent: 3, D, E, F, d, e, or f. This is different for the numbers 1, 7, 9, and 0 (1 and 0 have no associated letters, and 7 and 9 have 4 associated letters instead of 3). Following from this, the digits 72779673 could be converted to 20,253,807 possible alphanumeric passwords (9x7x9x9x9x7x9x7). For example, it could be converted to 'password', but it could also be converted to 'PASSWORD' or even 'q2S7Y6pD'

For Fidelity to verify my keyed in password if they just store the hash of the password, they would have to cycle through the 20+ million possible alphanumeric passwords and compare each to the stored hash until they found a result. I convinced myself that there is no way they are doing this.

So how are they making this work? My speculation is as follows: They must be storing the hashed password, and they are also storing the hash of the password converted to digits. By storing hash('password'), you are able to login to the website. And by also storing hash(converted('password')) which in this case is hash('72779673'), you can be authenticated using a phone keypad.

My final thought on this was the following: I setup my account about 10 years ago, and most likely Fidelity has implemented this phone authentication functionality after I opened the account. Before they implemented this functionality, it's unlikely they were storing the hash(converted('password')) in their database. So how did they roll out the functionality? Did they force everyone to change their password? Probably not --- they just disabled the functionality on a user-by-user basis until you logged in via the website for the first time after the functionality rolled out. Then, since they could verify your password with comparison against hash('password'), and they have your plain-text password that you entered, they can calculate hash(converted('password')), store it, and then enable the phone functionality for you. Pretty neat, and a fun thought exercise for me!

So my question is: Am I missing something? Are there other security-related items to consider here? Am I even thinking about this the right way? I'm curious to get your thoughts.
