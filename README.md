# PhysicsWebSite

Support web site for Python and Laboratories in Undergraduate Physics

This is the source for a web site, developed in the [Hugo](https://gohugo.io) web framework using the [Academic](https://themes.gohugo.io/academic/) theme, to provide support and tutorials to undergraduate students in UCD Physics.

For [online documentation]( https://sourcethemes.com/academic/docs/) for the Academic theme.

## Instructions for Contributors:

The Python documentation is in content/courses/python

The Data Analysis Content is in content/courses/data-analysis

## Become a contributor:

First fork it on github and then clone the fork to your own machine.
Then cd into the website folder and run:
` git submodule update --init --recursive` 

Whn you have made changes in your own version you can then to a pull request
for the changes to be reviewed and incorporated into the main version.

## Deployment:
TBD



### Menu system

The file 'config/default/menus.toml' is where links that appear
in the top menu and menus that appear on the left-hand
side of the page for courses (page type 'doc') are defined and
ordered (by the weight parameter). Note thay for the courses
the menu mist match the name of the course folder.


### Including images

In Hugo/Academic images can be place in (subfolders) of /statc/img
and included using, e.g.:
{{< figure library="true" src="python/anaconda.png" title="" lightbox="true" width="200">}}.
Any .md file can access images in this static/img folders in this way.

Images may also be included in the same folder as the .md files but it appears
only _index.md (or index.md) can access the images, e.g. 
{{< figure src="binary.png" title="Figure: Binary Numbers" lightbox="true" width="500" >}}

So, if a page has lots of images the suggestion is to make a page bundle in
a folder (the name of the folder will serve as the page name) with all of the images
and use index.html


### Linking to other .md pages

There appear to be relative and absolute links:

e.g. [front matter]({{< relref "front-matter.md" >}})

For information on how to use in Jupyter [see here]({{< ref "courses/python/jupyter/index.md#matplotlib" >}})


### Weights:

It can be a pain to keep track of weights as the amount of content grows!
There appear to be three separate weights applied to 'doc' pages and menus:
1. The weights in the config/_default/menus.toml determine the orders of the menus
2. In a doc page there are two more:
   1. The weight inside the "menu:" section of the front matter determines the order of appearance within that menu item
   2. The weight in the front matter section of the page determines overall wiight for automatically linking to the "Previous" and "Next" items.


