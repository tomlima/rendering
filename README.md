
# Rendering process  

## A brief description of how rendering process works




- Browser request an HTML page to the web server.
- Webserver response with an HTML page.
- Browser starts a parse step ( transform data received into DOM and CSSOM ).
- Render engine creates a Tree render from DOM and CSSOM. 
- Starting layout and painting step. 


## Notes

- Browsers are optimized to avoid repainting the UI whenever they can. If the browser finds a CSS file, it keeps downloading stuff but stops rendering until the CSS file is downloaded and parsed. 
 

- If the browser finds a JavaScript file, it stops rendering and stops downloading other files. Because JS can add and remove elements from the UI, the browser wants to know what the final layout is before continuing. 

- Waiting to obtain CSS doesn't block HTML parsing or downloading, but it does block JavaScript, because JavaScript is often used to query CSS properties' impact on elements.


## Recomendations

- Use fonts in WOFF 2.0 format 
- Preload fonts ( good when LCP candidate is a text node )   
- Split javascript in chunks and priorate the critical ones.


## References

[Fetch Prioritization](https://docs.google.com/document/d/1bCDuq9H1ih9iNjgzyAL0gpwNFiEP4TZS-YLRp_RuMlc/edit)

[Async vs Defer vs Preload vs Server Push](https://webspeedtools.com/async-vs-defer-vs-preload-vs-server-push/)

[How browsers work](https://developer.mozilla.org/en-US/docs/Web/Performance/How_browsers_work)

[How browsers work](https://developer.mozilla.org/en-US/docs/Web/Performance/How_browsers_work)


