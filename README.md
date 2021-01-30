# Mac Miller Lyrics Dataset

The lyrics from Mac Millers releases were scraped from genius.com at the end of 2020. The following releases are covered:  

| Album                                        | Year |
| -------------------------------------------- | ---- |
| But My Mackin Ain’t Easy                     | 2007 |
| But My Mackin’ Ain’t Easy (Original Version) | 2007 |
| The High Life                                | 2009 |
| The Jukebox: Prelude to Class Clown          | 2009 |
| K.I.D.S.                                     | 2010 |
| Blue Slide Park                              | 2011 |
| I Love Life, Thank You                       | 2011 |
| On and On and Beyond                         | 2011 |
| Best Day Ever                                | 2011 |
| Macadelic                                    | 2012 |
| Live from Space                              | 2013 |
| Watching Movies with the Sound Off           | 2013 |
| Live from London                             | 2013 |
| Live from Space                              | 2013 |
| Faces                                        | 2014 |
| Balloonerism*                                | 2014 |
| GO:OD AM                                     | 2015 |
| The Divine Feminine                          | 2016 |
| Spotify Singles                              | 2018 |
| Swimming                                     | 2018 |
| K.I.D.S. (Deluxe)                            | 2020 |
| Circles                                      | 2020 |
| Circles (Deluxe)                             | 2020 |
| Unreleased Songs                             | n/a  |

### Duplicate Songs
If songs were released twice, for example due a Deluxe album release, they are usually only included once. That is because the url to the lyrics is the same. However, there still are duplicate songs, e.g. on live albums.

### Data Structure
Each song is wrapped in a json with three fields:  
1. `lyrics`: containing the actual lyrics of the song  
2. `metadata`: containing various metadata about the song, but at least `title`, `album` and `release_date`
3. `annotations`: marking the sections of the song, e.g. intro, verse, etc. `start` and `end` indicate the line numbers in the lyrics.
```json
{
        "lyrics": [
            "Yeah, yeah, yeah, yeah, yeah, yeah",
            "Yeah, things like this ain't built to last",
            "I might just fade like those before me",
            "When will you forget my past?",
            "Got questions, ask, you know the stories",
            "And you need to let me know",
            "When you're leaving, where you go",
            "Can I come?",
            "Do you believe me, are you close?",
            "Yeah, even if you don't",
            "That'll get you sprung",
            "Do I, do I, do I love?",
            "Can I, can I, can I get enough?",
            "Yeah, don't run away, love",
            "Hate love, heartbreak will have you bankrupt",
            "Too many days in a daze, better wake up",
            "I put your face in a place where the space was",
            "Nobody makes you feel like you but (Do I?)",
            "And you don't know what you should do",
            "You just lookin' for someone to make you move, ooh, tell me (Do I?)",
            "I make this planet feel like home",
            "It's us versus time, the door is closing",
            "So far beyond all our control",
            "You saved a soul so close to broken",
            "It's so much better when you wait",
            "Forever and a day, that's all I got",
            "Put it together then it break",
            "All the energy it take, it never stop",
            "Do I, do I, do I love?",
            "Can I, can I, can I get enough?",
            "Yeah, I never slip, I never fall",
            "I tried to tell you 'bout a better life",
            "And get involved big or small",
            "It's been my fault, I keep it safe, it's in the vault",
            "Blindfolded, keep it going 'til we hit a wall, yeah",
            "I'm never going through the motions",
            "I'm just tryna lay your body down slowly",
            "We can only go up",
            "We can only go up",
            "Do I, do I, do I love?"
        ],
        "metadata": {
            "title": "Woods",
            "album_title": "Circles",
            "written_by": "David Ruoff, Dennis Juengel, Elias Klughammer, Eric “E. Dan” Dan, Jon Brion, Joshua Gottmanns, Mac Miller",
            "distributor": "Warner Records",
            "keyboard": "Jon Brion",
            "copyright": "Warner Records",
            "phonographic_copyright": "Warner Records",
            "associate_producer": "Vic Wainstein",
            "mastering_engineer": "Patricia Sullivan",
            "mixing_engineer": "Greg Koller",
            "assistant_recording_engineer": "Rouble Kapoor",
            "recording_engineer": "Eric Caudieux, Greg Koller, Vic Wainstein",
            "additional_production": "Jon Brion",
            "guitar": "Wendy Melvoin",
            "bass": "Jon Brion",
            "label": "Warner Records",
            "release_date": "17-01-2020",
            "interpolates": "Throw Some D’s",
            "interpolated_by": "Telescope (Woods Demo)"
        },
        "url": "https://genius.com/Mac-miller-woods-lyrics",
        "annotations": [
            {
                "section": "Intro",
                "start": 0,
                "end": 1
            },
            {
                "section": "Verse 1",
                "start": 1,
                "end": 11
            },
            {
                "section": "Chorus",
                "start": 11,
                "end": 13
            },
            {
                "section": "Verse 2",
                "start": 13,
                "end": 28
            },
            {
                "section": "Chorus",
                "start": 28,
                "end": 30
            },
            {
                "section": "Bridge",
                "start": 30,
                "end": 39
            },
            {
                "section": "Chorus",
                "start": 39,
                "end": 40
            }
        ]
    },
```
