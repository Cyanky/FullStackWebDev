## The HTML Document
  
  Every HTML document you create or load is derived from this basic format:

  
  You can think of it as a template. And, following this template will help ensure that the page is displayed as the developer (you) intended. It not only says what should be displayed, but also includes relevant information that tells the browser how to display it.

  
  This template can be broken down into 3 parts:

  
  DOCTYPE: Describes the type of HTML. While there are technically different types, for 99.999% of the HTML you'll write, you’ll likely be fine with <!DOCTYPE html>.
  
  head: Describes meta information about the site, such as the title, and provides links to scripts and stylesheets the site needs to render and behave correctly.
  
  body: Describes the actual content of the site that users will see.  
## Quirks Mode and Standards Mode
  
  In the old days of the web, pages were typically written in two versions: One for Netscape Navigator, and one for Microsoft Internet Explorer. When the web   
  standards were made at W3C, browsers could not just start using them, as doing so would break most existing sites on the web. Browsers therefore introduced two   
  modes to treat new standards compliant sites differently from old legacy sites.

  
  There are now three modes used by the layout engines in web browsers: quirks mode, almost standards mode, and full standards mode. In quirks mode, layout emulates   
  nonstandard behavior in Navigator 4 and Internet Explorer 5. This is essential in order to support websites that were built before the widespread adoption of web   
  standards. In full standards mode, the behavior is (hopefully) the behavior described by the HTML and CSS specifications. In almost standards mode, there are only   
  a very small number of quirks implemented.

  
  ## How do browsers determine which mode to use?
  
  For HTML documents, browsers use a DOCTYPE in the beginning of the document to decide whether to handle it in quirks mode or standards mode. To ensure that your   
  page uses full standards mode, make sure that your page has a DOCTYPE like in this example:

```<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset=UTF-8>
    <title>Hello World!</title>
  </head>
  <body>
  </body>
</html>  
```  


  
  The DOCTYPE shown in the example, <!DOCTYPE html>, is the simplest possible, and the one recommended by HTML5. Earlier versions of the HTML standard recommended   
  other variants, but all existing browsers today will use full standards mode for this DOCTYPE, even the dated Internet Explorer 6. There are no valid reasons to   
  use a more complicated DOCTYPE. If you do use another DOCTYPE, you may risk choosing one which triggers almost standards mode or quirks mode.

  
  Make sure you put the DOCTYPE right at the beginning of your HTML document. Anything before the DOCTYPE, like a comment or an XML declaration will trigger quirks   
  mode in Internet Explorer 9 and older.

  
  In HTML5, the only purpose of the DOCTYPE is to activate full standards mode. Older versions of the HTML standard gave additional meaning to the DOCTYPE, but no   
  browser has ever used the DOCTYPE for anything other than switching between quirks mode and standards mode.
