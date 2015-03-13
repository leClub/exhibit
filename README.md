# Exhibit

Beats of code to run things on exhibition

## Read video with Pi

### Convert video to H264

    sudo apt-get install ffmpeg
    ffmpeg -i input_file.avi -vcodec copy -an -bsf:v h264_mp4toannexb video.h264


## Play video with Omxplayer
 
Play without GUI from the command-line in Command (using GPU)

    omxplayer -p -o hdmi video.mp4

### Launch on start

http://www.cenolan.com/2013/03/looping-video-playlist-omxplayer-raspberry-pi/

    cd ~
    git clone https://github.com/leClub/exhibit.git
    mkdir videos 
    # copy the videos in the videos rep

add this line to your ```/etc/rc.local``` to autostart

    /home/pi/videoplayer.sh

You can control the video with OMX Player commands

    1 Increase Speed
    2 Decrease Speed
    j Previous Audio stream
    k Next Audio stream
    i Previous Chapter
    o Next Chapter
    n Previous Subtitle stream
    m Next Subtitle stream
    s Toggle subtitles
    q Exit OMXPlayer
    Space or p Pause/Resume
    - Decrease Volume
    + Increase Volume
    Left Seek -30
    Right Seek +30
    Down Seek -600
    Up Seek +600
