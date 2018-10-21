# TiVo Playlisting

**TiVo Playlisting Console**

We're providing an interactive Playlisting Prototype and select assets from our music metadata catalog, to provide interactive experiences around:

* Track, Release, Album, Artist objective and subjective metadata
* Tones, Themes, Moods, and Similar Artists
* Artist & UMG album artwork

{% embed url="https://discovery-beta-admin-0.digitalsmiths.net/console/login" %}

User: CapitalHackathon

Password: CapitalJune2018

**Editorial & Automated Playlist Creation**

Navigation Pane: Select Carousels from the left navigation pane

Editorial Playlists: Click the “+” in the top left of the to create a newcarousel

1. Provide an alphanumeric path name which will be part of the URL to

   call this carousel’s API. This can simply be the Name of the carousel

   with no spaces or special characters

2. Select the type “Editorial”

![page4image3865824](blob:https://cloudinary.gitbook.io/721d717b-3c42-40ca-b711-f2d1d04d6db3)

3. Provide the name for your carousel. This will be the label for it when it is displayed. Click OK.

4. In the “Search” tab, search for a series or title you know, find it in the results, and drag it into the right window. Repeat a few times.

5. Hover over the sliders on the right pane to understand what each means. Try to slide a few of them over and note how the results in the Live Preview change order.

![page5image3855744](blob:https://cloudinary.gitbook.io/a07aec2f-f332-47ec-a47e-fd035f3e6006)

6. Click the disk icon on the top right of the screen to save it. You’ve created an Editorial Carousel.

**Automated Playlists**

Click the “+” in the top left of the screen to create anew carousel

1. Provide an alphanumeric path name which will be part of the URL to

   call this carousel’s API. This can simply be the Name of the carousel

   with no spaces or special characters

2. Select the type “Automated”
3. Provide the name for your carousel. This will be the label for it when it is

   displayed. Click OK.

4. Click the “+” next to the “Any of the following are true...” message in

   the yellow strip

5. Select the “Filter” from drop-down
6. Select an available filter
7. Select the “Type” you want to use from the drop-down
8. Click in the “Values” field to see what options are available to you to

   select. As you start typing, the values will be searched against and limit the results. Select the value\(s\) you want.

![page5image5906752](blob:https://cloudinary.gitbook.io/ec18828b-4c9b-43c0-bf6f-c1c4634681f9)

9. View the Live Preview in the right pane. Use the arrows in the bottom of the pane to scroll through results.

10. Click the “+” on the right side of the dark gray strip of the center pane. This will add an additional filter. Both filters must be satisfied for the results to make it to the Live Preview pane. Additional filters can continue to be added as needed.

11. Click the “X” next to one of the filters. This will delete a filter.

12. Click the “+” next to the “Any of the following are true...” in the center pane. This has created a new set of filters. If any of the set of filters between the dark gray strips are satisfied, then they will be present in the Live Preview.

13. Hover over the sliders on the right pane to understand what each means. Try to slide a few of them over and note how the results in the Live Preview change order.

14. Click the disk icon on the top right of the screen to save it. You’vecreated an Automated Carousel.

**Removing Playlists**

1. Click the trash can icon at the top of the left pane to enter delete

   mode.

2. Click the “X” next to each carousel you just created.
3. Click the trash can icon at the top of the left pane again to come out

   of delete mode.

**Downloading Playlists**

1. Click the drop down, “Toggle Info” icon at the top of the center pane to enter delete mode.
2. Click on the pathway“sd/tivo-music/carousels/...”

![page7image5907872](blob:https://cloudinary.gitbook.io/b75cd4ff-c38a-4ec6-9e39-4d37cdac5717)

3. With a JSON or XML web browser plug-in, you will be able to download and view the TiVo music metadata for each playlist

![page7image5913920](blob:https://cloudinary.gitbook.io/9431c8d9-c692-4d34-8a78-44977fba9c23)

**UI Screen Testing**

1. Select Screens from the left navigation pane
2. Click the “+” in the top left of the to create a new screen
   1. Provide an alpha numeric path name which will be part of the URL to call this screen’s API. This can simply be the Name of thescreen with no spaces or special characters
   2. Provide the name for your carousel. This will be the label for it when it is displayed.
   3. Enter a default number of rows of carousels you want to return on your screen.
   4. Enter a default number of items you want to return in each carousel on your screen. Click OK.
   5. Drag a carousel from the lower left pane into the middle screen pane.
   6. Drag several more carousels into the middle screen pane. Note the listing of content in the Live Preview.
   7. Drag a carousel from the middle screen pane to a different position to update the ordering of carousels on the screen. Note the change in the Live Preview.
   8. Click the disk icon on the top middle of the screen to save it.  You’ve created a Screen.

3. Click the trash can icon at the top of the left pane to enter delete mode.

1. Click the “X” next to each screen you just created.
2. Click the trash can icon at the top of the left pane again to

   come out of delete mode.

**Prototype Limitations**

1. Navigation Pane: “ItemLists”, “Publish” & “Problems” do not work
2. Carousel: “Smart” Carousels do not work
3. Current TiVo Music Metadata Customers may be familiar with a much

   greater array of metadata elements for ‘Filters’. 

Note: the prototype is intentionally limited to the following ‘Filters’: Album/ArtistTones & Themes, Original Release Year, Song Popularity, Artist, Song Genre. All imagery and factual metadata is provided by TiVo Music Metadata

