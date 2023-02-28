Fish Transect Survey Analysis Protocol
Created by: Ian Combs (icombs@mote.org) 09/24/2021
Last Updated: Ian Combs 09/24/2021

------------------------------

Three video transects were captured at each site over three time periods 1 month and 12 months post-outplant.

Transects were captured using a GoPro Hero 5 shooting at 60fps and 1080p.

The camera was swam at a constant height ~1m from the bottom and a constant speed.

The diver waited ~5min between consecutive transects to allow fish to return after being disrupted by the diver's presence.

------------------------------
Video Processing

We are adapting video analysis methods from [Bacheler et al. 2013 ](https://www.sciencedirect.com/science/article/abs/pii/S0165783613000167?via%3Dihub).
However, since our videos are considerably shorter, we are taking more frequent stills.
Using the free software [FFmpeg](www.ffmpeg.org), we are extracting frames every 3 seconds.

We are using the following FFmpeg script to extract the stills.

ffmpeg -i "%i" -r 0.3 "%i_%03d.png"

Note: if you wish to batch process your videos, the following script will batch process all .MP4 videos in your folder.

for %i in (*.MP4) do ffmpeg -i "%i" -r 0.3 "%i_%03d.png"

Once stills are extracted each frame will be analyzed for fish.
