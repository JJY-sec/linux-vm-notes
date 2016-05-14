# Linux VM Notes

__NOTE:__ I'll be targeting [Linux 4.6-rc7][linux-4.6-rc7] for now until 4.6 is
 released release is made (quite likely tomorrow, 15th May 2016), at which point
 that will remain (for now :) the target release version these notes refer to.

## Contents

* [Fundamentals](fundamentals.md)

## Assumptions

* I target [(almost-)4.6][linux-4.6-rc7].

* To begin with I'm going to focus on bog-standard x86-64 UMA
  (i.e. non-[NUMA][numa]) - the notes will, without necessarily saying so,
  assume this is the only system in existence.

* I am stupid and constantly make mistakes. Don't take what I say to be
  correct - check everything. I'm keeping track of the 'certainty level' of each
  document which should act as some kind of guide.

* Arsenal will win the league at some point in the future.

## Introduction

This repo is a place for me to write up some notes on the linux 4.6 VM
subsystem. I don't make any claim to their quality or usefulness, this is just a
'scratchpad' of sorts for me to use a reference in the future.

These originate from [notes][linux-gorman] I took from the excellent
[Understanding the Linux Virtual Memory Manager][amazon-gorman] by
[Mel Gorman][gorman] which, while great, target the 2.4.22 kernel which was
released in 2003, somewhat out of date :)

I am specifically targeting the 4.6 kernel since it is the (almost-)current
mainline version at the time of writing and should remain a sane and stable
basis for notes and hacks for the foreseeable future.

I may update to newer kernel versions over time depending on whether it makes
sense to do so (and if I succeed at this project of course!)

## Hacks

Talking of hacks, the sister repo to this one - [linux-vm-hacks][vm-hacks] - is
where I'm keeping code and patches intended to help me understand the VM
subsystem.

## Utilities

For tools that might be of some actual use, [memutils][memutils] is the place to
be.

Additionally, I've created some [kernel hacking scripts][kernel-scripts] that
some people might find useful for configuring, compiling and running kernels
under qemu amongst other things.

## License

These notes are licensed under [Creative Commons BY-NC-SA][license] - basically
do what you want with them as long as you:

1. Use them in a non-commercial setting.

2. Provide proper attribution.

3. Distribute them under the same license.

Take a look at the official Creative Commons site if you need more details.

[linux-4.6-rc7]:https://github.com/torvalds/linux/tree/v4.6-rc7
[numa]:https://en.wikipedia.org/wiki/Non-uniform_memory_access
[linux-gorman]:https://github.com/lorenzo-stoakes/linux-gorman-book-notes
[amazon-gorman]:http://www.amazon.co.uk/Understanding-Virtual-Memory-Manager-Perens/dp/0131453483
[gorman]:http://www.csn.ul.ie/~mel/blog/
[vm-hacks]:https://github.com/lorenzo-stoakes/linux-vm-hacks
[memutils]:https://github.com/lorenzo-stoakes/memutils
[kernel-scripts]:https://github.com/lorenzo-stoakes/kernel-scripts
[license]:http://creativecommons.org/licenses/by-nc-sa/4.0/
