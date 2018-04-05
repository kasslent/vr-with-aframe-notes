---
layout: lessons
module: 4
lesson: 4
title: Special Saturday VR Coffee House
description: Reimagining Long Lake 58 in 150 years
permalink: module4-4.html
---

## What is VR?

**Virtual Reality** is a computer-generated 3D environment that simulates a real experience. Level of interactivity can vary from passively observing to device-assisted interactions.

Examples:
* <a href="https://www.youtube.com/watch?v=hEK-J3ZgCZA">Tilt Brush</a>
* <a href="https://experiments.withgoogle.com/webvr/konterball">Konterball (ping pong in VR)</a>
* <a href="https://aframe.io/a-blast/">Mozilla AR A-Blast</a>

**Augmented Reality** is a computer-generated experience where a virtual world is superimposed on the user's view of the real world.

Examples:
* <a href="https://www.pokemongo.com/en-ca/">Pokémon Go</a>
* <a href="https://www.youtube.com/watch?v=QN95nNDtxjo">Super Mario Bros AR prototype</a>.  
* <a href="https://experiments.withgoogle.com/ar/justaline">Just a Line (AR drawing app)</a>




## Why VR?

*Why create virtual experiences?*

*What's the value of using virtual experiences over real-life experiences?*

Besides providing immersive storytelling and gaming experiences, VR is also being used to positively impact society! Here are a few examples:

**VR Therapy**: Using VR to face fears like <a href="https://newatlas.com/fearless-spider-fear-oculus-rift-vr/45146/">arachnophobia</a> or <a href="https://newatlas.com/public-speaking-simulation-gear-vr/44871/">public speaking</a>.

**VR + Healthcare**: As a tool for surgical training, or to help patients <a href="https://med.stanford.edu/news/all-news/2017/09/virtual-reality-alleviates-pain-anxiety-for-pediatric-patients.html">manage pain</a>.

**VR + Education**: Providing students access to new places and experiences via <a href="https://edu.google.com/expeditions/#about">Google Expeditions</a>



### Some Considerations

* Motion sickness
* Unstability or 'newness'
* Accessibility and cost



## VR versus WebVR

**WebVR** is a JavaScript API that makes it possible to experience VR in our browser. We can use WebVR to develop, experience, and share VR projects.

*Another example of an API (Application Programming Interface) is the <a href="https://developers.google.com/maps/">Google Maps API</a>, which allows developers to add customized maps to websites and apps.*



## Intro to A-Frame

**A-Frame** is an open source framework for developing WebVR. A-Frame is based on HTML, using the `<a-scene>` element. Because it is cross-platform, we can experience A-Frame projects using anything from an Oculus Rift, to the browser on our desktop computer.

Just like other websites, A-Frame projects can be inspected using a built-in visual 3D inspector. We can access this by opening any A-Frame scene, then hitting `<ctrl> + <alt> + i`


### What Can We Create?

Go to [https://aframe.io/](https://aframe.io/) to explore example projects.

>Navigate within a scene by using WASD and arrow keys. Click and drag to turn.



## Today's project

We'll be reimagining Long Lake 58 in 150 years and building a virtual experience to share our vision with others.

*Embed example here*



## Getting Started

## Primitives

A-Frame uses HTML elements called **primitives**. These can be customized using HTML attributes (e.g. `color="red"`).

<img alt="primitives" src="img/aframe-primitives.jpg" class="print-hide"/>

* **Position** defines an object's position in 3D space (X,Y,Z)
  * X = left-right
  * Y = up-down
  * Z = forward-back
* **Rotation** defines an object's orientation in 3D space (X,Y,Z) - measured in degrees
  * X = pitch
  * Y = yaw
  * Z = roll

<img alt="rotation" src="img/paper-plane.png" class="print-hide"/>



## Remixing Projects

We'll be using Glitch to edit and save our A-Frame projects.

### Open the Example Project

1. Go to [https://glitch.com/~aframe](https://glitch.com/~aframe)
1. Select "Remix Your Own" <br> <img alt="remix your own" src="img/aframe-remix.png" class="print-hide"/>
1. Click "Show Live" to preview the project <br> <img alt="show live" src="img/show-live.png" class="print-hide"/>


### Edit the Code

1. Go back to the project tab
1. Open index.html. *Anything look familiar?* <br> <img alt="see index" src="img/see-index.png" class="print-hide"/>
1. Sign in with GitHub to begin editing. <br> <img alt="sign in" src="img/sign-in.png" class="print-hide"/>


>## CHALLENGE:
> * Change the colour of the sphere
> * Change the rotation of the box
> * Change the position of the cylinder
> * Add a line of text in the center of your scene (see <a href="https://aframe.io/docs/0.8.0/primitives/a-text.html"> A-Frame primitives</a>)



## Using Assets

### Uploading Images

1. Upload images to the "assets" folder
<br><img alt="add asset" src="img/add-asset.png" class="print-hide"/>

**Background Images**

We can add a background image by applying a 360 image texture to the sky primitive.

For more image options, check out these <a href="https://www.flickr.com/groups/equirectangular/">360° images from Flickr</a>. Save an image by clicking on the image, then the Download icon (bottom, right). <br> <img alt="download image" src="img/flickr-save.png" class="print-hide"/>

*Note: We can also capture 360 images using apps like <a href="https://play.google.com/store/apps/details?id=com.google.vr.cyclops&hl=en">Cardboard Camera</a>*

**Textures**

We can add textures to objects, too!

For more image options, check out these <a href="https://www.flickr.com/groups/freetextures/">free textures from Flickr</a>. Save an image using the same steps as above.


### Using the Asset Management System

This system helps your browser cache the images, to help the scene load more quickly. We can use the asset management system by adding a new primitive called `<a-assets>`.

1. Add an `<a-assets>` opening and closing tag just inside of your `<a-frame>`
1. Copy the image URL <br> <img alt="copy url" src="img/copy-img-url.png" class="print-hide"/>
1. Create an `<img>` tag that links to this url
1. Name the image by adding an `id`  

``html
    <a-scene>
      <a-assets>
        <img id="rocklands" src="https://cdn.glitch.com/linktoimage1">
      </a-assets>

      <!--other primitives go here-->

    </a-scene>
``


### Adding a Background Image

1. Reference the asset by adding a `src` attribute to the `<a-sky>` primitive

    `<a-sky src="#rocklands"></a-sky>`


### Adding Textures to Objects

1. Copy the image URL (same as above) <br> <img alt="copy url" src="img/copy-img-url.png" class="print-hide"/>
1. Create an `<img>` tag that links to this url
1. Name the image by adding an `id`  
1. Reference the asset by adding a `src` attribute to the object primitive

``html
  <a-scene>
    <a-assets>
      <img id="rocklands" src="https://cdn.glitch.com/linktoimage1">
      <img id="ice" src="https://cdn.glitch.com/linktoimage2">
    </a-assets>
    <a-plane src="#ice" position="0 0 -4" rotation="-90 0 0" width="4" height="4" shadow></a-plane>
    <!--other primitives go here-->
  </a-scene>
``

## Adding Movement



## Adding Interactivity



## Main Project

>## Think, Pair, Share
> Q: Fast forward 150 years! What does Long Lake 58 look like in 2067? <br>
> Q: What do you wish for this community, what do you hope to see?





## Experience your Virtual World!

Google Cardboard


### Next Steps

**Get Inspired!** Check out <a href="https://twitter.com/aframevr">A-Frame's Twitter page</a> to see what other developers are building.



>### Take-Home Exercise
> Any Minecraft fans? Check out: [aframe-aincraft](aframe-aincraft) <br>
> You can recreate this project by following <a href="https://aframe.io/docs/0.5.0/guides/building-a-minecraft-demo.html">this tutorial</a>.



~ End ~


### Heading

>Pink box

**bold**

*Italics*

Code:
    <tag>Content that shows on page.</tag>
      |                               |
      |--opening tag                  |--closing tag

or `code`

[image](http://html5doctor.com/lets-talk-about-semantics/)
