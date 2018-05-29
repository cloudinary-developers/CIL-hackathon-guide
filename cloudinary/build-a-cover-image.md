---
description: By Dan Zeitman and Miki Shiran
---

# Build a cover image

In this example we'll take a performance image and create a cover image.   Here we have the amazing Jazz artist, Wayne Shorter  - image copyright and courtesy of Capitol Music Group.

![](http://res.cloudinary.com/capitol-music-group/image/upload/w_400/v1526606182/wayne-shorter/speak-no-evil/WSHORW12.jpg)

Beautifully cropped square image, but to make it a cover image we need the image to fit into a 16:9 aspect ratio.  We will need to pad the image to make up the image fit into the new aspect ratio.   First step is to example the direction the performer's eyes are gazing.  Wayne is looking to the left so let's add lead space and pad the image to the left.

![](http://res.cloudinary.com/capitol-music-group/image/upload/ar_16:9,c_lpad,g_east/w_600/v1526606182/wayne-shorter/speak-no-evil/WSHORW12.jpg)

```text
http://res.cloudinary.com/capitol-music-group/image/upload/
ar_16:9,c_lpad,g_east/v1526606182/wayne-shorter/speak-no-evil/WSHORW12.jpg
```

We added aspect ratio of 16:9, cropping of lpad and gravity east to create the image and move it to the right. This done simply by adding the params into the url as follows:

```text
ar_16:9,c_lpad,g_east
```

Nice but would it be better if the background color matched the exact same color as the backgound in our original?   Easy!  Just add background auto to our url: 

```text
b_auto
```

![](http://res.cloudinary.com/capitol-music-group/image/upload/ar_16:9,b_auto,c_lpad,g_east/w_600/v1526606182/wayne-shorter/speak-no-evil/WSHORW12.jpg)

```text
http://res.cloudinary.com/capitol-music-group/image/upload/
ar_16:9,b_auto,c_lpad,g_east/v1526606182/wayne-shorter/speak-no-evil/WSHORW12.jpg
```

Looking good! Now lets optimize this for performance and quality.

![](http://res.cloudinary.com/capitol-music-group/image/upload/ar_16:9,b_auto,c_lpad,dpr_auto,f_auto,g_east,q_auto:best/w_600/v1526606182/wayne-shorter/speak-no-evil/WSHORW12%20)

We can optimize the dpi, format, and quality with a few additional params in our url:  

```text
dpr_auto,f_auto,q_auto:best
```

The addition of these params will improve performance and delivery of the final image tremendously,  In general you should always use them. 

```text
http://res.cloudinary.com/capitol-music-group/image/upload/
ar_16:9,b_auto,c_lpad,dpr_auto,f_auto,g_east,q_auto:best/
w_1600/v1526606182/wayne-shorter/speak-no-evil/WSHORW12
```

You'll notice we also added a width param: **w\_1600**  - You'd set this to fit the image into a explicit layout size, if you omit it you'll get the original image size.  The example here were set at a width of 600 to fit nicely in the layout.

Our cover image allready looks awesome, but let add a artistic filter to enhance the black and white image.  Adding the effect param with a named filter is how we do it.

```text
e_art:red_rock
```

![](http://res.cloudinary.com/capitol-music-group/image/upload/ar_16:9,b_auto,c_lpad,dpr_auto,f_auto,g_east,q_auto,e_art:red_rock/w_600/v1526606182/wayne-shorter/speak-no-evil/WSHORW12)

Nice vibe!  You can almost hear Wayne's smooth jazz sounds.   We have dozens of artistic filters, text and image overlays to experiment with and make that cover image pop.

![](http://res.cloudinary.com/capitol-music-group/image/upload/ar_16:9,b_auto,c_lpad,dpr_1.0,e_art:red_rock,g_east,q_auto:best/c_scale,fl_relative,w_0.3,g_west,l_overlays:4194-wayne-shorter-speak-no-evil-mm-cover-1900-ljc,x_0.05,a_-20/c_scale,w_600/wayne-shorter/speak-no-evil/WSHORW12.jpg)

Add some text:

![](http://res.cloudinary.com/capitol-music-group/image/upload/ar_16:9,b_auto,c_lpad,dpr_1.0,e_art:red_rock,g_east,q_auto:best/c_scale,fl_relative,w_0.3,g_west,l_overlays:4194-wayne-shorter-speak-no-evil-mm-cover-1900-ljc,x_0.05,a_-20/l_text:roboto_155_stroke_center_line_spacing_-10:Speak%20No%20Evil,co_white,bo_5px_solid_black,g_north_west,x_400,y_80,w_580,c_fit/l_text:impact_55_stroke_center_line_spacing_-10:Wayne%20Shorter,co_white,bo_5px_solid_red/c_scale,w_600/wayne-shorter/speak-no-evil/WSHORW12.jpg)

```text
http://res.cloudinary.com/capitol-music-group/image/upload/
ar_16:9,b_auto,c_lpad,dpr_1.0,e_art:red_rock,g_east,q_auto:best/
c_scale,fl_relative,w_0.3,g_west,
l_overlays:4194-wayne-shorter-speak-no-evil-mm-cover-1900-ljc,x_0.05,a_-20/
l_text:roboto_155_stroke_center_line_spacing_-10:Speak%20No%20Evil,
co_white,bo_5px_solid_black,g_north_west,x_400,y_80,w_580,c_fit/
l_text:impact_55_stroke_center_line_spacing_-10:Wayne%20Shorter,co_white,bo_
5px_solid_white/c_scale,w_600/wayne-shorter/speak-no-evil/WSHORW12.jpg
```

#### Variations

![](http://res.cloudinary.com/capitol-music-group/image/upload/w_600/ar_16:9,b_auto,e_gradient_fade:symmetric_pad,x_0.2,c_pad,f_auto,g_east,q_auto/v1526782137/blue-note/wayne-shorter/MI0001444348.jpg.jpg)

```text
http://res.cloudinary.com/capitol-music-group/image/upload/
ar_16:9,
b_auto,e_gradient_fade:symmetric_pad,x_0.2,
c_pad,f_auto,g_east,q_auto/v1526782137/
blue-note/wayne-shorter/MI0001444348.jpg.jpg
```

This variation pulls in the background color and eases in the transition with gradient fade:

```text
b_auto,e_gradient_fade:symmetric_pad,x_0.2
```

![](http://res.cloudinary.com/capitol-music-group/image/upload/w_600/ar_16:9,b_white,e_gradient_fade:symmetric_pad,x_0.2,c_pad,f_auto,g_east,q_auto/v1526782137/blue-note/wayne-shorter/MI0001444348.jpg.jpg)



Here we use the gradient fade to transition the background to white:

```text
http://res.cloudinary.com/capitol-music-group/image/upload
ar_16:9,
b_white,
e_gradient_fade:symmetric_pad,x_0.2,c_pad,f_auto,g_east,q_auto/
v1526782137/blue-note/wayne-shorter/MI0001444348.jpg.jpg
```

You can also have the that gradient fade into transparency to reveal the background;  remember to change the format extension to png.

![](http://res.cloudinary.com/capitol-music-group/image/upload/w_600/ar_16:9,b_transparent,e_gradient_fade:symmetric_pad,x_0.2,c_pad,f_auto,g_east,q_auto/v1526782137/blue-note/wayne-shorter/MI0001444348.jpg.png)

```text
http://res.cloudinary.com/capitol-music-group/image/upload/
ar_16:9,b_transparent,e_gradient_fade:symmetric_pad,x_0.2,
c_pad,f_auto,g_east,q_auto
/v1526782137/blue-note/wayne-shorter/MI0001444348.jpg
.png
```

Now see how this technique might look on a web page with an interesting background:

![](../.gitbook/assets/transparent-background.png)

