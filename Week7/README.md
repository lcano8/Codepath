# Project 7&8 - WordPress Pentesting

Time spent: 10 hours spent in total

> Objective: Find, analyze, recreate, and document **three vulnerabilities** affecting an old version of WordPress

## Pentesting Report

1. Authenticated Stored Cross-Site Scripting via Image Filename
  - [ ] Summary: Title of file image is not well sanitized.
    - Vulnerability types:Stored XSS
    - Tested in version:4.2
    - Fixed in version: 4.2.10
  - [ ] GIF Walkthrough: 
    - [Link 1](https://github.com/lcano8/Codepath/blob/master/Week7/Authenticated%20Stored%20Cross-Site%20Scripting%20via%20Image%20Filename.gif)
  - [ ] Steps to recreate: 
  - Download a JPG file (any picture).
  - Upload file onto media tab.
  - Rename file to <img src=a onerror=alert('*')>, fill in '' with desired result.
  - After an admin clicks on the image, the result should show as a GIF.
  - [ ] Affected source code:
    - [Link 1](https://core.trac.wordpress.org/browser/tags/version/src/source_file.php)
    - [Link 2](https://sumofpwn.nl/advisory/2016/persistent_cross_site_scripting_vulnerability_in_wordpress_due_to_unsafe_processing_of_file_names.html1)
 
 2.Authenticated Cross-Site Scripting (XSS) via Media File Metadata
  - [ ] Summary: The audio file contains javaspcript
    - Vulnerability types: Stored XSS
    - Tested in version: 4.2
    - Fixed in version: 4.2.13
  - [ ] GIF Walkthrough: 
    - [Link 1](https://github.com/lcano8/Codepath/blob/master/Week7/Media%20File%20Metadata.gif)
  - [ ] Steps to recreate: 
  - Download mp3 file on browser (Google chrome).
  - Upload under media file the audio file that has been downloaded.
  - After an admin clicks on it, the result should show the javascript.
  - [ ] Affected source code:
    - [Link 1](https://core.trac.wordpress.org/browser/tags/version/src/source_file.php)
    - [Link 2](https://www.securify.nl/advisory/SFY20160742/) 
    - [Link 3](https://securify.nl/advisory/SFY20160742/xss.mp3)
3. 4.2 - Unauthenticated Stored Cross-Site Scripting (XSS) 
- [ ] Summary: 
    - Vulnerability types:
    - Tested in version: 4.2
    - Fixed in version: 4.2.1
  - [ ] GIF Walkthrough: 
  - [ ] Steps to recreate: 
  - [ ] Affected source code:
    - [Link 1](https://core.trac.wordpress.org/browser/tags/version/src/source_file.php)
    - [Link 2](https://packetstormsecurity.com/files/131644)
    ## Assets

List any additional assets, such as scripts or files

## Resources

- [WordPress Source Browser](https://core.trac.wordpress.org/browser/)
- [WordPress Developer Reference](https://developer.wordpress.org/reference/)

GIFs created with [LiceCap](http://www.cockos.com/licecap/).

## Notes

WPscan can be broad and not provide enough information to understand exploits.
It might require additional researching to complete some of the exploitations.

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
