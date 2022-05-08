If you want to try removing the style from the Youtube homepage yourself, follow these instructions:

Visit https://www.youtube.com/ or any other website of your choice.
Right click anywhere on the page, and click "Inspect" (on Mac) or "Inspect Element" (Firefox)
You'll see a panel showing HTML. Inside the <head> element, delete any line that has rel="stylesheet". For example:
<link rel="stylesheet" href="//s.ytimg.com/yts/cssbin/www-core-webp-vflCayM79.css" name="www-core" class="css-httpssytimgcomytscssbinwwwcorewebpvflCayM79css">
