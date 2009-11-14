# server side google analytics

!SLIDE
# web analytics
* web beacon type
    * urchin
    * site catalist
    * visionalist
    * google analytics
* server log type
    * basicly apache-log
        * analog
        * awstats
        * (urchin)
* packet caputure type
    * rtmetrics

!SLIDE
# google analytics

good analize web access

but only javascript

so this cannot anallize mobile sites

(because mobile phone disable javascipt)

!SLIDE
# mobile sites

apache-log analize

OR

unoficaily google analytics server side

(because google say "DO NOT USE REVERSE ENGINIERING")

* http://eos.exbridge.jp/projects/show/ga4k
* http://it.kndb.jp/entry/show/id/2376

!SLIDE

# google show snipet!

* [google analytics blog](http://analytics.blogspot.com/2009/10/google-analytics-now-more-powerful.html)
* [google zip file](http://www.google.com/analytics/googleanalyticsformobile.zip)
* [import to github](http://github.com/sanemat/ga4m)

!SLIDE

# excited!

!SLIDE

# too bad php snipet...

!SLIDE

# perl script

I understand perl a bit but

* use strict pragma
* use cpan modules

!SLIDE

# php script

* use global namespace
* use global function
* use global valiables
* send http header automaticaly
* ...

!SLIDE

# search BETTER

i search server-side php script

inspired this

* source-forge
* github

but i do not hit yet

so please tell me!

!SLIDE

# these server-side google analytics is slow?

javascript version works after page rendering

server-side one is before page rendering

!SLIDE
# use task-queue system?

use queue only push before page render

and other server read queue

and send request for google analytics server

## but it is hard to cookie tracking

!SLIDE

# what's a better idea?

