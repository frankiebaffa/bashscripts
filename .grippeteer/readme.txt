grippeteer (Frankie Baffa <frankiebaffa@gmail.com>)
A program to convert Github-flavored Mardown (GFM) documents into formatted PDFs.
=======
USAGE:
grippeteer -F [INPUTFILE] [OPTIONS]

DESCRIPTION:
Utilizing grip to convert Markdown to a Github-readme styled html document, then puppeteer-pdf to convert html into a PDF through headless-chrome.  grippeteer also allows for custom tags to add more formatting options which is not innate to Markdown or GFM.

OPTIONS:
-F | --filename [FILENAME]      Specifies which markdown file will be converted.
-f | --force                    Allows for the deletion of existing files.
-h | --help                     Displays this message.
-d | --debug-html               Keeps .html file generated in the conversion process for debugging purposes.
-G | --debug-grip-html          Keeps .html file generated directly from grip for debugging purposes.
-v | --verbose                  Prints messages during runtime.
-g | --log                      Prints verbose messages with timestamps.
-L | --logfile [LOGFILE]        Prints log messages to specified file.

CUSTOM TAG-LIKES:
These can be included in the markdown document and will be replaced with html tags after the html conversion step.
INLINE TAG-LIKES:
//small//Inner text//-small//   Wraps the "Inner text" with the <small> html tag.
BLOCK TAG-LIKES:
\pagebreak                      Inserts a <div> html tag with a style tag that forces the "page-break-after" css attribute with the value "always".
