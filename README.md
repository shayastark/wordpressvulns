# wordpressvulns
Finding and exploiting vulnerabilities in wordpress websites.

WordPress version: 4.2

In this XSS exploit I was able to get a user’s cookie by creating a post using JavaScript.
By selecting Add New in the Posts section, JavaScript is allowed as an entry. I simply entered <body onload=alert(document.cookie)> in the title of the post. It didn’t matter what I entered in the main section of the post, because when the post is saved and the page reloads, a server-side alert is displayed containing the cookie.
