# Class SongTracker Desing Recipe


## 1. Describe the Problem

_Put or write the user story here. Add any clarifying notes you might have.

As a user
So that I can keep track of my music listening
I want to add tracks I've listened to and see a list of them.

potential objects:
MusicTracker
tracks
MusicListened

Potential functions;
keep track music
add tracks
songs list


## 2. Design the Class Interface

Include the initializer, public properties, and public methods with all parameters, return values, and side-effects.

class SongTracker():

    def __init__(self):
        # Properties:
        #   song_list: list
        # Side effect:
        #    sets song listened to an empty list
        # Return:
        nothing 

    def add_tracks(self, track):
        # Properties:
        # track: string representing song 
        #side effect:
        #   adds songs to the self.song_list

    def see_tracks(self):
        # Properties:
        #   None
        # Side effects:
        #   None (but it returns the song_list: list )
        # Returns:
        #   returns self.song_list



## 3. Create Examples as Tests

Make a list of examples of how the class will behave in different situations.

"""
Given a new instance for SongTracker
It comes with an empty list
"""
song_tracker = SongTracker()
actual = song_tracker.song_list
expected = []
assert actual = expected # => []

"""
Given I add a track to the song_list
I want to see the tracks in the song_list
"""
song_tracker = SongTracker()
song_tracker.add("song1")

actual = song_tracker.song_list
expected = ["song1"]
assert actual == expected # => ["song1"]

"""
Given I add two tracks to the song_list
I want to see the tracks in the song_list
"""
song_tracker = SongTracker()
song_tracker.add("song1")
song_tracker.add("song2")

actual = song_tracker.song_list
expected = ["song1", "song2"]
assert actual == expected # => ["song1", "song2"]

"""
Given I add some tracks to the song_list
I want to see all the tracks in the song_list
"""
song_tracker = SongTracker()
song_tracker.add("song1")
song_tracker.add("song2")
song_tracker.add("song3")

actual = song_tracker.song_list
expected = ["song1", "song2", "song3"]
assert actual == expected # => ["song1", "song2", "song3"]


## 4. Implement the Behaviour

After each test you write, follow the test-driving process of red, green, refactor to implement the behaviour.