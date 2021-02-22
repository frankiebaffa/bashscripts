md_to_pdf

AUTHOR:
Frankie Baffa <frankiebaffa@gmail.com>

OVERVIEW:
A program to convert Github-flavored Mardown (GFM) documents into formatted PDFs.

USAGE:
md_to_pdf -i [INPUTFILE] -o [OUTPUTFILENAME] [OPTIONS]

DESCRIPTION:
Utilizing grip to convert Markdown to a Github-readme styled html document, then puppeteer-pdf to convert html into a PDF through headless-chrome.  md_to_pdf also allows for custom tags to add more formatting options which is not innate to Markdown or GFM.

OPTIONS:
-i | --input [INPUTFILE]        Specifies which markdown file will be converted.
-o | --output [OUTPUTFILENAME]  Specifies the name of the output file (no file extension).
-f | --force                    Allows for the deletion of existing files.
-h | --help                     Displays this message.
-d | --debug-html               Keeps .html file generated in the conversion process for debugging purposes.

CUSTOM TAG-LIKES:
These can be included in the markdown document and will be replaced with html tags after the html conversion step.
INLINE TAG-LIKES:
//small//Inner text//-small//   Wraps the "Inner text" with the <small> html tag.
BLOCK TAG-LIKES:
\pagebreak                      Inserts a <div> html tag with a style tag that forces the "page-break-after" css attribute with the value "always".
