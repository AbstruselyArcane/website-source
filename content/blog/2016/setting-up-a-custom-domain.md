+++
date = "2016-09-16T17:20:46+08:00"
draft = false
tags = ["", ""]
title = "Setting Up a Custom Domain"
+++

Instead of doing my Calculus homework, I decided that it would be great idea to try setting up a custom domain for this website. Now that it is done, instead of doing said calculus homework, I'm going to write about setting up the custom domain! (Yes, calculus homework is really boring.)

### Buying a Domain

Buying a domain was pretty easy. I am using [Hover](https://hover.com/) as my registrar, which was highly recommended by my friends. The domain costs $14/year. Yes, there are cheaper prices, but I think the extra dollar or two per year is worth the nice UI and support. 

After creating A records pointing to Github's servers, and creating a CNAME file in Github, the DNS settings propagated to Google's DNS servers within a minute. Visiting [isaackhor.com](https://isaackhor.com/) navigated to the right location. However, I noticed something :

![Where's the SSL?](img/setting-up-a-custom-domain-nossl.png)

No HTTPS? Ok, I should be able to set a certificate somewhere...

### Setting up HTTPS

Google told me that I can either have encryption, or a custom domain, but not both. However, Google also presented me with a workaround: use [CloudFlare](https://cloudflare.com/). So, that's exactly what I did. After configuring everything on CloudFlare, I spent the next 5 minutes doing this (what calculus homework? I don't know what you're talking about):

    ~$ dig isaackhor.com +nostats +nocomments +nocmd

By the way, if you have a custom, local DNS cache, you should disable it. It took me a few minutes to realise that this was happening:

```
;; Query time: 8 msec
;; SERVER: 127.0.0.1#53(127.0.0.1)
;; WHEN: Fri Sep 16 17:58:47 2016
;; MSG SIZE  rcvd: 47
```

After changing DNS to 8.8.8.8, finally:

```
~$ dig isaackhor.com

; <<>> DiG 9.8.3-P1 <<>> isaackhor.com
;; global options: +cmd
;; Got answer:
;; ->>HEADER<<- opcode: QUERY, status: NOERROR, id: 49246
;; flags: qr rd ra; QUERY: 1, ANSWER: 2, AUTHORITY: 0, ADDITIONAL: 0

;; QUESTION SECTION:
;isaackhor.com.			IN	A

;; ANSWER SECTION:
isaackhor.com.		299	IN	A	104.27.147.99
isaackhor.com.		299	IN	A	104.27.146.99

;; Query time: 38 msec
;; SERVER: 8.8.8.8#53(8.8.8.8)
;; WHEN: Fri Sep 16 18:06:08 2016
;; MSG SIZE  rcvd: 63
```

Test isaackhor.com in the browser, everything works correctly. Final step: force all traffic to HTTPS:

![CloudFlare Page Rules](img/setting-up-a-custom-domain-cloudflare-pagerule.png)

Test in Chrome, yep, HTTPS works:

![HTTPS is working](img/setting-up-a-custom-domain-ssl.png)

Now, to get back to that calculus homework ... wait ... I can have custom email, don't I? Why don't I set it up right now?

To be continued ...