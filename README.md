# GetOldTweets-python-FIX
Fix to GOT after twitter change the class name for the username. It will now return the username when requested.

Twitter have changed the class name for the username from `username js-action-profile-name` to `username u-dir`.
To fix it I changed line 35 in `got3/manager/TweetManager.py` and line 38 in `got/manager/TweetManager.py` from:
```
usernameTweet = tweetPQ("span.username.js-action-profile-name b").text();
```
To:
```
usernameTweet = tweetPQ("span.username.u-dir b").text();
```

Anyone is welcome to clone this repo until origional if fixed.


You can find the origional repo with its documentation [here](https://github.com/Jefferson-Henrique/GetOldTweets-python).
