# CSS Grid

## HTML is broken
+ HTML pages are meant to be read top to bottom line by line. If we want to change a layout of the page we need to break the document and put it back together.
+ Bootstrap can fix this, but it uses JavaScript and DOM manipulation. Also you need a 3rd party application for something that should be built in
+ Flexbox can fix this. But you will need to create a lot of unnecessary divs.

## The problem
+ Current tools for web layout are content-out and one dimensional
+ One dimensional: you apply layout to a single item and relate that item to everything else

## Solution
+ Needed: layout-in
+ Make a grid first and determine what part of the grid should be for which element
+ Define a grid
+ place items in the grid
+ grid-template-column
+ grid-template-row

+ grid template areas allows you to name the cells, almost like acii, you write out the grid in names with text

## How to use CSS Grid
+ Build mobile-first layout without grid
+ Use mobile layout as fallback if browser doesn't support your site
+ Use @supports to detect grid support
+ Create grid at appropriate grid length
+ Firefox has a grid inspector
+ see: Grid by example by Rachel Andrew
