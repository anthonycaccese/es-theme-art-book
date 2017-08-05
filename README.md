# Art Book, an EmulationStation theme (WIP)
A simple theme for Emulation Station and RetroPie based around the look of a coffee table book.  
Discussion ongoing in this thread: https://retropie.org.uk/forum/topic/11728/new-theme-art-book

## Preview

### Screenshots

*Detailed View*
![Detailed View](http://i.imgur.com/45WMfc3.png)

*Video View*
![Video View](http://i.imgur.com/rjfopnF.png)

*Basic View*
![Basic View](http://i.imgur.com/YH4oAci.png)


## Details

- Has support for system, basic, detailed and video views
- Support for new All Games, Favorites, Recently Played and Custom Collections in latest version of Emulation Station
- Displays the following metadata on detailed and video views: rating, description, # of players, genre, publish date & last played
- 16x9 resolutions only (tested at 1280x720 and 1920x1080)
- Layout designed to support hardware accelerated OMX player on video views
- Has SMB (Super Mario), TLOZ (Legend of Zelda) and Megaman custom systems

## Acknowledgments

- Inspired by old console poster designs (see: http://imgur.com/J4eeTun and http://imgur.com/Ut0SWfJ for examples) 
- All Logo graphics are from the default Carbom theme made by Eric Hettervik (see: https://github.com/RetroPie/es-theme-carbon/)
- Static.mp4 default video from OldRoom theme by Nismo (see: https://retropie.org.uk/forum/topic/5823/looking-for-testers-for-es-video-preview-on-raspberry-pi/20)
- Video support possible because of work done by fieldofcows (see: https://retropie.org.uk/forum/topic/4820/video-preview-in-emulationstation)
- Theme tutorial written by mattrixk was a huge help in learning how to build this (see: https://github.com/RetroPie/RetroPie-Setup/wiki/Creating-Your-Own-EmulationStation-Theme)

## Scraping

### Arcade

- First Scrape Flyers (from GDB): /opt/retropie/supplementary/scraper/scraper -mame=true -mame_src=gdb,adb,ss -mame_img=fly,b,t,s -max_height=540 -max_width=394 -image_dir=media -image_path=media

- Then Scrape Videos and Marquees (from SS): /opt/retropie/supplementary/scraper/scraper -mame=true -mame_src=ss,gdb,adb -download_videos=true -download_marquees=true -image_dir=media -image_path=media -video_dir=media -video_path=media -marquee_dir=media -marquee_path=media

### Console

- First Scrape Media: /opt/retropie/supplementary/scraper/scraper -console_src=ss -max_height=540 -max_width=505 -download_videos=true -download_marquees=true -image_dir=media -image_path=media -video_dir=media -video_path=media -marquee_dir=media -marquee_path=media

- Then Scrape Clean Names: /opt/retropie/supplementary/scraper/scraper -use_nointro_name=false -strip_unicode=true -download_videos=true -download_marquees=true -image_dir=media -image_path=media -video_dir=media -video_path=media -marquee_dir=media -marquee_path=media

### Game & Watch

- Run this command in the /roms/gameandwatch folder: /opt/retropie/supplementary/scraper/scraper -console_src=ss -console_img=clabel,b,s -img_format=png -max_height=540 -max_width=505 -image_dir=media -image_path=media
