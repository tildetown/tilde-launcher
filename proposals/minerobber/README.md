# `tilde` - A tilde-launcher proposal in Python

This is my proposal for the tilde town program launcher. Here are the features that make it compliant with the specs:

 - It has a help menu that, while not meeting the format of the specs, gives an example usage string and description.
 - It implements the contrib system beautifully (IMO)

Here are the things I have left to make before this proposal can be considered a true answer to the specs:

 - [ ] Implement submit process
 - [ ] Implement other commands shown in help example (see below)
 - [ ] Polish some rough logic

## Top-level commands

 - [X] help - complete
 - [X] contrib - complete
 - [X] chat - complete
 - [ ] mail - just need to write this one
 - [ ] page - see Questions section below
 - [ ] poetry - just need to write this one to work with prosaic (I assume)
 - [ ] submit - probably can use the same mechanic as page (unless a volunteer admin could be tasked with this, in which case, this would submit to the volunteer portal
 - [ ] toot and tweet - just need to write these
 - [ ] wiki - not gonna lie, just going to wrap the wiki tool as it exists on this one; you want thin, you got it

## Questions

### `tilde page`

 - How should this be accomplished?
 - Is this supposed to be only for vilmibm or for an admin in general to help?
 - If the answer to the previous question is the latter, how should this be accomplished?

### `tilde submit`

Same as above.

## Requirements

In `/tilde/special`, put:

 - `chat` - launches IRC (however you want to do it)
 - `list` - see list program in this directory
