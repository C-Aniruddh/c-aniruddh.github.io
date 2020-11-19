---
layout: post
title:  "Monitoring Road Conditions throughout the city & 3D reconstruction - Winning the Deep Blue Challenge Season 4"
author: aniruddh
categories: [ Machine Learning ]
image: https://aniruddh-chandratre-e877.netlify.app/static/8845b517f7a3a3d34e0033a029f1126e/eeb1b/Screenshot-from-2019-11-27-00-07-35.png
toc: true
---

Developing a system for monitoring city-wide road conditions with a continous loop of communication between a citizen and the concerned government agency.


## Demo

<iframe width="560" height="315" src="https://www.youtube.com/embed/XX66sdlBIIE" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>


## Featured on Times NOW (Indian News Channel)

(at 0:45)

<iframe width="560" height="315" src="https://www.youtube.com/embed/vKCzrUAA2ks" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

## Need of the hour

Road conditions has a very important place in travel safety throughout the world. However, for some reasons, the road infrastructure is not up-to the mark in majority of the world. For example, in India, an average of 150,000 people are involved in road accidents that can be directly or indirectly linked to improper road conditions.

From the 150,000, 50,000 people suffer major injuries or temporarily major injuries (those who heal in less than 6 months). Among the 50,000, 10,000 people lose their life to such accidents or are crippled for life. The numbers are huge, and no one can be held accountable for such incidents.

This is where the solution comes in. The solution consists of an app which enables citizens to upload photos of damaged roads. The application fist classifies the road damage and if the road damage type is a pothole, then the application proceeds to calculate the cost of repairs for the same.

## How does it work?

The main pipeline can be broken down into 4 stages.


1. Upload : Upload deals with how the citizen is going to interact with the people of interest. The application asks the user to take 2 pictures of the road damage with some variation in both (the app guides the movement of the camera). The application makes use of GPS to geotag the image Exif tags such that they can be extracted later.
2. Pre-processing : Photogrammetry algorithms heavily rely on the intrinsic parameters of the lens being used in order to create a mesh or a point cloud. However, by deviating from traditional photogrammetry algorithms, the solution makes use of three deep neural networks running together to provide the depthmap from the two images. We perform a transform such that the intrinsic parameters are normalised.
3. Depth Calculation : The three networks work together to provide a depth map, and the guided movement of the camera provides us with an accurate measurement of distance between the position of the camera in the first and the second image. Using this information, we can create a to-scale depth map. This depth map is then exported as a point cloud for visualisation purposes. The volume is estimated and the cost of ingredients is computed for repairs.
4. Update database : The information that is extracted above is then used to report the road damage to the respective authorities.

### Modes of operation
One very important thing to keep in mind when designing solutions is the user experience. For this solution, I realised that most of the users who would want to report a pothole would be in a moving vehicle. So we made two usage modes :

1. Autonomous Mode : This mode can be activated in background, and the phone can be mounted onto the windshield or the data can be captured by using dash-cams. The potholes reported with this method do not support calculation of costs using 3D reconstruction.
2. Manual Mode : The application can be used as a hand held device to click two proper pictures of the road damage.

## Actively saving lives
Yes, the application delivers reports to the particular authorities, but the authorities take time to fix the road damage. So how does the application help in this case?

The citizen can opt-in for road damage alerts on his/her device. The application will run in background and will provide a heads-up notification 40-50 meters prior to arriving at the spot with the road damage (The road damage should have been reported earlier). This provides enough reaction time and preparation time for the driver to either switch lanes or to slow down in order to avoid an accident.

## No Cheating possible
Once the pothole has been fixed, the agent responsible for fixing the damage has to upload a picture onto the portal in order for the issue to be marked as resolved. If the new picture consists of a new type of damage, or senses that the pothole was not repaired properly, the platform will mark the issue as unresolved.

## Prize
The solution was submitted to the Mastek Deepblue Challenge Season 4 under the citizen service portal track. The final demonstration received a standing ovation for proper execution, and secured the first position among 500+ (including the initial abstract submissions) teams.