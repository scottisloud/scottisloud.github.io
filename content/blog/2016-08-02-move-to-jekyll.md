---
date: "2016-08-02"
layout: post
published: true
title: Moving my website from Wordpress to Jekyll
---
My regular reader will have noticed recent change to the appearance of Recall These Thoughts. For the second time in one year I've changed blog platforms. You, dear reader, will likely remember the move away from Squarespace over to Wordpress. This was motivated as both a cost-saving measure and a way to gain a bit of additional flexibility. I love Squarespace, but a big part of having a blog for me is having a little toy to tinker with. Wordpress offered a bit more of that type of freedom.  

But Wordpress has its downsides. For one, it was very difficult to modify templates. The CSS was was already condensed and extremely complex – thus largely inscrutable. This made some template modifications difficult to make. Moreover, if you neglected to make a child template prior to making all of your changes (as I did) and an update is issued to your template, you're in for a world of hurt.

I also found the backend to be "weighty". There was a lot of stuff back there, a lot of things I didn't need. The editor was a bit fussy, it didn't always handle markdown very well, and it really just offered more than I needed.

Overall Wordpress was just *too much* and not really that fun to play with. It is a powerful and popular platform, but it didn't offer me the type of tinkering I really yearned for. I wanted something a little simpler, a little faster, a little more fun to play with for this amateur coder.

I had tried to install Jekyll about a year ago. Jekyll is a Ruby and Liquid based static website generator. Having no familiarity with Ruby and only the most basic competence with the command line, I got hung up and frustrated with Jekyll.

Fast forward about a year. During an evening of being unable to sleep I poked around and worked on installing Jekyll once more. Sure enough I was able to get it installed, located a template that would make a good foundation for my site, and off I went learning and tweaking. At this point things moved quickly. While unfamiliar with SASS as a styling language, it's a lot like CSS with which I am extremely familiar. I found my way around the single CSS file quickly and learned with little trouble the classes that were used in the various layout files.

I also got the hang of the Liquid variables that Jekyll uses, making theme modification even easier. I even went ahead and created a few conditional loops to auto-detect when I make a "linked list" style post and have it format that correctly and offer a permalink.

I used Ben Balter's [Jekyll Exporter Wordpress plugin](https://wordpress.org/plugins/jekyll-exporter/) to export my posts from Wordpress, which it did with amazing accuracy. There were a few things that needed tidying that got a bit messed up converting from HTML to markdown, but most of that could be accomplished using find and replace. Beyond that I had all my old posts locked and loaded, my theme thoroughly customized, and was ready to pull the trigger. I synced the built site from my development directory to my host, and the new site launched with only a couple hitches.

So what is the payoff? The biggest payoff is, perhaps, that the site loads about 4X faster and is about 1/8th the size. This is important for me because I have extremely cheap hosting, and I value the experience of my one regular reader.

The other payoff is portability. My posts are written in markdown and live in a directory on my computer. They are not in an SQL database with a bunch of auto-generated HTML. While there are ways to write and backup posts for Wordpress, Jekyll's workflow has easy writing, local storage, and portability built into the process.

There is still work to be done, for sure. I have to migrate some more content over, fix a few posts that broke way back during the Squarespace migration, and I have a lot of little styling tweaks. But overall I'm very pleased with Jekyll and I look forward to making lots more content to enjoy.
