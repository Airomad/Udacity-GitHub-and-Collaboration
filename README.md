# Github & Collaboration

[Back to main repository](https://github.com/Airomad/Udacity)

## Links:
[Backup when do rebase](https://www.youtube.com/watch?time_continue=117&v=H5JqcdIB5y0)

## Git Notes:
- **shortlog** - A quick way that we can see how many commits each contributor has added to the repository.
  * Flags:
    * **-s** - to show just the number of commits (rather than each commit's message);
    * **-n** - to sort them numerically (rather than alphabetically by author name).
- **log** - Shows the commit logs.
  * Flags:
    * **--merges** - Print only merge commits. This is exactly the same as --min-parents=2.
    * **--graph** - Draw a text-based graphical representation of the commit history on the left hand side of the output. 
    * **--pretty[=<format>]** - Pretty-print the contents of the commit logs in a given format, where <format> can be one of oneline, short, medium, full, fuller, email, raw, format:<string> and tformat:<string>. When <format> is none of the above, and has %placeholder in it, it acts as if --pretty=tformat:<format> were given.
    * **--author="some author"** - Show only commits provided by specific author.
    * **--grep="some entry"** - Filter down to just the commits that reference the specific string.

- **show <SHA>** - Shows one specific commit.
- **rebase** - The command will move commits to have a new base. For instance:
  ```shell
  $ git rebase -i HEAD~3
  ```
  In the command git rebase -i HEAD~3, we're telling Git to use HEAD~3 as the base where all of the other commits (HEAD~2, HEAD~1, and HEAD) will connect to. The -i in the command stands for "interactive".