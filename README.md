# patname

## Name

**patname** − an alternate [RFC1178](https://tools.ietf.org/html/rfc1178) implementation to generate pronounceable, sometimes even memorable, "pat names", consisting of a random combination of adverbs, an adjective, and "patrick," to specifically and affectionately mess with the many patricks in his life, and especially [@mocha](https://github.com/mocha).

## Synopsis

```
usage: patname [-w|--words INT] [-l|--letters INT] [-s|--separator STR] [-d|--dir STR] [-c|--complexity INT] [-u|--ubuntu] [-p|--patrick NAME]
```

## Options
- `-w|--words` number of words in the name, default is 2,
- `-l|--letters` maximum number of letters in each word, default is unlimited,
- `-s|--separator` string used to separate name words, default is `'-'`,
- `-d|--dir` directory containing `adverbs.txt`, `adjectives.txt`, `names.txt`, default is `/usr/share/patname/`,
- `-c|--complexity` [0, 1, 2]; 0 = easy words, 1 = standard words, 2 = complex words, default=1,
- `-u|--ubuntu` generate ubuntu-style names, alliteration of first character of each word.
- `-p|--patrick` change patrick for a different name, in the event that the target of your affection is actually named katrina, matthew, or something else.

## Description

This utility will generate "pat names", consisting of a random combination of an adverb, adjective, and "patrick". These are useful for unique hostnames or container names, for instance.

## Examples

```bash
$ patname
wiggly-patrick

$ patname --words 1
patrick

$ patname --words 3
primly-lasting-patrick

$ patname --words 4
angrily-impatiently-sage-patrick

$ patname --separator ":"
cool:patrick

$ patname --separator "" --words 3
comparablyheartlypatrick

$ patname --ubuntu
pretty-patrick

$ patname --complexity 0
massive-patrick

$ patname --patrick katrina
wiggly-katrina

$ patname --ubuntu --patrick katrina
kindly-katrina
```

## Author

This project is a joke made by Coleman Collins and his coding assistant Claude, based on [petname](https://github.com/dustinkirkland/petname) by Dustin Kirkland, where every animal name has been replaced with "patrick". Permission is granted to copy, distribute and/or modify this document and the utility under the terms of the Apache2 License.
