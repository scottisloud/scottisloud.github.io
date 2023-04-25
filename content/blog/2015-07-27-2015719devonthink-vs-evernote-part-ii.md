---
id: 55
title: DEVONthink and Evernote Part II
date: 2015-07-27T15:23:00+00:00
author: scottisloud
layout: post
---
[Last post]({{site.baseurl}}/2015/07/21/2015719devonthink-vs-evernote-part-i/) we left off with how Evernote and DEVONthink handle data a bit differently. This week we begin with a very useful feature in both applications, but with slight differences in their implementation, which lead to very different possibilities.

### Evernote allows you to create links to notes {#evernoteallowsyoutocreatelinkstonotes}

&#8220;Note Links&#8221; are great for a few reasons. Note links are hyperlinks (like you see on any website), but they take you to specific Evernote notes. You can use links _within_ Evernote to connect one Evernote note to another, or even use a link _outside_ of Evernote to bring you to that specific note.

Here's an example of using note links within Evernote. You might, for example, collect some travel documents for an upcoming trip: Hotel Confirmation email, flight itinerary, your airport shuttle ticket, and some interesting sights near your hotel. They live in your Travel notebook and perhaps you tag them &#8220;italy1014&#8221; (my tagging scheme involves the place name, followed by a MMYY suffix so, Italy October 2014 in the case of this example). You might also make a &#8220;Table of Contents&#8221; note by selecting all of these notes and choosing &#8220;Create Table of Contents&#8221;. You then end up with a nice single note that has links to all the itinerary items like this one:

<figure>
  <img src="/img/en-travel-toc.png" alt="An example of a travel itinerary Table of Contents in Evernote" title="An example of a travel itinerary Table of Contents in Evernote" />
</figure>
An example of a travel itinerary Table of Contents in Evernote is pictured above. Now you can put this table of contents note in your Evernote shortcuts for easy access to ALL of your tip documents, instead of putting every travel document in your shortcuts which would cluttering things up!

<figure>
  <img src="/img/en-calendar-note-link.png" alt="An event with an Evernote link in a shared calendar" title="An event with an Evernote link in a shared calendar" />
</figure>

An example of using note links outside of Evernote: My partner and I have a collection of recipes in a shared notebook that we add to regularly. We also share a household calendar. We plan our dinners out for each week (well, most of the time we at least _try_ to do that) and create calendar events for each dinner. In the URL section for each event, if the recipe is stored in Evernote, we'll put a note link to that recipe. This way, no matter who happens to be home that day to cook, she and I both have access to the recipe easily from our Mac or iOS device (Yes, the links even work for Calendar and Evernote in iOS even if you set up the link on the Mac!). The same goes for task managers. I use OmniFocus and regularly use note links to surface important documents associated with an action in Omnifocus.

### DEVONthink allows you to create links to any document or file {#devonthinkallowsyoutocreatelinkstoanydocumentorfile}

You can make links to any file in DEVONthink, just as you can in Evernote, and you can also make Table of Contents notes. The major difference with DEVONthink is that you can link directly to any file imported to, or indexed by, DEVONthink, not just a note containing an attachment. This is a bit more elegant in some respects.

With PDFs you can go one step further and make links to specific PDF pages. One of the major benefits of this is discussed in my previous post [Summarizing Academic Literature with OmniOutliner and DEVONthink](/blog/2015/7/17/a85blcjcd1f84oww91896arr04v2g3). As with Evernote, I also use links to DEVONthink documents in Calendar and OmniFocus to surface important files related to events or actions. DEVONthink can even (automatically) make wiki-like links between files in your DEVONthink database, which is pretty special, but perhaps deserving of its own post.

### Evernote has a web clipper {#evernotehasawebclipper}

It is dead simple and works well almost all of the time.

### DEVONthink has a web clipper {#devonthinkhasawebclipper}

It is more complicated but a great deal more flexible, and works well once you figure out which combination of settings works for your needs.

### Evernote shows me three notes (and external content) related to my current note {#evernoteshowsmethreenotesandexternalcontentrelatedtomycurrentnote}

Evernote has a feature called &#8220;Context&#8221; (formerly &#8220;Related Notes&#8221;). This feature shows a few related notes, LinkedIn contacts, or articles from select news publications related to the content of the note you are viewing. I have never found this immensely useful for surfacing things I desperately need, but it is an interesting feature (which can be disabled). The idea is to connect you to related things to what you are reading. I've never found it immensely successful.

### DEVONthink shows me where to put my files, and suggests dozens of related files as well {#devonthinkshowsmewheretoputmyfilesandsuggestsdozensofrelatedfilesaswell}

DEVONthink has what they refer to as an &#8220;Artificial Intelligence&#8221; engine that, among other things, serves two functions. One, &#8220;Classify&#8221;: It analyzes the contents of the currently open database and suggests which folders the selected file belongs in. For me, this is especially helpful when I have just added a whole pile of new journal articles to my database of academic literature. Instead of dwelling on where to put each one, the AI makes some suggestions that, in general are solid fits. One stroke of the keyboard shortcut and that article is filed away in the appropriate folder in DEVONthink.

<figure>
  <img src="/img/dt-see-also-classify.png" alt="The right hand drawer shows suggestions for where this article should be sorted. The lower half of the drawer suggests related content" title="The right hand drawer shows suggestions for where this article should be sorted. The lower half of the drawer suggests related content." />
</figure>

Second, &#8220;See Also&#8221;: DEVONthink suggests other files that might be related to the one you currently have selected, as shown in the above image. When you have a large library of PDFs like I do, it can be very nice to have DEVONthink suggest a slew of related articles, allowing you to easily go down a bit of a literature-reviewing rabbit hole. More about how this set of features works can be found on DEVONtechnologies' [write up](http://www.devontechnologies.com/technology.html).

### Miscellany {#miscellany}

  * Both applications can be controlled with automator/applescripts, but DEVONthink is <s data-preserve-html-node="true">a bit more capable</s> waaaaayyy more capable in this regard.

    <blockquote data-preserve-html-node="true" class="twitter-tweet" lang="en">
      <p data-preserve-html-node="true" lang="en" dir="ltr">
        <a data-preserve-html-node="true" href="https://twitter.com/ScottIsLoud">@scottisloud</a> On automation, you wrote, &#8220;DEVONthink is a bit more capable&#8221;. Change &#8220;a bit&#8221; to &#8220;WAAAAAAAYYYY MORE&#8221;.<br /> No seriously.<br /> :^)
      </p>

      <p>
        — DEVONtechnologies (@devontech) <a data-preserve-html-node="true" href="https://twitter.com/devontech/status/626129501357879296">July 28, 2015</a>
      </p>
    </blockquote>

  * DEVONthink (Pro Office, the top tier version) allows you to use a Mail.app plugin to add mail messages or mailboxes to DEVONthink. Evernote requires you to forward messages to an special email address (and sometimes the results aren't perfect).
  * DEVONthink (Pro Office, the top tier version) allows you to turn scans of text into selectable, searchable text with extremely good accuracy (Using ABBYY's OCR package). Evernote has no such function, but Evernote will make images of text, including handwriting searchable (but NOT selectable), with a surprisingly high level of accuracy.
  * Evernote imposes &#8220;upload&#8221; limits on some subscription levels, and also various other seemingly arbitrary usage limits. DEVONthink has no limits except for your computer's resources.
  * DEVONthink's documentation is detailed, accurate, and up-to-date. Evernote's documentation lacks detail, is frequently out of date, and is not centralized (this is, in part, a reflection of the level of complexity of the two applications. DEVONthink needs detailed documentation even to get a handle on the basic, Evernote is slightly more straightforward, at least at a basic level).
  * Both applications offer robust search capabilities. Evernote's search is syntax driven, which makes it easy to generate good search terms if you remember the syntax. DEVONthink's searching is perhaps more powerful on the whole, but it is not fully syntax-driven and thus, generating a search term can be a bit more of a chore.

    ## Conclusions {#conclusions}

    As you can see the two programs serve very different sets of needs, and this only scratches the surface of what both applications are capable of. I hope that this set of contrasts helps you to understand that it is not a matter of deciding _between_ DEVONthink and Evernote, but rather it is about how each one may or may not suit your needs in various contexts. This post is intended to be a set of broad strokes to showcase some of the similarities and differences between the applications. It was not intended to be instructional or a comprehensive guide to features. I'll be making more posts dedicated to specific features and workflows in the future. If you haven't already, do check out my workflow for summarizing documents in DEVONthink and OmniOutliner. If you are curious about any specific details contact me on twitter or comment below and if its something I am knowledgable about, I'll reply or perhaps even dedicate a post to answering the question.

    I'd also strongly encourage you to check out Christopher Mayo's great post about [Getting Started with DEVONthink](http://www.christopher-mayo.com/?p=2237), and explore [his other DEVONthink posts](http://www.christopher-mayo.com/?cat=40).
