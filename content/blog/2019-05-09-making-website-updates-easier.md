---
date: 2019-05-09
title: Making Jekyll Website Updates Easier with rsync
layout: post
---

This website is created using [Jekyll](https://jekyllrb.com/). Jekyll is great for making simple, static websites like this one. Jekyll makes composing new posts super easy since posts are just basic markdown files. What does take a bit of effort is actually publishing a post. I run Jekyll locally, so there is no "publish" button I can just press and let loose my words on the world like users of fully hosted CMS (e.g., Wordpress) can. Every time a Jekyll site is modified it needs to be rebuilt and the modified files uploaded to the server. 

This was just enough friction to seriously discourage posting or otherwise updating this site. Until recently my workflow looked something like this:

![alt-text]({{site.baseurl}}/img/jekyll-serve.png)

1. Open the local directory for my site in BBEdit. 
2. Use an [Alfred](https://www.alfredapp.com) workflow to run in terminal ```jekyll serve --livereload```, and then launch a new Safari tab displaying the locally-served version of this site to see changes as they happen. 
3. Make the desired changes/compose a new post
4. Use an Alfred workflow to run ```bundle exec jekyll build``` to build the final version of the site
5. Launch [Transmit](https://www.panic.com/transmit/)
6. connect to my host and navigate to the correct remote and local directories, 
7. upload the files via SFTP using Transmit's Sync function.

![alt-text]({{site.baseurl}}/img/transmit.png)

While I made certain Jekyll-related tasks a bit easier with the help of Alfred, such as live-monitoring changes and doing the final build with just a couple keystrokes, I never quite got around to streamlining that fifth step. That fifth step was where the friction was. Uploading the site always took longer than I'd like, requiring me to babysit Transmit while it did its thing and make sure I was in the correct directory locally and remotely so I don't accidentally [delete the entire contents of the server](https://twitter.com/ScottIsLoud/status/1123608344147763200). In general it was just a lot of clicking and waiting. 

I finally sat down to streamline that fifth step. If I could write a quick bash script to copy the files from my local machine to the server, I could invoke it with Alfred and hopefully make more of the upload process automatic.  My first instinct was to use ```scp``` in the command line, which could have worked with a few tweaks to how my Jekyll site gets build locally. ```sftp``` could also have worked but seemed a bit more challenging to write into a standalone script. ```rsync``` ended up being my weapon of choice. It's secure, it only transfers modified and new files, and is not fussy in terms of scripting. 

The result is a much faster and less error-prone workflow:
1. Open the local directory for my site in BBEdit. 
2. Trigger (jserve) an [Alfred](https://www.alfredapp.com) workflow to run in terminal ```jekyll serve --livereload```, and then launch a new Safari tab displaying the locally-served version of this site to see changes as they happen. 
3. Make the desired changes/compose a new post
4. Trigger (jbuild) an Alfred workflow to run ```bundle exec jekyll build``` to build the final version of the site
5. Trigger (jpush) an Alfred workflow to execute the ```rsync```. 

The entire site is updated in a matter of seconds, whereas the previous method took minutes for Transmit to perform its sync task – and that's after I did all of the launching and navigating. 

The one potential downside – though not a major concern for me personally - is that in order for the ```rsync``` to work in a totally hands-off manner, I had to set up key-based SSH authentication *without a passphrase* (a straightforward guide is available from [Linode](https://linode.com/docs/security/authentication/use-public-key-authentication-with-ssh/)). This makes life a lot easier but the absence of a passphrase means it is a bit less secure. 

Look forward to more posts and updates on here courtesy of this new streamlined workflow. If you know of other, potentially better ways to accomplish this, reach out!