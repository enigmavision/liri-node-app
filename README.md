# LIRI-bot

This repository serves as an introduction to Node.js and running JavaScript in an environment other than the Browser.

###Usage

The LIRI-bot takes 4 commands: <br>
1. my-tweets <br>
2. spotify-this-song <br>
3. movie-this <br>
4. do-what-it-says <br>

First command will fetch my last 20 tweets. (can be configured to find another user's tweets.) <br>
Second command takes a song title as an argument and returns relevant info. <br>
Third command does the same thing as the song, but with a movie title <br>
Fourth command will do any of the above 3, but will read command input out of a text file named random.txt

## Usage
<pre>
$ node liri.js
Usage: node liri.js my-tweets|spotify-this-song <song>|movie-this <movie>|do-what-it-says
Notes: For 'do-what-it-says', a file called random.txt is parsed for a comma-delimited command to execute.
</pre>

## Examples

### Dump your 20-most recent tweets

<pre>
$ node liri.js my-tweets
my-tweets
----------------------------------------------
Tweet # 1 Fri Dec 02 00:09:19 +0000 2016 hello, Twitter :-)
Tweet # 2 Fri Dec 02 00:23:18 +0000 2016 Ghostbusters https://t.co/JMVBJ1onHQ via @YouTube

"... for a moment, forget I ever knew anything about metallurgy, or physics, or node.js"
</pre>

### Look up song info on Spotify

<pre>
$ node liri.js spotify-this-song "eye of the tiger"
spotify-this-song
----------------------------------------------
Artist(s): Original Motion Picture Soundtrack
Song: eye of the tiger
Album: Rocky IV
Preview link: https://p.scdn.co/mp3-preview/9e37f230afd37042e49f3d144c3b94e0b39ef8ba
</pre>

### Look up movie information on OMDB

<pre>
$ node liri.js movie-this "groundhog day"
movie-this: groundhog day
----------------------------------------------
Title: Groundhog Day
Year: 1993
IMDB Rating: 8.1
Country: USA
Language: English, French, Italian
Plot: A weatherman finds himself living the same day over and over again.
Actors: Bill Murray, Andie MacDowell, Chris Elliott, Stephen Tobolowsky
Rotten Tomato Rating: 8.0
Rotten Tomato URL: http://www.rottentomatoes.com/m/groundhog_day/
</pre>

### Perform a LIRI command in random.txt

<pre>
$ cat random.txt
spotify-this-song,"I Want it That Way"

$ node liri.js do-what-it-says
spotify-this-song
----------------------------------------------
Artist(s): Backstreet Boys
Song: "I Want it That Way"
Album: The Hits--Chapter One
Preview link: https://p.scdn.co/mp3-preview/e72a05dc3f69c891e3390c3ceaa77fad02f6b5f6
</pre>
