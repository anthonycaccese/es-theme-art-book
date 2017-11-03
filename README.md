# Art Book, an EmulationStation theme
A simple theme for Emulation Station and RetroPie based on the look of a coffee table book.  
Discussion is ongoing in this thread: https://retropie.org.uk/forum/topic/11728/new-theme-art-book

## Preview

### Video Walkthrough
https://www.youtube.com/watch?v=k_fKUiH_j-8

### Screenshots

*Detailed View*
![Detailed View](http://i.imgur.com/BVkhz56.png)

*Video View*
![Video View](http://i.imgur.com/7QDFPud.png)

*Basic View*
![Basic View](http://i.imgur.com/YH4oAci.png)

*System View*
![System View](http://i.imgur.com/VsXBB6E.png)

## Details

- Full list of supported systems: https://docs.google.com/spreadsheets/d/1gzaP0klzaBaE5_oB1_hQwr46qOmQnacSvSU3o-p5Q7U/edit#gid=0
- Has many custom themes as well - mario (Super Mario Bros), zelda (Legend of Zelda), megaman, etc... (see "custom themes" tab in the google doc above for the full list) 
- System, basic, detailed and video views are supported
- Support for new "All Games", "Favorites", "Last Played" and "Custom Collections" features in latest version of EmulationStation
- Displays rating, description, # of players, genre, publish date & last played metadata on detailed and video views
- 16x9 resolutions only (tested at 1280x720 and 1920x1080)
- Layout designed to support hardware accelerated OMX player on video views

## Acknowledgments

- System logos modified from the Carbom theme by Eric Hettervik
- Controller artwork created by Eric Hettervik from the Carbon theme (see: https://github.com/RetroPie/es-theme-carbon)
- ChangaOne font by Eduardo Tunni
- Static.mp4 default video from OldRoom theme by Nismo (see: https://retropie.org.uk/forum/topic/8019/oldroom-theme-w-i-p-new-1-9-beta-media-packs)

## Scraping 
using selph's scraper: https://github.com/sselph/scraper

### Arcade
- Run the following commands in an arcade system's folder (i.e. /roms/mame-libretro, /roms/fba): 
- First Scrape Flyers (from theGamesDB): /opt/retropie/supplementary/scraper/scraper -mame=true -mame_src=gdb,adb,ss -mame_img=fly,b,t,s -max_height=540 -max_width=394 -image_dir=media -image_path=media
- Then if you want Videos and Marquees (from ScreenScraper) run this: /opt/retropie/supplementary/scraper/scraper -mame=true -mame_src=ss,gdb,adb -download_videos=true -download_marquees=true -image_dir=media -image_path=media -video_dir=media -video_path=media -marquee_dir=media -marquee_path=media

### Console

- Run this command in a system's folder (i.e. /roms/nes): /opt/retropie/supplementary/scraper/scraper -console_src=ss -max_height=540 -max_width=505 -download_videos=true -download_marquees=true -image_dir=media -image_path=media -video_dir=media -video_path=media -marquee_dir=media -marquee_path=media -use_nointro_name=false 
- Other Notes: 
- If you only want images (no video/marquee) then you can modfiy the command to this: /opt/retropie/supplementary/scraper/scraper -console_src=ss -max_height=540 -max_width=505 image_dir=media -image_path=media -use_nointro_name=false 
- If you want higher quality art, add -img_format=png to the end of the command (that will download pngs instead of jpgs but will also result in larger filesizes - which may add lag if you are on a pi0)

### Game & Watch

- Run this command in the /roms/gameandwatch folder: /opt/retropie/supplementary/scraper/scraper -console_src=ss -console_img=clabel,b,s -img_format=png -max_height=540 -max_width=505 -image_dir=media -image_path=media
