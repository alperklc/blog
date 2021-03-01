---
date: "2018-02-23T14:20:00Z"
tags:
  - nodejs
  - censorship
  - proxy
title: Bypass internet filtering by building your own tiny proxy server
---

The project is called [your-own-personal-proxy](https://github.com/alperklc/your-own-personal-proxy). I started coding this 10 days ago. There are actually solutions for users living in the countries where internet is censored. Either free or paid, there are always risks when it comes to privacy, while surfing behind a tunnelling website or any kind of VPN service. Rolling your own solution might be the safest, unless cloud provider is not sharing the data of users.

The repository includes a nodejs application which is designed for tunneling the traffic between server and the client. It works, once it's deployed in the cloud environment. Works out of the box, once it's deployed on Heroku.

Tested in Turkey by browsing the Wikipedia, so it works!

**Usage**
`node index.js` or `npm run start` will run the proxy server.

If you browse the url where proxy server is deployed, you will see a straightforward index page.
![-](/content/images/2018/03/-.png)

Or the desired website could be browsed through the proxy by altering the url parameter at the end of URL: `https://[YOUR-OWN-PROXY-SERVER-URL]/?url=[URL_OF_DESIRED_WEBSITE]`

Proxy server is also rendering a minimal banner on the top in every page it brings to the client, where user can type the URL of the website to browse.

**Current Capabilities**

- Altering targets of all relative links on the page for providing them behind the proxy, by using the library [JSDOM](https://www.npmjs.com/package/jsdom).
  E.g: `/posts/{post-id}` => `https://[YOUR-OWN-PROXY-SERVER-URL]/?url=[URL_OF_DESIRED_WEBSITE]/posts/{post-id}`

  ```
  const replaceLinks = (links, rootUrl) => {
    links.forEach(link => {
      const isRelativeLink = link.href.charAt(0) === '/'
         link.href = isRelativeLink ? `/?url=${rootUrl}${link.href}` : `/?url=${link.href}`
    })

    return links
  }
  ```

- Logging access information and errors in .log files.

**Future ideas**

- Beautifying the templates and code.
- Caching feature.
- Downloading CSS files and page scripts from CDNs or asset servers and embedding them within the `<head>` of HTML files. Currently it's displaying websites without styles.

I'm inviting everyone to hack with this. Pull requests are welcomed.
