# Project 7 - WordPress Pentesting

Time spent: 8 hours spent in total

> Objective: Find, analyze, recreate, and document **three vulnerabilities** affecting an old version of WordPress

## Pentesting Report

1. (Required) Vulnerability Name or ID: Unauthenticated Stored Cross-Site Scripting (XSS) CVE-2015-3438
  - [X] Summary: 
    - Vulnerability types: XSS
    - Tested in version: 4.1.1
    - Fixed in version: 4.1.2
  - [X] GIF Walkthrough: https://imgur.com/a/7eWvQ
  - [X] Steps to recreate: Go to any post to make a comment. In the comment part, use the html tags. After the html tags, add your XSS script and when the user or admin view the comment, the script will run.
  - [X] Affected source code:
    - [Link](https://cedricvb.be/post/wordpress-stored-xss-vulnerability-4-1-2/)
  
2. (Required) Vulnerability Name or ID
  - [X] Summary: 
    - Vulnerability types: XSS
    - Tested in version: 4.1.1
    - Fixed in version: 4.1.2
  - [X] GIF Walkthrough: https://imgur.com/a/JgmBX
  - [X] Steps to recreate:  User admin privilege to enter the following harmful tags in a page or posting using the HTML edit mode:
  sometext\<a href="[caption code=">]\</a><a title=" onmouseover=alert('test')  ">link\</a>
  
  - [X] Affected source code:
    - [Link 1](https://klikki.fi/adv/wordpress3.html)
    
3. (Required) Vulnerability Name or ID: Authenticated Shortcode Tags Cross-Site Scripting CVE-2015-5714
  - [X] Summary: 
    - Vulnerability types:XSS
    - Tested in version: 4.1.1
    - Fixed in version: 4.1.6
  - [X] GIF Walkthrough: https://imgur.com/a/JgmBX
  - [X] Steps to recreate: Loged in as admin, make a post containing the following script
       XSS!!![caption width="1" caption='<a href="' ">]\</a>\<a href="http://onMouseOver='alert(1)'">Click me\</a>
       When the content is loaded, the harmful html tags will be filtered out but when we use nested tags, this filter will not work as expected, thus leaving out a backdoor for hackers.
  - [X] Affected source code:
    - [Link 1](https://wpvulndb.com/vulnerabilities/8186)
    - [Link 2](http://blog.checkpoint.com/2015/09/15/finding-vulnerabilities-in-core-wordpress-a-bug-hunters-trilogy-part-iii-ultimatum/)


## Assets

List any additional assets, such as scripts or files

## Resources

- [WordPress Source Browser](https://core.trac.wordpress.org/browser/)
- [WordPress Developer Reference](https://developer.wordpress.org/reference/)

GIFs created with [LiceCap](http://www.cockos.com/licecap/).

## Notes

Describe any challenges encountered while doing the work

## License

    Copyright [2017] [RONGFA LU]

    Licensed under the Apache License, Version 2.0 (the "License");
    you may not use this file except in compliance with the License.
    You may obtain a copy of the License at

        http://www.apache.org/licenses/LICENSE-2.0

    Unless required by applicable law or agreed to in writing, software
    distributed under the License is distributed on an "AS IS" BASIS,
    WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
    See the License for the specific language governing permissions and
    limitations under the License.
    
    
