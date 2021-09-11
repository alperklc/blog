---
date: "2021-04-26T08:23:25Z"
tags:
  - writing
  - hobby project
  - software development
title: The making of a note-taking app / Part 1 - Why I started building it
---

The pandemic gave me a lot of boredom. And boredom has different effects on different people: some try new things, some rediscover usual hobbies or activities. Living under lockdown conditions made me try new things especially at home: I built shelves and decoration articles from wood and scratched wallpapers to make the living room look like a cafe for example. I spent much time with plants as well. I planted a couple of avocado seeds like many people. It is nice to watch them growing slowly as time flies.

I wanted to work on something beneficial, especially for organizing my mental resources. Since I spend a lot of time in front of a computer screen, no wonder why most of the problems I observed are rooted in my digital life. Time spent on the internet has side effects - most people experience a decrease in focus due to the amount of multitasking and constantly getting stimulated by the notifications.

Gathering the thoughts together gets easier once you start writing regularly, therefore I wanted to form a habit. As I started working on this, I put thought into identifying problems I want to solve by being a better writer:

- **Getting lost in the digital world**: I'm exposed to a continuous stream of information. Sometimes I need to find a code snippet that I need for my current task at work. Or the recipe of a pasta sauce I discovered recently, while I'm at the supermarket. I should be able to find my content easily on my computer and my smartphone.

- **Lack of aggregated search across platforms/apps**: Platforms I use usually let me keep a list of stuff I like. I like tweets on Twitter or give stars to projects on Github. Sometimes I need to search one word and find content from independent platforms. To this end, I have to visit all of these sites and -if they don't offer a search feature- scroll down on the list until I find the thing I liked. An aggregated experience for searching everything I like on multiple platforms at the same time is what I need.

    I could get information from other platforms in two ways, first one is to develop applications to fetch information via APIs of Twitter, GitHub, or any platform I would like to communicate with. It would take plenty of time since I had to work on each platform individually. The second way is to make a web or mobile application that should be reachable on my mobile device native share target list so that I could click on the share button and select my app to keep this information. It wouldn't automate the information sharing between applications but it would absolutely take less time to develop. I could build the same feature for my laptops via browser extensions.

- **Disorganized online reading habits**: I like to store bookmarks on browsers. Browsers make it possible to search within the bookmarks and sync it between devices. It is helpful, depending on how we use it. For instance, a blog post with an interesting title will land on the pile of bookmarks. Sometimes I don't even read it. The cognitive load of unread posts or articles makes it difficult to find the one that I'm looking for. Although the browsers let you search your bookmarks, they do not indicate if you've already visited them. I'd delete the ones that stay unread more than a week, for having more headspace.

- **Searching bookmarks by scrapped page content**: It is not possible to search by the page content on stored bookmarks on my browser. Plus, the content of the pages could be deleted or changed as well. There must be a service to parse all the pages for me and I should be able to keep and search within all content I keep.

- **Having own cloud services like Google Drive or Dropbox**: There are gif pickers on lots of platforms like Slack or Discord. It works quite nice but I wish I had something personalized for sending my content to chats. Or find the scanned copy of my rental contract without searching within my emails. I needed a structure that could keep folders filled with my meme collection or boring stuff, that is reachable via a web app. And sometimes I need to give links to these files from my personal notes. Having files and notes in the same application would make the usage of it much easier.

## Why did I start building my own app?

Given all problems, I noticed that I was undecided about the tools and mediums. And there isn't a one-size-fits-all solution. Problems about storing and searching textual data could be solved by taking notes. It's all about finding the right tool for the use case and building habits around it. Of course, there are hundreds of software for that. And people often switch to another one easily. Bookmarks could also be stored as notes and there are of course nice apps specialized for this use case, such as Pocket (Read Later). Pictures that could be stored on a service like Google Cloud / Imgur could be shared by sending public links to these files. Since I had too much time on my hands, why wouldn't I build my own solution? As I started working on it, I reflected on my decision and thought of these reasons:

**Nudging myself to write more**: Creating a virtuous cycle by building an app to write more and writing more to test the app that I'm building. Practicing writing and programming at the same time as a result.

**Not relying on services outside of my control**: Apps on the cloud can be shut down, change their features/design, or their payment plans. If I can have control over the applications' source code, I would eliminate these risks. Nevertheless, security breaches would still be a problem because application security requires expertise in the field.

**Gaining experiences in software architecture and giving back to society**: I'm not the only developer who built a note-taking app for sure. There are too many examples on the internet. Most of them are open source too, there are too many resources to get inspiration. There could be as many note-taking apps on GitHub as Stairway to Heaven guitar cover videos on YouTube. I used lots of resources on the internet and I'd be more than happy if I could inspire other developers and give back to the internet.

**Developing an application for my own usage**: As many of us think that building software as a hobby requires intrinsic motivation, I believe it's true. Working on a product that I use in my daily life gives me the motivation I need.

**Having something to show on my portfolio**: Having a useful and working application on my portfolio is much better than tens of weekend projects I wrote for trying a new programming language or a library.

## Thinking along the way

Everything I write here summarizes the motivation that kept me working on this side project. I didn't start working on this project by writing about what I'm going to build. The application I'm building literally helped me to write these lines; I kept a journal to record what's on my mind about the project and added notes now and then.

This post is just a compilation of short notes I have taken during the development of this project. Instead of defining clear goals before getting started, wanted to think about my objectives along the way. This is not the final version of this post neither, this post will keep receiving updates as long as I work on the project.
