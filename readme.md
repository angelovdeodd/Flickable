Flickable
=========

Flickable is a simple Javascript library for creating iOS-style flickable galleries on touch-enabled devices.

Demo
----

A demo can be viewed at [flickable.aurlien.net](http://flickable.aurlien.net).

Usage
-----

The library provides a single function, `Flickable`, which takes two arguments:

1. A selector for the flickables
2. A settings object

The matched element(s) should contain a second element, which should contain the actual slides. The slides must be of the exact same width, and should be of the same height (for aestethic reasons).

The file `flickable.css` contains the recommended CSS rules for the flickable elements.

Simple usage:

    <div class="flickable">
        <ul>
            <li>First</li>
            <li>Second</li>
            <li>Third</li>
        </ul>
    </div>
    <script type="text/javascript">
        Flickable('.flickable', {
            width: 320
        });
    </script>

Settings reference
------------------

- `width`: The width of each item, including margin, padding and border. Use 'screen' to auto-fit and resize with screen. **Default:** `'screen'`
- `offset`: Which item to start at. **Default:** `0`
- `enableMouseEvents`: Whether to enable mouse events (useful for testing). **Default:** `false`
- `showIndicators`: Whether to show indicators for which item is selected. **Default:** `true`
- `showNumbers`: Whether to show indicators in form of numbers like "2/23". **Default:** `false`. Supports caption display as well, the caption must be provided in `data-caption` attribute of `<li>` tag.
- `showButtons`: Whether to show next/previous-buttons for devices that support touch events. **Default:** `false`
- `nextButtonText`: Text for next-button. **Default:** `'Next'`
- `prevButtonText`: Text for previous-button. **Default:** `'Previous'`
- `indicatorClass`: The class name for the dots indicator wrapper element. **Default:** `'flickableIndicatorDots'`
- `numberIndicatorClass`: The class name for the numbered indicator wrapper element. **Default:** `'flickableIndicatorNumbers'`
- `activeIndicatorClass`: The class name for the active indicator element. **Default:** `'flickableIndicatorActive'`
- `callback`: A function to be called each time the slide changes. The function will be passed the slide number (zero-indexed) as a parameter.

_Licensed under the MIT license: http://www.opensource.org/licenses/mit-license.php_