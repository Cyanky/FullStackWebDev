## The difference between vw/vh and %
Suppose you have a <div>, direct child of <body> that you want filling the whole viewport, so you use width: 100vw; height: 100vh;. It all works just the same as width: 100%; height: 100vh; until you add more content and a vertical scrollbar shows up. Since the vw account for the scrollbar as part of the viewport, width: 100vw; will be slightly bigger than width: 100%;. This little difference ends up adding a horizontal scrollbar (required for the user to see that little extra width) and by consequence, the height would also be a little different on both cases.

That must be taken into consideration when deciding which one to use, even if the parent element size is the same as the document viewport size.

Example:

Using width:100vw;:

.fullviewport {
  width: 100vw;
  height: 100vh;
  background-color: red;
}

.extracontent {
  width: 100vw;
  height: 20vh;
  background-color: blue;
}
<html>
<body>
<div class="fullviewport"></div>
<div class="extracontent"></div>
</body>
</html>

  
  
Using width:100%;:

.fullviewport {
  width: 100%;
  height: 100vh;
  background-color: red;
}

.extracontent {
  width: 100%;
  height: 20vh;
  background-color: blue;
}
<html>
<body>
<div class="fullviewport"></div>
<div class="extracontent"></div>
</body>
</html>
