# A review of the (paid) video course "Building an Application with CoffeeScript" by Darko Bozhinovski

Available at : http://www.packtpub.com/building-an-application-with-coffeescript/video

Last week I replied to an email on the CoffeeScript mailing list asking for reviewers for a video course published by Packt.

Some background : I don't often watch screencasts (with the exception of the excellent Destroy All Software, and some Coursera MOOCs).
I know JavaScript, web development and CoffeeScript relatively well, but still got something out of this video course.

It has a total length of 1 hour and 40 minutes but is split in 8 chapters of about 3 videos each, so each video is pretty short, which I found really nice.

A github repo contains companion wiki pages and code : https://github.com/DBozhinovski/coffeescript-course/.
The example app can also be forked at https://github.com/DBozhinovski/awesomepad.

My first impression was not the best : I found it a bit hard to understand the voice, it took some getting used to the accent (even though the english is very good).
However I soon got used to it and it did not bother me after the first instants.

## contents

Section 1.1, the intro, is pretty good, and short. It briefly presents CoffeeScript.

I liked the emphasis on reading the CoffeeScript docs (website), and pointers all through the course to wikipedia pages, MV* frameworks, the github help, TodoMVC, caniuse.com, html5rocks.com, microjs.com, MDN, etc.

I liked the 'Table of contents' on the CoffeeScript website, I often read that page and looked for things with Cmd-F, but never noticed the table of contents.

In Chapter 3 on Models : I liked how the CRUD / persistence code is clean and short.
I liked the way we see the code being typed in the editor, nice speed.
The chapter also shows how to use local storage for persistence.

Chapter 4 on Routers and Views goes faster, the code isn't typed.
A bit fast for me, but we can always pause, rewind and watch it again. Or study the code in the repo. It would be too long to see it all being typed.
I found it very interesting to see how the author implemented a simple router and controller.
Those are concepts I sort of know about and use in my work but I should really dig deeper.

Chapter 5 introduces the event emitter concept, nice to see an example of that (and a mention of Backbone.Events).

Chapter 6 : here we see some fat arrows and lean arrows, I do not remember seeing an explanation.
So as I should have expected from the title, the screencast is indeed about building an application with CoffeeScript, not so much about the CoffeeScript language itself.
I somehow had a slightly wrong expectation there, and it would surely be too long to explain all of CoffeeScript here.
Likewise, in this chapter a for loop could have been written more concisely (or idiomatically) with a for comprehension, but the focus is more on building the app than on CoffeeScript itself.

Nice seeing the application changing, with new features added, and how the MVC structure makes that easy.

Chapter 7 shows an example of integrating external libraries to allow rich text editing and exporting documents to PDF, nice.

I learned about the html5 Blob API in chapter 8, that was cool.
It also shows the code for a little node server to publish a document to a Wordpress blog, neat.

I do not remember automated testing being mentioned, that would have been nice.

## conclusion

All in all I do not regret spending the time to watch these videos.
It covers briefly many interesting topics and gives many good pointers for further exploration.

It reminded me that even though I do not do it often I really like watching screencasts of people writing and describing code (for that, I cannot recommend 'Destroy All Software' highly enough).

Thanks, and good job, Darko!
