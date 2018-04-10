# taladan.github.io

Learning python with Evennia, github, pycharm and more!  I explore the thoughts and issues behind my code here.

#### Relevant links
> * [Todo list](todo.md)
> * [Configurations](configs.md)
> * [Questions](questions.md)

##### What I'm currently working on
---

<sup>04-08-18, (08:10)</sup> - So, I thought I was done with testing creation of jobs, turns out I wasn't.  I'm now working on testing the failure of job creation.  This testing process really makes you think differently about how your data is being used - at least it does for me.


<sup>04-09-18, (17:01)</sup> - Today I've set up Debian 9 on a virtual machine on my desktop to run as a development environment.  It runs faster and more dependably than my laptop, so I'm going to try and start using it during the day when I'm able to have some quiet time to program.  YAY NEW DEV ENVIRONMENT!  Oh, and the host name?  Bellerophon, for those of you in the know ;).

#### Research issues
---
(. . .)

<br>

#### Bucket recode:
---
* Bucket should hold the method for creation with Bucket.create()
* Added method for Bucket.create() - still testing

> in progress

<br>

#### Job code:
---

Ideas:
* Messages only belong to a unique object type Job()
* "Reply" functionality appends messages to extant messages

 Reply structure:
>+job/reply Job/id=message

The job will be the listing (index + 1) of the job in the order of self.jobs_list

#### Tiered level commenting system:
* Each message should have a unique id (hash)
* Comment children can be handled via tags.

#### Access:
Access is going to get a little wonky, I'm going to have to revisit how I have Bucket access set up and look into Lockstrings
Players who run factions should be able to be tagged as "BucketAdmin" category:"jobs"
and be allowed to administer just that bucket for faction stuff...perhaps a jobs
subsystem for guilds or factions so they can separate issues?

Need hooks so that when a person is added to a faction the addition to the job/bbsys
can be automagic.
