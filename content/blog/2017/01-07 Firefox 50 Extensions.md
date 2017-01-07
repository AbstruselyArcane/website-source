+++
date = "2017-01-07T20:22:00+08:00"
draft = false
tags = ["", ""]
title = "Firefox 50 Extensions"
+++

About four months after my switch to Firefox, my extensions situation seems to have finally stabilised. Thus, it's time to take a comprehensive inventory of my entire browser system, for the sake of documentation in case I need to set up this system again.

I hope to still be using this in a year, but with Firefox extensions, you will never know.

## UI Enhancements

1. __Tab Centre:__ Tabs laid out vertically makes much more sense that the default horizontal configuration. The main reason is that I don't like to have wide browser windows, since most webpages utilise _vertical_ rather than _horizontal_ space, and having tabs laid out vertically makes it easier for me to find everything anyways.
2. __Reddit Enhancement Suite:__ Self-explanatory. Browsing reddit without RES drives me insane.
3. __1Password:__ While not strictly a purely UI addon, I will include it here anyways. My username and password system is beyond the scope of this article; all you need to know is that everything is managed through 1Password (along with some scripts I hacked together).
4. __DevEdition theme enabler:__ The default theme looks ugly. What more can I say?

## Privacy

1. __uBlock Origin:__ Yes, I run an adblocker, and yes, it is not purely for privacy reasons. I used to use AdBlock, but as many others have discovered, uBlock is the best when it comes to CPU and memory usage. 
2. __Ghostery:__ I am actually experimenting with removing Ghostery, since the things it blocks should already be included in uBlock, but it stays for now.
3. __Self-Destructing Cookies:__ I used to maintain a cookie whitelist, but I have found that to be _way_ to much work; setting certain websites to have their cookies kept with SDC is a system that is just as practical and requires almost no work.
4. __NoScript:__ JavaScript-blocking is a must. I don't trust most websites enough to run their code on my machine, and most pages work just fine without JS anyways. I am pretty strict with enabling JavaScript, and even with that most websites still work just fine. 
5. __Decentraleyes:__ This is a local CDN cache that requires very little maintenance, and is here for no reason other than it provides _some_ protection against fingerprinting.
6. __Random Agent Spoofer:__ This extension, as it name suggests, spoofs the UserAgent that your browser sends; it is a great protection against browser fingerprinting. It also includes some options for countering other forms of fingerprinting, like disabling JS canvas support, some of which are enabled.
7. __HTTPS Everywhere:__ Despite my misgivings about the EFF, this remains a must-have extension, since I don't like MiTM attacks, and neither should you.


## Utilities

1. __Dorando keyconfig:__ This extension is for binding shortcuts to Firefox, since it uses a custom keyboard event-handling system that is opaque and extremely hard to configure. I have just recently started playing with Hammerspoon, and I am currently experimenting with removing this extension and migrating my shortcuts over to Hammerspoon.
2. __Test pilot:__ Dependency for Tab Center; I can't remove it even if I wanted to.
3. __Add-on Compatibility Reporter:__ Temporary while I puzzle over the migration to e10s.