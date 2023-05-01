It is a sequence of steps a browser takes to convert HTML from server into a workink web page.

1. **Browser requests** web page from server
2. **Server returns HTML**
3. Browser starts **parsing** the recieved HTML
	1. Split content into tokens (by tags)
	2. Convert tokens to nodes
4. If it encounters links to external resources, it **makes new requests**
	1. Blocking requests set parsing of HTML on pause: external script, `<script>`
	2. Not blocking requests made behind the scenes: image, css, ...
5. Building of **[[DOM]]**
6. Once DOM is ready, browser creates **[[CSSOM]]** 
> [!info] 
> Building CSSOM blocks render because css rules may override each other
7. DOM + CSSOM = **[[Render Tree]]**
   > [!info]
   > Render Tree only captures visible content
8. **Layout** determines where and how the elements are positioned on the page, determining the width and height of each element, and where they are in relation to each other.
   >[!info]
   >Layout repeats every time render tree changes
9. **Painting** pixels to the screen
	1. Whole screen paints on load
	2. After that only needed pieces get re-painted

[CRP](https://developer.mozilla.org/en-US/docs/Web/Performance/Critical_rendering_path)
[CRP Medium](https://medium.com/jspoint/how-the-browser-renders-a-web-page-dom-cssom-and-rendering-df10531c9969)
[CSS triggers](https://csstriggers.com/)

#CSP #rendering #DOM #CSSOM #renderTree