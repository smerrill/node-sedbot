# Important Warning

There's a chance that **you will get hacked** if you run this this bot.

The bot does **a pretty good job** escaping of single quotes, but
I am not sure that it's impossible to break out of the sed argument
and run arbitrary commands at the moment.

# About

I had a habit of correcting the things I said in IRC like so:

    smerrill: That was realy quite a good demo.
    smerrill: s/l/&l/g

This bot will let you do just that. The above conversation would look
like this with sedbot around:

    smerrill: That was realy quite a good demo.
    smerrill: s/l/&l/g
    sedbot: What smerrill meant to say was:
    sedbot: That was really quite a good demo.
    smerrill: s/demo/&n/;s/\./!/
    sedbot: What smerrill meant to say was:
    sedbot: That was really quite a good demon!

# Requirements

You will need the following three npm modules installed to run sedbot:

- jerk
- coloured
- log

# Running sedbot

##Environment Variables

The following environment variables can be used, and have the below fallbacks
if not specified:

    export SEDBOT_SERVER='chat.freenode.net'
    export SEDBOT_POPT=6667
    export SEDBOT_CHANNEL='#yourchannel'
    export SEDBOT_NICK='sedbot'
    export SEDBOT_SEDBIN='sed'

To run sedbot, optionally export the above env. variables (or just edit
sedbot.js default options). Then, invoke it as any other node program:

    node sedbot.js

