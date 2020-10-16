# tagging

**what is tagging**
- basicly marking points in a repository's history as important
 - e.g. release points
 - [Git Basics Tagging](https://git-scm.com/book/en/v2/Git-Basics-Tagging)
 - [tutorial for tagging](https://dev.to/neshaz/a-tutorial-for-tagging-releases-in-git-147e)

## basics commands

**`$ git tag`**
- lists all existing tags in alphabetical order

**`$ git tag -1 <tagname>`**
- searching a tag that matches the pattern

## create tags

1. **annotated tags**
**`$ git tag <tagname> -m '<message>'`**
- contains tagger name
- email
- date and time
- tagging messsage
- running _git show <tagname>_:
 - diplays 1st the informations above,
 - than the tagged commit


2. **lightweight tags**
**`$ git tag <tagname>`**
- basicly the commit checksum stored in a file
- creates a tag for the current HEAD
- running _git show< tagname>_:
 - just shows the tagged commit

3. **tagging later**
**`$ git tag -a <tagname> <GitID>`**
- its possible to pick a commit from history and tag it
- running _git show <tagname>_:
 - displays same informations like an annotated tag
