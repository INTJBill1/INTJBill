---
title: "Sunset 6: Finally DeGoogled"
categories:
- "2021"
tag: tech
---

It's that time again, let's play 1999's *[It's All About the Pentiums](https://www.youtube.com/watch?v=qpMvS1Q1sos)*!

It started out simple enough with my production machine: I wanted to optimize its battery usage.  In Windows, my laptop has all sorts of stamina, but in Linux, it tends to gas out early.  So, I thought I'd see if someone has written a package to rein in the horses a bit.

I didn't find anything immediately in the official repository, so I went Googling on Startpage.   A few forums later, someone made a reference to a tool.  Against my better judgment of adding outside PPA's, I added one that was mainly in Spanish.  This immediately gave me second thoughts, but I *so wanted* battery optimization!  As English is the lingua franca of the world, it's especially relevant in the Linux world, though Czechs make a surprisingly strong showing.  Still, there's an expecation if it's a collaborative work, it's gonna be in English.  

Well, you guessed it: I hosed my installation.  If it wasn't for a Timeshift save, I wouldn't have been able to recover access to my files.  Not that it was *critical*, as I had a Home backup that was a day or so old, but I'd hate to lose everything I did for the day.  And I also got a chance to see how easy it to recover a COMPLETELY flummoxed Linux Mint system! Kernel panic on boot every time!

Momentarily, I flirted with the notion to returning to Big Tech's embrace.  I mean, c'mon, don't cloud backups pull Robert Palmer onto the stage for a chorus of *Simply Irresistible*?

I came to my senses especially after the restoration of my box, but not after giving considerable thought on how delightful it would be to bring my two Chromebooks back online, prospects that seems to plummet immediately without a Google account.  

That said, even if I kept my Google account, I could no longer use those Chromebooks because Google just arbitrarily decides to end their support, that is, I now have two unpatched boxes roaming the Internet whose sole purpose is be online.  Great.  

So, I decided to change that. Insert the video montage.

Along the way, I ran across this helpful tool: [mrchromebox.tech/#fwscript](https://mrchromebox.tech/#fwscript).

...and it's use reminded of how friggin' controlling Google can be!  Just layer after layer of software hassles, in a weird bid to push me in the mud so that I wouldn't alter my own system!  With the last bit, it's just...well, it just further informs me of their proselytizing doodles!  The last barrier for me to blast through like the Kool-Aid Man for both Chromebooks was to remove the case (something I've always found unsettling with a laptop—must be these paws of mine) and pull a screw off the motherboard whose purpose was just to stop software changes!  Control much?  This ain't Apple!  This is an entity that espouses the virtues of open source software, whose Android and browser are both based on open source projects!  

So, I yanked 'em off and was able to replace ChromeOS "developer" mode with a REAL bios!  This was pivotal for a couple of reasons:  1) I can boot any USB drive; and 2) if I didn't remove it, there was this weird mode that if upon startup, I followed its default directions, it must wipe the MBR 'cause faster than a falling floppy diskette, there's this big ball of fire of wanton destruction as my ability to access MY operating system and MY files is GONE!  Oh, Google and your dark magic transforming my Elven friend into an Orcish fiend!

Once the dust settled, what was once two, mothballed machines on the shelf are now two, fully-updated laptops that are full-fledged computers, not just armorless browsers.  And the funny thing:  I can actually run the most current Chrome browser if I want!  They're not jacked—that's for sure, with one having 2 GB RAM and the other with 4 GB, but I'm trying out some lightweight distros.  Unfortunately, I keep ramming into the lack of volume across Debian-based distributions—when I get a chance, this will hopefully resolve it:

[bugs.launchpad.net/ubuntu/+source/alsa-ucm-conf/+bug/1833116](https://bugs.launchpad.net/ubuntu/+source/alsa-ucm-conf/+bug/1833116)

Most importantly, for today and all of 2022, I am DeGoogled.
