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

> Haven't started on this yet

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
Players who run factions should be able to be tagged as "BucketAdmin" category:"jobs"
and be allowed to administer just that bucket for faction stuff...perhaps a jobs
subsystem for guilds or factions so they can separate issues?

Need hooks so that when a person is added to a faction the addition to the job/bbsys
can be automagic.

> #### Anomaly stuff:
> Jobs has a tiered access structure. By changing who has access to
> various commands, you can selectively allow players like builders into the
> system so they can work. The access locks are on the bucket object.
> Bucket access locks are stored at the bucket level.
>
>> HAS_ACCESS: Return TRUE if a player can access the +jobs system.
>>
>> ADD_ACCESS:      Returns True if a player can use the /add command.
>> APPROVE_ACCESS:  Returns True if a player can /approve jobs.
>> COMPLETE_ACCESS: Returns True if a player can /complete jobs.
>> CREATE_ACCESS:   Returns True if a player can use the /create command.
>> DENY_ACCESS:     Returns True if a player can /deny jobs.
>> EDIT_ACCCESS:    Returns True if a player can use the /edit command.
>> GIVE_ACCESS:     Returns True if a player can use +bucket/access.
>> LOG_ACCESS:      Returns True if a player can /log a job.
>> MAIL_ACCESS:     Returns True if a player can /query and /mail.
>> STATS_ACCESS:    Returns True if a player can pull reports on the system.
>>
>> A player must pass HAS_ACCESS before the other locks are applied.
>>
>> Access to buckets are set at the bucket level (see 'baccess').
>> You can also restrict actions by bucket (see 'aaccess').
>>
>> Actions can be restricted by bucket. This allows you to customize the
>> available actions to, for instance, prevent jobs from being tampered
>> with in automated buckets. The format for this is:
>>
>> &<action code>>_ACCESS <bucket>>=<return 1 to access, 0 to deny>>
>>
>> The <action>>_ACCESS code allows for one argument: %0 == PlayerDB#.
>>
>> Example: If you do not want a job to ever be transferred out
>> of an automated XP bucket (not included) you can prevent
>> this behavior if you know the three-letter action code (in this
>> example, TRN):
>>
>> &TRN_ACCESS XP=0
>>
>> See also: access, codes
>>
>> Bucket access is set on the bucket itself, as the ACCESS attribute:
>>
>> &ACCESS <Bucket DB#>>=[switch(get(%0/RACE),VAMPIRE,1,0)]
>>
>> It should return True for access and False for no access.
"""

#### CmdJob code

# Cmd stuff
* def _approve(self, jobid, comment):
* def _assign(self, jobid, player=None):
* def _catchup(self):
* def _checkin(self, jobid):
* def _clean(self):
* def _credits(self):
* def _checkout(self, jobid):
* def _claim(self, jobid):
* def _clone(self, jobid):
* def _complete(self, jobid, comment):
* def _create(self): \*
> Job creation rests on the job object itself through Job().create(bucket, title, text) cmdjobs handles testing before allowing creation.
* def _delete(self, jobid):
* def _deny(self, jobid, comment):
* def _due(self, jobid, date=None):
* def _edit(self, jobid, entryid, old, new):
* def _esc(self, jobid, priority):
* def _help(self, jobid):
* def _joblist(self, *args, **kwargs):
* def _last(self, jobid, num):
* def _list_untag(self, jobid, player_list):
* def _list(self, bucket):
* def _lock_job(self, jobid):
* def _log(self, jobid):
* def _mail(self, jobid, message):
* def _merge(self, source, destination):
* def _overdue(self):
* def _player_tag(self, jobid, player):
* def _pri(self):
* def _publish(self, jobid, comment):
* def _query(self, player_list, title, query):
* def _rename(self, jobid, name):
* def _reports(self, report=None):
* def _search(self, pattern):
* def _select(self, expression):
* def _set(self, jobid, status):
* def _sort(self, sorttype):
* def _source(self, jobid, player_list):
* def _summary(self, jobid):
* def _sumset(self, jobid, sumset, value):
* def _tag(self, jobid):
* def _trans(self, jobid, bucket):
* def _unlock(self, jobid):
* def _untag(self, jobid):
* def _who(self, jobid):
* def _assign_job(self):
