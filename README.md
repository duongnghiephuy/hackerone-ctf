# hackerone-ctf
Memo for ctf

## General techniques 
1. Look for url. Flag may be hidden there.
2.  Enumerate page with id parameter. There may be a page that you shouldn't have access to. (Automate to enumerate it). 
Sign: you create a page then some ids are skipped. 
4. Tamper input with XSS: script tag, img attribute. Stored XSS can affect other pages as well. Inspect element for flag. 
5. SQL injection on page id (get request). Test by inserting ' or ' OR '1' = '1. 
   If there is a different response, there is a chance that SQL injection is going to work.
6. SQL injection on input (post request). Similar test. Union strategy. 
   Post request here can be triggered from a click, scroll,...
   Similar test such as insert 1+1 to see if the expression is evaluated.
   Union strategy. 
   XLM injection is also great.. 
7. Blind SQL injection by sqlmap 
8. Perform get, post requests that are not supposed to be accessed by your current access level.
    Can combine with enumerating id.
10. Simple password cracking or tool 
11. Hidden input form. Tamper with post request body to server
12. Fixated session cookies (cookies = MD1 hash of the user id). Temper with cookies to sign in different accounts. 

