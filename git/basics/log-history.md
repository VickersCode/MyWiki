# Log History
[Table of Contents](../../README.md) | [Markdown Cheatsheet](../../Markdown%20Cheatsheet.md)

credit: [https://git-scm.com/book/en/v2](https://git-scm.com/book/en/v2)
___
There is an easy way to view previous snapshots.
Here's an example of running `git log` on this project
![git log](git-log.PNG)

This table shows the most common tags used with `git log`

|Option|Description|
|---|---|
|`-p`|Show the patch introduced with each commit.|
|`--stat`|Show statistics for files modified in each commit.|
|`--shortstat`|Display only the changed/insertions/deletions line from the `--stat` command.|
|`--name-only`|Show the list of files modified after the commit information.|
|`--name-status`|Show the list of files affected with added/modified/deleted information as well.|
|`--abbrev-commit`|Show only the first few characters of the SHA-1 checksum instead of all 40.|
|`--relative-date`|Display the date in a relative format (for example, “2 weeks ago”) instead of using the full date format.|
|`--graph`|Display an ASCII graph of the branch and merge history beside the log output.|
|`--pretty`|Show commits in an alternate format. Option values include `oneline`, `short`, `full`, `fuller`, and `format` (where you specify your own format).|
|`--oneline`|Shorthand for `--pretty=oneline --abbrev-commit` used together.|

We can also run `git log -<n>` where n equals the number of commits we want to show.

Or show the list of commits made in the past two weeks with `git log --since=2.weeks`

This table shows options to limit the output of `git log`

|Option|Description|
|---|---|
|`-<n>`|Show only the last n commits.|
|`--since`, `--after`|Limit the commits to those made after the specified date.|
|`--until`, `--before`|Limit the commits to those made before the specified date.|
|`--author`|Only show commits in which the author entry matches the specified string.|
|`--committer`|Only show commits in which the committer entry matches the specified string.|
|`--grep`|Only show commits with a commit message containing the string.|
|`-S`|Only show commits adding or removing code matching the string.|
