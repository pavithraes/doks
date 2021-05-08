---
title: "Importing Blogs to Medium"
description: "How to move/import your existing blog posts to Medium."
lead: ""
date: 2020-07-06T23:00:00+0530
lastmod: 2021-04-12T23:21:46+05:30
draft: false
weight: 50
contributors: ["Pavithra Eswaramoorthy"]
aliases: [/posts/importing-to-medium/]
---

[Bokeh](https://bokeh.org/) recently decided to move it's blog, hosted at https://blog.bokeh.org/, to the popular publishing platform [Medium](https://medium.com). This comes with a set of advantages and disadvantages, but we won't go there today. The decision was taken after careful consideration and after listening to both sides of the debate. Let's leave it at that.

Here is my overall experience moving old posts to Medium. If you plan on doing this sometime, my learnings here might be helpful. Happy reading!

## Backdating posts

When we want to move previous posts to Medium, we would also want to backdate them. Medium allows writers to ["import" posts](https://help.medium.com/hc/en-us/articles/214550207-Import-a-post). If your original blog handled the date of publishing well, then importing posts should backdate them. You will notice a line at the end of your imported blog *"Originally published at <your_blog> on <date_published.>"*

If the *date_published* is not shown, Medium is not able to parse the date you published the blog on. I added a time tag with the class attribute set to "published".

```<time datetime="{{ page.date }}" class="published">{{ page.date | date_to_long_string }}</time>```

This did the trick. :)

## Importing doesn't work flawlessly

Medium did not do a great job of importing all blog items. Please go through your posts properly before publishing.

I noticed that list items, svg images, headings and code blocks were either not imported at all or were imported incorrectly. You can copy-paste all missing elements, but it is manual work.

## Extra stuff to note

### Accessibility

Medium allows you to add alternate text to media elements (but limits it to 125 characters, why Medium?!)

I doubt medium imports any alt text from the previous blog, so take a few minutes to add it. [Accessibility Handbook by Katie Cunningham](https://www.amazon.com/dp/1449322859/ref=cm_sw_em_r_mt_dp_U_0O1aFbQEJM9XY) is a good resource that talks about the best practices for writing alt text for general images, tables and more.

### Interactive elements

Bokeh is an interactive visualization library for modern web browsers. So, of course, Bokeh's blog post have a lot of cool interactive plots. How do we import these to Medium?

We settled on creating gifs. XD

## Ouch, notifications!

My post is ready to be published!

I hit publish, and my phone buzzes with a notification from Medium (on my personal account) about the blog I just published. Hmm... this is not cool. I don't want to spam all of Bokeh's followers with old blog posts.

I couldn't find anything on the internet, so I contacted their support. They kindly wrote back. :)

So, turns out, we need to "unlist" the post, then publish it, then make it public by "listing(?)" it again. Two extra steps, but well, something is better than nothing.

## Final verdict

Not a bad experience. Things could have gone smoother, but I do understand that it's not really Medium's fault. Personal blogging websites are all built differently and parsing everything accurately would be tricky.

Medium's support staff replied promptly and were super helpful. So, even though there were a lot of quirks, it wasn't too painful.
