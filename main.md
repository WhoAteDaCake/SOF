# Email client

<div style="width:100%;height:100%;padding-bottom:6em;display:flex;justify-content:flex-end;">
  <p style="text-align: center;margin-top:auto;">By Augustinas Jokubauskas 2018</p>
</div>

---

## Document introduction

Email is considered as a medium that provides maximum reach for minimal investment and has served as an essential element of many marketing campaigns across all industries. Especially now, when more people than ever are getting access to internet. As developers we want the email clients to be easy and comfortable to use, but how do we do that?

### Solution

By using ethnomethodology and field work to observe paper mail handling workflow at home to get the insight of human behaviour in dealing with mail. Paper mail can differ from home to home, so we will be observing behaviours to determine, what functionality does our email client require. We will also be using the data collected by Richard Harper and his book "Inside the Smart Home"

---

## Informal requirements report

### The common approach to handling mail at home

Mail arrives at a delivery point

> Our client needs to have an entry point which the emails will be sent to. Always has to be one and all users should have access to it.

Mail is collected and placed to a shared space

> Our client needs a shared space which users have access to and can sort the mail that was directed to the house or to a specific user. Also directed mail can not be open by anyone else than the specified receiver, which means the system needs an authentication system

Mail is sorted and spam is gotten rid of

> Our client should be able to show visual queues for emails, so that obvious spam letter can be gotten rid of and mail can be sorted into relative groups based on importance. Users should also be able to assign letters to other users.

Mail is viewed by the receiver in private

> Our client should allow for separate user accounts which have unique identifications for storing emails, so that privacy is maintained.

---

Mail that does not require immediate action is placed somewhere where it can be dealt with later on

> Our client needs to be able to make reminders about mail and allow users to set dates when to be reminded of the mail

Mail that does not require to be dealt with is put away

> Our client should allow users to move email into long term storage, where it would not interfere with new incoming email

Mail that is unique (birthday, holiday, thank you cards etc. )

> Our client should allow users to create email storage groups for separating email.

---

### Findings by Richard Harper

Small scale survey has shown that women will share up to 57 per cent of the letters addressed to them (this includes all types of letters from personal to direct mail)

> Our client should allow to share email contents between users.

Parents will not only sift out what they believe their children should or should not receive; sometimes they will ensure that their children know that this is being done

> Our client should be able to handle priveleges and permissions, so that some users can view all of the email and send it out to other users

Sharing may be supported in a sequential process with e-mail,when for example, a mother and child take turns with a screen. Alternatively, email can be shared concurrently, with various members of the household having their own screens in various places.

> Our client should be accessible from multiple devices and be able to read different data in parallel.

Imagine a scenario where an organisation using paper-mail recognises that some types of information or product offering should be sent to the household, rather than to some particular person within a household.

> Our client should have a house address, which can accept all incomming mail, that then can be further spread out

---

### Additional improvements

The household can receive a lot of spam mail. And it needs to be dealth with

> Out system should allow users to tag mail senders as spam, so the mail can be filtered out

---

## Functional requirements of the system

| ID     |                                          Requirement                                           |
| ------ | :--------------------------------------------------------------------------------------------: |
| FREQ-1 |    System should have an entry point (email address) for all letters sent to house address     |
| FREQ-2 |                    All users should have access to systems collection point                    |
| FREQ-3 |          System should have a visual interface, where all emails should be displayed           |
| FREQ-4 | System should have user system, where people can register with their name,surname and password |
| FREQ-5 |                   System should only the recipients of the email to open it                    |
| FREQ-6 |                    System should allow users to assign email to other users                    |
| FREQ-7 |                 System should allow openning email that was sent to the house                  |
| FREQ-8 |                              System should allow to delete emails                              |

---

| ID      |                                    Requirement                                     |
| ------- | :--------------------------------------------------------------------------------: |
| FREQ-9  |           System should allow to preview contents of email sent to house           |
| FREQ-10 |            System should should have a grouping system for house email             |
| FREQ-10 |    System should should allow users to access their email from multiple devices    |
| FREQ-11 |                System should be able to set reminders about emails                 |
| FREQ-12 |                  System should have long term storage for emails                   |
| FREQ-13 |                     System should have ability to group emails                     |
| FREQ-14 |             System should allow users to share emails with other users             |
| FREQ-15 |                      System should have a permissions system                       |
| FREQ-16 | System should allow users to monitor incomming mail if they have right permissions |
| FREQ-17 |              System should allow multiple users to use system at once              |

---

## Non-functional requirements of the system

| ID      |                                           Requirement                                            |
| ------- | :----------------------------------------------------------------------------------------------: |
| NFREQ-1 |     System must have one server that can handle incomming emails without loosing any of them     |
| NFREQ-2 |       System must host one authentication server that can store data of more than 7 users        |
| NFREQ-3 | System shall have a visual interface that users can interact with with no grater than 1s latency |
| NFREQ-4 |                         System must support more than 7 concurrent users                         |
| NFREQ-5 |   All incomming emails should take no longer than 5 minutes to appear on the visual interface    |
| NFREQ-6 |           System should be able to store long term store emails for at least 2 months            |
| NFREQ-7 |       System should be able to load back up after going down in no longer than 10 minutes        |

---

## System overview

![Alt Text](./images/sytem_context_diagram.png "Context diagram")

---

## Formal description of the system behaviour

![Alt Text](./images/System_activity_diagram.png "Activity diagram")

![Alt Text](./images/sequence_diag.png "Activity diagram")

---

## Examples of system usage

* A person living in a house receives an email, he loooks at the master email client to see that it just contains some spam for a local dealership, person deletes the email.

* A person living in a house receives an email, he finds out that it's a greeting from his aunt, he moves it to notice board, so everyone can see it.

* A person living in a house receives an email, he finds out that it's a personal phone bill, so he moves the email to his own account.
