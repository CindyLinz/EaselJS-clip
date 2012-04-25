EaselJS-clip
============

Add the clipping feature to [Easel.js][EaselJS]

[EaselJS]: http://easeljs.com/

Synopsis
========

Import the script file in the *lib* directory **after** you import the original [EaselJS][]' file.

```html
    <!-- If EaselJS' url or version is changed, remember to change this line below. -->
    <script src="https://raw.github.com/CreateJS/EaselJS/master/lib/easeljs-0.4.2.min.js" type="text/javascript" charset="utf-8"></script>
    <script src="easeljs-clip.js" type="text/javascript" charset="utf-8"></script>
```

Using [EaselJS][]'s *Graphics* object to specify the clipping region,
and then assign this object to the *clip* field of your clipped target.

```javascript
    var clipped_disk = new Shape;
    clipped_disk.graphics.beginFill('#00ff00').drawCircle(0, 0, 100);

    var clipping_rect = new Graphics;
    clipping_rect.drawRect(0, -50, 100, 100);
    clipped_disk.clip = clipping_rect;

    var container = new Container;
    container.addChild(clipped_disk);
    container.x = 150;
    container.y = 150;

    var stage = new Stage(document.getElementById('canvas'));
    stage.addChild(container);
    stage.update();
```

License
=======

Copyright 2012, Cindy Wang (CindyLinz)

Dual licensed under the MIT or GPL Version 2 licenses.

Date: 2012.4.25
