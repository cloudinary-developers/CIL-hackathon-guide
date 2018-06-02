# Using TiVo & Lyricfind APIs’

![](../../.gitbook/assets/tivo_lockup_blk_blue_2%20%281%29.png)

> At TiVo, we’re always innovating to create the ultimate entertainment experience. When it comes to music, we deliver the personalized, engaging listening experiences fans can’t resist. Our best-in-class Music Metadata covers millions of albums and tracks, and offers standardized IDs, unique descriptors, high-quality imagery and more. Streaming providers can enhance their services, while labels, publishers and distributors can more effectively market and merchandise their catalogs. Around the world, leading brands choose TiVo to deliver the music fans want and introduce them to their next obsession, creating loyal customers in the process.

**TiVo Music** API Documentation

You may know of us from our former name, AMG/Rovi, and a website that was formerly a property of ours which featured our music metadata \([allmusic.com](https://www.allmusic.com)\).

We're providing unlimited access \(500 requests/sec, no daily limit\) to the same music metadata powering services such as Spotify, Pandora, Apple Music, etc.

You can use the API Key/Secret below which is also included in the Cloudinary sample app.

API Key - 7d9vkau5knchkpa4z9pkcg7d

API Secret - mmj58xRfZw

> {% embed data="{\"url\":\"http://prod-doc.rovicorp.com/mashery/index.php/Data/APIs/Rovi-Music\",\"type\":\"link\",\"title\":\"Data/APIs/Rovi-Music - ROVI API\",\"icon\":{\"type\":\"icon\",\"url\":\"http://prod-doc.rovicorp.com/favicon.ico\",\"aspectRatio\":0}}" %}

TiVo Music API Console - this can be used to quickly preview all of our different types of music metadata without having to write any code !  Click on the following link and choose 'Metadata and Search APIs' from the drop-down menu - [http://developer.rovicorp.com/io-docs](http://developer.rovicorp.com/io-docs).  Enter the API Key and Secret from above to return a JSON response from any of the API endpoints in the list.

For example, use the 'Name ID' to retrieve artist styles, themes, moods, etc. using the 'Name' API \(scroll toward the end of the IO-Docs page\) - Wayne Shorter = MN0000250435 \(for 'include' enter musicStyles,moods,themes\).

**TiVo Playlisting Console**

We're providing an interactive Playlisting Prototype and select assets from our music metadata catalog, to provide interactive experiences around:

* Track, Release, Album, Artist objective and subjective metadata
* Tones, Themes, Moods, and Similar Artists
* Artist & UMG album artwork

{% embed data="{\"url\":\"https://discovery-beta-admin-0.digitalsmiths.net/console/login \",\"type\":\"link\",\"title\":\"TiVo Personalized Content Discovery Engagement Console\",\"description\":\"The Personalized Content Discovery Engagement Console for managing Search & Recommendations\",\"icon\":{\"type\":\"icon\",\"url\":\"https://discovery-beta-admin-0.digitalsmiths.net/console/favicon.ico\",\"aspectRatio\":0}}" %}

User: CapitalHackathon

Password: CapitalJune2018

**LyricFind** API Documentation

> [http://www.lyricfind.com/documentation/?key=eyJkb2N1bWVudCI6IndlYl9zZXJ2aWNlIiwib3B0aW9ucyI6eyJwcmVtaXVtIjoidHJ1ZSIsIm9sZGtleXR5cGVzIjoiZmFsc2UifX0=\#the-lyric-display-api](https://emea01.safelinks.protection.outlook.com/?url=http%3A%2F%2Fwww.lyricfind.com%2Fdocumentation%2F%3Fkey%3DeyJkb2N1bWVudCI6IndlYl9zZXJ2aWNlIiwib3B0aW9ucyI6eyJwcmVtaXVtIjoidHJ1ZSIsIm9sZGtleXR5cGVzIjoiZmFsc2UifX0%3D%23the-lyric-display-api&data=02%7C01%7CChingChing.Chen%40umusic.com%7Cd5c76183868e484eb22708d5c5d0512d%7Cbbcb6b2f8c7c4e2486e46c36fed00b78%7C1%7C0%7C636632422086228515&sdata=E%2FjiVhqSmlEpaSvin%2BV3Rh1hfsdmhF3WTzFVdgrUJPg%3D&reserved=0)

Use the ISRC from the TiVo/7Digital API response or Cheat Sheet to retrieve lyrics for a track - certain tracks may include a 'lrc' object which will contain lyric sync timestamps that can be used to sync the lyrics to the audio track from 7Digital.

[http://api.lyricfind.com/lyric.do?apikey=14c9a53ff33f0adf99435f207d9c4b2f&territory=US&reqtype=default&trackid=isrc:USUM71203819&format=lrc&lrckey=230ac06cba8d3ecd6996466e8356b6e4](http://api.lyricfind.com/lyric.do?apikey=14c9a53ff33f0adf99435f207d9c4b2f&territory=US&reqtype=default&trackid=isrc:USUM71203819&format=lrc&lrckey=230ac06cba8d3ecd6996466e8356b6e4)

If the ISRC can't be used to retrieve track lyrics, use the 'AMG' T\_ID from the TiVo/7Digital API response or Cheat Sheet to retrieve lyrics for a track \(only use the numbers in the ID\).  Here's an example using 'Tangled' from Maroon 5 \(AMG 'T 26901151' - note: the leading 'T' and space has been stripped for the LyricFind API\)

[http://api.lyricfind.com/lyric.do?apikey=14c9a53ff33f0adf99435f207d9c4b2f&territory=US&reqtype=default&trackid=amg:26901151&format=lrc&lrckey=230ac06cba8d3ecd6996466e8356b6e4](http://api.lyricfind.com/lyric.do?apikey=14c9a53ff33f0adf99435f207d9c4b2f&territory=US&reqtype=default&trackid=amg:26901151&format=lrc&lrckey=230ac06cba8d3ecd6996466e8356b6e4)

**Cheat** **Sheet** of all artists/albums/tracks used for the Capitol360 Hackathon Catalog

Use the below link and choose File&gt;Download As&gt;CSV to import a CSV into your SQL/Mongo DB or to simply preview the artists, albums, and tracks in the catalog.

{% embed data="{\"url\":\"https://docs.google.com/spreadsheets/d/e/2PACX-1vQbyyXIbfNvjStvG7Jlhv5M2djSEsc\_YU0cTA5K6NYtabPgtxojrZBTHeyiTAAJ9BDfgToRKYbnh039/pubhtml\",\"type\":\"link\",\"title\":\"Capitol360HackathonCatalog\",\"icon\":{\"type\":\"icon\",\"url\":\"https://docs.google.com/favicon.ico\",\"aspectRatio\":0}}" %}

**TiVo Music ID** Breakdown

'MN' = Artist ID - TiVo's 'Name' or Artist ID helps to uniquely identify artists across the music industry.  Our 'Name' ID represents an individual, group, organization, or character that contributes or exists within the universe of music.  For example, Wayne Shorter = MN0000250435

Use this ID to retrieve artist metadata such as the following: AKAs/aliases, associated artists, collaborators, contemporaries, discographies, followers, group members, images, influencers, member of \(if the artist has been part of a group\), moods, biographies, music credits, music styles, similar artists, songographies, and themes.

'MW' = Album ID - TiVo's Album ID helps to uniquely identify albums - an album represents musical works \(one or more audio tracks\) produced by an artist or group of artists. Albums are conceptual entities, describing a specific work \(e.g., “The White Album”\) and do not refer to a format \(Vinyl, CD, Digital, etc.\). Each album relates to one or more releases representing the form of the album made available to consumers.  For example, the following two Wayne Shorter albums and our associated metadata - 

Speak No Evil = Album ID MW0000247834 - credits, moods, review, releases, similar, styles, themes

Without A Net = Album ID MW0002445530 - credits, moods, review, releases, styles, themes

'MR' - Release ID - TiVo's Release ID defines releases of an album, either physical or digital.  Our Release ID will also be associated with an industry standard UPC Product Code which can be used as a common identifier between 7Digital and TiVo !  Note: UPC values returned by 7Digital APIs may have leading zeros which should be stripped to return release metadata from the TiVo Music APIs.

'MT' - Track ID - TiVo's Track ID defines information about a specific audio track on a release.  Our Track ID will also be associated with an industry standard ISRC Code which can be used as a common identifier between 7Digital and TiVo.  Our track metadata includes genre/subgenre, moods, styles, themes, and we provide a 30 second audio sample.

'SD' - Song ID - TiVo's Song ID isn't used as part of our API however it can be used to filter duplicates and uniquely identify songs on a work level - for example,  the Kanye West song 'Champion' from the album Graduation actually has multiple ISRCs and thus multiple Track IDs associated with it however they'll share a single 'SD' ID - SD0000326091.  This can be found in the Cheat Sheet above -   

| Champion | USUM70749083 | MT0027760520 | T 12224802 | SD0000326091 |
| --- | --- |
| Champion | USUM70749084 | MT0041589685 | T 23962028 | SD0000326091 |

'SI' - Composition ID -   TiVo's Composition ID isn't used as part of our API however it can be used to create a unique discovery experience using cover songs across genre boundaries.  For example, the song 'Ain't No Sunshine' has been covered by numerous artists over the years and we now give you the ability to easily find all covers for this song in the catalog since they share the same Composition ID.

The Composition ID 'SI0005189120' represents this song and using the Cheat Sheet above, we can see it has been covered by all of the following artists in the Capitol360 Catalog - Michael Jackson, Anthony Billups, Bill Withers, David Holmes, Jackyl, Lighthouse Family, Roy Ayers, The Neville Brothers.  Use the ISRC with the 7Digital to stream all of these covers.

**Cheat Sheet** - Master Genre/Subgenre/Style List

Use the below link and choose File&gt;Download As&gt;CSV to import a CSV into your SQL/Mongo DB for a master list of all TiVo Music genres, subgenres, and styles - this can come in handy to create a genre/subgenre/style map or discovery experience.

[https://docs.google.com/spreadsheets/d/e/2PACX-1vRn9fTzFh3xAcd4HTEe58YUDZOAs73SyISSAsjaNJleyPc7W7wSoMHyMcHnuj8uadwEwLqQCU8N-n\_q/pubhtml](https://docs.google.com/spreadsheets/d/e/2PACX-1vRn9fTzFh3xAcd4HTEe58YUDZOAs73SyISSAsjaNJleyPc7W7wSoMHyMcHnuj8uadwEwLqQCU8N-n_q/pubhtml)

