---
layout: page
title: "Podcasting With Jekyll"
permalink: /podcast.html
---

This site is built using the static site generator [Jekyll](https://jekyllrb.com/), the audio files live on [Amazon S3](https://aws.amazon.com/s3/) and (for the time being) the site itself is hosted on [GitHub pages](https://pages.github.com/).

### Why?

The simple answer is that podcasting relies on a pretty simple technology - RSS. RSS often gets generated for a website almost as a by-product of adding content, this allows people to "subscribe" to your website and be notified or fed updates. Jekyll generates RSS straight out of the box and every podcast needs a website so we thought - why not kill two birds with one stone?

### How?

After a bit of a search we stumbled across [Podcast Generator](http://www.podcastgenerator.net/) which seemed to be a useful tool and close to what we needed. Doug and Dai over at [TIDE podcast](http://tidepodcast.org/) use it and after having played with the setup - it's quick and easy. There was some concern about placing our audio files up on our webserver though, audio files can be quite large which can impact on traffic allowances. Tim asked around the [Reclaim Community](https://community.reclaimhosting.com/t/podcasting-with-reclaim/) and decided to have a go at Jekyll. After an evening of fiddling around the site was up and running. It was generating an RSS feed that complied with iTunes standards and was looking pretty nice too. Tim added a HTML5 player ([Plyr](https://github.com/Selz/plyr)) to the post page for each podcast so that people could sample and listen without having to subscribe or download anything. Next step was to move the files into an Amazon S3 bucket, which [this tutorial](https://growthedream.com/host-podcast-files-amazon-s3/) covers nicely. The final step was getting a domain name and pointing it at GitHub.

### Our Process

**1.** Record the conversation

**2.** Edit and export podcast

**3.** Edit metadata

**4.** FTP file to Amazon S3 - copy link

**5.** Create a new post in Markdown and add in the relevant front matter to the YAML section

``` yaml
layout: post
title: "Title Goes Here"
date: Publishing date and time
file: link to file in S3
summary: "Quick exerpt of episode"
description: "Longer information"
duration: "how long in minutes and seconds" 
length: "in seconds"
explicit: "do we swear" 
keywords: "keyword tags"
block: "hold back publishing it" 
```
