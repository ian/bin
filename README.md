
# Installation

```
cd ~
git clone https://github.com/ian/bin.git bin
```

Then add `~/bin` to your path (in `.bash_rc` or wherever)

```
export PATH="./bin:$PATH"
```

# Usage

## rmds

Recursively gets rid of those damn `.DS_Store` files OSX keeps lying around everywhere

## prune

Prune out merged in git branches, local and remote.

```
~/Projects/foo [master]
→ prune
Already on 'master'
Your branch is up-to-date with 'origin/master'.
Deleted branch test (was 1234567).
```

## squash

Squashes a branch down to a single commit based on its divergence SHA

```
~/Projects/foo [feature]
→ squash "Some feature I've been working on"
[feature 1234567] commit blah blah
 14 files changed, 306 insertions(+), 143 deletions(-)
 create mode 100644 files/foo.rb
 create mode 100644 files/bar.rb
 rewrite files/baz.rb (99%)
 ...
Squashed back to 'abcdef1234567890abcdef1234567890abcdef12'
```

If you're doing git flow (aka feature branching) you'll definitely want to use this.
