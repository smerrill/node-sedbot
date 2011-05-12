# Important Warning

You will **almost certainly get hacked** if you run this this bot.
It is not safe to use at the moment and may never be.

The bot does **extremely basic** escaping of single quotes, but
you could easily break out of them and run arbitrary commands at
the moment.

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

