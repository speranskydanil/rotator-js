# rotator-js

rotator-js is a JavaScript library which uses canvas for rotating of images.
It consists of two parts: core and app.

## Core

```
<script src="../../js/rotator.js"></script>
```

```
var rotator = new Rotator({
  container: document.getElementById('container'),
  src: '../lenna.jpg',
  angle: 45,

  grid: {
    visibility: true,
    width: 1,
    color: '#5aa',
    step: 40
  },

  change: function (rotator) {
    console.log(rotator.angle);
  }
});
```

```
rotator.rotate(15);
```

![screen](https://raw.github.com/speranskydanil/rotator-js/master/core.png)

## App

```
<link href="../../css/rotator-app.css" media="all" rel="stylesheet" type="text/css">
<link href="http://code.jquery.com/ui/1.10.2/themes/smoothness/jquery-ui.css" media="all" rel="stylesheet" type="text/css">
```

```
<script src="http://code.jquery.com/jquery-1.10.2.js"></script>
<script src="http://code.jquery.com/ui/1.10.2/jquery-ui.js"></script>
<script src="../../js/rotator.js"></script>
<script src="../../js/rotator-app.js"></script>
```

```
$(document).ready(function () {
  var rotator_app = new RotatorApp({
    container: $('#container'),
    toolbar: $('#toolbar'),

    src: '../lenna.jpg',
    angle: 45,

    grid: {
      visibility: true,
      width: 1,
      color: '#5aa',
      step: 40
    },

    change: function (rotator) {
      console.log(rotator.angle);
    }
  });
});
```

![screen](https://raw.github.com/speranskydanil/rotator-js/master/app-1.png)

![screen](https://raw.github.com/speranskydanil/rotator-js/master/app-1.png)

