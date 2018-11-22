# wordpressvulns
Finding and exploiting vulnerabilities in wordpress websites.

Reflected Cross-Site Scripting
WordPress version: 4.2
"XSS-test1"

In this XSS exploit I was able to get a user’s cookie by creating a post using JavaScript.
By selecting Add New in the Posts section, JavaScript is allowed as an entry. I simply entered <body onload=alert(document.cookie)> in the title of the post. It didn’t matter what I entered in the main section of the post, because when the post is saved and the page reloads, a server-side alert is displayed containing the cookie.

"XSS-test2"

In this exploit, I demonstrate the same behavior when commenting on a post that is already created. 
In the Comments section, below a post, I typed the same JavaScript action: <body onload=alert(document.cookie)>
After posting the comment, the server error displays the cookie again.
  
"XSS-test3"

This test shows how more functonality of JavaScript is reflected in a post. I enter the syntax to display a botton, that triggers an alert when clicked. After, submitting the post and clicking on the screen, a server-side alert is displayed.


These are examples of reflected cross-site scripting because the JavaScript I entered is being reflected back to the the person viewing it.
