jQuery UI Vertical Tabs
=======================

An extension of the jQuery UI tabs widget that adds the ability to display tabs vertically.

### Show me a demo

Ok. [Here you go.](http://jsfiddle.net/tj_vantoll/dbYHL/)

### How does it work?

The extension adds a single `orientation` option to the jQuery UI tabs widget. For consistency with other jQuery UI widgets, the `orientation` option can be set to `"horizontal"` or `"vertical"`, and defaults to `"horizontal"`.

When the tabs are displayed vertically, the extension places a `ui-vertical-tabs` class name on the tabs element for styling purposes.

### Show me some code

The following creates a vertical tabs control by setting the `orientation` option to `"vertical"`:

```
<link href="http://code.jquery.com/ui/1.11.0/themes/smoothness/jquery-ui.css" rel="stylesheet">
<link rel="stylesheet" href="vertical-tabs.css">

<div id="tabs">
    <ul>
        <li><a href="#tabs-1">One</a></li>
        <li><a href="#tabs-2">Two</a></li>
        <li><a href="#tabs-3">Three</a></li>
    </ul>
    <div id="tabs-1">
        One Contents
    </div>
    <div id="tabs-2">
        Two Contents
    </div>
    <div id="tabs-3">
        Three Contents
    </div>
</div>

<script src="http://code.jquery.com/jquery-2.1.1.js"></script>
<script src="http://code.jquery.com/ui/1.11.0/jquery-ui.js"></script>
<script src="vertical-tabs.js"></script>
<script>
    $( "#tabs" ).tabs({ orientation: "vertical" });
</script>
```

The option plays nice with jQuery UI widget conventions, so you can use the `option()` method to change the orientation...

```
$( "#tabs" ).tabs( "option", "orientation", "horizontal" });
```

...or you can change the default of the option by changing it on the widget's prototype. For instance the following changes the default from `"horizontal"` to `"vertical"`:

```
$.ui.tabs.prototype.options.orientation = "vertical";
```

### AMD Usage

The extension supports AMD usage, including the use of the [AMD modules that were introduced in jQuery UI 1.11](http://learn.jquery.com/jquery-ui/environments/amd/). For details on usage, refer to [this repository's packaged demo](https://github.com/tjvantoll/jquery-ui-vertical-tabs/blob/master/demos/usage-amd.html), which is a complete example of using this extension in an AMD setting.

### Bower Usage

`bower install jquery-ui-vertical-tabs`

### License

MIT. Go nuts.

### Want to learn more?

This extension, as well as the process of building and using jQuery UI extensions is thoroughly explained in [*jQuery UI in Action*](http://tjvantoll.com/jquery-ui-in-action.html).