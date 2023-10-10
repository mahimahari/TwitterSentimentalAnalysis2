# Twitter Sentiment Analysis on FlaskApp :notebook:
In this repo i created a twitter sentiment analysis on flask app (web base).

[![](https://camo.githubusercontent.com/2fb0723ef80f8d87a51218680e209c66f213edf8/68747470733a2f2f666f7274686562616467652e636f6d2f696d616765732f6261646765732f6d6164652d776974682d707974686f6e2e737667)](https://python.org)

You can also check a demo website :point_right: [click here](http://hitalfashion.pythonanywhere.com/)
# Directory Tree :cactus:
```bash
.
├── images
│   ├── 1.png
│   ├── 2.png
│   ├── 3.png
│   ├── 4.png
│   └── 5.png
├── LICENSE
├── main.py
├── README.md
├── static
│   ├── logo.png
│   └── style.css
└── templates
    ├── index.html
    └── sentiment.html

3 directories, 12 files
```



# Disclaimer :skull_and_crossbones:
I am not provideing twitter **API** keys. You have get twitter API keys on twitter developer account. Get [API Keys](https://developer.twitter.com/)

Get a API key and put in the below code section
```python
def sentiment():
    userid = request.form.get('userid')
    hashtag = request.form.get('hashtag')

    if userid == "" and hashtag == "":
        error = "Please Enter any one value"
        return render_template('index.html', error=error)
    
    if not userid == "" and not hashtag == "":
        error = "Both entry not allowed"
        return render_template('index.html', error=error)
    
    #=====================Insert Twitter API Here==========================
    consumerKey = ""
    consumerSecret = ""
    accessToken = ""
    accessTokenSecret = ""
    #=====================Insert Twitter API End===========================
    
    authenticate = tweepy.OAuthHandler(consumerKey, consumerSecret)
    authenticate.set_access_token(accessToken, accessTokenSecret)
    api = tweepy.API(authenticate, wait_on_rate_limit = True)
   ```



## ScreenShot :camera_flash:
![](https://github.com/mahimahari/TwitterSentimentalAnalysis2/images/3.png)
![](https://github.com/mahimahari/TwitterSentimentalAnalysis2/images/4.png)
![](https://github.com/mahimahari/TwitterSentimentalAnalysis2/images/5.png)

