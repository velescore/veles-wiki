# Veles Core Wiki documentation
This directory contains documentation about the Veles Core Wiki itself and guidelines about writing Veles Core Wiki articles. We recommend read the [Veles Wiki Contributing documentation](https://github.com/mdfkbtc/veles-wiki/blob/master/docs/CONTRIBUTING.md) to learn more about contributing rules and customs. 

## The Markdown Format
The wiki pages need to be authored using the [Markdown](https://daringfireball.net/projects/markdown/) format,
a lightweight markup language which results in easy-to-read, easy-to-write plain text documents that can be 
converted to valid HTML documents. 

The [website application](https://github.com/velescore/veles-website) uses the [Python-Markdown](https://python-markdown.github.io/) library to render 
wiki articles written as Markdown documents to HTML. Python-Markdown is almost completely compliant with 
the reference implementation, although there are a few very minor [differences](https://python-markdown.github.io/#differences).

In addition to the base Markdown syntax which is common across all Markdown implementations, this wiki uses
extended Markdown syntax to enable easier editing and content management for the purpose of wiki articles.

## Supported Markdown Extensions
- [WikiLinks](https://python-markdown.github.io/extensions/wikilinks/) (*note: our implementation converts spaces to "-" instead of "_"*)
- [Meta-Data](https://python-markdown.github.io/extensions/meta_data/)
