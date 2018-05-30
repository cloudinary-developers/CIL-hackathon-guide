# Discover Music

{% hint style="success" %}
### **Discover Music is a complete, ready-to-run example app that integrates APIs from The 7Digital UMG Catalog, Cloudinary, Microsoft, Tivo, and more!** 
{% endhint %}

![](../.gitbook/assets/screen-shot-2018-05-29-at-07.36.19.png)

{% hint style="info" %}
See it here:  [https://discover-music-live.herokuapp.com](https://discover-music-live.herokuapp.com)
{% endhint %}

The app consists of two main components:

1. [a Vue-based front end](https://github.com/cloudinary-developers/discover-cmg-music)

which consumes data from

2. [a serverless endpoint](https://github.com/cloudinary-developers/music-discovery-service), running on Auth0 extend.

It allows you to search and sort your way through a massive music catalog, supplied by 7Digital. Notable features:

* Album and artist images are cropped, padded, optimized and delivered using Cloudinary
* Artists, albums, and tracks are fetched using the [Music Discovery Service API](https://github.com/cloudinary-developers/music-discovery-service), which wraps APIs from 7Digital, Microsoft, and Rovi.
* Notable Vue components used on the front-end include [Vue-APlayer](https://vue-aplayer.js.org), and [vue-social-sharing](https://www.npmjs.com/package/vue-social-sharing).

Feel free to use, modify and extend any part of this blueprint app for your hack. Make it your own!


