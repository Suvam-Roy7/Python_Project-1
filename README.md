# Python_Project-1

import feedparser
import requests

url = input('Enter URL : ')

'https://timesofindia.indiatimes.com/rssfeedstopstories.cms'

r = requests.get(url)

news  = feedparser.parse(r.text)

for item in news['entries']:
    tit = item['title']
    print(tit.upper())
    print(item['description'])
    print(item['link'])
    print()
