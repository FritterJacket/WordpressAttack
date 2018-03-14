# Project 7 - WordPress Pentesting

Time spent: 20 hours spent in total

> Objective: Find, analyze, recreate, and document **three vulnerabilities** affecting an old version of WordPress

## Pentesting Report

1. XSS in Comments
  - [ ] Summary: Any js command will execute when put into the Comment section of any page 
    https://www.youtube.com/watch?v=UD-iwqphWlk 
  - [ ] GIF Walkthrough:https://github.com/FritterJacket/WordpressAttack/blob/master/GIF%20of%20XSS.gif 
  - [ ] Steps to recreate: Just open up the wordpress website and input javascript commands into a comment. Once the comment is posted it will execute
  - [ ] Screenshots: https://github.com/FritterJacket/WordpressAttack/blob/master/XSS.PNG
                     https://github.com/FritterJacket/WordpressAttack/blob/master/XSSinComments.PNG
2. Authenticated Cross-Site Scripting (XSS) via Media File Metadata*
  - [ ] Summary: JavaScript code can be put in an mp3 file and uploaded to the website. When the site attempts to play the mp3 file, it will execute the code instead.
  - [ ] GIF Walkthrough: https://github.com/FritterJacket/WordpressAttack/blob/master/GIF%20of%20MediaFiles.gif
  - [ ] Steps to recreate: Create a text file that includes a javascript script that exexcutes the commands you want. Then save that file as an mp3 file. Edit a post on the site and add the mp3 file as a media element. When the mp3 attempts to play, it will execute the script.
3. Authenticated Shortcode Tags Cross-Site Scripting (XSS)*
  - [ ] Summary: JavaScript scripts can be put in the title of a post. The script will be executed when it's conditions are met 
  - [ ] GIF Walkthrough: https://github.com/FritterJacket/WordpressAttack/blob/master/GIF%20of%20PostTitle.gif
  - [ ] Steps to recreate: Create a new post. Set the title as some kind of javascript script. Wait for it to execute.
    

## Assets



## Resources

- [WordPress Source Browser](https://core.trac.wordpress.org/browser/)
- [WordPress Developer Reference](https://developer.wordpress.org/reference/)

GIFs created with [LiceCap](http://www.cockos.com/licecap/).

## Notes
  *I was not able to get either 2 or 3 to function on my machine. I was working with other students in this class and we got these exploits to work on theirs but couldn't figure out why it would work on mine. I included descriptions of each one and how to duplicate as well as a GIF of me attempting and failing to get it to execute.


## License

    Copyright [yyyy] [name of copyright owner]

    Licensed under the Apache License, Version 2.0 (the "License");
    you may not use this file except in compliance with the License.
    You may obtain a copy of the License at

        http://www.apache.org/licenses/LICENSE-2.0

    Unless required by applicable law or agreed to in writing, software
    distributed under the License is distributed on an "AS IS" BASIS,
    WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
    See the License for the specific language governing permissions and
    limitations under the License.
