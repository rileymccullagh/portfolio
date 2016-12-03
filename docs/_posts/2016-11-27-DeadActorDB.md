---
layout: post
title: DeadActorDB
---

I've been working on a morbid little REST API and database of actors and their temporality called [DeadActorDB](http://deadactordb.com).

It stemmed from a conversation I had with [Aldous Scales](http://aldousscales.com) where we discussed automatically generatingnews articles when a famous actor died. I reasoned that I could probably scrape enough info off the web to build a database of living and dead actors, and create an API that would return various things, such as actors who died on a certain day. That would mean if you sent it today's date, you would get a list of actors who the scraper had figured were dead, and you could build a news article based on this.

I thought about including extra info to assist in creating the article, but I am wary of ethical issues of people generating articles about people who are still alive. Were I less scrupulous, this would be fully functional.

The API uses Nginx and Gunicorn as a reverse proxy to serve a Flask application. It uses a PostgreSQL database to store the API data. The IMDB scraper is written in Python, using BeautifulSoup4 to render the data.
