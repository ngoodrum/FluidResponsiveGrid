Fluid Responsive Grid FTW
===================

###IE8+ Simpler but flexible, progressively enhanced, fluid based responsive grid

After going through many versions of grids, percentages, and responsive designs, I decided to try and build a hopefully simpler "framework". 

The main push of this version is to allow you to make your own layouts for different screen resolutions, rather than just falling back to 100% once you hit most handheld landscape view. I assume a bit with what most users would like to have for their different views (number of columns). Another aspect, is that this should progressively enhance into what you want. 

The path goes:
s  ( small [ ~ handheld ] ) 
sw ( small wide [ ~ handheld landdscape ] ) 
m  ( medium [ ~ tablet portrait ] ) 
mw ( medium wide [ ~ lower end desktop size / tablet landscape ] ) 
l  ( large [ ~ wider desktops ] )

That's right after much discussion over the Internets, I understand that really we might want to shy away from saying phone, tablet, and desktop. Mobile is more a state of mind than an actual size now that more and more devices access the web. Laptops are becoming the majority "desktop" experience. Why not just call them like the sizes they are? 

###What all is resolved with this approach:

* If you happen to have a browser that doesn't understand media queries you get a full 100% view of your content. And you thought your oh so great not so smart phone shouldn't be able to view content. Really, it will probably still look like crap but we won't delve too deep into that for the base. 

* If the browser understands media queries and happens to be larger than 256px (could set it to be 0 if you so desire and I may so desire as well down the road). Then you are served up a full 100% width version but with some options to have two columns.

* Zoom is potentially your friend for once. Zoom and you can frolic around since we go with an em based set of media queries.

* But I love the 960 grid, how could I ever give it up? We've got that as well. This lines up with your designs in 960 and 1140 since it is a 12 grid system. I'll potentially add push/pull soon but wanted to put my initial thoughts down.

###Dependencies to make this work:

* ems will become your friend and pixel based fonts will be your frienemy. Moral of the story, we shouldn't overwrite our base font size with pixels. This will help you forge the bond with your friend Zoom. Don't tell me you forgot about it.

* On that note, I would suggest using a form of normalize rather than reset for your base. Normalize does a good job of avoiding overwrites that include pixel based aspects as best as possible.

* Respond.js: IE8- just needs it. This helps handle your media queries since older IE doesn't quite grasp them. But wait, there's an extra bonus in there. Max-width on box-sizing elements in IE8 fail and that makes many a sad panda. Respond.js has the extra firepower that kicks IE back into shape and max-width works again. (The max-height/min-height issues with some browsers is another story and let's just hope you don't need to use them ( ^_~)

* Box-sizing. It is the key piece in all of this so you better thank it properly. But the person I'm designing for thinks IE7 is the bees-knees. Well, too bad! Okay, you might try a polyfill for box-sizing as well. 
