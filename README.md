# Test repository

This is a test repo that will be removed after the tests complete.

Tested:
- push to main blocked (require PR)
- require linear history (set by ruleset)
- require review from code owner
- do not require review if PR by only code owner

Test FAILED:
- do not require review if PR by one of several code owners


Results:
- permissions work to block unwanted PRs merging
- permissions too restrictive:
  - GOOD: PRs changing code owner by 1 user only require review is PR was created by someone else
  - BAD:  PRs changing code owned by a team of 1 require review from other user (that does not exist if owners created the PR)
  - UGLY: PRs changing code owned by PR author STILL require a review 

REQUIRE bypass for maintainers: needed to fix problems from last 2 results

