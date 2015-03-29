## Website Performance Optimization portfolio project

Matt Holloway's project 4

Part 1: Index.html (all scrores shown for mobile, desktop scored better)
------------------------------------------------------------------------
 - set the javascript to async, to prevent blocking
 - optimized the images using Kraken.io (https://kraken.io/web-interface), the page speed got to a score of 86
 - changed the font loading, moved the css to inline, to prevent render blocking, got to a score of 88
 - used grunt with cssmin, uglifier and htmlmin to minify the JS, CSS and HTML, got to a score of 93

Part 2: Pizza.html (main.js optimization)
-----------------------------------------
 - watched Google Developers video (https://www.youtube.com/watch?v=BaneWEqNcpE), starting around 18:27
    - This gave insight into the FPS component of the project, which lead me to put the document.body.scrollTop into a variable, rather than query for it continuously in the loop
    - Also, the https://www.igvita.com/slides/2012/devtools-tips-and-tricks/jank-demo.html site referenced in the code had given insight into how to resolve as well, with the cached document.body.scrollTop rather than query for it in every loop iteration.

 - Research on querySelectorAll, searched on Google for performance of it, and ended up on http://ryanmorr.com/abstract-away-the-performance-faults-of-queryselectorall/
    - this site pointed out that there are much higher performing methods available, so I repleaced it with the getElementsByClassName, which gave a dramatic improvement.
