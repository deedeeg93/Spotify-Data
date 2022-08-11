# Spotify-Data

CREATE TABLE BIT_DB.Spotifydata (
id integer PRIMARY KEY,
artist_name varchar NOT NULL,
track_name varchar NOT NULL,
track_id varchar NOT NULL,
popularity integer NOT NULL,
danceability decimal(4,3) NOT NULL,
energy decimal(4,3) NOT NULL,
key integer NOT NULL,
loudness decimal(5,3) NOT NULL,
mode integer NOT NULL,
speechiness decimal(5,4) NOT NULL,
acousticness decimal(6,5) NOT NULL,
instrumentalness text NOT NULL,
liveness decimal(5,4) NOT NULL,
valence decimal(4,3) NOT NULL,
tempo decimal(6,3) NOT NULL,
duration_ms integer NOT NULL,
time_signature integer NOT NULL 
)

SELECT * FROM BIT_DB.Spotifydata

I used the analytics to see what are the most popluar artists on Spotify

SELECT *FROM BIT_DB.Spotifydata WHERE (popularity >90)

Then I decided to choose artists where their song had a high tempo.

SELECT * FROM BIT_DB.Spotifydata WHERE (tempo >130)

Then I wanted to see which songs had both high popularity and a high tempo

SELECT * FROM BIT_DB.Spotifydata WHERE( tempo >130 and popularity >90)

I decided to see who the lower scoring artists were

SELECT * FROM BIT_DB.Spotifydata WHERe (popularity <80)

Then I chose to find the top 10 songs

SELECT
artist_name
,track_name
FROM BIT_DB.spotifydata
WHERE (popularity >90)
LIMIT 10
