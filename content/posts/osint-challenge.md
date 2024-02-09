---
title: "OSINT Challenge - Feb 7th Iraq Airstrike"
date: 2024-02-08T21:04:34-08:00
draft: false
---


On February 7th, 2024 at 9:30 PM in Baghdad, Iraq the U.S military conducted an air strike on a single vehicle that contained a senior leader of Kata’ib Hezbollah who [USCENTCOM](https://www.centcom.mil/MEDIA/PRESS-RELEASES/Press-Release-View/Article/3669808/uscentcom-conducts-strike-killing-kataib-hezbollah-senior-leader/) says both planned and took part in attacks of U.S forces in the region. At this time USCENTCOM says that other than the passengers there are no other fatalities. 

For the past two days I have been trying to learn and practice practical OSINT. I thought about debunking some misinformation on twitter, or geolocating a friend in a picture. But after seeing the anger in Iraq because of the strike I thought that there might be enough info on social media for me to work with in narrowing down the location. My goal was simple, use as little outside info to get the exact coordinates of the strike using only public resources and reporting. I started by collecting photos and stills from videos both shortly after the airstrike, and later on during clean up efforts when more people would be filming. But first I needed to get down to the rough area of the strike. Looking through media reports and [X posts](https://twitter.com/i/status/1755301942501195958) I saw several mentions of `Al Mashtal area`and ` Al Mashtal neighborhood, eastern Baghdad, Iraq`. 

![a](/images/osint-chal/outline.png#center)


A good start, but still a large area. And since I don't read or write (or speak) Arabic, signs and google maps locations wouldn't be a huge help. Not to mention its not google street view widely available in this part of the world. Even still I started to pick apart videos and images to gather some clues. Looking at this picture we can see the car after the strike was lifted with a truck with a crane. And presumably at or near its position at the time of the strike.

![a](/images/osint-chal/first-image.png#center)

The text on the building is clear. So let's run it through google lens to try to either identify the building or the text.

![a](/images/osint-chal/first-image-text-1.png#center)
![a](/images/osint-chal/first-image-text-2.png#center)

Okay I don’t know what to make of this, using different search engines I get no clear link to this building. Based on the translation we may be able to conclude it serves a religious purpose, but one time I used google translate on a Honda radiator cap and it translated to “ming dynasty” so keeping my expectations low. 

Here is a still from a video just after the strike. The text is blurry so no point in using google lens, but knowing a billboard is on the building may help later when looking at satellite photos for confirmation.

![a](/images/osint-chal/bill_board_first.png#center)

This still presumably near the site there is either a car supply or maintenance vendor, but looking at all car related locations in the Al Mashtal area in google maps there is now way I could narrow it down off of this alone, but again might be good for confirmation later. 

![a](/images/osint-chal/auto.png#center)

Another still from a video shows another angle of both the car and the possible religious building from earlier. With the car being on what appears to be a flatbed it's fair to assume that this intersection is the site. And another video still appears to show the same building with the billboard from earlier. So now we know for sure this is the intersection and have a rough idea what the building shapes are. 

![a](/images/osint-chal/both.png#center)
![a](/images/osint-chal/layout.png#center)

At this point I go back to twitter after having no luck with using google images of local shops to try to pinpoint nearby spots. I found [this X post](https://twitter.com/anadoluagency/status/1755567150742340020) claiming to have the “exact location” on a map. But it's still hard to discern the location, and the link did not contain the coordinates, so I used it to further shrink the area of observation.

![a](/images/osint-chal/exact-location.png#center)

The point appears to be right on the outskirts of the area off a main road, which makes sense for why the strike commenced when it did. Late at night, likely little traffic, and a wide road compared to rest of the area. In conjunction with the map, I start following the main turn offs near the red dot using other roads and nearby bodies of water to guide me. Finally I have a seemingly solid match from the satellite imagery, but I want to have further proof.

![a](/images/osint-chal/building-match.png#center)

Using this [Al Jazzera video from X](https://twitter.com/AJEnglish/status/1755508927876514102) we can see a building in the distance with green trim that protrudes out slightly, which we saw from the auto shop photo, and in the opposite direction a large metallic structure on a roof behind the billboard building.

![a](/images/osint-chal/aj-green-building.png#center)
![a](/images/osint-chal/aj-metal-structure.png#center)
![a](/images/osint-chal/all-three.png#center)

Okay cool we another match. But is there anything else? Maybe the trees down the street show up in [another video](https://twitter.com/i/status/1755310845368897622)? 

![a](/images/osint-chal/tree-crop.png#center)

Bingo. `33.32494626126921, 44.487224557000324`
