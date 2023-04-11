
Conversation opened. 2 messages. All messages read.

Skip to content
Using Gmail with screen readers
in:sent 
4 of 8
Coding Assignment- Testvagrant Technologies
Inbox

Niranjan B niranjanb@testvagrant.com via sender.zohorecruit.com 
Apr 3, 2023, 10:56 AM (8 days ago)
to me

Hi Lavvanya Selvaraj,

Thank you for showing interest in exploring a career opportunity with TestVagrant Technologies.

 

As mentioned, please find the Test Link below. The submission time line is 2 days max.

Please try and attempt this assignment on Github. Post Completion please submit the github link with us.
 

​
Test Link :

https://docs.google.com/document/d/15zxR5pD8tVIDMRLhMj98_r0IoQ973cbG1cV_5e-hMcg/edit
​

Kindly read the problem statement carefully & do not hesitate to ask queries/concerns if any.

 

You are free to use any language, any approach. Just ensure to demonstrate good coding practices. Below are the few points you can keep in mind while working on the task

·      


Must Have
- Submit the complete project
- Tech Stack is no bar - use any combination of scripting language, test frameworks, build tools etc.,
- Commit your code at regular intervals, we will look for the sanctity of commit messages
- Make sure the code is object-oriented and strictly adheres to the language conventions
- Add a readme with clear instructions for local execution
- We highly recommend use of good coding conventions
- Share your code via git repo.

Best of luck with your assignment.
 

To know more about TestVagrant visit the below websites

 

Company Website – www.testvagrant.com

Instahyre: https://www.instahyre.com/jobs-at-testvagrant/

Blog: https://medium.com/testvagrant

Who Should Join TestVagrant Blog: https://www.linkedin.com/pulse/who-should-join-testvagrant-sukesh-kumar/?trackingId=lgN2dVu8azwbOHM8g5H%2FDQ%3D%3D
Glassdoor: https://www.glassdoor.co.in/Reviews/TestVagrant-Reviews-E1488447.htm 


Regards,

Niranjan B | Ph : 

LinkedIn 


 One attachment
  •  Scanned by Gmail

Lavvanya Selvaraj <lavvanyaselvaraj03@gmail.com>
Attachments
Apr 5, 2023, 2:22 PM (6 days ago)
to Niranjan

Hi Niranjan,

Thanks for your passions and apologies for the inconvenience made.

Please find the attached test validation code for the given assessment.

Please be informed that I was not able to pull it to the repository, as I've been hospitalised due to an emergency.

Thanks and Regards,
Lavvanya Selvaraj.

 One attachment
  •  Scanned by Gmail
Test to ensure that the in-memory store is created with the correct initial capacity:

def test_initial_capacity():
    store = InMemoryStore(10)
    assert len(store.songs) == 0
    assert len(store.user_songs_map) == 0
    assert store.capacity == 10

Test to ensure that the store can store a list of song-user pairs and fetch recently played songs based on the user:

def test_store_and_fetch():
    store = InMemoryStore(10)
    store.add_song_user_pair("song1", "user1")
    store.add_song_user_pair("song2", "user1")
    store.add_song_user_pair("song3", "user2")
    assert store.get_recently_played_songs("user1") == ["song2", "song1"]
    assert store.get_recently_played_songs("user2") == ["song3"]

Test to ensure that the store eliminates the least recently played songs when the store becomes full:

def test_store_full():
    store = InMemoryStore(2)
    store.add_song_user_pair("song1", "user1")
    store.add_song_user_pair("song2", "user1")
    store.add_song_user_pair("song3", "user1")
    assert store.get_recently_played_songs("user1") == ["song3", "song2"]

Test to ensure that the store can handle accommodating N songs per user:

def test_store_N_songs_per_user():
    store = InMemoryStore(10)
    store.add_song_user_pair("song1", "user1")
    store.add_song_user_pair("song2", "user1")
    store.add_song_user_pair("song3", "user1")
    store.add_song_user_pair("song4", "user1")
    assert store.get_recently_played_songs("user1") == ["song4", "song3", "song2", "song1"]
Coding Test Report.txt
Displaying Coding Test Report.txt.
