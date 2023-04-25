---
date: 2017-03-09
title: Introducing iMessageR for R
layout: post
---

## What it does
iMessageR is a small and simple package for the R statistics package that allows a user to send iMessages to any phone number or email address registered with iMessage service.

I know that there are a number of similar ways that this can be done, such as making a system call to ```mail```, but this requires that postfix be properly configured on the system, and this is not always the case. Even when this is properly configured, ```mail``` would send to conventional email addresses without issue, but receiving messages sent to carrier-provided SMS email addresses (e.g., 5551234567@txt.att.net) was unreliable. This was not ideal.

There are also a number of packages for sending messages from R using gmail. This is great but also requires some amount of additional configuration in R in order to function. I figured iMessages was the lowest friction option for Mac and iOS users.

I suspect this will be especially helpful for R users who run lengthy analyses and would like an alert to their phone (or any other iMessage capable device) indicating when the analysis is complete.

Since you can use this function any number of times and customize the message, you could even take things one step further and use iMessageR to help with debugging. For example, you could insert calls to this function at different locations in your script to indicate progress through your program. Alternatively you could insert it into a trycatch() or some other exception-handling system to alert you of an error.

## No iPhone?
Since iMessages is available to any user with a Mac, whether or not that user has an iPhone, iMessageR could be used by a Mac user regardless of the type of phone they use. Without an iPhone, the user would, of course, only be able to receive notifications on their Mac (or any other Mac also configured with that iMessage email address or phone number). So while an iPhone (or iPod Touch) is ideal in order to receive the most benefit, even Mac users without an iOS device will likely find some utility here.

## Installation

The iMessageR package can be downloaded [directly from cran](https://cran.r-project.org/package=iMessager) or can be installed from within R:

```
install.packages("iMessager")
library(iMessager)
```

This will give you access to the  function
```
send.imessage(recipient: STRING, message: STRING)
```

## Known Issues
* If the message string contains single or double quotes, the function will fail.
* If the email address or phone number is incorrect or unrecognized, there is no notice to the user.

## The future
I'd like to try to make this package more accessible to different platforms. I hope to add support for a wider range of platforms by adding options for different services. Presently I am thinking of Pushbullet or WhatsApp but this will depend on the level of API integration those services expose.

I should note that I am neither a computer programmer nor a habitual R user, so this is very new territory for me in a number of ways! As such I will try and address issues and add enhancements in my spare time, as my nascent skills allow.

## Connect with me
Connect with me on [github](https://github.com/scottisloud/imessager) where you can submit an issue or fork away!

Or reach out to me on twitter: [@scottisloud](http://twitter.com/scottisloud).
