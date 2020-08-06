###### Taylor Swift Song Recommender

### "You need to calm Down"
### "Blank Space"
### "Me!"
### "Lover".....the list is endless

Many of us love the songs of Taylor Swift right? Why not try to build a simple song-recommender based on it?

I recently found a very interesting Kaggle Dataset which contained all the lyrics of all the songs of Taylor Swift, right upto the latest album- "Folklore". Check out the dataset- https://www.kaggle.com/pradhanmanva/taylorswiftlyrics

For making this, I have taken major inspiration from the following blog post- https://towardsdatascience.com/the-abc-of-building-a-music-recommender-system-part-i-230e99da9cad. It is a really good Medium article for making song Recommendation systems.

Initially I took a naive approach on the basis of TF-IDF scores(https://towardsdatascience.com/natural-language-processing-feature-engineering-using-tf-idf-e8b9d00e7e76)- a method for comparing similarity between texts. But that gives no context between words- and only takes exact words as similar.

To counter this, I used a pre-trained NLP model trained on English language, available in SpaCY- a very good Python library for performing NLP tasks. And then I compared the similarilty between meanings of lyrics.

To recommend, I ask for one of the songs by the user, and then the system generates the top 'n' similar songs based on that.
