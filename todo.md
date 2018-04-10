# Todo
|key|Action|
|---|------|
-|Planning
\*|in progress
✓ | Finished
<sup>_If there is nothing at the end of an item, that item has not yet been started._</sup>

All settings files should have a SYSTEM variable that holds which system it's part of.

### Fixes \*

- [ ] fix returns in cmdjobs \*
> Jobs should be returning a dict object with a single key 'msg' in which it stores pertinent information being returned from a method.  The following methods need to be checked.

#### Bucket Recode -

- [ ] Maintain functionality of bucket
- [ ] Gather inventory of functions
- [ ] Clean documentation
- [ ] Refactor internal functionality
- [ ] Refactor CmdBuckets functionality

* _action_handler
* all_jobs
* _add_msg
* _set_job_number
* set_job
* table

### Feature request: Test suites
- [ ] Unit testing *

#### Jobs test suite *
* Jobs *
    - syntax to remember:
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
04-09-18, (22:20) - Outline todo list for next session.  Started planning outline for Bucket/CmdBucket recode

---

#### Functionality to test:

##### Job Object
> - [x] setUp ✓
> - [x] tearDown ✓
> - [x] create ✓
> - [ ] _getpos
> - [ ] info
> - [ ] _update_actlist
> - [ ] _hashobj
> - [ ] _add_msg

##### CmdJobs Object

> - [ ] approve
> - [ ] assign_job
> - [ ] assign
> - [ ] catchup
> - [ ] checkin
> - [ ] clean
> - [ ] create
> - [ ] credits
> - [ ] checkout
> - [ ] claim
> - [ ] clone
> - [ ] complete
> - [ ] delete
> - [ ] deny
> - [ ] due
> - [ ] edit
> - [ ] esc
> - [ ] help
> - [ ] joblist
> - [ ] last
> - [ ] list_untag
> - [ ] list
> - [ ] lock_job
> - [ ] log
> - [ ] mail
> - [ ] merge
> - [ ] overdue
> - [ ] player_tag
> - [ ] pri
> - [ ] publish
> - [ ] query
> - [ ] rename
> - [ ] reports
> - [ ] search
> - [ ] select
> - [ ] set
> - [ ] sort
> - [ ] source
> - [ ] summary
> - [ ] sumset
> - [ ] tag
> - [ ] trans
> - [ ] unlock
> - [ ] untag
> - [ ] who

#### Buckets test suite -
* Buckets -

#### Jgroups test suite -
* Jgroups -

