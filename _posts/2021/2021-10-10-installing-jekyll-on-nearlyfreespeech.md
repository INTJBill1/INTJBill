---
title: "Installing Jekyll On NearlyFreeSpeech"
categories:
- "2021"
---

If you're a cool cat like me, you want your own website.  Go with [NearlyFreeSpeech.NET](https://www.nearlyfreespeech.net/) for your webhost and domain name registrar.  It's not required to use their webhosting; there's GitHub.  Point to your own [GitHub Page](https://pages.github.com/): it's free and is beneficial in learning how Jekyll works.  You can easily generate a starter theme.  Before building my own, I got started with [Minimal-Mistakes's remote theme starter](https://mmistakes.github.io/minimal-mistakes/docs/quick-start-guide/) to gain a foothold.  Beyond education, the theme stands well on its own.  I like [Katerina Bosko's implementation](https://www.cross-validated.com/index.html).

If you're only running GitHub Desktop or use its web interface, you could just add your page/post and stick around for a few minutes for it to render out—there's a soft limit of 10 renders per hour. However, I prefer a little bit more immediacy to see things shape and hence local dev environment.

The setup is a LOT easier on Windows than what the docs indicate.  Just [grab the installer from here](https://rubyinstaller.org/) and [follow this on JekyllRB](https://jekyllrb.com/docs/).

But, what if you want your own home?  Well, bring it on back to NearlyFreeSpeech.

I threw together my own notes on how to create a Jekyll setup (as unoptimized as they are), just so that I have a checklist on hand when I decide to blow away my site for one reason or another!  Hey, in my 40s, admittedly, a step or two does slip out the backdoor; it's good to have everything there!  There's docs out there on the process, but none (that I can ever find) seem to piece it together with clarity—or includes a truckload of non-essentials.

## Jekyll Checklist for NSFN Setup

1. Create a static site on NFSN.

2. Login via SSH.

3. Setup HTTPS:
`tls-setup.sh`

4. [JekyllRB.com: Troubleshooting](https://jekyllrb.com/docs/troubleshooting/) suggests these for NFSN, so let's run them:
```
export GEM_HOME=/home/private/gems
```
```
export GEM_PATH=/home/private/gems:/usr/local/lib/ruby/gems/1.8/
```
```
export PATH=$PATH:/home/private/gems/bin
```
```
export RB_USER_INSTALL='true'
```
5. Install essentials:
`gem install jekyll bundler`

6. Within the *private* directory, create a folder (*content*) to hold markdown and site config files.

7. Upload content!

8. Enter that newly-created directory (*content*) to install GEMs by running:
`bundle install`

9. Stay there and render the content into HTML!  For all future updates, do this as well:
`bundler exec jekyll build --destination /home/public`

10.  Oh no! Once the shell session ends, the gem location is lost! Fix this for the next session by making .bash_profile and .bashrc files the same (located in *private*) by editing the .bash_profile:
```
if [ -f ~/.bashrc ]; then
   source ~/.bashrc
fi
```
11. ...and edit .bashrc:
```
export RB_USER_INSTALL='true'
export GEM_HOME=/home/private/gems
```

12. Log in via SSH and run step # 9 as deep longings necessitate while your heart hammers in ecstasy!
