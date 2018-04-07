# Todo
|key|Action|
|---|------|
-|Planning
\*|in progress
✓ | Finished
<sup>_If there is nothing at the end of an item, that item has not yet been started._</sup>

### Fixes -

- [ ] fix returns in cmdjobs -
> Jobs should be returning a dict object with a single key 'msg' in which it stores pertinent information being returned from a method.  The following methods need to be checked.

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
* 04-07-18, (18:52) - testing suite setUp, tearDown, creation test complete

##### Functionality to test:
> - [x] setUp ✓
> - [x] tearDown ✓
> - [ ] approve
> - [ ] assign_job
> - [ ] assign
> - [ ] catchup
> - [ ] checkin
> - [ ] clean
> - [ ] credits
> - [ ] checkout
> - [ ] claim
> - [ ] clone
> - [ ] complete
> - [x] create ✓
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

