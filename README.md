# Douban Movie Review Dataset (DMR-Dataset)
## Introduction
* DMR-Dataset contains spam movie review sampels and non-spam movie review samples collected by a crawler.
* The dataset is stored in the form of Json, with reviews.json for the movie reviews and movies.json for the movie profiles.
* As of Jan 31, 2022, the candidate samples collected by the crawler and the various information of the samples in DMR-Dataset are shown in the following table. Once new data is updated later, the statistics in this table will be updated.

Name | #Reviews | #Spam | #Non-spam | #Movies | #Users
 --- | --- | --- | --- | --- | --- 
Candidates | 1,012,555 | - | - | 560 | 174,267
DMR-Dataset | 3,318 | 1,660 | 1,658 | 36 | 3,229

* The detailed information fields of a review include:

Field Name | Description | Example
 --- | ------- | ----
user_id | The encrypted Douban ID of user who makes this review. | 5323ae9435a1efb493a53753c007225d
movie_id | The Douban ID of the movie which this review is written for. | 25779217
text | The review text writen by this user. | 前几天在中央六台电影频道看了这部电影，服道化有点差强人意，剧情逻辑挺好，演员们表现还可以，值得一看！
date | The time when this review is written. | 2021-03-31 22:11:01
stars | The number of stars given this user. | 5
useful | The number of useful votes received. | 28
label | If the review is labeled as spam by us, it is 0, otherwise it is 1. | 0
user_profile | A dictionary which includs the user profile of this user. | *shown below*.
user_reviews | A dictionary which includes the past reviews (The review time of those reviews is earlier than this review.). | *shown below*.

* The detailed information fields of user_profile include:

Field Name | Description | Example
---- | ---------- | --
screen_name | User nickname. | 豆友233403034
set_picture | If user set a cover image, it is 1, otherwise it's 0. | 0
register_time | The time when this user join Douban. | 2021-02-18
address | The address that user set. | 
self_description | The self description writen by user. |
follow_count | The number of user followings. | 0
followers_count | The number of user followers. | 0
long_review_count | The number of long review writen by user. | 0
viewed_count | The number of movies that user has watched. | 49
on_viewing_count | The number of movies that user is watching. | 0
want_viewing_count | The number of movies that user wants to watch. | 32

* The detailed information fields of user_reviews include:

Field Name | Description | Example
--- | -------- | -
review0 | The first review made by this user. It's value is a dictionary containing the detailed infomation (*movie_id, text, date, stars, useful, tags*) about this review. | 
review1 | The second review made by this user...  |
... | ... | 
 
 
