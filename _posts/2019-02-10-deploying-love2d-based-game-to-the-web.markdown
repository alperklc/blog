---
layout: post
title: Deploying Löve2D based game as a web app
date: '2019-02-10 18:35:27'
tags:
- love2d
- lua
- global-game-jam
- game-development
---

![L-ve2d_logo](/content/images/2019/02/L-ve2d_logo.png)

It's been a while since I wrote a blog post about anything and did something in the field of game development. Well, this time it started with some game development and it leaded to this blog post. 

Recently I've attended a Global Game Jam event in Hamburg with [@Sarge](https://twitter.com/sgt3v) and it was quite fun. (I will write another blog post about Global Game Jams later) It wasn't my first attendance in the Global Game Jam actually. I attended first time in 2014, during my bachelor.

During the event, I started to look for source code of our game we made in 2014 and when I finally found it (thousand thanks to [@Sarge](https://twitter.com/sgt3v)) I uploaded it to a [Github repository](https://github.com/alperklc/am-i-who-i-am)

And I wanted to deploy it as a web application so that everyone could play it. 

As far as I found on the internet [love.js](https://github.com/TannerRogalsky/love.js) makes it possible to deploy the Löve2D games as a web application. All you need is some patience and Python 2.7 on your machine.

Instructions:
- `git clone https://github.com/TannerRogalsky/love.js.git`
- After cloning the project, clone the game from `initial-version-with-love-0.9.x` branch and copy the game folder under `love.js/debug` folder.
- Run the following command (this works with python 2.7, if you have python 3+ on your machine you could install python 2.7 and run this command with python2.7 instead of python)
```python ../emscripten/tools/file_packager.py game.data --preload ./am-i-who-i-am@/ --js-output=game.js```
- This command will create `game.data`, `game.js` and `index.html` files inside the folder.
- Opening `index.html` might not work locally because of CORS. Serving it from localhost via `nginx` or a local nodejs server should work.

P.S: The game is available on [itch.io](https://alperklc.itch.io/am-i-who-i-am) Enjoy!