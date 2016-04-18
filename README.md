# video3d

So, the idea is quite simple, let's make a __3D video with a
regular camera__!

In order to create a 3D illusion, our brain must get the _same scene
from both eyes, with almost the same perspective_ but different
enough, in the same way we would if we actually were where the lens
are when the camera is shooting/recording.

## How do we show each eye a different image?

There are several ways in which we can accomplish this task.
Key words to explore alternatives are:

- Anaglyph
- Stereographic
- Polarized 3D
- Active Shutter 3D
- 3D gif (not really what we're trying to do)

A quick search will give you all the information about these methods
and many more.

## Why anaglyph?

As anaglyph googles are easy to find and quite cheap, I have chosen
this method to create the 3D effect by means of red (left eye),
cian (right-eye) googles.

## Are there any mathematics behind this method?

Yes, there are!

A digital image is usually stored as a NxMx3 matrix. The number 3
stands for the Red, Green and Blue channels.
Thus, we have three matrices that contain N by M elements.
These elements are usually integers withing the range: 0-255 (8bits).

## What do I need to do with those matrices?

First you need to have two images, one for each eye. Furthermore,
you need to know what image belongs to each perspective.

Then, as you wont see the red channel with your right eye, you need to
take the right image and drop the red layer. In its place, we are going
to insert the information of the left image, but not just the red channel.
Instead, we are going to combine the three layers of the left image,
as if we were converting it to grey scale, and then attach it to the
previous image where the red channel used to be.

If the perspective of both images was accurate enough, we should be
able to already see the 3D effect.

__Doesn't this seem too simple?__

The trick here is taking the images with the right distance in between,
and maintain the same horizon in both of them.

## How can we do this?

Trial and error. Grab a camera and test your skills! In the beginning
I thought I needed more distance between pictures, but our eyes are
not 6cm appart by chance.


...to be continued...
