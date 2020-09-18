## What is Mixed content block and how can we create a proxy server?

Hi everyone, recently I have encountered a problem when working on a react project. I created the project with a basic login and a dashboard page. I have deployed it to Heroku, now started to test in my browser visiting the URL and entering the login credentials there got an error alert on my login screen then went to developer tools and checked what is the error in the network tab.

I got these two errors in dev tools saying mixed content block restricted.

* Network tab errors

![image.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1600445970241/JRGT7Rbky.png)

* Browser console errors

![image.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1600445836036/IBxZz56HR.png)





* Now I began to wonder what is a mixed content block, I have never encountered it till now, so began to search what is it in [MDN](https://developer.mozilla.org/en-US/) as it is the best where can find answers about any issue related to web applications. I will explain the gist of it now.


* What is Mixed content block?

> When a user visits a page served over HTTPS, their connection with the webserver is encrypted with TLS and is therefore safeguarded from most sniffers and man-in-the-middle attacks. An HTTPS page that includes content fetched using cleartext HTTP is called a mixed content page. Pages like this are only partially encrypted, leaving the unencrypted content accessible to sniffers and man-in-the-middle attackers. That leaves the pages unsafe.

* There are two types of mixed content blocks here :

1.**Mixed passive/display content:**

Mixed passive/display content is content served over HTTP that is included in an HTTPS webpage, but that cannot alter other portions of the webpage.

* **Passive content list**

This section lists all types of HTTP requests which are considered passive content:

   * `<img>`(src attribute)
   * `<audio>`(src attribute)
   * `<video>`(src attribute)
   * `<object>`subresources (when an <object> performs HTTP requests) 

2.**Mixed active content:**

Mixed active content is content that has access to all or parts of the Document Object Model of the HTTPS page. This type of mixed content can alter the behavior of the HTTPS page and potentially steal sensitive data from the user. Hence, in addition to the risks described for mixed display content above, mixed active content is vulnerable to a few other attack vectors.

* **Active content examples**

This section lists some types of HTTP requests which are considered active content:

* `<script>`(src attribute)
* `<link>`(href attribute) (this includes CSS stylesheets)
* `<iframe>`(src attribute)
* `XMLHttpRequest` requests
* `fetch()` requests
* All cases in CSS where a `<url>` value is used (`@font-face`,`cursor`, `background-image`, and so forth).
* `<object>`(data attribute)
* `Navigator.sendBeacon` (url attribute)

Here I got problem mainly due to my backend server having HTTP IP Adress and the browser is blocking the HTTP calls due to MIxed content.

For this type of errors, we can create a proxy for our IP address. Now what happens is we make a request from the browser it calls our HTTPS proxy address that in turn calls an HTTP address. This works perfectly because the browser will only know that we are calling HTTPS to HTTPS it won't know the other HTTP call we are making from the proxy server.

* Now we can create a simple proxy server using these 

* create a `package.json` using `npm init` command 

* Now install an npm package called [http-proxy npm package](https://www.npmjs.com/package/http-proxy). 

* create a `server.js` file write the following code

```
const http = require("http");
const httpProxy = require("http-proxy");

const PORT = process.env.PORT || 8080;
httpProxy.createProxyServer({ target: "http://139.XX.0.96:XXX" }).listen(PORT);

```

* Now run the server using `node server.js`.

* Now our proxy server is ready. we can request any type of request from our local to sever to the HTTP server.

* we can deploy either in AWS or Heroku or any other platform. we can use that server IP to call our HTTP address.

### References 

MDN Docs links: 

https://developer.mozilla.org/en-US/docs/Web/Security/Mixed_content/How_to_fix_website_with_mixed_content

https://developer.mozilla.org/en-US/docs/Web/Security/Mixed_content

NPM package link : 

https://www.npmjs.com/package/http-proxy

> If you have any doubts related to this article or anything related to tech or software-engineering in general, drop a comment here or you can message me on twitter [@ksridhar02](https://twitter.com/ksridhar02).
  

