# WebSecurityWeek7And8
Project 7 - WordPress Pentesting
Time spent: **5** hours spent in total

> Objective: Find, analyze, recreate, and document **five vulnerabilities** affecting an old version of WordPress

## Pentesting Report

1. WordPress => 4.2 – Authenticated stored Cross-Site Scripting (XSS)
  - [X] Summary: 
    - Vulnerability types:XSS
    - Tested in version:4.2
    - Fixed in version: 4.3
  - [X] GIF Walkthrough: 
  ![XSS](https://github.com/shahan27/WebSecurityWeek7And8/blob/master/firstExample.gif)
  
  - [X] Steps to recreate: Make a new post >> Write the following javascript"<script type="text/javascript">alert("Your text goes here");</script>" Publish it >> Then view to post!
 
2. WordPress =>2.5 – 4.6 - Authenticated Stored Cross-Site Scripting (XSS) via Image frame 
  - [X] Summary: 
    - Vulnerability types:XSS
    - Tested in version:4.2
    - Fixed in version: 4.6.1
  - [X] GIF Walkthrough: 
  ![XSS2](https://github.com/shahan27/WebSecurityWeek7And8/blob/master/secondExample.gif)
  
  - [X] Steps to recreate: Upload a new image to the library >> Then click on that image >> Then in the title section, add the following JavaScript "<IMG SRC="#" ONERROR="alert('HACKED HACKED HACKED')"/>" Then clck next to the image name.
 
3. (Required) WordPress  4.0-4.7.2 - Authenticated Stored Cross-Site Scripting (XSS) in YouTube URL Embeds
  - [X] Summary: 
    This vulnerablity allows remote attackers to inject arbitrary web script or HTML via video URL in YouTube emebeds. infected code runs when the page is rendered.
    - Vulnerability types: XSS
    - Tested in version: 4.2
    - Fixed in version: 4.6
  - [X] GIF Walkthrough: 
![xss2_embeddedlink](https://github.com/shahan27/WebSecurityWeek7And8/blob/master/thirdExample.gif)  
- [X] Steps to recreate: 
        Create a new page in WP and add the code in page's body. Code will be execcuted when page is rendered.
    ```[embed src='https://youtube.com/embed/testtestest\x3csvg onload=alert(1)\x3e'][/embed]```
  - [x] Affected source code:
    - [Link 1](http://wpdistillery.dev/?page_id=43)
  
## Assets

Just used gifs to record examples 

## Resources

- [WordPress Source Browser](https://core.trac.wordpress.org/browser/)
- [WordPress Developer Reference](https://developer.wordpress.org/reference/)

## Notes

Describe any challenges encountered while doing the work.

Challenges faced during this work was the amount spent on setting up vagrant and having to switch between both Vm and Os terminals. 

## License

    Copyright [Spring 2019] [Shahan Rahman]

    Licensed under the Apache License, Version 2.0 (the "License");
    you may not use this file except in compliance with the License.
    You may obtain a copy of the License at

        http://www.apache.org/licenses/LICENSE-2.0

    Unless required by applicable law or agreed to in writing, software
    distributed under the License is distributed on an "AS IS" BASIS,
    WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
    See the License for the specific language governing permissions and
    limitations under the License.
