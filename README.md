# tilde-launcher

## background

As [tilde.town](https://tilde.town) has grown over the years, many users have
produced interesting, useful, and/or fun tools for the community to use. It
goes like this:

- person writes a tool
- person tells people in IRC about it
- people link it from their ~/bin or just call the person's script directly
- someone asks for the tool to be globally linked
- eventually ~vilmibm runs `ln -s ~/coolperson/bin/thing /usr/bin/`

This works, but new users often ask "what tilde-specific commands can i run?"
this is a good and reasonable question and it's hard to answer.

## purpose

`tilde-launcher` serves as a welcome mat to all things tilde.town and
executable.

## usage

an interaction with `tilde-launcher` should look something like this:

```
$ tilde
    Welcome to tilde.town :) this program is your gateway to town-specific
    commands and features. Run tilde help to see the sort of things you can
    do.
$ tilde help
   You can use the following commands with the tilde program:
   
   chat     join the local IRC server
   contrib  run a community command like 'feels'
   help     display this help
   mail     check your tilde.town email
   page     alert ~vilmibm to an emergency
   poetry   generate poetry from cut-up text
   toot     post a message to the community mastodon
   tweet    post a message to the community twitter
   wiki     access or update the town wiki

   You can also run:

   tilde help command

   and replace "command" with one of the above commands to get help specific
   to that command.
$ tilde contrib
    This command helps you run various community-maintained programs. If you
    want to see them all, use --list
$ tilde contrib --list
    botany
    feels
    writo
    # truncated for example's sake
$ tilde contrib botany
    # ...runs botany
```

## project goals

- As thin as possible. No actual logic should be run here.
- Easy to add to. Commands should be made available with symlinking.
- Beginner friendly. Shouldn't use any words that go undefined or aren't
  self-evident for a newcomer to Unix/Linux.

## Open questions

0. Should this be implemented in a shell script? Or something higher level?
1. Does this obsolete
   [tildetown-scripts](https://github.com/tildetown/tildetown-scripts) should
   it?
2. Should this eventually expose the admin functions afforded by
   [tildetown-admin](https://github.com/tildetown/tildetown-admin)?
