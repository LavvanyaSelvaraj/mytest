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
