# scalper

Online shop availability checker

This lightweight Node.js application will detect and notify you when an item becomes available/unavailable at an online shop.

Can be useful given the recent stock shortages of PlayStation 5, Xbox Series X or Nvidia graphics cards.

Currently only works with Amazon.

I recommend using a **VPN**, just in case...

## Setup

1. Install nodejs

   > sudo apt install nodejs

2. Install npm

   > curl https://www.npmjs.com/install.sh | sudo sh

3. If using Raspberry Pi or other device with ARM architecture, install Chromium:

   > sudo apt install chromium-browser chromium-codecs-ffmpeg

4. Install all Node dependencies:

   > cd scalper

   > npm i

5. Modify the source code to your preferences

   Edit the **config.js** file to:

    - add shops and links to items you're interested in. Shop names must match the function names in **parse.js**. Currently only Amazon is supported. Add support for more online shops by editing the **parse.js** file.

    - perform an action when the item is available. It's up to you what you want to do with it, for example: post a Tweet, send an email, or buy the item instantly. There are three functions you can customize: **becameAvailable**, **becameUnavailable** and **hasNotChanged**.

6. Run the app:

   > node index