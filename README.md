# o-aside-panel [![Build Status](https://travis-ci.org/Financial-Times/o-aside-panel.png?branch=master)](https://travis-ci.org/Financial-Times/o-aside-panel)

___
Content module with a heading and one or more panels.
___

__o-aside-panel__ provides styling for:

* Heading
* Tabs (optional)
* Panel body (minimum of 1), but _not_ panel contents

If tabs are used, then [o-tabs](http://registry.origami.ft.com/components/o-tabs)'s JavaScript must also be included in the page to provide the tabs' behaviour. __o-tabs__ is not a dependency of this module.

If multiple panels are used, the module will be sized to accommodate the tallest panel, regardless of which panel is in view.
In other words, any content below will not shift up and down as the panel in view is changed.

## Markup

__Without tabs__

```html
<div data-o-component="o-aside-panel" class="o-aside-panel">
    <div class="o-aside-panel__header">
        <h3 class="o-aside-panel__heading">Heading <a href="#">Link</a></h3>
    </div>
    <div class="o-aside-panel__body">
        o-aside-panel body content
    </div>
</div>
```

__With tabs__

```html
<div data-o-component="o-aside-panel" class="o-aside-panel">
    <div class="o-aside-panel__header">
        <h3 class="o-aside-panel__heading">Heading</h3>
        <ul data-o-component="o-tabs" class="o-tabs o-aside-panel__tabs--theme" role="tablist">
            <li role="tab"><a href="#oPanelContent1">Tab 1</a></li>
            <li role="tab"><a href="#oPanelContent2">Tab 2</a></li>
            <li role="tab"><a href="#oPanelContent3">Tab 3</a></li>
        </ul>
    </div>
    <div id="oPanelContent1" class="o-aside-panel__body">
        o-aside-panel body content 1
    </div>
    <div id="oPanelContent2" class="o-aside-panel__body">
        o-aside-panel body content 2
    </div>
    <div id="oPanelContent3" class="o-aside-panel__body">
        o-aside-panel body content 3
    </div>
</div>
```

Note that the `o-aside-panel__tabs--theme` must also be set on the __o-tabs__ root element.

## Core experience

No _tabs_ will be shown, and _panel bodies_ will all be shown one below the other.

## Primary experience

_Tabs_ will be shown (if declared in markup) and will be functional. Only the _panel body_ for the selected _tab_ will be shown.
