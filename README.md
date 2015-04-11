# rotator-js

rotator-js is a JavaScript library which uses canvas for rotating of images.
It consists of two parts: core and app.

## Core

### <a href="http://speranskydanil.github.io/rotator-js/demo/rotator/index.html">DEMO</a>

```html
<script src="../../js/rotator.js"></script>
```

```javascript
var rotator = new Rotator({
  container: document.getElementById('rotator'),
  src: '../lenna.jpg',
  angle: 45,

  grid: {
    visibility: true,
    width: 1,
    color: '#5aa',
    step: 40
  },

  load: function (rotator) {
    console.log('load ' + rotator.angle)
  },

  change: function (rotator) {
    console.log('change ' + rotator.angle);
  }
});

rotator.rotate(15);
```

![screen](https://raw.github.com/speranskydanil/rotator-js/master/core.png)

## App

### <a href="http://speranskydanil.github.io/rotator-js/demo/rotator-app/index.html">DEMO</a>

```html
<link rel="stylesheet" href="https://code.jquery.com/ui/1.11.3/themes/smoothness/jquery-ui.css">
<link rel="stylesheet" href="../../css/rotator-app.css">

<script src="https://code.jquery.com/jquery-1.11.2.min.js"></script>
<script src="https://code.jquery.com/ui/1.11.3/jquery-ui.min.js"></script>
<script src="../../js/rotator.js"></script>
<script src="../../js/rotator-app.js"></script>
```

```javascript
$(document).ready(function () {
  var rotator_app = new RotatorApp({
    container: $('#rotator-app'),
    toolbar: $('#toolbar'),

    src: '../lenna.jpg',
    angle: 45,

    grid: {
      visibility: true,
      width: 1,
      color: '#5aa',
      step: 40
    },

    load: function (rotator) {
      console.log('load ' + rotator.angle)
    },

    change: function (rotator) {
      console.log('change ' + rotator.angle);
    }
  });
});
```

![screen](https://raw.github.com/speranskydanil/rotator-js/master/app-1.png)

![screen](https://raw.github.com/speranskydanil/rotator-js/master/app-2.png)

**Author (Speransky Danil):**
[Personal Page](http://dsperansky.info) |
[LinkedIn](http://ru.linkedin.com/in/speranskydanil/en) |
[GitHub](https://github.com/speranskydanil?tab=repositories) |
[StackOverflow](http://stackoverflow.com/users/1550807/speransky-danil)
