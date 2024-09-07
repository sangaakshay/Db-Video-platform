# Database_video-sharing-platform
Project Cont'd
Consider an online video-sharing platform like YouTube which hosts tens of thousands of channels and crores of users.

You have to analyse the data and provide meaningful insights on the type of content that drives engagement, users growth, and many more to all the stakeholders. Let’s roll our sleeves up for an insightful analysis!

Database
The given database consists of tables that stores the information of online video-sharing platform. 

Tables
user table
user_id	name	gender	age	country	premium_membership
2000	John White	M	63	AUSTRALIA	1
2001	John Andrews	M	67	AUSTRALIA	1
...	...	...	...	...	...
user table stores the data of the user including  user_id , name,gender,age,country and whether they have a premium_membership or not.

channel table
channel_id	name	owner_id	created_datetime
350	Motivation grid	1011	2014-10-05 17:32
351	Marvel	1011	2014-10-05 17:32
...	...	...	...
channel table stores the data of the channel i.e., channel_id,name , owner_id and created_datetime.

video table
video_id	name	duration_in_secs	published_datetime	no_of_views	channel_id
1000	Getting My Driver's License	3652	2011-12-05 19:00	10619	367
1001	Apple iPhone X Review: The Best Yet!	4556	2021-01-19 20:12	140012	362
...	...	...	...	...	...
video table stores the data of the video i.e., video_id , name , duration_in_secs , published_datetime , no_of_views and the channel_id which it was related to.

genre table
genre_id	genre_type
201	ACTION
202	COMEDY
...	...
genre table stores the data of genre including genre_id and genre_type.

channel_user table
channel_id	user_id	subscribed_datetime
100	1	2020-12-10 10:30:45
100	7	2020-10-10 11:30:45
...	...	...
channel_usertable stores the data of the channel_id, their subscribers user_id and subscribed_datetime.

First row in the table represents that the user with user_id = 1 is subscribed to the channel with channel_id = 100 at 2020-12-10 10:30:45

user_likes table
user_id	video_id	reaction_type	reacted_at
1	10	LIKE	2020-12-10 10:30:45
7	10	DISLIKE	2020-10-10 11:30:45
...	...	...	...
Similarly, user_likestable stores the data of the video_id and the user_id who reacted to the video, along with their reaction_type and the time they reacted_at.

video_genre table
video_id	genre_id
10	201
10	202
...	...
Similarly,video_genretable stores the data of video_id and the genre_id that the corresponding video belongs to.

Let’s dive in to analyze the in and outs of each part of the data. Here we go!
