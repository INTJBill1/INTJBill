---
title: "Bruce Springsteen - Born to Run '75"
categories:
- "2020"
---

I've been playing around with a Jekyll and GitHub Pages environment as a replacement for this WordPress hosting. The chief advantage is in its inherently static nature in the context of providing an "easy" way to update across all pages, something in which is historically hard to do with static pages, though I've had limited success in capturing keystrokes through Notepad++ if every page I created follows the same template.

The Jekyll and Github solution promotes its ease of use and you'll have to know far less, unlike WordPress's HTML, CSS, PHP, JavaScript, MySQL, and whatever else. In practice, however, a WordPress user can just use the GUI and press post whereas Jekyll/GitHub requires a developer's mindset.

Now, life would be a lot easier if I currently was running with Linux Mint, but as I'm not, setting up a Ruby environment which in turn utilized a Linux subsystem in a Windows 10 context just for Jekyll to run was NOT like the ease for which I set up my XAMPP dev environment. Though to be fair, I don't know if the Ruby Installer option actually requires the subsystem.

Fortunately, the documentation is helpful: [jekyllrb.com/docs/installation/windows/](https://jekyllrb.com/docs/installation/windows/)

Then the rest of the Jekyll setup is straightforward: [jekyllrb.com/docs/](https://jekyllrb.com/docs/)

Now, you can begin! I hope you're talented at fetching documentation for configuration and know your way around a solid text editor!

I found the default theme to be unwieldy and could never get the pagination to work correctly. I'm sure I could eventually getting it to run, but C'MON, I'm just crossing the threshold of your environment and I gotta run down solutions for things that should just work out of the box—it's hard to garner adoption.

Still, after stumbling across a data scientist's personal site [cross-validated.com](https://www.cross-validated.com/Personal-website-with-Minimal-Mistakes-Jekyll-Theme-HOWTO-Part-II/)...

...I was led to a GREAT theme with AWESOME documentation: [mmistakes.github.io/minimal-mistakes/docs/configuration/](https://mmistakes.github.io/minimal-mistakes/docs/configuration/)

The theme's author breaks from the standards in Front Matter, but nothing Notepad++'s find-and-replace couldn't mop up! I migrated my site's content and was ecstatic that the theme's author made the equivalent of a child-theme for my CSS additions.

Everything ran great on my local system! Before studying how GitHub works, I just figured I'd use the GitHub Desktop and just ram it up onto the host, not unlike I would in a FTP Client. No dice. I then opted to upload my 2 MBs of data through the GitHub site. Whether or not this worked, I don't know, because I realized my chief concern: what good is the service in the rural context of being ever so fragilely tethered to the Internet via my phone's mobile hotspot that for every single post, I'd have to upload 2 MB each time?! Of course, this is in the backdrop of my current lack of knowledge with GitHub Desktop.

Still, I'm a bit curious in how I can make the transition, even if it's a chore to publish one post, basically starting from Step 3 here, followed by a cascade of button pushing: [guides.github.com/activities/hello-world/](https://guides.github.com/activities/hello-world/)

It's not exactly the stuff of WordPress's one-click to live.

I don't mind using markdown for composition for in an HTML context, it leaves the hassle of P tags behind and I've never been good with table creation, though markdown's table creation remains arcane in comparison to the WP plugin I use (TablePress). It's not as simple as WordPress's word processor environment, but there was a time I used to run WordPress without that feature and just tagged by hand (I never liked all the meta data it adds).

Have I left the Jekyll/GitHub combo? I've only fooled with it for a couple days and I need more time with GitHub itself. I'd assume that it only uploads after I run the Jekyll build locally, and if that's the case, then I'm more apt to make the move.

But for now, my workflow is to write in FocusWriter, paste into WordPress and just click play.
