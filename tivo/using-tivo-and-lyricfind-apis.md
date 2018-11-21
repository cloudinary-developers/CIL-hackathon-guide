# Using TiVo & Lyricfind APIs’

![](../.gitbook/assets/tivo_lockup_blk_blue_2%20%281%29.png)

> At TiVo, we’re always innovating to create the ultimate entertainment experience. When it comes to music, we deliver the personalized, engaging listening experiences fans can’t resist. Our best-in-class Music Metadata covers millions of albums and tracks, and offers standardized IDs, unique descriptors, high-quality imagery and more. Streaming providers can enhance their services, while labels, publishers and distributors can more effectively market and merchandise their catalogs. Around the world, leading brands choose TiVo to deliver the music fans want and introduce them to their next obsession, creating loyal customers in the process.

**TiVo Music** API Documentation

You may know of us from our former name, AMG/Rovi, and a website that was formerly a property of ours which features our music metadata \([allmusic.com](https://www.allmusic.com)\).

We're providing unlimited access \(500 requests/sec, no daily limit\) to the same music metadata powering services such as Spotify, Pandora, Apple Music, etc.

You can use the API Key/Secret below which is also included in the Cloudinary sample app.

API Key - 7d9vkau5knchkpa4z9pkcg7d

API Secret - mmj58xRfZw

TiVo Music API Console - this can be used to quickly preview all of our different types of music metadata without having to write any code !  Click on the following link and choose 'Metadata and Search APIs' from the drop-down menu - [http://developer.rovicorp.com/io-docs](http://developer.rovicorp.com/io-docs).  Enter the API Key and Secret from above to return a JSON response from any of the API endpoints in the list.

For example, use the 'Name ID' to retrieve artist styles, themes, moods, etc. using the 'Name' API \(scroll toward the end of the IO-Docs page\) - Wayne Shorter = Name ID MN0000250435 \(for 'include' enter musicStyles,moods,themes\).

If you're using our APIs outside of the Cloudinary sample application, we provide the following tool to help create your own API signature since all requests require a combination of the API Key and API Signature  - [http://developer.rovicorp.com/siggen](http://developer.rovicorp.com/siggen)

Alternatively, use the following JavaScript example that combines the API Key/Secret with the MD5 library here - [http://developer.rovicorp.com/files/md5\_2.js](http://developer.rovicorp.com/files/md5_2.js) .

    function genSig\(\) {

    var apikey = "valid\_apikey";

    var secret = "valid\_secret";

    var curdate = new Date\(\);

    var gmtstring = curdate.toGMTString\(\);

    var utc = Date.parse\(gmtstring\) / 1000;

    return = hex\_md5\(apikey + secret + utc\);

}

You can also use the following node.js function - Math.floor\(new Date\(\) / 1000\) to create a UNIX epoch timestamp and then concatenate it with our API Key/Secret.  Use a MD5 hash on the entire string to create your signature.

Although the majority of the APIs that will be needed for your use-case are already a part of the Cloudinary application, we're providing complete API documentation below on all of our various APIs.

>

**LyricFind** API Documentation

> [http://www.lyricfind.com/documentation/?key=eyJkb2N1bWVudCI6IndlYl9zZXJ2aWNlIiwib3B0aW9ucyI6eyJwcmVtaXVtIjoidHJ1ZSIsIm9sZGtleXR5cGVzIjoiZmFsc2UifX0=\#the-lyric-display-api](https://emea01.safelinks.protection.outlook.com/?url=http%3A%2F%2Fwww.lyricfind.com%2Fdocumentation%2F%3Fkey%3DeyJkb2N1bWVudCI6IndlYl9zZXJ2aWNlIiwib3B0aW9ucyI6eyJwcmVtaXVtIjoidHJ1ZSIsIm9sZGtleXR5cGVzIjoiZmFsc2UifX0%3D%23the-lyric-display-api&data=02%7C01%7CChingChing.Chen%40umusic.com%7Cd5c76183868e484eb22708d5c5d0512d%7Cbbcb6b2f8c7c4e2486e46c36fed00b78%7C1%7C0%7C636632422086228515&sdata=E%2FjiVhqSmlEpaSvin%2BV3Rh1hfsdmhF3WTzFVdgrUJPg%3D&reserved=0)

Use the ISRC from the TiVo/7Digital API response or Cheat Sheet to retrieve lyrics for a track - certain tracks may include a 'lrc' object which will contain lyric sync timestamps that can be used to sync the lyrics to the audio track from 7Digital.

[http://api.lyricfind.com/lyric.do?apikey=14c9a53ff33f0adf99435f207d9c4b2f&territory=US&reqtype=default&trackid=isrc:USUM71203819&format=lrc&lrckey=230ac06cba8d3ecd6996466e8356b6e4](http://api.lyricfind.com/lyric.do?apikey=14c9a53ff33f0adf99435f207d9c4b2f&territory=US&reqtype=default&trackid=isrc:USUM71203819&format=lrc&lrckey=230ac06cba8d3ecd6996466e8356b6e4)

If the ISRC can't be used to retrieve track lyrics, use the 'AMG' T\_ID from the TiVo/7Digital API response or Cheat Sheet to retrieve lyrics for a track \(only use the numbers in the ID\).  Here's an example using 'Tangled' from Maroon 5 \(AMG 'T 26901151' - note: the leading 'T' and space has been stripped for the LyricFind API\)

[http://api.lyricfind.com/lyric.do?apikey=14c9a53ff33f0adf99435f207d9c4b2f&territory=US&reqtype=default&trackid=amg:26901151&format=lrc&lrckey=230ac06cba8d3ecd6996466e8356b6e4](http://api.lyricfind.com/lyric.do?apikey=14c9a53ff33f0adf99435f207d9c4b2f&territory=US&reqtype=default&trackid=amg:26901151&format=lrc&lrckey=230ac06cba8d3ecd6996466e8356b6e4)

**Cheat** **Sheet** of all artists/albums/tracks used for the Capitol Royale Hackathon Catalog

Use the below link and choose File&gt;Download As&gt;CSV to import a CSV into your SQL/Mongo DB or to simply preview the artists, albums, and tracks in the catalog.

[https://docs.google.com/spreadsheets/d/1NO7v6o58JAPjpRJuHQh86pIrI69dCKaobZby-6XpGps/edit?usp=sharing](https://docs.google.com/spreadsheets/d/1NO7v6o58JAPjpRJuHQh86pIrI69dCKaobZby-6XpGps/edit?usp=sharing)

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
| :--- | :--- | :--- | :--- | :--- |
| Champion | USUM70749084 | MT0041589685 | T 23962028 | SD0000326091 |

'SI' - Composition ID -   TiVo's Composition ID isn't used as part of our API however it can be used to create a unique discovery experience using cover songs across genre boundaries.  For example, the song 'Ain't No Sunshine' has been covered by numerous artists over the years and we now give you the ability to easily find all covers for this song in the catalog since they share the same Composition ID.

The Composition ID 'SI0005189120' represents this song and using the Cheat Sheet above, we can see it has been covered by all of the following artists in the Capitol Royale Catalog - Michael Jackson, Anthony Billups, Bill Withers, David Holmes, Jackyl, Lighthouse Family, Roy Ayers, The Neville Brothers.  Use the ISRC with the 7Digital to stream all of these covers.

If you don't have an artist ID, UPC or album ID, ISRC or TrackID, it's still possible to retrieve artist/album/song information using one of the following:

In the following example, we're using Michael Jackson - 

[http://api.rovicorp.com/data/v1.1/name/info?name=Michael+Jackson&country=US&language=en&format=json&apikey=](http://api.rovicorp.com/data/v1.1/name/info?name=Michael+Jackson&country=US&language=en&format=json&apikey=szkmrmm95jgxdkpsjqa7bvnx&sig=)[7d9vkau5knchkpa4z9pkcg7d](http://api.rovicorp.com/data/v1.1/album/info?album=Anthology%3A+The+Best+Of++Michael+Jackson&country=US&language=en&format=json&apikey=7d9vkau5knchkpa4z9pkcg7d)[&sig=](http://api.rovicorp.com/data/v1.1/name/info?name=Michael+Jackson&country=US&language=en&format=json&apikey=szkmrmm95jgxdkpsjqa7bvnx&sig=)

In the following example, we're using the album, 'Anthology: The Best Of  Michael Jackson' - 

[http://api.rovicorp.com/data/v1.1/album/info?album=Anthology%3A+The+Best+Of+Michael+Jackson&country=US&language=en&format=json&apikey=7d9vkau5knchkpa4z9pkcg7d](http://api.rovicorp.com/data/v1.1/album/info?album=Anthology%3A+The+Best+Of++Michael+Jackson&country=US&language=en&format=json&apikey=7d9vkau5knchkpa4z9pkcg7d)

In the following example, we're using the song, 'Tangled' by Maroon 5 - adding the artist name to the query ensures we don't retrieve any other songs with the same title by other artists.

[http://api.rovicorp.com/data/v1.1/song/info?track=Tangled&country=US&language=en&format=json&apikey=7d9vkau5knchkpa4z9pkcg7d&sig=&artist=Maroon%205](http://api.rovicorp.com/data/v1.1/song/info?track=Tangled&country=US&language=en&format=json&apikey=7d9vkau5knchkpa4z9pkcg7d&sig=d36a53e7377df8dc0f80359270121dfa&artist=Maroon%205)

**Cheat Sheet** - Master Genre/Subgenre/Style List

Use the below link and choose File&gt;Download As&gt;CSV to import a CSV into your SQL/Mongo DB for a master list of all TiVo Music genres, subgenres, and styles - this can come in handy to create a genre/subgenre/style map or discovery experience.

[https://docs.google.com/spreadsheets/d/1PgrGIifacbLokkh7mZgjU2JIi1zUGdVA0HMx4wlJIGs/edit?usp=sharing](https://docs.google.com/spreadsheets/d/1PgrGIifacbLokkh7mZgjU2JIi1zUGdVA0HMx4wlJIGs/edit?usp=sharing)

**Cheat Sheet** - Master Moods List

[https://docs.google.com/spreadsheets/d/1K\_o6rKLHZ5zTkGbxLRw9ERXzpX3SfnKQSjKIKKaQHtM/edit?usp=sharing](https://docs.google.com/spreadsheets/d/1K_o6rKLHZ5zTkGbxLRw9ERXzpX3SfnKQSjKIKKaQHtM/edit?usp=sharing) 

**Cheat Sheet** - Master Themes List

[https://docs.google.com/spreadsheets/d/1OMA091NxeAFpOUAfPBU6AoP4iixNg3y1lDFK\_u9G2gk/edit?usp=sharing](https://docs.google.com/spreadsheets/d/1OMA091NxeAFpOUAfPBU6AoP4iixNg3y1lDFK_u9G2gk/edit?usp=sharing) 

**Real-Time** **Trending & All-Time Popularity**

TiVo uses a proprietary content Knowledge Graph to determine assets that are trending and popular based on real-time changes on social media, blogs, news sites and other sources.

These results change throughout the day \(updated approximately every 10-15mins\) depending on what is happening in the world.

Top 100 Trending Artists 

[http://api.veveo.net/music/data/trends?custid=rovi&with\_gid=1&filter\_by\_gid\_type=person](http://api.veveo.net/music/data/trends?custid=rovi&with_gid=1&filter_by_gid_type=person)

Top 100 Trending Tracks

[http://api.veveo.net/music/data/trends?custid=rovi&with\_gid=1&filter\_by\_gid\_type=track](http://api.veveo.net/music/data/trends?custid=rovi&with_gid=1&filter_by_gid_type=track) 

We also have a concept of all-time popularity for an artist or track which is returned by the Cloudinary sample application.

Our all-time artist popularity is based on a scale of 0-800, and our all-time track popularity is based on a scale from 0-300.



