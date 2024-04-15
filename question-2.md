# rendering and pipeline composition on the browser

1. there are two different things from DOM tree and render tree
2. introduction off CSSOM (CSS Object Model) which allows you to modify the CSS within the JS (read: CSS-in-JS)
3. each of composition run on each pipeline, eq: CSSOM and dom tree run on the GPU separately but at the end render tree will combine it and becoming like 1 visual or viewport of the page
