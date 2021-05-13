# Installation

Just download the file `confluence.lua` and put it in a convenient location. Pandoc includes a lua interpreter, so lua need not be installed separately. You need at least Pandoc version 1.13, released August 2014 (this release adds --template support for custom writers).

Make sure confluence has the [Confluence Source Editor](https://marketplace.atlassian.com/apps/1210722/confluence-source-editor?hosting=server&tab=overview) plugin installed, so that the output of the conversion can be used.

# Usage

To convert the markdown file example1.md into the confluence storage format, use the following command:

`$ pandoc example1.md -t path-to/pandoc-confluence-writer/confluence.lua -o confluence-out.xhtml`

Then edit the confluence page, click the `< >` button in the top right, and paste the contents of `confluence-out.xhtml` into the window.

### NOTES

Look at https://github.com/mfenner/pandoc-jats/blob/master/sample.lua (footnotes)


https://github.com/jgm/pandoc/blob/master/data/pandoc.lua


In fact, put in into confluence storage format!

https://confluence.atlassian.com/doc/confluence-storage-format-790796544.html#ConfluenceStorageFormat-Lists

(start from sample.lua)

https://stackoverflow.com/questions/6345948/css-for-specific-text-on-confluence


# TODO

* Better Handling of images (attached or not)
* Trying to fix footnotes's link which is after a paragraph annotation (link is one line down).
* Adding configurable CSS stylesheet

# CSS for image caption

https://bitbucket.org/ryanackley/confluence-image-captions/wiki/Home
