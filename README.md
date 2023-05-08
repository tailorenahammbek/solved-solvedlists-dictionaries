Download Link: https://assignmentchef.com/product/solved-solvedlists-dictionaries
<br>
1 Fish Catch 1.1 Details Download the plain text ﬁles “ﬁshcatch.txt” and “ﬁshcatch.dat” from D2L and open them both with gedit or any plain text editor (don’t use Notepad). 1 The “ﬁshcatch.txt” ﬁle gives an explanation of the data contained in the “ﬁshcatch.dat” ﬁle. Read the explanation to understand what is in the “ﬁshcatch.dat” ﬁle. For this assignment we’ll only be interested in the name and weight of each ﬁsh in the “.dat” ﬁle. Create a new ﬁle called “ﬁshcatch.py”. In the ﬁle: 1.) Write a function called ﬁsh dict from ﬁle that takes a single string parameter giving the name of a ﬁle to read. i.) In the function make a literal dictionary containing the mapping from the Numeric Species Code to the English ﬁsh name. • For example, in your literal dictionary the key 1 will map to the value “Bream”. If your literal dictionary is called fishmap then the following expression would be True: fishmap[1] == “Bream” • You’ll use this dictionary in the next step to get the name of each ﬁsh. ii.) Next create an empty dictionary and read each ﬁsh Species and Weight from the “ﬁshcatch.dat” ﬁle into the dictionary, mapping the English name of each ﬁsh onto a list containing the weights of all of the ﬁsh of that type that were caught. • i.e. for each diﬀerent ﬁsh name the dictionary will contain a single list of ﬂoats. – e.g. the dictionary will have one key-value pair for “Bream”. The key will be “Bream” and the value will be a list of ﬂoats containing the weights of all of the Bream that were caught. • Skip any ﬁsh that has a missing weight value (i.e. weight is “NA”). iii.) Return the dictionary that contains the ﬁsh names and weights. 2.) In main: i.) Call your function to get a dictionary of ﬁsh names and weights. ii.) Print a report showing for each ﬁsh the number of ﬁsh of that type, the name of the ﬁsh, and the mean weight of that ﬁsh type in grams. • The report should show the ﬁsh in alphabetical order. • Make it pretty as shown in the following example: # NAME MEAN WT 11 ? 154.8g 34 Bream 626.0g 56 Perch 382.2g 17 Pike 718.7g 20 Roach 152.1g 14 Smelt 11.2g 6 Whitefish 531.0g 3.) Verify that your documentation makes sense and that you’ve added documentation to each of your functions. 4.) Verify that your program works 5.) Upload your ﬁle to the Program 9 dropbox folder on D2L 2 2 Emoticons (50 points) 2.1 Details Download the plain text ﬁle “twitter emoticons.dat”. The ﬁle contains actual Twitter data1 about tweets that contained emoticons. Each row in the ﬁle represents a single tweet. Each row contains the emoticon text characters, a tweet ID, a user ID, and a timestamp. Here are the ﬁrst few lines of the ﬁle: “D:” 5646373703 “0049961833” 20091112110207 “;-)” 5646377600 “0003829631” 20091112110222 “;-)” 5646425002 “0035714667” 20091112110544 “:(” 5646427235 “0031244602” 20091112110554 … The ﬁrst record is from a tweet containing D: with tweet ID 5646373703, tweeted by user 0049961833 with a timestamp of 20091112110207. The second record is from a tweet containing &#x1f609; with tweet ID 5646377600, tweeted by user 0003829631 with a timestamp of 20091112110222. For this program we’ll only be interested in the emoticon and the user ID. Create a new ﬁle called “emoticons.py”. In the ﬁle: 1.) Write a function called load twitter dicts from ﬁle that takes three parameters: filename (the name of a twitter data ﬁle to read), emoticons to ids (an empty dictionary), and ids to emoticons (an empty dictionary). i.) The function should read the given ﬁle and load the two dictionaries with key-value pairs: • emoticons to ids will contain the emoticons as keys. Each emoticon will have as its value a list containing the user IDs (strings) from all tweets involving that emoticon. – there will be multiple entries in the list for users who tweeted the same emoticon on multiple occasions • ids to emoticons will contain the user IDs as keys. Each user ID will have as its value a list containing the emoticons from all tweets authored by that user. – there will be multiple entries in the list for emoticons that were used on multiple occasions • NOTE: in the “.dat” ﬁle the emoticons and the user IDs are wrapped in double quotes (e.g. “;-)”. You should remove the wrapping double quotes from around emoticons and IDs before using them as keys and values in your dictionaries. ii.) The function does NOT return anything. 2.) Write a function called ﬁnd most common that takes a single dictionary parameter. Assume the keys of the dictionary will be strings (e.g. emoticons) and each value will be a list of strings (e.g. user IDs). i.) The function should ﬁnd the key that has the longest list as a value and print out that key and the length of its list. Print in the following format: 1Source: http://www.infochimps.com/datasets/twitter-census-smileys 3 &#x1f642; occurs 871 times ii.) The function returns the key that had the longest list. 3.) In main: i.) Create two empty dictionaries (emoticons to ids and ids to emoticons) ii.) Call your load twitter dicts from file function passing it the ﬁle name and the two dictionaries. iii.) Print the number of diﬀerent emoticons found in the data ﬁle: Emoticons: 98 iv.) Print the number of diﬀerent user IDs found in the data ﬁle: UserIDs: 2878 v.) Next call your find most common function, passing it the emoticons to ids dictionary The result should look like this: &#x1f642; occurs 871 times • Now pop the most common emoticon from the dictionary and again call your find most common function on the emoticons to ids dictionary. Since the &#x1f642; is gone a diﬀerent emoticon will be the most common. • Repeat this process ﬁve times. Your output from all ﬁve function calls should look like this: &#x1f642; occurs 871 times &#x1f600; occurs 377 times &#x1f641; occurs 231 times &#x1f609; occurs 219 times &#x1f61b; occurs 134 times 4.) Verify that your documentation makes sense and that you’ve added documentation to each of your functions. 5.) Verify that your program works 6.) Upload your ﬁle to the Program 9 dropbox folder on D2L