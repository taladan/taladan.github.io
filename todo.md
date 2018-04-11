
---

##### syntax to remember:
> `super(CommandTest, self).setUp()`
> `self.assertIsequal()`
> `self.call(command, "", "expected return")`

##### Current progress:
* 04-07-18, (18:52) - testing suite setUp, tearDown, `Job().create` pass/fail tests complete

---

* 04-09-18, (21:44) - Dev environment bellerophon set up for primary development.
                      set up some preliminary test stuff for `CmdJobs().create` but it is not
                      working yet.  I'm hoping now that I've got the primary development enviroment
                      set up, I can speed up a little.

---

* 04-09-18, (22:20) - Outline todo list for next session.  Started planning outline for Bucket/CmdBucket recode

---

* 04-10-18, (11:56) - Gathered list of functions that currently exist within the scope of the jobs system.  Marked the few that I've worked on thus far, and organized my todo list accordingly.  Started some on refactoring buckets - `world.utilities.pegasus_utilities.py` is now a thing, and currently the only (TESTED!) method in there is hash - this will take two different types of strings (though they can be identical strings) and return a unique hash of those strings as an md5().hexdigest() string.  Centralized this so that all systems under pegasus can access the hash functionality if it needs to without having to do any spooky voodoo with requiring cross-system utilities.

___
---

###### Todo Key
|key|Action|
|---|------|
|-|Planning|
|\*|in progress|
|✓ | Finished|
<sup>_If there is nothing at the end of an item, that item has not yet been started._</sup>

<sup>_All settings files should have a SYSTEM variable that holds which system it's part of._</sup>


Functionality to test
===


#### Bucket Recode

- [ ] Maintain functionality of bucket
- [x] Gather inventory of functions
- [ ] Clean documentation
- [ ] Refactor internal functionality
- [ ] Refactor CmdBuckets functionality
   
##### inventory of functions

`world.jobs.bucket.py`:
---
- [ ] associated
- [ ] at_channel_creation
- [x] create
- [ ] grant_access
- [ ] has_access
- [ ] has_jobs
- [ ] info
- [ ] jobids
- [ ] monitoring
- [ ] my_jobs
- [x] per_player_actions
- [x] remove_access
- [ ] set
- [ ] _pct_complete
- [ ] _total_jobs
 

`world.jobs.cmdbuckets.py`:
---
- [ ] switchparse
- [ ] _access
- [ ] _argparse
- [ ] _assign_bucket
- [ ] _bucket_table
- [ ] _can_access
- [ ] _check
- [ ] _check_actions
- [ ] _check_table
- [ ] _character_validate
- [ ] _create
- [ ] _delete
- [ ] _info
- [ ] _monitor
- [ ] _rename
- [ ] _parse
- [ ] _parse_right
- [ ] _parse_left
- [ ] _pass_lock
- [ ] _set
- [ ] _set_timeout
- [ ] _setting_validate

`world.jobs.cmdjobs.py`:
---
- [ ] get_sortby
- [ ] all_jobs
- [ ] set_job
- [ ] table
- [ ] _act
- [ ] _action_handler
- [ ] _add_msg
- [ ] _all
- [ ] _approve
- [ ] _assign
- [ ] _assign_job
- [ ] _catchup
- [ ] _checkin
- [ ] _checkout
- [ ] _claim
- [ ] _clean
- [ ] _clone
- [ ] _complete
- [ ] _create
- [ ] _credits
- [ ] _delete
- [ ] _deny
- [ ] _due
- [ ] _edit
- [ ] _esc
- [ ] _help
- [ ] _joblist
- [ ] _last
- [ ] _list
- [ ] _lock_job
- [ ] _log
- [ ] _mail
- [ ] _merge
- [ ] _overdue
- [ ] _pri
- [ ] _publish
- [ ] _query
- [ ] _rename
- [ ] _reports
- [ ] _search
- [ ] _select
- [ ] _set
- [ ] _set_job_number
- [ ] _sortby
- [ ] _source
- [ ] _summary
- [ ] _sumset
- [ ] _tag
- [ ] _trans
- [ ] _unlock
- [ ] _untag
- [ ] _who


`world.jobs.job.py`:
---
- [ ] at_channel_creation
- [ ] create
- [ ] info
- [ ] _getpos
- [ ] _update_actlist
- [ ] _all
- [ ] _add_msg


`world.utilities.pegasus_utilities`:
---
- [x] hash
- [x] parse_args 
