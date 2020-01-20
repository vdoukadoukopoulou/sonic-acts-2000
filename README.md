# sonic-acts-2000

Intiall attempt into piecing together a sonic acts website using infromation from the wayback machine

To assemble the website, this attempt makes use of the [Wayback Machine Downloader](https://github.com/hartator/wayback-machine-downloader)

it is  good to remember that Wayback Machine, archives sites incrementally, so if you have have to check when a page was archived by looking into the timestamp , do another download request and then assemble the website manually.
timestamps appear on the webarchive URL formatted as YYYYMMDD (YEARMONTHDATE) followed by the site URL

Example:

`https://web.archive.org/web/20011221121908/http://www.interfaculty.nl/sonicacts.com/00/index.html`

So in this example, `http://www.interfaculty.nl/sonicacts.com/00/index.html` was archive on 2001/11/22 

To navigate the website please click the blocks of the space invader gif
published at https://vdoukadoukopoulou.github.io/sonic-acts-2000/


when confronted with a lot of individual paths to image files make an automate bash script to speed up the process.
collect all the relevant url from the capture form info
make a `.sh file`

```#!/bin/bash
url=('http://www.individuallink/here/picture.jpg'
'http://www.individuallink/here/picture.jpg'
'http://www.individuallink/here/picture.jpg')

for i in "${url[@]}"; do
wayback_machine_downloader $i
done
