# CDACProjectUsingRLAN

Prerequisite to run the program - 

1) Install mongo db on your system.

2) Install pymongo, nltk, tensorflow, keras, tweepy, pandas, numpy for your python using pip or conda. Open a python terminal and type the following commands-
	import nltk
	nltk.download('all')

3) Create a db called CDAC

4) 		Create 3 collections.
			The 3 collections are - 
			i)tweetIdScore - keep classification scores of classified ids
			ii)tweetIdText - store tweet id and text
			iii)tweetIdStatus - keep Status of tweets

			Columns  in collections are - 
			i)tweetIdText - tweet_id, tweet_text, created_at, geo, entities, extended_entities, retweeted_status
			ii)tweetIdStatus - tweet_id, classified, trained, clusterAnalysis, viralTrained
			iii)tweetIdScore - tweet_id, violentExtremism, nonViolentExtremism, radicalViolence, nonRadicalViolence, notRelevant







How to run the program - 

1) Open Terminal.

2) Type sudo service mongodb start.

3) Type mongo.

4) 		Type the following commands - 
		i)use CDAC;
		ii)db.createCollection("tweetIdText");
		iii)db.createCollection("tweetIdScore");
		iv)db.createCollection("tweetIdStatus");
		v)db.createCollection("twitterKeys");
		vi)db.tweetIdText.createIndex({"TTL":1},{expireAfterSeconds:0});
		vii)db.tweetIdScore.createIndex({"TTL":1},{expireAfterSeconds:0});
		viii)db.tweetIdStatus.createIndex({"TTL":1},{expireAfterSeconds:0});
		ix)db.twitterKeys.createIndex({"TTL":1},{expireAfterSeconds:0});


5) Exit the mongo shell by typing "ctrl+d" .

6) Go to initTrainer Directory and run initTrainer.py to initiallty train the model. Make sure the models are created in the models folder.

7) Run initKeys file to initially store the keys

8) Run main.py	



The functions are quite straightforward. In case of any queries, I can be contacted at arinjayakhare1@gmail.com
