# SLackathon-RADS-01

## Overview:
The Road Accident Detection System, or RADS, is used to identify crashes seen on the roadways and transmit information about them to the closest medical facility and police stations. The cameras installed alongside the road are the hardware used to collect this data, and the Ardino that is attached to it is utilised for processing. Location of the Accident, Impact of the Accident, Type of Vehicle(s), Probable Number of Injured, and Vehicle Owner's Information are among the details supplied.

## How can technology help?
Road accident victims who pass away owing to delays and/or accidents in remote areas will receive prompt medical care, thanks to RADS.

## The idea
The goal is to locate vehicles that have been involved in accidents because they were unable to cross the indicated territory in the allotted maximum time, and to analyse the reason why, by scanning the whole coverage area using object detection with OpenCV.
Once it is determined that the object(s) have not moved in the last five minutes, footage from that time period is examined to determine their average speed prior to collision. The impact of the collision can then be calculated based on how long it might take for the object(s) to travel to the accident point.

## Demo Video
https://user-images.githubusercontent.com/47938204/195777875-12a10fbe-0659-4ac5-b617-40252ba01a75.mp4

## Detailed Description:
1.	In the video, we intend to provide the coordinates of the road to the code for the beginning(**S**) and end(**E**) where the accident is to be detected.
2.	Using a speed of 5 km/hr, a maximum time (**M**) is estimated to travel the specified distance.
3.	A dictionary with the vehicle's unique ID is kept from the time the vehicle enters the point S until it exits the point E, where the unique ID is the key and the time of entry into the point S is the value.
4.	The dictionary's key-value pair for the stored vehicle ID is destroyed as soon as the car leaves point E.

### Parallel to that, the following occurs:

1.	A method is activated every minute to determine whether the time for each object in the dictionary is less than the maximum duration of crossing (M).
2.	If a higher number is discovered, the entire route between points S and E is examined to look for any stationary vehicles that might be involved in an accident.
3.	For every such suspected vehicle, the last five minutes of video are analysed to determine the car's speed(v) before to the collision. This speed v and a predetermined average vehicle mass (m) could be used to calculate the impact of a collision.
4.	By zooming in on the wrecked car or accident site, specific information is attempted to be captured, such as the likely number of injured and the vehicle owner's details.
5.	The closest hospitals and police station receive all the information right away for further rapid action.



