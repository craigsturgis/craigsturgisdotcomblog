---
layout: page
title: "Yet Another Website Rebuild: Wordpress to Octopress and more!"
date: 2013-08-21 22:59
comments: true
sharing: true
footer: true
---

For those of you bored or crazy enough to care about the process I went through to convert this website from Wordpress to Octopress plus the various other technical details about my new hosting situation that went into the process, consider this your lucky day!

Google is full of great blog posts and tutorials on getting up and running on Octopress, as well as on converting an existing Wordpress site. I ended up using a mishmash of the excellent official [Octopress documentation][1], and information distilled from a few different blog posts, chiefly [this overview][2] and portions of [this post][3] which had the best explanation of how to manage a separate git repository including your content but also pull in updates from the [main Octopress][4] repo. As someone relatively new to git, this was extremely helpful. It also introduced me to the [s3cmd][5] utilities which I have found useful at work even though I'm not deploying my site to S3. 

 [1]: http://octopress.org/docs/
 [2]: http://jason.pureconcepts.net/2013/01/migrating-wordpress-octopress/
 [3]: http://www.julianbonilla.com/blog/2012/11/05/octopress-on-amazon-s3/
 [4]: https://github.com/imathis/octopress
 [5]: http://s3tools.org/s3cmd

As for the content and design of the site, the content exports mostly went ok, but not well enough that I didn't have to spot check every post it converted for broken links and such. I wanted to footnote old posts anyway so this wasn't such a tragedy. It did take a good long while though. I settled on the [Whitespace][14] Octopress theme, with a few tweaks to my own taste. I replaced the default Google web fonts with [Source Sans Pro][15] served from [Adobe Edge Web Fonts][16] just to mix it up a bit. GWF also has it hosted there.

 [14]: https://github.com/lucaslew/whitespace
 [15]: http://blogs.adobe.com/typblography/2012/08/source-sans-pro.html
 [16]: http://html.adobe.com/edge/webfonts/

Why am I not deploying this site to S3 even though it would probably be dirt cheap? Flexibility. S3 does a lot of neat things now that make it good enough for a lot of static web content, but I prefer having the power of a full web server in case I want to use it. One major motivating factor in moving my sites was I wanted to get a [VPS][6] that I controlled completely anyway. 

  [6]: http://en.wikipedia.org/wiki/Virtual_private_server

I have had no complaints with my cheap Hostgator shared hosting that I've had for 6 years, but the variety of VPS options available at even cheaper prices made it hard to not switch, and there would be no reason to keep my shared hosting once I had a VPS with a web server on it.

I ended up settling on hosting with [Digital Ocean][7]. Their smallest "droplet" is more than adequately powered and has SSDs, at a whole $5/month instead of the $10/month my shared hosting cost. I added automatic backups at an extra $1/month.

 [7]: https://www.digitalocean.com/?refcode=c6a383baeacc

The one part of my previous shared hosting plan that wasn't taken care of easily in the VPS was email for my domains. After hearing a lot of people say good things about it, I took a flyer on a [Fastmail][8] Enhanced account, which has a killer web interface with keyboard shortcuts, imap, no ads, and the ability to add virtual domains and aliases easily. The enhanced account is $39 for a year. I've only used it for a short time, but I'm really impressed with it and am kicking around the idea of trying to import the contents of my gmail account- it's that good.

 [8]: http://www.fastmail.fm/?STKI=11493413

The part I had the most trouble with was getting the DNS records for the two domains set up correctly. I did take the opportunity while everything was moving around to move my domains to [Hover][9] which does a great job of having a good interface and not being sleazy like a lot of other domain registrars. I also made it difficult on myself by registering the vanity URL [csturg.is][10] which I had to purchase directly from Iceland's national registrar and use one of their approved list of approved Icelandic DNS providers. Luckily a guy had put together a very helpful [article][11] detailing the whole process. 39 Euros, a credit card hold, and A few A and MX records later and I was in business.

 [9]: https://hover.com/LOMlP7j5
 [10]: http://csturg.is
 [11]: http://web.peterhartree.co.uk/2012/how-to-register-an-icelandic-is-domain-name/

The .is domain is currently just a 302 redirect to the main site, but I plan at some point to install or fork / build a url shortener to put on the site, that and try and use it for email, although that may be short sighted since it's the domain with the highest degree of difficulty to maintain.

The VPS itself really just has [nginx][12] installed as its web server and that's about it for now, I'm going to try and keep it as lean and mean[^1] as I can.

 [12]: http://wiki.nginx.org/Main
 [^1]: AKA avoid installing php or any big web application packages.

The next big step is relaunching the band website as a static site. I don't need a platform like Octopress necessarily since there's not a lot of written content that gets generated, although it would be nice to edit the pages as markdown vs straight up html. 

Either way I think I'm going to use one of the free themes from [html5up][13] as a base and get something up even if it's not perfect. It never hurts to sharpen the CSS wrestling skills. 

 [13]: http://html5up.net/

 *(This page includes [referral links.][17])*

 [17]: /affiliate-links/