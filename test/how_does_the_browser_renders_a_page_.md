### How does the browser renders a page?

1.  Construct DOM tree: a tree of nodes corresponding html elements
2.  Construct CSSOM tree: a tree of nodes corresponding to css selectors
3.  Construct Render tree: browser traverse DOM tree and match every element with appropriate style from CSSOM tree.
4.  Layout phase. geometry phase where browsers calculate position of every element
5.  Painting phase: browser uses render tree to paint or display pixels currently within your viewport
6.  Repainting phase: if we change DOM tree, browser must repaint the affected regions