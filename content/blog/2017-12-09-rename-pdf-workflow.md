---
date: "2017-12-09"
layout: post
title: Workflow for renaming journal articles on iPad
---
I've created a [workflow][workflow] to easily rename PDF files on iOS in the following pattern:
```
author year - title.pdf
```
**[Download the Workflow application for iOS][workflowapp]**

**[Download my PDF Namer workflow][workflow]**

#### The Basics

I love reading academic journal articles on my iPad. But what about *finding* those articles and saving the PDFs of those articles in an appropriate location with a nice title? Often, while reading, I'll come across a citation to an article I want to track down. Ideally I'd be able to download and rename the file without switching devices (because lets face it, if I don't do it right this moment, I'll never do it). This can be somewhat cumbersome on an iPad, particularly if you don't have your external keyboard deployed. It can be tricky to rename a file, while viewing that file, in iOS. You got to keep, in your frail human working memory, all the details such as the title and authors that you want to include in the name.

This was the perfect sort of problem to be solved by the very powerful iOS app called [Workflow][workflowapp]. If you aren't familiar with Workflow on iOS, Workflow allows users to automate certain repetitive or complex tasks using a straightforward drag-and-drop interface ( it's a bit like Automator on the Mac).

For a primer on Workflow, check out the [great guide put together at iMore][imore], and all the detailed [articles put together by Federico Viticci at MacStories][macstories]

I've written a workflow that walks users through the process of renaming a file stored in iCloud Drive, Dropbox, or Box. Once you install the Workflow app (if you don't already have it installed), you can simply [download my workflow][workflow] to include it in your collection.

Once installed, all you have to do is run the workflow (either from the Today widget, or from within the Workflow application itself) and you'll be walked through the process of renaming the file. Here's how that should go:

1. A dialogue box will prompt you to select the PDF you want from iCloud Drive
2. Once selected, it will show you a preview of the PDF and ask you to copy the title to the clipboard and click "Done" in the top right.
3. You'll be presented with a text box containing the clipboard contents for you to confirm that you've got the title right.
4. You'll be shown a preview of the PDF again and prompted to copy the publication year to the clipboard and tap "done". If there's no easily-copiable year, you can just click Done and manually enter it in the next step.
5. You'll once again be presented with a text box filled with the date you selected. This allows you to confirm the correct year was selected, or manually enter the year if you didn't copy it to the clipboard in step 4.
6. You'll be prompted to indicate the number of authors on the article.
7. For each author (up to 3) you'll go through the preview-copy-done routine we've been through several times. If you indicate that the article has more than three authors, the workflow will only ask you for the first author's name and append "et al". If there are superscript numerals attached to authors' names, don't worry about trying to avoid copying those, the workflow will remove them for you.
8. You'll be presented with a text box containing all the author names for you to verify or enter manually.
9. Workflow will then delete the original file and prompt you to chose a location to save the newly renamed file.

Typically what I'll do is save the PDF from Safari to the root directory (the bare /iCloud Drive or /Dropbox folder) and run the workflow from the Today widget. At the end of the workflow, I save the renamed file in the proper location (whichever folder matches the subject matter of the article) and the workflow simply deletes un-named file in the root directory.

#### Nitty Gritty

This seems like a lot of steps, but the beauty of this workflow is that you can go through the renaming process without having to touch the keyboard at all.

Now for some more technical details for those who want to get into the weeds a bit.

For such a simple task – renaming a file and saving it back to the location you choose – it looks somewhat complicated. I've included a number of conditionals and error-correcting steps to try account for as many contingencies as possible.

1. Not all PDFs contain selectable text, or the actual text layer is corrupt. This is why you are prompted to verify the clipboard contents: if there are errors this allows you to correct it, if the text isn't selectable, you can enter it manually. This adds an extra step to each part of the title, but it means that this workflow is still usable in most cases even for old or edge-case PDFs.
2. I deal with strange capitalizations and strip special or unwanted characters like trailing spaces at each step. In many cases, journals will use superscript numerals to denote author affiliations. I've noticed that using the iOS text selectors, it can be hard to avoid these numerals, so in the Author selection stage, I use a REGEX query to find numerals and delete them. A similar issue exists with journal titles that span across a line. In some cases, this may actually result in a line-break being copied to the clipboard. Again, a REGEX query finds these and replaces them with a space.
4. If there are more than three authors, I want to append an "et al" rather than have the user copy and paste a dozen author names. This required me to set up several nested conditionals for one author, between 1 and 4 authors, and 4 or more authors.

#### Customizations
My default the workflow prompts you to select a file from iCloud Drive, which is my file sync of choice. If you want to have it prompt you to select files from Dropbox or Box, simply make the appropriate change to "Get File" and "Save File" actions at the beginning and end of the Workflow.

Unfortunately, if you would like to have the filename contain different information or ordered differently, that would require some extensive reconfiguring of the workflow. Feel free to dive in to try and do it yourself if you'd like, or reach out to me and I'll see what I can do.

Reach out to me on Twitter and let me know how it goes!

[workflow]: https://workflow.is/workflows/0cba45c16ab74b00a83148d67bf4ee25
[workflowapp]: https://itunes.apple.com/us/app/workflow/id915249334?mt=8
[imore]: https://www.imore.com/how-use-workflow-ios-when-you-dont-know-where-start
[macstories]: https://www.macstories.net/tag/workflow/