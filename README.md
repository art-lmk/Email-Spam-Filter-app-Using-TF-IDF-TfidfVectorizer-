# Email-Spam-Filter-app-Using-TfidfVectorizer
A deep dive into TF-IDF (Term Frequency-Inverse Document Frequency) vectorization, implemented through a practical email spam filter. This project demonstrates how raw text is transformed into meaningful numerical data that machines can understand and learn from.

📊 What is TF-IDF?
TF-IDF is a statistical measure that evaluates how relevant a word is to a document in a collection of documents. It's the product of two statistics:

Term Frequency (TF): How often a word appears in a document

Inverse Document Frequency (IDF): How important a word is across all documents

🎯 Why TF-IDF Matters for Spam Detection
1. Traditional keyword matching fails because:

2. Spammers constantly evolve their language

3. Legitimate emails might contain "spammy" words occasionally

4. Context matters more than individual words

5. TF-IDF solves this by identifying words that are:

6. Frequent in spam emails (high TF)

7. Rare in legitimate emails (high IDF)

Therefore highly indicative of spam (high TF-IDF score)


Let's see TF-IDF in action with a simple example:

Corpus (Email Collection):

"Win free prize now click here" → Spam

"Meeting scheduled for tomorrow at 3 PM" → Ham

"Congratulations you won a gift card" → Spam

"Project update attached please review" → Ham

TF-IDF Calculation for the word "win":

TF("win", doc1): 1/5 = 0.2

TF("win", doc3): 1/4 = 0.25

IDF("win"): log(4/2) = log(2) ≈ 0.693

TF-IDF("win", doc1): 0.2 × 0.693 ≈ 0.139

TF-IDF("win", doc3): 0.25 × 0.693 ≈ 0.173

The word "win" gets moderate TF-IDF scores because:

It appears in spam emails (moderate TF)

But doesn't appear in all spam emails (good IDF)

Now for the word "click":

Appears only in spam emails

High TF in those documents

Very high IDF (appears in few documents)

Result: Very high TF-IDF score → Strong spam indicator!
