# taladan.github.io
Learning python with Evennia, github, pycharm and more!  I explore the thoughts and issues behind my code here.

This is what I'm currently working on

#### Taladan's Macros
> @b (blk) - insert ">" at head of line
> @c (chkbx) - insert "- [ ] " at head of line
> @v (blkchkbx) - insert "> - [ ] " at head of line

- [ ] fix returns in cmdjobs
> * _action_handler
> * all_jobs
> * _add_msg
> * _set_job_number
> * set_job
> * table

#### Bucket recode:
---
> * Bucket should hold the method for creation with Bucket.create()

#### Job object:

Ideas:
---
* Messages only belong to a unique object type Job()
* "Reply" functionality appends messages to extant messages

> Reply structure:
> +job/reply Job/id=message

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
Feature request: CmdJobs test suite
- [ ] Unit testing

> * Jobs
>    - [ ] approve
>    - [ ] assign_job
>    - [ ] assign
>    - [ ] catchup
>    - [ ] checkin
>    - [ ] clean
>    - [ ] credits
>    - [ ] checkout
>    - [ ] claim
>    - [ ] clone
>    - [ ] complete
>    - [ ] create - In progress
>    - [ ] delete
>    - [ ] deny
>    - [ ] due
>    - [ ] edit
>    - [ ] esc
>    - [ ] help
>    - [ ] joblist
>    - [ ] last
>    - [ ] list_untag
>    - [ ] list
>    - [ ] lock_job
>    - [ ] log
>    - [ ] mail
>    - [ ] merge
>    - [ ] overdue
>    - [ ] player_tag
>    - [ ] pri
>    - [ ] publish
>    - [ ] query
>    - [ ] rename
>    - [ ] reports
>    - [ ] search
>    - [ ] select
>    - [ ] set
>    - [ ] sort
>    - [ ] source
>    - [ ] summary
>    - [ ] sumset
>    - [ ] tag
>    - [ ] trans
>    - [ ] unlock
>    - [ ] untag
>    - [ ] who

Issue: Feature Request: Buckets test suite
> * Buckets

Issue: Feature Request: Jgroups test suite
> * Jgroups
>
>

Todo:
=====

### Questions for staff
> - [ ] Ask Beag/Bolide about what the exact names of the command syntax should be:
>> #### options
>> - +command/action lh.Target/lh.action = rh.Target/rh.action
>> - +command/verb lh.noun/lh.verb = rh.noun/rh.verb

### Research issues
> - [ ]
> - [ ]

