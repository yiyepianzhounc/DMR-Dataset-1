SUMMARY
================================================================================
This dataset named DMR-dataset is a spam movie review dataset for Chinese constructed in paper 
"GAIM: Graph-aware Feature Interactional Model for Spam Movie Review Detection", which contains
 3,318 reviews of 36 movies made by 3,229 users of Douban Movie. It includes 1,660 spam movie
 review and 1,658 non-spam movie review. Meanwhile, a feature vector consisting of 28 features
 is constructed for every review.

USAGE LICENSE
================================================================================
* The user may not violate the privacy protection policy of Douban.
* The user may not state or imply any endorsement from our research group.
* The user may not redistribute the data without separate permission.
* The user may not use this information for any commercial or revenue-bearing purposes.

CITATION
================================================================================
to be determined

REVIEWS FILE DESCRIPTION
================================================================================
All reviews are contained in the file "reviews.csv" and are in the following format:

uno	mno	review	label

- uno: renumbered user_id, range between 0 and 3,228
- mno: renumbered movie_id, range between 0 and 35
- review: the review text written by user
- label: if the review is regarded as spam movie review, the value of label is 0, else 1

USERS FILE DESCRIPTION
================================================================================
For the sake of privacy protection, the user_id is encrypted, and the details of user
are not provided yet.
User information is in the file "users.csv" and is in the following format:

uno	user_id

- uno: renumbered user_id, range between 0 and 3,228
- user_id: encrypted string of the real user_id in Douban

MOVIES FILE DESCRIPTION
================================================================================
Movie information is in the file "movies.csv" and is in the following format:

mno	movie_id	movie_name	directors	writers	actors	roles	genres	release_country	release_date	language	movie_length	avg_rating

- mno: renumbered movie_id, range between 0 and 35
- movie_id: the movie_id of the movie in Douban
- movie_name: the title of the movie in Douban
- directors	: the directors of the movie
- writers: the writers of the movie
- actors: the actors of the movie
- roles: the roles of the movie
- genres: the genres of the movie
- release_country: the release country of the movie
- release_date: the release date of the movie
- language: the language of the movie
- movie_length: the duration of the movie
- avg_rating:  the average rating of the movie in Douban (10-star scale)

FEATURES FILE DESCRIPTION
================================================================================
The feature vectors constructed by the feature engineering is in the file "features.csv",
in which every review includes 28 features. The source of each feature is detailed in the
paper  "GAIM: Graph-aware Feature Interactional Model for Spam Movie Review Detection".
The feature vector is in the following format:

uno	mno	RL	EXT	ETF	ARP	SP	SA	NFD	NFI	LSD	NWM	NOM	NVM	NLR	RNR	RPR	ARL	RRT	RES	MNR	ISR	ARA	ARD	ARW	ARG	ARR	ADEV	ERD	AETF

- uno: renumbered user_id, range between 0 and 3,228
- mno: renumbered movie_id, range between 0 and 35
- RL: Review Length. The length of a movie review in the word count.
- EXT: Extreme Rating. Spammers tend to give extreme ratings (2~3 stars or 4~5 stars)
- ETF: Early Time Frame. Spammers often review early to impact people's sentiment.
- ARP: Account Registration Purpose. Spammers often temporarily register accounts for the target movie.
- SP: Set Picture. Whether the user has set a picture?
- SA: Set Address. Whether the user has set an address?
- NFD: Number of Followed.
- NFI: Number of Following.
- LSD: Length of Self-description. The length of the user's self-description in the word count.
- NWM: Number of Want-viewing Movies in Douban.
- NOM: Number of On-viewing Movies in Douban.
- NVM: Number of Viewed Movies in Douban.
- NLR: Number of Long Reviews (a kind of review in Douban).
- RNR: Ratio of Negative Movie Reviews.
- RPR: Ratio of Positive Movie Reviews.
- ARL: Average Movie Review Length. The average of RL (Review Length).
- RRT: Ratio of Records with Tags. Non-spammers give reviews more sincerely and mark movies with tags.
- RES: Ratio of Exclamation Reviews. Ratio of exclamation reviews containing "!".
- MNR: Max. Number of Movie Reviews Written in a Day.
- ISR: Is Singleton?
- ARA: Weighted Average Rating Deviation of Actors.
- ARD: Weighted Average Rating Deviation of Directors.
- ARW: Weighted Average Rating Deviation of Writers.
- ARG: Weighted Average Rating Deviation of Genres.
- ARR: Weighted Average Rating Deviation of Regions.
- ADEV: Average Rating Deviation. The average of DEV (Rating Deviation).
- ERD: Entropy of Rating Distribution.
- AETF: Average Early Detection Frame. User's reviews all appear near the time movie released is suspicious.