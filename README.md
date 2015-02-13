simpleportal
============

*   Version 0.1.0 [2015-02-14]
*   Author  Jeffrey Silverman <jeffrey.d.silverman@gmail.com>
*   License See: LICENSE

Overview
--------

This is a javascript one-page app that builds a tabbed-interface bookmarks portal from a YML file

To make this work, *the index.html file must be accessed from a web server*. i.e. Served over HTTP. (Unfortunately the JS YAML lib I
used requires that YAML files be served over HTTP.)

Instructions
------------

To add or edit links, do this

1.  Edit the YML file "items.yml", per these instructions
2.  Add an icon image in images/. Use existing images for guidance. *Name the image after the "label" indicated in the
    YML example, below.*
    *   Image icons must be in PNG format
    *   File name must be all lowercase
    *   Image should be exactly 72x72 pixels square

The resulting HTML links are arranged in alphabetical order within each panel

The YML contains the following elements for each tab, and each link within a tabbed panel:

The "category" is mandatory. The category is the un-indented items (See example, below).

The "label" is mandatory. The label is the first-indented items (See example, below).

The following bookmark attributes are mandatory

*   "url:"
*   "url_linkname:"

"description:" is optional. But really, you should fill that one in, too.

Example items.yml
-----------------

    Main:				    <-- Category
        generic:			<-- label. The icon image should be named after this label. In this example, that would be "generic.png" 
            url:  "thing"
            url_linkname:  "thing"
            description:  "thing"
