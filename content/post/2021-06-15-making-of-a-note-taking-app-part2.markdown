---
date: "2021-06-15T18:52:02Z"
tags:
  - writing
  - hobby project
  - software development
title: The making of a note-taking app / Part 2 - On hobby projects
---

In my [my previous post](https://www.alperkilci.com/blog/post/2021-04-26-making-of-a-note-taking-app-1/), I reflected on the reasons to build a note taking application. I gained many experiences along the journey. There are lots of content on the internet about the usage of tools and they get outdated quickly. Therefore I'd like to share my thoughts and opinions about building a side project, rather than teaching how to use the tools I used.

Before starting to code, I've had a couple of code snippets from unfinished side projects. At first, I thought it shouldn't take much time to bootstrap a project and create a prototype to get started. It's easy to get started, indeed. But soon after getting started, the project feels like a never-ending "choose your own adventure" book. This feeling is especially noticeable, once some architectural decisions have to be made. Each decision taught me a lesson on trade-offs in software engineering. It also made me think of differences between professional work and hobby work.

# Quality

Ancient Roman architect and engineer [Vitruvius](https://en.wikipedia.org/wiki/Vitruvius) said that all buildings should have three attributes: "firmitas", "utilitas", and "venustas". In English; "strength", "utility", and "beauty". We could think of these attributes in the context of a software project as well. Since software products have other qualities than physical buildings, we could replace "strength" with "quality" and "security".

Hobby projects and professional projects have many differences. The most significant difference is the potential number of users -assuming the hobby project never goes public-, I have fewer users than the number of services in this project for example. Having only a few users reduces the pressure on the quality. But this does not mean that the quality is not important at all, it only has a little less importance of having something useful in a short time, where the resources are limited. The audience (for this project, only one person - it's me) is restlessly waiting for the features to be completed. You definitely don't want to disappoint your audience. Once you're sure that the feature you've just built works as expected you can deploy it and try it out immediately. After some time of using, improve and refactor it along the way and add a couple of tests to your code.

# Teamwork

In a professional environment, there are usually many people helping to keep the design consistent and beautiful, build and maintain the software, test the product before approving it for release and manage the whole process. Members of a team communicate with each other and work towards a common goal. Waiting for feedback before taking an action could slow us down. In the end, precision is important. Members of the team expect clarity from other team members. There is room for experimentation but reaching the common goal without compromising the precision and the quality is way more important.

Defining a timeline and goals have a place in a hobby project too. But the resources are much limited. Getting support from other team members pushes the project forward in a professional environment. Shortage of labor slows us down in hobby projects in the long run. It is harder to find bugs or mistakes with fewer people. As the only developer, I might fail to see visual design issues as well. Or the potential performance issues of the backend will not be apparent to my eyes, since the project might never go live to the public and meet the crowds.

# Timeline

In the professional world, projects are expected to take progress linearly. A large-scale project could could be developed in multiple tracks at the same time. The maintainer of a hobby project might need to jump to different sides of the project during the development. A hobby project might have unfinished parts and its maintainer could complete, change or remove these parts along the way.

Building software in a professional setting feels like depth-first-search, where each path is traced until the end before starting to trace a new path. A feature is done, once it passes through all phases of development. On the other hand, working on a hobby project can feel like breadth-first-search; where the developer can jump between areas in the project. Jumping to different areas is important to see the limits of our ideas and test our creations before investing too much time in them. Starting to build an autocomplete search component after leaving the dashboard page unfinished is normal. In the end, it's still working -enough- and there are no showstoppers. Sometimes hobbyists could even toss some unfinished parts of the project, once better ideas come to mind. Course-correcting is not a crime.

# Experimenting

Imagine you've recently joined a company as a software developer. Most of the time a legacy system is waiting for you to maintain. Legacy systems could be rigid and might not allow experimenting, due to their design. But sometimes we get assigned to a role to build a system from scratch. A greenfield project offers more room for experimentations, depending on the requirements.

A hobby project itself is an experiment. There is a lot of room for learning since a maintainer is a developer, designer, tester, and the project manager at the same time. There have to be lots of trial and error, for assessing different technologies or techniques for different use cases. It's also crucial to detect the dead-ends and limitations of tools we are using to save time in the future. Therefore experimenting has its importance in software engineering, we could take advantage of our experiences in future projects.

-------

This post is not meant to be a finished post. I'm going to update this, as soon as I find new insights into working on the hobby projects.
