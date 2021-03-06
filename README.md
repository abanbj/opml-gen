# opml-gen
## What is it and what does it do?
Tiny util to construct OPML files for use with the Overcast podcast player. A util like this doesn't exist (I think?), so I made one. All you need is the podcast URL. Feed it to opml-gen and voila; you're own cooked OPML file, just for you.

## Short description
The opml format is simple. It consists basically of some header lines and one line per podcast/entry. That means that the file sie will vary depending on how many podcasts you subscribe to.

### Example files
This shows an exmaple of an opml file that I exported from my iPhone. It shows the header and three lines between the ```<body></body>``` tags; i.e. I'm subscribing to three podcasts.

```
<?xml version="1.0"?>
<opml version="1.0">
<head>
<title>Overcast Podcast Subscriptions</title>
</head>
<body>

<outline type="rss" text="Ekko" title="Ekko" xmlUrl="http://podkast.nrk.no/program/ekko_-_et_aktuelt_samfunnsprogram.rss" htmlUrl="https://radio.nrk.no/serie/ekko-hovedsending"/>
<outline type="rss" text="Abels t&#xE5;rn" title="Abels t&#xE5;rn" xmlUrl="http://podkast.nrk.no/program/abels_taarn.rss" htmlUrl="https://radio.nrk.no/serie/ekko"/>
<outline type="rss" text="Security Now (MP3)" title="Security Now (MP3)" xmlUrl="http://feeds.twit.tv/sn.xml" htmlUrl="https://twit.tv/shows/security-now"/>

</body>
</opml>
```

So there are 5 paramteres that need to be set for each podcast; ``outline type``, ``text``, ``title``, ``xmlUrl`` and ``htmlUrl``

For more info about the OPML format, see [Wikipedia](https://en.wikipedia.org/wiki/OPML).

## How do I use it?
Add the URL to the podcasts you want to subscribe to. Send the generated OPML file to yourself in an email and send to/open with Overcast.
