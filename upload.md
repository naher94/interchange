---
layout: default
title: Upload
---
# Introduction

Hello SoA graduate student. Welcome to the Interchange upload page. This page will give you all you need to know about submitting your work.

Each student can submit upto 4 projects. There will be a curation process for all submitted work. If any project submission a profile will be required. Every student may have a profile without the requirment of any projects.

Deadline for submission is **Jan 30th 11:59pm**
# Getting Started

Download the file structure template [here](/img/template.zip).
Upload your .zip to the [dropbox](https://goo.gl/forms/Ia76PNelAHKoNRlx1).

# The Meat

## Profile 

For the companies to learn a little about you.

### Requirements

* Headshot
* Biography (100 word limit)
* Program Affiliation (ie. MTID, MSCD)
* Graduation Month & Year

### Optionals

* Resume (PDF)
* Goal / One Liner "what kind of position are you looking for?"
* Personal Portfolio Link

### Other Stuff

This is what the profile file looks like (andrewCarnegie.markdown)
Make sure to update all fields and the main section. For the optional fields if you would like to opt out please delete that line. Make sure to conform to the format below: program as an abbreviation `MAAD`,`MSAECM`,`MSBPD`,`MSSD`,`MTID`,`MSCD` and `MUD`, graduation as `YYYY-MM-DD`, no worries if you don't know the exact day, leave it at `15` if unknown and make sure to match casing `Andrew Carnegie` **not** `andrew carnegie`.

```
---
layout: people
title:  "Andrew Carnegie"
thumbnail: "andrewCarnegie.png"
program: "MTID"
graduation: 2017-12-15

resume: "andrewCarnegie.pdf"
website: "andrewcarnegie.com"
goal: To obtain a full-time position that will help me to awesome stuff and this and that.
---

This is where your bio goes. Etiam lacinia, lectus quis sollicitudin ultrices, lacus tellus feugiat ante, pharetra congue mauris nunc id felis. Nullam porta nisi eu lorem finibus, sed rutrum sapien fringilla. Nullam elit ante, sagittis sed volutpat ut, hendrerit vitae urna. Curabitur tincidunt dolor odio. Maecenas quis enim dictum risus lobortis viverra eget at leo. Vivamus turpis erat, vehicula id elit et, luctus imperdiet diam. Donec vitae dui gravida, placerat sapien a, tempus lacus. Curabitur aliquam purus et eros accumsan, sed luctus dui gravida. Vestibulum vel eros felis. Proin eget dictum erat. Ut augue arcu, sodales eget.
```

## Projects

For the companies to see what you do. Keep in mind that these should be easy to ready through.

### Requirements

* Title
* Completion Month & Year
* Hero Image
* Short Description (100 word limit)
* Tile Image
* Body Content
  * Text
  * Video (Embed code from [Youtube](https://support.google.com/youtube/answer/171780?hl=en) or [Vimeo](https://help.vimeo.com/hc/en-us/articles/224969968-Embedding-videos-overview))
  * Images (See File Requirements)
  * Links (`[The Clicable](http://link.com)`)
  * Code (Github links or [MarkDown Styling](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet#code))
  
### Other Stuff

This is what a project file looks like. Named `projectName-intials.markdown` just like the project folder. Make sure to conform to the formatting below including casing `Andrew Carnegie` **not** `andrew carnegie`. Again data is `YYYY-MM-DD`. `tile-name` is to give a peak at the project before clicking it, generally better to make this slightly generic `Photoshop Plugin` over `Pixel Scaling Function`. Tags are a good way to help people find your project. Tags are space seperated. Here is a list of tags available to you.

* tag
* tag2
* tag3
* tag4

```
---
layout: post
title:  "Project Name"
tile-name: "Photoshop Plugin"
thumbnail: "coLab-rb.png"
author: "Andrew Carnegie"
date:   2016-03-01

tags: digital branding
---

![Hero Image](/img/projectName-ac/hero.png)

Your short description goes here. 100 word max.

this is what an image looks like
![2 Word Image Description](/img/projectName-ac/thisImage.png)

this is what a video embed looks. please update width to be `100%` and height to be `600` otherwise it will break on mobile devices.

<iframe width="100%" height="600" src="https://www.youtube.com/embed/IdneKLhsWOQ" frameborder="0" allowfullscreen></iframe>

and this is how you include a link into stuff [link](http://cmu.edu). want to see where the link goes?

```

## File Requirements

| Item           | File Format          | Dimensions               | File Size Maximum | Naming Convension |
| -------------- | -------------------- | ------------------------ | ----------------- | ----------------- |
| Headshot       | PNG                  | 470px **x** 470px        | 400 KB | firstLast.png ([Lower Camel Case](http://wiki.c2.com/?LowerCamelCase))|
| Tile Image     | PNG                  | 500px **x** 375px        | 400 KB | projectName-ab.png (lowerCamelCase-initials.png) |
| Hero Image     | PNG                  | ???px **x** ???px        | 1 MB   | hero.png |
| All Other Image| PNG or GIF (animated)| <=1400px **x** <=1400px  | 1 MB   | lowerCamelCase.png or lowerCamelCase.gif |
| Resume         | PDF                  | 8.5 **x** 11 recommended | 1 MB   | firstLast.pdf |


## File Structure

```
andrewid.zip
├── headshot.png
├── resume.pdf
├── profile.markdown
├── project1
│   ├── project1.markdown
│   ├── tileImage.png
│   ├── hero.png
│   ├── thisImage.png
│   └── thatImage.gif
```

# Extras

If you need help reducing the file size check out an image optimzers [ImageOptim](https://imageoptim.com) for mac & [XnView](http://www.xnview.com/en/) for windows machines.

if you want to render markdown in the browser check out [Dillinger](http://dillinger.io) & if you want to know the syntax check [here](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet).

If you feel like making other changes to **your** pages while maintaining the style of the site, feel free to submit a pull request over at the GitHub [repo](https://github.com/naher94/interchange). The site is build using [Jekyll](https://jekyllrb.com). If you need some help setting it up check out this [tutorial](https://dzgn.io/wdw.html). Here is another [tutorial](https://scottylabs.org/portfolio/) focused on general web developement. Happy Building! <span class="emoji emoji-party"></span> <span class="emoji emoji-wrench"></span>
